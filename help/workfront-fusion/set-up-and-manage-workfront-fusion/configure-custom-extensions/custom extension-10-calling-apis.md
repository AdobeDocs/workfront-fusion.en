# 10. Calling Workfront & Fusion APIs from your extension

The [context](./06-fusion-context-reference.md) gives you the signed-in user's
**IMS token**, so a natural next step is to call Workfront or Fusion APIs and
show real data. This page covers the one thing that surprises everyone when they
try it - **CORS** - and the clean way around it using an App Builder **runtime
action** as a server-side proxy. It ends with a worked example (the event
subscriptions dashboard).

## Why a direct browser call fails (CORS)

Your visible UI runs in an `<iframe>` served from Adobe's CDN
(`https://<your-app>.adobeio-static.net`). When that page does `fetch(...)` to a
Workfront or Fusion API on a **different** origin, the browser enforces
[CORS](https://developer.mozilla.org/docs/Web/HTTP/CORS): unless the API
explicitly returns `Access-Control-Allow-Origin` for your CDN origin, the browser
blocks the response. These APIs do not allowlist arbitrary extension origins, so
**direct calls from the guest fail.**

## The fix: call your own runtime action (no CORS)

App Builder apps can include **runtime actions** - small serverless functions
that run on Adobe I/O Runtime, *server-side*. Server-to-server calls are not
subject to browser CORS. And because the action is part of *your* app, the guest
can call it with a **relative URL**, which is **same-origin** - so that call is
not blocked either.

```
  Guest UI (browser, adobeio-static.net)
     │  fetch('/api/v1/web/<app>/wf-proxy?...')   ← relative = same-origin, no CORS
     ▼
  Your runtime action  (Adobe I/O Runtime, server-side)
     │  fetch('https://fusion.adobe.com/api/v3/...')  ← server-to-server, no CORS
     ▼
  Workfront / Fusion API
```

The action receives the user's IMS token from the guest and **forwards it
upstream**, so calls are still made on the user's behalf with their permissions.

## Step 1 - Declare the action

Runtime actions are declared in `app.config.yaml` under the extension's
`runtimeManifest`. Add a `wf-proxy` action next to your extension:

```yaml
extensions:
  fusion/nav-organization/1:
    $include: src/fusion-nav-organization-1/ext.config.yaml
    runtimeManifest:
      packages:
        fusion-uix-guest:                # ← your package name; part of the action URL
          license: Apache-2.0
          actions:
            wf-proxy:
              function: src/fusion-nav-organization-1/actions/wf-proxy/index.js
              web: 'yes'                  # exposes it at /api/v1/web/<package>/wf-proxy
              runtime: nodejs:22
              inputs:
                LOG_LEVEL: debug
              annotations:
                require-adobe-auth: false # see note below
                final: true
```

The action becomes reachable at:

```
/api/v1/web/<package>/<action>     e.g.  /api/v1/web/fusion-uix-guest/wf-proxy
```

### `require-adobe-auth`: true vs. false

This annotation controls whether Adobe's gateway validates an IMS token
**before** your action runs.

- **`true`** is the secure default: the gateway rejects unauthenticated calls.
  However, the validator is strict about which headers it expects and **can
  reject requests or drop custom headers** that your upstream call needs - which
  shows up as a confusing `401` even though your token is valid.
- **`false`** skips the gateway check. Your action is then publicly invocable, so
  you **must** enforce auth yourself: require an `Authorization` bearer in the
  action (reject if missing) and forward it upstream, where Workfront/Fusion
  validate it. Combined with a strict **target allowlist** (Step 2), this is the
  reliable path for a proxy that needs to pass custom headers.

> Try `true` first. If you hit a `401` that you cannot explain (token is valid,
> works elsewhere), switch to `false` **and** keep the bearer check + allowlist
> in your action so security is still enforced upstream.

## Step 2 - Write the action (allowlisted proxy)

Create `src/fusion-nav-organization-1/actions/wf-proxy/index.js`. Two rules keep
this safe: an **allowlist** of upstream targets (so the action can't be used as
an open relay) and a **required bearer token** that is forwarded upstream.

```js
const fetch = require('node-fetch')
const { Core } = require('@adobe/aio-sdk')
const { errorResponse, getBearerToken, checkMissingRequestInputs } = require('../utils')

// Only these upstreams may be reached. Never build the URL from arbitrary input.
const TARGETS = {
  subscriptions: {
    method: 'GET',
    url: () => 'https://<your-wf-host>/attask/eventsubscription/api/v1/subscriptions',
  },
  hooks: {
    method: 'GET',
    // Fusion hooks are team-scoped: teamId is a REQUIRED query param (see below).
    url: (p) => `https://fusion.adobe.com/api/v3/hooks${p.teamId ? `?teamId=${encodeURIComponent(p.teamId)}` : ''}`,
  },
  scenarios: {
    method: 'GET',
    url: (p) => `https://fusion.adobe.com/api/v3/scenarios${p.fusionOrgId ? `?organizationId=${encodeURIComponent(p.fusionOrgId)}` : ''}`,
  },
}

async function main (params) {
  const logger = Core.Logger('main', { level: params.LOG_LEVEL || 'info' })
  try {
    const missing = checkMissingRequestInputs(params, ['target'], ['Authorization'])
    if (missing) return errorResponse(400, missing, logger)

    const target = TARGETS[params.target]
    if (!target) return errorResponse(400, `unknown target '${params.target}'`, logger)

    const token = getBearerToken(params)              // reads params.__ow_headers.authorization
    const headers = { authorization: `Bearer ${token}`, 'content-type': 'application/json' }
    if (params.orgId) headers['x-gw-ims-org-id'] = params.orgId        // Adobe IMS org id
    if (params.fusionOrgId) headers['x-organization-id'] = params.fusionOrgId  // Fusion tenant id
    if (params.teamId) headers['x-team-id'] = params.teamId            // Fusion team id

    const res = await fetch(target.url(params), { method: target.method, headers })
    const text = await res.text()
    let body
    try { body = JSON.parse(text) } catch (e) { body = text }

    if (!res.ok) {
      return { statusCode: res.status, body: { error: `upstream ${res.status}`, target: params.target, details: body } }
    }
    return { statusCode: 200, body }
  } catch (error) {
    logger.error(error)
    return errorResponse(500, 'server error: ' + error.message, logger)
  }
}

exports.main = main
```

`getBearerToken`, `errorResponse`, and `checkMissingRequestInputs` come from the
generated `actions/utils.js` (the template scaffolds them). `getBearerToken`
reads `params.__ow_headers.authorization`, which is where the gateway puts the
incoming `Authorization` header.

## Step 3 - Call the action from the guest

From your UI, `fetch` the action with a **relative** URL (same-origin) and send
the IMS token as a bearer. Pass the org/team ids the upstream needs as query
params.

```js
const PROXY_URL = "/api/v1/web/fusion-uix-guest/wf-proxy";

async function callProxy(target, token, { imsOrgId, fusionOrgId, teamId } = {}) {
  const params = new URLSearchParams({ target });
  if (imsOrgId) params.set("orgId", imsOrgId);          // → x-gw-ims-org-id
  if (fusionOrgId) params.set("fusionOrgId", fusionOrgId); // → x-organization-id
  if (teamId) params.set("teamId", teamId);             // → x-team-id
  const res = await fetch(`${PROXY_URL}?${params.toString()}`, {
    headers: { authorization: `Bearer ${token}` },
  });
  if (!res.ok) throw new Error(`${target} request failed: ${res.status}`);
  return res.json();
}
```

Get `token`, `imsOrgId`, `fusionOrgId`, and `teamId` from the
[context](./06-fusion-context-reference.md):

```js
const token       = connection.sharedContext.get("imsToken");
const imsOrgId    = connection.sharedContext.get("imsOrgId");
const fusionOrgId = connection.sharedContext.get("organization")?.id; // Fusion tenant id
const teamId      = connection.sharedContext.get("team")?.id;
```

## Fusion v3 API specifics

What worked for the dashboard against `https://fusion.adobe.com/api/v3`:

| Header / param | Value | Notes |
|----------------|-------|-------|
| `Authorization` | `Bearer <imsToken>` | The user's IMS token from the context. |
| `x-organization-id` | `organization.id` | **Fusion's own tenant id**, not the IMS org id. Fusion identifies the tenant by this. |
| `x-team-id` | `team.id` | Send when the call is team-scoped. |
| `x-gw-ims-org-id` | `imsOrgId` | Adobe IMS org id, for the gateway. |

Endpoint quirks that cost us time:

- **`GET /api/v3/hooks` is team-scoped:** `teamId` is a **required query param**
  (`/api/v3/hooks?teamId=...`). Without it you get a `400`. This means hooks come
  back for the *active team only*; to cover an org, loop teams and merge.
- **`GET /api/v3/scenarios`** works with `organizationId`
  (`/api/v3/scenarios?organizationId=...`).

> The official reference is Adobe's
> [Workfront Fusion APIs](https://developer.adobe.com/workfront-fusion-apis/).
> Header/auth requirements vary by gateway; the table above reflects what the
> demo actually needed. If a call returns `401`/`400`, re-check these headers
> first.

## Security checklist

- **Allowlist upstreams.** Never construct the target URL from raw client input;
  map a short `target` key to a fixed URL (Step 2). This prevents your action
  from becoming an open relay.
- **Require the bearer token** in the action and forward it upstream; let
  Workfront/Fusion enforce the user's permissions.
- **Never log the token** (`imsToken` is a credential). Keep `LOG_LEVEL` mindful
  of what `stringParameters` prints.
- **Forward only over HTTPS** to trusted Adobe/Workfront hosts.

## Worked example: the event subscriptions dashboard

The demo dashboard joins three sources to show, per Workfront event
subscription, whether a matching Fusion scenario is healthy:

1. `fetchSubscriptions()` → Workfront event subscriptions (with received/passed
   counters).
2. `fetchHooks(teamId)` → Fusion hooks for the active team.
3. `fetchScenarios(fusionOrgId)` → Fusion scenarios for the org.

The **join** chains them: a subscription's `targetUrl` matches a hook's `url`;
the hook's `scenarioId` matches a scenario's `id`:

```
subscription.targetUrl  ──▶  hook.url
                              hook.scenarioId  ──▶  scenario.id
```

Status is derived from the join:

- **Broken** - no matching hook, or the hook is `gone`.
- **Filtering** - matched, but `passed < received` (events arrive but are
  filtered out before the scenario runs).
- **Healthy** - matched and passing.

Because real payload shapes vary, the client maps fields defensively (try several
candidate keys per field) so a minor API difference does not break the table:

```js
function pick(obj, keys, fallback) {
  for (const key of keys) {
    const value = key.split(".").reduce((acc, part) => (acc == null ? acc : acc[part]), obj);
    if (value != null) return value;
  }
  return fallback;
}
// e.g. targetUrl: pick(sub, ["url", "endpointUrl", "targetUrl", "target.url", "callbackUrl"], "")
```

This is just one example; the same proxy pattern works for any Workfront or
Fusion API you need.

Next: [Troubleshooting →](./08-troubleshooting.md)
