# 8. Troubleshooting

Solutions to the problems you are most likely to hit, roughly in the order they
occur during development.

## Quick checklist

If something does not work, verify these first:

- [ ] Node.js is version **18 or 20** (`node --version`).
- [ ] You are signed in (`aio login`) and on the **correct org/project/workspace**
      (`aio console where`).
- [ ] The extension point name matches **exactly**, including the version:
      `fusion/nav-organization/1`.
- [ ] The `url` in `getWidget()` matches a **route** in your app.
- [ ] Your visible UI calls **`attach({ id })`**.
- [ ] You deployed **and** published to the workspace Fusion is reading
      (`Stage` during testing).

---

## Error 1060: "Extension point does not exist"

**Full message:** `CoreConsoleAPISDK ... 1060: Extension point
'fusion/nav-organization/1' does not exist` during `aio app deploy`.

**Meaning:** the Fusion extension point is not enabled ("onboarded") for your
Adobe organization yet. Adobe validates, at deploy time, that the extension
point exists in your organization's catalog. This is **not** a problem with your
code or your YAML.

**Fix:** ask the Fusion team to onboard the extension point(s)
(`fusion/nav-organization/1` and/or `fusion/nav-team/1`) for your IMS
organization. When you request onboarding, include:

- your **IMS organization id** (`XXXX@AdobeOrg`),
- the **extension point(s)** you need,
- your **Developer Console project and workspace** names.

Once onboarding is confirmed, re-run `aio app deploy`.

---

## "Awaiting initial message from target iframe" / the panel spins forever

**Meaning:** Fusion opened your visible UI but it never completed the handshake,
so Fusion timed out.

**Fix:** make sure your **visible** component calls `attach({ id })` (see
[Build the UI](./05-build-the-ui.md)):

```jsx
useEffect(() => {
  attach({ id: extensionId }).catch(console.error);
}, []);
```

Common causes:

- `attach` is only in the registration component, not in the visible widget.
- The `url` in `getWidget()` points to a route that renders the **registration**
  component (or a blank page) instead of your widget.
- The `id` passed to `attach` differs from the `id` used in `register`. They must
  be identical — keep both in `Constants.js`.

---

## The nav button never appears in Fusion

Work through these in order:

1. **Deployed to the right workspace?** On **Stage**, a successful `aio app
   deploy` is enough for Fusion to discover the extension (no approval needed).
   On **Production**, you must also submit and obtain **approval** before it
   appears. See [Publish](./07-publish.md).
2. **Right workspace?** Fusion discovers from a specific workspace (`Stage`
   during testing). Deploy to that same workspace.
3. **Right organization?** Sign in to Fusion with an account in the **same** IMS
   organization you published to.
4. **Right section?** `fusion/nav-organization/1` shows under **Organization**;
   `fusion/nav-team/1` shows under **Team** (you must select a team first).
5. **Extension point name typo?** It must read exactly
   `fusion/nav-organization/1` in both `app.config.yaml` and the folder's
   `ext.config.yaml` include path.

---

## The button appears but the panel is blank

- **Route mismatch:** the `url` from `getWidget()` (for example
  `/index.html#/my-widget`) must match a `<Route>` in `App.js`. A mismatch loads
  a page with no component.
- **JavaScript error:** open your browser's developer tools (F12) → **Console**
  tab, and look for errors coming from the iframe. Fix the reported error and
  redeploy.
- **Header missing/duplicated:** `hideWidgetHeader` in `getWidget()` controls
  whether Fusion shows the title above your UI. Set it to `true` if you render
  your own header.

---

## The iframe is blocked (Content Security Policy / "refused to frame")

Fusion only allows extensions hosted on Adobe's App Builder CDN
(`*.adobeio-static.net`), which is where `aio app deploy` puts your files by
default. If you host your UI somewhere else (a custom domain), Fusion will refuse
to load it. Either deploy through App Builder as documented, or ask the Fusion
team whether your domain can be allowlisted.

---

## Context is empty or stale

- **Empty right after load:** read the context **after** `attach` resolves, not
  before. Until then show a "Connecting…" state.
- **Not updating when the user switches org/team:** subscribe to the
  `contextchange` event and re-read your keys inside the handler. See
  [Build the UI](./05-build-the-ui.md#step-3--read-the-context-fusion-shares).
- **Dates look wrong:** date fields arrive as ISO **strings**, not `Date`
  objects. Wrap them in `new Date(...)`. See
  [Context reference](./06-fusion-context-reference.md#a-note-on-dates).

---

## Calling an API fails with a CORS error

**Symptom:** the browser Console shows *"No 'Access-Control-Allow-Origin'
header"* (or the request is blocked) when your UI calls a Workfront/Fusion API
directly.

**Fix:** do not call those APIs from the browser. Route the call through your own
App Builder **runtime action** (server-side, no CORS) and have the guest call the
action with a relative, same-origin URL. See
[Calling Workfront & Fusion APIs](./10-calling-apis.md).

---

## Proxy action returns 401 even with a valid token

**Meaning:** with `require-adobe-auth: true`, Adobe's gateway validates the call
before your action runs and can reject it (or drop custom headers your upstream
needs), surfacing as a `401`.

**Fix:** set `require-adobe-auth: false` on the action **and** enforce auth
yourself - require an `Authorization` bearer in the action, forward it upstream,
and keep a strict target allowlist. See
[require-adobe-auth: true vs. false](./10-calling-apis.md#require-adobe-auth-true-vs-false).

---

## Fusion `GET /api/v3/hooks` returns 400

**Meaning:** the hooks endpoint is **team-scoped**; `teamId` is a required query
parameter.

**Fix:** call `/api/v3/hooks?teamId=<team.id>`. Hooks come back for the active
team only; to cover an organization, loop its teams and merge. Scenarios, by
contrast, accept `organizationId`. See
[Fusion v3 API specifics](./10-calling-apis.md#fusion-v3-api-specifics).

---

## `aio` errors

- **`aio: command not found`** — the CLI is not installed or not on your PATH.
  Re-run `npm install -g @adobe/aio-cli`, then open a new terminal.
- **Build/deploy fails on a brand-new Node version** — use Node **18 or 20 LTS**.
  Very new, non-LTS releases sometimes break the toolchain.
- **"You are not a developer" / cannot see your org** — your Adobe org admin
  must grant you the **Developer** role and App Builder access. See
  [setup](./02-setup.md).
- **401 / invalid token during deploy or discovery** — your session expired or
  you are mixing environments. Run `aio logout` then `aio login`, confirm
  `aio console where`, and deploy to the workspace Fusion reads.

---

## Still stuck?

Collect this information before asking for help; it makes diagnosis much faster:

- the exact command you ran and the **full** error output,
- your **IMS organization id**, **project**, and **workspace**,
- the **extension point** you are targeting,
- whether `aio app deploy` succeeded, and whether the extension is **Published**,
- any errors in the browser **Console** (F12) when opening the panel in Fusion.
