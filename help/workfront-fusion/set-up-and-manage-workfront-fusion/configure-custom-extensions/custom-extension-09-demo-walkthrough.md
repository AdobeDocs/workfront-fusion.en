---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: fusion
navigation-topic: workfront-fusion-navigation-topic
title: Troubleshooting custom extensions
description:  Troubleshooting custom extensions
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

# Demo walkthrough of creating a custom extension in Fusion

>[!NOTE]
>
>This article assumes some familiarity with software development tools. 

This demo walks through creating a custom extension, deploying it, and running it in Fusion.

It includes:

* Scaffold an App Builder app from the generic Experience Cloud Shell template
* Retarget the app to a Fusion extension point
* Deploy the app to Stage
* Show the app running inside Fusion

Starting from the template rather than an empty `--standalone-app` means the SPA bootstrap is generated for you:  `index.js`, `exc-runtime.js`, `App.js` with routing and `ErrorBoundary`, and a sample `ExtensionRegistration`. Live steps in the demo are to retarget the config and edit two files, which is exactly how the real `fusion-uix-guest` was built.

>[!NOTE]
>
> **Time:** The live demo takes around 10 minutes after your tools are set up. You must do the one-time setup  (Node 18/20, `aio` CLI, `aio login`) **before** the demo. For instructions, see [Set up UI Extension tools and account](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).


## Before you start

This needs to be done only once, and can be done off-camera before your demo.

```sh
node --version          # must be 18 or 20
aio --version           # @adobe/aio-cli installed
aio login               # signs you into your Adobe org
aio console org select  # pick the org you'll demo in (same org as Fusion)
```

Two things must be true in the demo org:

* The `fusion/nav-organization/1` extension point is onboarded for the org. If it is not onboarded, deploy fails with error 1060. FOr more information, see [Troubleshooting custom extensions](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).
* In the Fusion host, the `fusion-ui-extensions` Split flag is **on** (it defaults to `on`). The host discovers from the Stage workspace and auto-selects the stage vs. prod App Registry from your IMS token, so a Stage deploy is all you need to demo.

## Step 1: Generate the app from the generic template

```sh
aio app init my-fusion-extension --template @adobe/generator-app-excshell
cd my-fusion-extension
```

* Select **Create new project** when prompted, and accept the suggested name.
* `@adobe/generator-app-excshell` is the generic **Experience Cloud Shell** UI-extension template and is not product-specific. It scaffolds a complete, working SPA under `src/dx-excshell-1/`.

>[!NOTE]
>
>If you Prefer the menu, run `aio app init my-fusion-extension`, choose **Add extensions or standalone app** > **Templates**, and select **"App Builder UIX Extension for Experience Cloud Shell"**.

You will get a set of files, including the following:

```
my-fusion-extension/
|-- app.config.yaml
|-- src/dx-excshell-1/
    |-- ext.config.yaml
    |-- web-src/src/
        |-- index.js          // SPA bootstrap (exc-app Runtime + React render)
        |-- exc-runtime.js    // Experience Cloud Shell runtime glue
        |-- components/
            |-- App.js                    // Router + ErrorBoundary (generated)
            |-- ExtensionRegistration.js  // sample registration (generated)
```

## Step 2: Add the Fusion guest library

The template already includes React, React Spectrum and exc-app. Add the one library that talks to the Fusion host:

```sh
npm install @adobe/uix-guest
```

## Step 3: Retarget the config to Fusion

Open **`app.config.yaml`** and change **only the extension-point key** from the Experience Cloud Shell point to the Fusion one (leave the `$include` path as-is):

```yaml
extensions:
  fusion/nav-organization/1:                 # was: dx/excshell/1
    $include: src/dx-excshell-1/ext.config.yaml
```

You do not need to change anything else in the config. The folder name `dx-excshell-1` is internal and doesn't affect Fusion, so you can leave it. Rrenaming would also mean updating any action paths. Skip that for the demo.

>[!NOTE]
>
>If you are targeting the **Team** section, use `fusion/nav-team/1` instead. To ship **both** org and team in production, use **two separate projects**. One extension-point bundle per registry name avoids a shared-app collision.

## Step 4: Edit registration and widget files

All paths are under `src/dx-excshell-1/web-src/src/components/`.

### **`ExtensionRegistration.js`**

The generated file registers an Experience Cloud Shell sample. Replace its `methods` with the Fusion **`dashboard.getWidget`** contract so Fusion knows your title and where the UI lives:

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

  return <Text>Registering with Fusionâ&euro;¦</Text>;
}

export default ExtensionRegistration;
```

If `Constants.js` doesn't exist next to it, create it:

```js
module.exports = { extensionId: "my-fusion-extension" };
```

### `DashboardWidget.js`

Create this file. It completes the handshake and shows the live Fusion context:

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
      <Heading level={2}>Hello from App Builder ðŸ'‹</Heading>
      {!ctx ? (
        <Text>Connecting to Fusionâ&euro;¦</Text>
      ) : (
        <Flex direction="column" gap="size-100" marginTop="size-200">
          <Text>User: {ctx.user?.name ?? ctx.imsUserId}</Text>
          <Text>Organization: {ctx.organization?.name} (id {ctx.organization?.id})</Text>
          <Text>Team: {ctx.team?.name ?? "â&euro;""}</Text>
        </Flex>
      )}
    </View>
  );
}
```

## `App.js`

The generated router already sends `index` / `index.html` to `ExtensionRegistration`. Add a route for the widget and import it:

```js
import DashboardWidget from "./DashboardWidget";
// ...inside <Routes>, alongside the existing ExtensionRegistration routes:
<Route exact path="widget" element={<DashboardWidget />} />
```

> The route path (`widget`) must match the hash in `getWidget().url` (`/index.html#/widget`). Keep the generated `index.js` / `exc-runtime.js` and the rest of `App.js` exactly as scaffolded because that's the bootstrap you wanted the template to provide.

## Step 5: Build

```sh
aio app build
```

This compiles the front-end and runs the metadata hook that generates `app-metadata.json`. Fix any errors before continuing.

## Step 6: Deploy to Stage

```sh
aio console workspace select     # choose Stage
aio app deploy
```

`deploy` hosts your UI on Adobe's CDN and registers the extension endpoint in the Stage workspace, which is what lets Fusion discover it. The CLI prints the endpoint URL, such as `https://<project>-stage.adobeio-static.net`.

## Step 7: Show the extension in Fusion

1. Open Fusion on the Experience Cloud, signed in to the same organization you deployed to.
1. Go to the **Organization** area of the left navigation.

   Your **"My Fusion tool"** button appears
1. Click the **My Fusion tool** button.
1. Your UI loads in the main panel and shows the live user, organization, and team.
1. **Switch the active organization or team** in Fusion.

   The panel updates, demonstrating live context (`contextchange`).

>[!TIP]
>
>If the button does not appear, hard-refresh once, because discovery is cached per session. Then see [Troubleshooting custom extensions](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).


## Iterating during the demo

Make a change, then rebuild and redeploy.  Users see the updated extension next time they open it.

```sh
aio app build && aio app deploy
```

## Going to Production after the demo

Stage is enough to demo. To release organization-wide, switch to the Production workspace, deploy, and submit the approval request. The request must be submitted using a System Administrator role. For the full process, see  [Release on Production](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md#release-on-production).

## Demo talk-track (optional)

You may want to make the following points during your live demo:

* **"I started from the generic Experience Cloud Shell template."** It scaffolds the whole SPA shell, so I only retargeted the extension point and edited two files.
* **"Fusion is the host, my app is the guest."** They run in separate frames and talk over Adobe's UI Extensibility SDK â&euro;" no custom networking.
* **"Registration vs. view."** The hidden frame *registers* what I offer (`dashboard.getWidget`), and the visible frame *attaches* and reads context.
* **"Stage is enough."** The host reads the Stage workspace and auto-picks the stage/prod registry from my token, so I didn't need a production release.
* **"Live context."** Switching org or team re-sends context, and the guest re-renders.
