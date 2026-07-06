# 9. Demo walkthrough (generate → deploy → run in Fusion)

A single, linear, copy-paste script for a **live demo**: scaffold an App Builder
app from the generic **Experience Cloud Shell** template, retarget it to a Fusion
extension point, deploy to Stage, and show it running inside Fusion.

Starting from the template (rather than an empty `--standalone-app`) means the
SPA bootstrap is generated for you — `index.js`, `exc-runtime.js`, `App.js` with
routing + `ErrorBoundary`, and a sample `ExtensionRegistration`. Your live steps
become **"retarget the config + edit two files,"** which is exactly how the real
`fusion-uix-guest` was built.

> **Time:** ~10 minutes once your tools are set up. Do the one-time
> [setup](./02-setup.md) (Node 18/20, `aio` CLI, `aio login`) **before** the demo.

---

## Before you start (one-time, off-camera)

```sh
node --version          # must be 18 or 20
aio --version           # @adobe/aio-cli installed
aio login               # signs you into your Adobe org
aio console org select  # pick the org you'll demo in (same org as Fusion)
```

Two things must be true in the demo org:

- The `fusion/nav-organization/1` extension point is **onboarded** for the org
  (otherwise deploy fails with error 1060 — see [troubleshooting](./08-troubleshooting.md)).
- In the Fusion host, the `fusion-ui-extensions` Split flag is **on** (it
  defaults to `on`). The host discovers from the **Stage** workspace and
  auto-selects the stage vs. prod App Registry from your IMS token, so a Stage
  deploy is all you need to demo.

---

## Step 1 — Generate the app from the generic template

```sh
aio app init my-fusion-extension --template @adobe/generator-app-excshell
cd my-fusion-extension
```

- Pick **Create new project** when prompted; accept the suggested name.
- `@adobe/generator-app-excshell` is the generic **Experience Cloud Shell**
  UI-extension template — not product-specific. It scaffolds a complete, working
  SPA under `src/dx-excshell-1/`.

> **Prefer the menu?** Run `aio app init my-fusion-extension`, choose
> **"Add extensions or standalone app" → templates**, and select
> **"App Builder UIX Extension for Experience Cloud Shell"**.

What you get (the parts that matter):

```
my-fusion-extension/
├── app.config.yaml
└── src/dx-excshell-1/
    ├── ext.config.yaml
    └── web-src/src/
        ├── index.js          ← SPA bootstrap (exc-app Runtime + React render)
        ├── exc-runtime.js    ← Experience Cloud Shell runtime glue
        └── components/
            ├── App.js                    ← Router + ErrorBoundary (generated)
            └── ExtensionRegistration.js  ← sample registration (generated)
```

## Step 2 — Add the Fusion guest library

The template already includes React, React Spectrum and exc-app. Add the one
library that talks to the Fusion host:

```sh
npm install @adobe/uix-guest
```

## Step 3 — Retarget the config to Fusion

Open **`app.config.yaml`** and change **only the extension-point key** from the
Experience Cloud Shell point to the Fusion one (leave the `$include` path as-is):

```yaml
extensions:
  fusion/nav-organization/1:                 # was: dx/excshell/1
    $include: src/dx-excshell-1/ext.config.yaml
```

That's the only config change. The folder name `dx-excshell-1` is internal and
doesn't affect Fusion, so we leave it (renaming would also mean updating any
action paths — skip that for the demo).

> Targeting the **Team** section? Use `fusion/nav-team/1` instead. To ship
> **both** org and team in production, use **two separate projects** (one
> extension-point bundle per registry name avoids a shared-app collision).

## Step 4 — Edit two files (registration + widget)

All paths are under `src/dx-excshell-1/web-src/src/components/`.

**4a. `ExtensionRegistration.js`** — the generated file registers an Experience
Cloud Shell sample. Replace its `methods` with the Fusion **`dashboard.getWidget`**
contract so Fusion knows your title and where the UI lives:

```js
import { Text } from "@adobe/react-spectrum";
import { register } from "@adobe/uix-guest";
import metadata from "../../../../app-metadata.json";
import { extensionId } from "./Constants";

function ExtensionRegistration() {
  const init = async () => {
    await register({
      id: extensionId,
      metadata,
      methods: {
        dashboard: {
          getWidget() {
            return {
              id: extensionId,
              title: "My Fusion tool",          // label on the Fusion nav button
              description: "Hello from App Builder",
              url: "/index.html#/widget",       // route to the visible UI (4b)
              widgetSize: { defaultWidth: 6, defaultHeight: 6 },
              hideWidgetHeader: false,
            };
          },
        },
      },
    });
  };
  init().catch(console.error);

  return <Text>Registering with Fusion…</Text>;
}

export default ExtensionRegistration;
```

If `Constants.js` doesn't exist next to it, create it:

```js
module.exports = { extensionId: "my-fusion-extension" };
```

**4b. `DashboardWidget.js`** — create this; it completes the handshake and shows
the live Fusion context:

```js
import { useEffect, useState } from "react";
import { Flex, Heading, Text, View } from "@adobe/react-spectrum";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

export default function DashboardWidget() {
  const [ctx, setCtx] = useState(null);

  useEffect(() => {
    attach({ id: extensionId })
      .then((guest) => {
        const read = () =>
          KEYS.reduce((acc, k) => ({ ...acc, [k]: guest.sharedContext.get(k) }), {});
        setCtx(read());
        guest.addEventListener("contextchange", () => setCtx(read()));
      })
      .catch((e) => console.error("attach failed", e));
  }, []);

  return (
    <View padding="size-300">
      <Heading level={2}>Hello from App Builder 👋</Heading>
      {!ctx ? (
        <Text>Connecting to Fusion…</Text>
      ) : (
        <Flex direction="column" gap="size-100" marginTop="size-200">
          <Text>User: {ctx.user?.name ?? ctx.imsUserId}</Text>
          <Text>Organization: {ctx.organization?.name} (id {ctx.organization?.id})</Text>
          <Text>Team: {ctx.team?.name ?? "—"}</Text>
        </Flex>
      )}
    </View>
  );
}
```

**4c. `App.js`** — the generated router already sends `index` / `index.html` to
`ExtensionRegistration`. Add a route for the widget and import it:

```js
import DashboardWidget from "./DashboardWidget";
// ...inside <Routes>, alongside the existing ExtensionRegistration routes:
<Route exact path="widget" element={<DashboardWidget />} />
```

> The route path (`widget`) must match the hash in `getWidget().url`
> (`/index.html#/widget`). Keep the generated `index.js` / `exc-runtime.js` and
> the rest of `App.js` exactly as scaffolded — that's the bootstrap you wanted
> the template to provide.

## Step 5 — Build

```sh
aio app build
```

Compiles the front-end and runs the metadata hook that generates
`app-metadata.json`. Fix any errors before continuing.

## Step 6 — Deploy to Stage

```sh
aio console workspace select     # choose Stage
aio app deploy
```

`deploy` hosts your UI on Adobe's CDN **and** registers the extension endpoint in
the Stage workspace (this is what lets Fusion discover it). The CLI prints the
endpoint URL, e.g. `https://<project>-stage.adobeio-static.net`.

## Step 7 — Show it in Fusion

1. Open Fusion (Experience Cloud) signed in to the **same org** you deployed to.
2. Go to the **Organization** area of the left nav.
3. Your **"My Fusion tool"** button appears — click it.
4. Your UI loads in the main panel and shows the live user/org/team.
5. **Switch the active organization or team** in Fusion → the panel updates,
   demonstrating live context (`contextchange`).

> Not appearing? Hard-refresh once (discovery is cached per session). Then see
> [Troubleshooting](./08-troubleshooting.md).

---

## Iterating during the demo

Make a change, then rebuild + redeploy; users pick it up on next open:

```sh
aio app build && aio app deploy
```

## Going to Production (after the demo)

Stage is enough to demo. To release org-wide, switch to the Production workspace,
deploy, and submit the approval request (System Administrator role). Full steps:
[Publish your extension → Part B](./07-publish.md#part-b--release-on-production).

## Demo talk-track (optional)

- **"I started from the generic Experience Cloud Shell template."** It scaffolds
  the whole SPA shell, so I only retargeted the extension point and edited two
  files.
- **"Fusion is the host, my app is the guest."** They run in separate frames and
  talk over Adobe's UI Extensibility SDK — no custom networking.
- **"Registration vs. view."** The hidden frame *registers* what I offer
  (`dashboard.getWidget`); the visible frame *attaches* and reads context.
- **"Stage is enough."** The host reads the Stage workspace and auto-picks the
  stage/prod registry from my token, so I didn't need a production release.
- **"Live context."** Switching org/team re-sends context; the guest re-renders.
