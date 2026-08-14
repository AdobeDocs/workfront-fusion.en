---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: fusion
navigation-topic: workfront-fusion-navigation-topic
title: Troubleshooting custom extensions
description: Troubleshooting custom extensions
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

# Troubleshooting custom extensions

>[!NOTE]
>
>This article assumes some familiarity with software development tools. 

This article presents some solutions to the problems you are most likely to encounter while creating custom extensions, roughly in the order they occur during development.

## Quick checklist

If something does not work, verify these first:

* Node.js is version 18 or 20 (`node --version`).
* You are signed in (`aio login`) and on the correct org/project/workspace (`aio console where`).
* The extension point name matches exactly, including the version: `fusion/nav-organization/1`.
* The `url` in `getWidget()` matches a route in your app.
* Your visible UI calls `attach({ id })`.
* You are looking at the right set of extensions in Fusion:
   * To see a Stage build, deploy to Stage and turn on the Stage extensions switch in your Fusion profile (Product Settings > Fusion Profile > Preferences).
   * To see a published extension, deploy to Production and get it approved.

## Error 1060: "Extension point does not exist"

**Full message:** `CoreConsoleAPISDK ... 1060: Extension point 'fusion/nav-organization/1' does not exist` during `aio app deploy`.

**Meaning:** The Fusion extension point is not enabled ("onboarded") for your Adobe organization yet. Adobe validates, at deploy time, that the extension point exists in your organization's catalog. This is **not** a problem with your code or your YAML.

**Fix:** Ask the Fusion team to onboard the extension point(s) (`fusion/nav-organization/1` and/or `fusion/nav-team/1`) for your IMS organization. When you request onboarding, include:

* your **IMS organization id** (`XXXX@AdobeOrg`),
* the **extension point(s)** you need,
* your **Developer Console project and workspace** names.

Once onboarding is confirmed, re-run `aio app deploy`.


## "Awaiting initial message from target iframe" / the panel spins forever

**Meaning:** Fusion opened your visible UI but did not complete the handshake, so Fusion timed out.

**Common causes:**

* `attach` is only in the registration component, not in the visible widget.
* The `url` in `getWidget()` points to a route that renders the **registration** component (or a blank page) instead of your widget.
* The `id` passed to `attach` differs from the `id` used in `register`. They must be identical, so keep both in `Constants.js`.

**Fix:** Make sure your **visible** component calls `attach({ id })`:

```jsx
useEffect(() => {
  attach({ id: extensionId }).catch(console.error);
}, []);
```

For more information, see [Build the custom extension UI](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).



## The nav button does not appear in Fusion

If the navigation button for your custom extension does not appear in Fusion, check these items in order:

1. **Are you looking at the right set of extensions?** By default Fusion shows only published extensions, which have been deployed to Production and approved. If you are testing a Stage build, turn on the Stage extensions switch in your Fusion profile (Product Settings > Fusion Profile > Preferences) and reload. Stage items are labeled **(Stage)**. 
   For more information, see [Publish your custom extension](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. **Was it revoked or retracted?** A revoked or retracted extension stops appearing in Fusion with no error. If a previously working button disappeared, confirm it is still active in Adobe Exchange before looking for a code problem.
1. **Is it deployed to the correct workspace?** Deploy to the workspace you are actually loading, the Stage workspace when you are using the Stage testing switch.
1. **Is it deployed to the correct organization?** Sign in to Fusion with an account in the **same** IMS organization you deployed to.
1. **Is it in the correct section?** `fusion/nav-organization/1` shows under **Organization**; `fusion/nav-team/1` shows under **Team** (you must select a team first).
1. **Is there an extension point name typo?** It must read exactly `fusion/nav-organization/1` in both `app.config.yaml` and the folder's `ext.config.yaml` include path.


## The button appears but the panel is blank

If the button appears but the panel is blank, check for the following:

* **Route mismatch:** the `url` from `getWidget()` (such as `/index.html#/my-widget`) must match a `<Route>` in `App.js`. A mismatch loads a page with no component.
* **JavaScript error:** open your browser's developer tools (F12) > **Console** tab, and look for errors coming from the iframe. Fix the reported error and redeploy.
* **Header missing/duplicated:** `hideWidgetHeader` in `getWidget()` controls whether Fusion shows the title above your UI. Set it to `true` if you render your own header.

## The iframe is blocked (Content Security Policy / "refused to frame")

Fusion only allows extensions hosted on Adobe's App Builder CDN (`*.adobeio-static.net`), which is where `aio app deploy` puts your files by default. If you host your UI somewhere else, such as a custom domain, Fusion refuses to load it. Either deploy through App Builder as documented, or ask the Fusion team whether your domain can be allowlisted.

## Context is empty or stale

* **Empty right after load:** Read the context **after** `attach` resolves, not before. Until then, show a "Connecting…" state.
* **Not updating when the user switches organization or team:** Subscribe to the `contextchange` event and re-read your keys inside the handler. For more information, see  [Read the context Fusion shares](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md#read-the-context-fusion-shares) in the article Build the custom extension UI.
* **Dates look wrong:** Date fields arrive as ISO **strings**, not `Date` objects. Wrap them in `new Date(...)`. See [Dates](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md#dates) in the article The Fusion context reference.

## Calling an API fails with a CORS error

**Symptom:** The browser Console shows *"No 'Access-Control-Allow-Origin' header"* (or the request is blocked) when your UI calls a Workfront/Fusion API directly.

**Fix:** Do not call those APIs from the browser. Route the call through your own App Builder **runtime action** (server-side, no CORS) and have the guest call the action with a relative, same-origin URL. For more information, see [Calling Workfront and Fusion APIs](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).


## Proxy action returns 401 even with a valid token

**Meaning:** With `require-adobe-auth: true`, Adobe's gateway validates the call before your action runs and can reject it or drop custom headers your upstream needs, surfacing as a `401`.

**Fix:** Set `require-adobe-auth: false` on the action **and** enforce authorization yourself. Require an `Authorization` bearer in the action, forward it upstream, and keep a strict target allowlist. See [require-adobe-auth: true vs. false](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#require-adobe-auth-true-vs-false).

## Fusion `GET /api/v3/hooks` returns 400

**Meaning:** The hooks endpoint is **team-scoped**, so `teamId` is a required query parameter.

**Fix:** Call `/api/v3/hooks?teamId=<team.id>`. Hooks come back for the active team only. To cover an organization, loop its teams and merge. Scenarios, by contrast, accept `organizationId`. See [Fusion v3 API specifics](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#fusion-v3-api-specifics).


## `aio` errors

* **`aio: command not found`:** The CLI is not installed or not on your PATH. Re-run `npm install -g @adobe/aio-cli`, then open a new terminal.
* **Build/deploy fails on a brand-new Node version:** Use Node **18 or 20 LTS**. Very new, non-LTS releases sometimes break the toolchain.
* **"You are not a developer" / cannot see your org:** Your Adobe org admin must grant you the **Developer** role and App Builder access. For more information, see [Set up UI Extension tools and account](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
* **401 / invalid token during deploy or discovery:** Your session expired or you are mixing environments. Run `aio logout` then `aio login`, confirm `aio console where`, and deploy to the workspace you are loading.

## Collecting information for support

Collect this information to make diagnosis much faster:

* The exact command you ran and the **full** error output.
* Your **IMS organization ID**, **project**, and **workspace**.
* The **extension point** you are targeting.
* Whether `aio app deploy` succeeded, and whether the extension is **published** (or, for a Stage test, whether the Stage extensions switch is on).
* Any errors in the browser **Console** (F12) when opening the panel in Fusion.
