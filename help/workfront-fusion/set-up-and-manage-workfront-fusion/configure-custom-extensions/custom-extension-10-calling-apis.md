---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: fusion
navigation-topic: workfront-fusion-navigation-topic
title: Calling Workfront and Fusion APIs from your extension
description: Calling Workfront and Fusion APIs from your extension
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
---

# Calling Workfront and Fusion APIs from your extension

>[!NOTE]
>
>This article assumes some familiarity with software development tools. 

The Fusion context reference gives you the signed-in user's IMS token, so a natural next step is to call Workfront or Fusion APIs and show real data. This is not possible due to CORS. This article shows how to get around that limitation using an App Builder runtime action as a server-side proxy, and includes an example (the event subscriptions dashboard).

## Why a direct browser call fails (CORS)

Your visible UI runs in an `<iframe>` served from Adobe's CDN (`https://<your-app>.adobeio-static.net`). When that page does `fetch(...)` to a Workfront or Fusion API on a **different** origin, the browser enforces Cross-Origin Resource Sharing (CORS). Unless the API explicitly returns `Access-Control-Allow-Origin` for your CDN origin, the browser blocks the response. These APIs do not allowlist arbitrary extension origins, so direct calls from the guest fail.

For information on CORS, see [CORS](https://developer.mozilla.org/docs/Web/HTTP/CORS).

## Call your own runtime action without CORS

The fix for this is to call your own runtime action without CORS.

App Builder apps can include runtime actions, which are small serverless functions that run on Adobe I/O Runtime, server-side. Server-to-server calls are not subject to browser CORS. And because the action is part of your app, the guest can call it with a relative URL, which is same-origin and therefore not blocked.

```
  Guest UI (browser, adobeio-static.net)
     │  fetch('/api/v1/web/<app>/wf-proxy?...')   ← relative = same-origin, no CORS
     ▼
  Your runtime action  (Adobe I/O Runtime, server-side)
     │  fetch('https://fusion.adobe.com/api/v3/...')  ← server-to-server, no CORS
     ▼
  Workfront / Fusion API
```

The action receives the user's IMS token from the guest and forwards it upstream, so calls are still made on the user's behalf with their permissions.

## Step 1: Declare the action

Runtime actions are declared in `app.config.yaml` under the extension's `runtimeManifest`. Add a `wf-proxy` action next to your extension:

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

This annotation controls whether Adobe's gateway validates an IMS token before your action runs.

* **`true`:** The secure default.  The gateway rejects unauthenticated calls. However, the validator is strict about which headers it expects and can reject requests or drop custom headers that your upstream call needs. If that happens, it shows up as a `401` even though your token is valid.
* **`false`:** Skips the gateway check. Your action is then publicly invocable, so you **must** enforce authorization yourself. Require an `Authorization` bearer in the action and reject if missing, then and forward it upstream, where Workfront and Fusion validate it. Combined with a strict target allowlist, described in Step 2, this is the reliable path for a proxy that needs to pass custom headers.

>[!TIP]
>
> Try `true` first. If you see a `401` that you cannot explain because the token is valid and works elsewhere, switch to `false` **and** keep the bearer check and allowlist in your action so security is still enforced upstream.

## Step 2: Write the action for an allowlisted proxy

Create `src/fusion-nav-organization-1/actions/wf-proxy/index.js`. Two rules keep this safe: an allowlist of upstream targets so the action can't be used as an open relay, and a required bearer token that is forwarded upstream.

```js
const fetch = require('node-fetch')
const { Core } = require('@adobe/aio-sdk')
const { errorResponse, getBearerToken, checkMissingRequestInputs } = require('../utils')

// Page-through query params (see "Paginate list results" below).
const pageQuery = (p) => {
  const q = new URLSearchParams()
  if (p.start != null) q.set('start', p.start)
  if (p.limit != null) q.set('limit', p.limit)
  return q
}

// Only these upstreams may be reached. Never build the URL from arbitrary input.
const TARGETS = {
  subscriptions: {
    method: 'GET',
    url: () => 'https://<your-wf-host>/attask/eventsubscription/api/v1/subscriptions',
  },
  hooks: {
    method: 'GET',
    // Fusion hooks are team-scoped: teamId is a REQUIRED query param (see below).
    url: (p) => {
      const q = pageQuery(p)
      if (p.teamId) q.set('teamId', p.teamId)
      return `https://fusion.adobe.com/api/v3/hooks?${q.toString()}`
    },
  },
  scenarios: {
    method: 'GET',
    url: (p) => {
      const q = pageQuery(p)
      if (p.fusionOrgId) q.set('organizationId', p.fusionOrgId)
      return `https://fusion.adobe.com/api/v3/scenarios?${q.toString()}`
    },
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

`getBearerToken`, `errorResponse`, and `checkMissingRequestInputs` come from the generated `actions/utils.js`, where the template scaffolds them. `getBearerToken` reads `params.__ow_headers.authorization`, which is where the gateway puts the incoming `Authorization` header.

## Step 3:  Call the action from the guest

From your UI, `fetch` the action with a relative (same-origin) URL and send the IMS token as a bearer. Pass the organization and team IDs that the upstream needs as query params.

```js
const PROXY_URL = "/api/v1/web/fusion-uix-guest/wf-proxy";

async function callProxy(target, token, { imsOrgId, fusionOrgId, teamId, start, limit } = {}) {
  const params = new URLSearchParams({ target });
  if (imsOrgId) params.set("orgId", imsOrgId);          // → x-gw-ims-org-id
  if (fusionOrgId) params.set("fusionOrgId", fusionOrgId); // → x-organization-id
  if (teamId) params.set("teamId", teamId);             // → x-team-id
  if (start != null) params.set("start", start);        // pagination offset
  if (limit != null) params.set("limit", limit);        // pagination page size
  const res = await fetch(`${PROXY_URL}?${params.toString()}`, {
    headers: { authorization: `Bearer ${token}` },
  });
  if (!res.ok) throw new Error(`${target} request failed: ${res.status}`);
  return res.json();
}
```

Get `token`, `imsOrgId`, `fusionOrgId`, and `teamId` from the context:

```js
const token       = connection.sharedContext.get("imsToken");
const imsOrgId    = connection.sharedContext.get("imsOrgId");
const fusionOrgId = connection.sharedContext.get("organization")?.id; // Fusion tenant id
const teamId      = connection.sharedContext.get("team")?.id;
``` 

For information on the context, see [The Fusion context reference](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

## Fusion v3 API specifics

What worked for the dashboard against `https://fusion.adobe.com/api/v3`:

| Header / param | Value | Notes |
| ---------------- | ------- | ------- |
| `Authorization` | `Bearer <imsToken>` | The user's IMS token from the context. |
| `x-organization-id` | `organization.id` | Fusion's own tenant ID, not the IMS org ID. Fusion identifies the tenant by this. |
| `x-team-id` | `team.id` | Send when the call is team-scoped. |
| `x-gw-ims-org-id` | `imsOrgId` | Adobe IMS org ID, for the gateway. |

Note the following caveats:

* **`GET /api/v3/hooks` is team-scoped:** `teamId` is a **required query param** (`/api/v3/hooks?teamId=...`). Without it you get a `400`. This means hooks come back for the *active team only*; to cover an org, loop teams and merge.
* **`GET /api/v3/scenarios`** works with `organizationId` (`/api/v3/scenarios?organizationId=...`).

>[!NOTE]
>
> The official reference is Adobe's [Workfront Fusion APIs](https://developer.adobe.com/workfront-fusion-apis/). Header/auth requirements vary by gateway. This table reflects what the demo actually needed. If a call returns `401`/`400`, re-check these headers first.

## Paginate list results

Fusion v3 list endpoints (hooks, scenarios) return one **page** at a time, not the whole set. A response looks like this:

```json
{
  "items": [ /* ...this page of records... */ ],
  "_page": { "start": 0, "limit": 100, "total": 342 }
}
```

The records are under **`items`**, and pagination metadata is under **`_page`**. You page with the **`start`** (offset) and **`limit`** (page size) query params. The proxy above passes both through, so page in the guest by looping until you have collected everything:

```js
const PAGE_LIMIT = 100;

async function fetchAllPages(target, token, opts = {}) {
  const all = [];
  let start = 0;
  // Stop when a page returns fewer than PAGE_LIMIT items, or when _page.total is reached.
  for (;;) {
    const res = await callProxy(target, token, { ...opts, start, limit: PAGE_LIMIT });
    const items = res.items ?? [];
    all.push(...items);

    const total = res._page?.total;
    const done = items.length < PAGE_LIMIT || (total != null && all.length >= total);
    if (done) break;
    start += PAGE_LIMIT;
  }
  return all;
}
```

If you would rather keep paging out of the browser, do the same loop inside the runtime action and return the merged `items` array in one response. Either way, do not assume the first page is the whole result set. A team with more than one page of hooks would otherwise look like it has missing scenarios.

## Security checklist

* **Allowlist upstreams.** Never construct the target URL from raw client input. Map a short `target` key to a fixed URL, as in Step 2. This prevents your action from becoming an open relay.
* **Require the bearer token** in the action and forward it upstream. Let Workfront and Fusion enforce the user's permissions.
* **Never log the token.** `imsToken` is a credential. Keep `LOG_LEVEL` mindful of what `stringParameters` prints.
* **Forward only over HTTPS** to trusted Adobe and Workfront hosts.

## Worked example: the event subscriptions dashboard

The demo dashboard joins three sources to show, per Workfront event subscription, whether a matching Fusion scenario is healthy:

1. `fetchSubscriptions()` → Workfront event subscriptions (with received/passed counters).
1. `fetchHooks(teamId)` → Fusion hooks for the active team (paged with `fetchAllPages`).
1. `fetchScenarios(fusionOrgId)` → Fusion scenarios for the org (paged with `fetchAllPages`).

The **join** chains them, but there is a catch worth calling out: a Workfront subscription and the Fusion hook it points at live on **different hosts**, so their URL fields are not byte-for-byte equal. What is stable is the **token at the end of the webhook URL** (the last path segment). Match on that trailing token, not the full URL. The hook's `scenarioId` then matches a scenario's `id`:

```
subscription.targetUrl  ──(trailing token)──▶  hook.url
                                                hook.scenarioId  ──▶  scenario.id
```

```js
// Reduce a webhook URL to its trailing token so hosts/bases can differ.
function hookKey(url) {
  if (!url) return "";
  const path = String(url).trim().toLowerCase().split(/[?#]/)[0].replace(/\/+$/, "");
  const i = path.lastIndexOf("/");
  return i >= 0 ? path.slice(i + 1) : path;
}

// Index hooks by token, then look each subscription up by the same token.
const hooksByToken = new Map(hooks.map((h) => [hookKey(pick(h, ["url", "address", "targetUrl"], "")), h]));
const hook = hooksByToken.get(hookKey(pick(sub, ["url", "endpointUrl", "targetUrl", "target.url", "callbackUrl"], "")));
```

Status is derived from the join:

* **Broken**: no matching hook, or the hook is `gone`.
* **Filtering**: matched, but `passed < received` (events arrive but are filtered out before the scenario runs).
* **Healthy**: matched and passing.

Because real payload shapes vary, the client maps fields defensively, trying several candidate keys per field, so a minor API difference does not break the table:

```js
function pick(obj, keys, fallback) {
  for (const key of keys) {
    const value = key.split(".").reduce((acc, part) => (acc == null ? acc : acc[part]), obj);
    if (value != null) return value;
  }
  return fallback;
}
```

This is just one example. The same proxy pattern works for any Workfront or Fusion API you need.
