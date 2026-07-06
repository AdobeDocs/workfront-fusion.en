---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: fusion
navigation-topic: workfront-fusion-navigation-topic
title: Create a project for UI Extensibility
description:  Create a project for UI Extensibility
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
#  Create a project for UI Extensibility

To create a custom UI extension, you must create an App Builder project for it.

This page describes how to generate a generic App Builder project with the `aio` command line. "Generic" means the project does **not** start from a product-specific template. Starting with a generic app keeps the project simple and allows it to connect with Workfront Fusion.

It may be useful to familiarize yourself with the following concepts and terminology regarding creating a project for use with Adobe Fusion AI Extensibility.

* The **Adobe Developer Console** (<https://developer.adobe.com/console>) is the web dashboard where your project lives. 

* **Terminology**:

   | Term | What it means |
   | ------ | --------------- |
   | **Organization** | Your company's Adobe org. The same org you use in Fusion. |
   | **Project** | A container for one app/extension. You will create one project for your extension. |
   | **Workspace** | A copy of the project's configuration for a stage of work. Every project has a **Production** workspace, and you typically also use a **Stage** workspace for testing. Think of workspaces like "environments." |
   | **Credentials / Services** | Permissions your app is allowed to use. The defaults created for you are enough to start. |

* There are two ways to create a project:

   * **Automatic (recommended):** The command `aio app init` creates the project and workspaces for you while generating the code. This article describes this process.
   * **Manual:** You create the project yourself in the Developer Console first, then point `aio` at it. We recommend doing this only  if your organization requires projects to be created centrally.

* When deciding which workspace to use, we recommend starting in **Stage**. Fusion discovers Stage-published extensions during development and testing. You can promote to **Production** later. 

   For more information on promoting to production, see [Publish your extension](./07-publish.md).


## Run `aio app init`

1. Open a terminal.
1. In the terminal, move to the folder where you keep projects
1. Run:

   ```sh
   aio app init my-fusion-extension --standalone-app
   ```

   * `my-fusion-extension` is the folder/app name. You can select this name, but use lowercase letters, hyphens, and no spaces.
   * `--standalone-app` tells the CLI to create a **plain application skeleton** instead of asking you to pick a product template. This is the key to avoiding the AEM (or any other) template.

1. When prompted, **select your Organization** (if you belong to more than one).
1. When prompted, select **Create new project** and accept the suggested name, or pick an existing empty project.
   
   The command sets up the **Stage** and **Production** workspaces automatically.

   The command also generates files into the `my-fusion-extension` folder and runs `npm install`.

1. Continue to [Confirm project creation](#confirm-project-creation).

>[!NOTE]
>
> **If you prefer the interactive menu:** run `aio app init my-fusion-extension` > (without `--standalone-app`). When it asks **"What templates do you want to search for?"** or shows a checklist of templates, do not select a product template like AEM. Choose the option to create a **standalone application** / **"All extension points &rarr; none"**.

## Check project creation

1. In the terminal, move into the created folder:

   ```sh
   cd my-fusion-extension
   ```

   You should see a structure similar to this (some files omitted):

   ```
   my-fusion-extension/
   |--- app.config.yaml   // main configuration (you will edit this)
   |---  package.json   //dependencies and scripts
   |---  src/    // your source code
   |---  web-src/  or  src/.../web-src/  // front-end files (HTML/JS)
   ```

   The two files you care about most are:

   * **`app.config.yaml`**: The central configuration. Later in the process you will add an `extensions:` section here that connects your app to a Fusion extension point.
   * **`package.json`**: Lists the libraries your app uses. You will add the Adobe UI Extensibility guest library here.

1. Continue to [Add required libraries](#add-required-libraries).

>[!TIP]
>
> Don't worry if your generated layout differs slightly between CLI versions. This procedure tells you exactly which files to create and what to put in them, so you can match the expected structure regardless of the starting point.

## Add required libraries

Your extension needs two libraries:

* **`@adobe/uix-guest`**: Lets your app talk to Fusion (the host).
* **`@adobe/react-spectrum`**: Adobe's React UI components, so your screen matches Adobe's look and feel. (Optional, but recommended; you can use plain HTML instead.)

To install these libraries:

1. In the terminal, run:

   ```sh
   npm install @adobe/uix-guest @adobe/react-spectrum
   ```

1. (Conditional) If your generated project does not already include React, also install it:

   ```sh
   npm install react react-dom react-router-dom
   ``` 

1. Continue to [Confirm the project builds](#confirm-the-project-builds).

## Confirm the project builds

Before changing anything, make sure the empty project builds

1. In the terminal, run:

   ```sh
   aio app build
   ```

If this completes without errors, your tools and project are correctly configured. You are ready to connect the project it to Fusion.

>[!TIP]
>
> **If the build fails,** the most common cause is an unsupported Node.js version. Run `node --version` and make sure it is 18 or 20 (see [Set up your tools]()). For other errors, see [Troubleshooting]().

<!--BECKY START HERE-->

Next: [Configure it for Fusion â†'](./04-configure-for-fusion.md)

# 4. Configure it for Fusion

This page connects your generic project to Fusion. You will:

1. Create a folder for your extension.
2. Tell App Builder about a Fusion **extension point** (in `app.config.yaml`).
3. Describe your extension's pieces (in `ext.config.yaml`).
4. **Register** your widget so Fusion knows its title and where its UI lives.

We use `fusion/nav-organization/1` throughout. To target the Team section instead, swap in `fusion/nav-team/1` everywhere. To support both, repeat the pattern for each.

## The folder layout you are aiming for

Create your files so the project looks like this:

```
my-fusion-extension/
â"œâ"&euro;â"&euro; app.config.yaml
â""â"&euro;â"&euro; src/
    â""â"&euro;â"&euro; fusion-nav-organization-1/          â† one folder per extension point
        â"œâ"&euro;â"&euro; ext.config.yaml
        â""â"&euro;â"&euro; web-src/
            â""â"&euro;â"&euro; src/
                â""â"&euro;â"&euro; components/
                    â"œâ"&euro;â"&euro; App.js
                    â"œâ"&euro;â"&euro; ExtensionRegistration.js
                    â"œâ"&euro;â"&euro; DashboardWidget.js
                    â""â"&euro;â"&euro; Constants.js
```

Naming the folder after the extension point (`fusion-nav-organization-1`) keeps things obvious, but the exact name is up to you, as long as it matches what you reference in `app.config.yaml`.

## Step 1 â&euro;" Declare the extension point in `app.config.yaml`

Open `app.config.yaml` and make its contents look like this:

```yaml
extensions:
  fusion/nav-organization/1:
    $include: src/fusion-nav-organization-1/ext.config.yaml
```

What this says:

* `extensions:` â&euro;" this app implements one or more extension points.
* `fusion/nav-organization/1` â&euro;" the Fusion slot you are plugging into. **The name must match exactly**, including the `1` version.
* `$include:` â&euro;" points to a second config file (next step) that describes this extension's contents. Keeping it in a separate file keeps `app.config.yaml` clean and lets you add more extension points later.

> **Targeting both sections?** List both, each with its own folder:
>
> ```yaml
> extensions:
>   fusion/nav-organization/1:
>     $include: src/fusion-nav-organization-1/ext.config.yaml
>   fusion/nav-team/1:
>     $include: src/fusion-nav-team-1/ext.config.yaml
> ```

## Step 2 â&euro;" Describe the extension in `ext.config.yaml`

Create `src/fusion-nav-organization-1/ext.config.yaml` with:

```yaml
operations:
  view:
    - type: web
      impl: index.html
web: web-src
hooks:
  pre-app-build: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
  pre-app-run: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
```

What each part means:

* **`operations.view`**: Declares that your extension provides a **view** (a visible UI), served from `index.html`. This is what makes your extension show a screen rather than run only in the background.
* **`web: web-src`**: The folder that holds your front-end files. App Builder builds everything under here and hosts it on Adobe's CDN.
* **`hooks`**: Small commands that run automatically at build/run time. The `generate-metadata.js` script ships with `@adobe/uix-guest`; it produces an `app-metadata.json` file that your registration code needs (see Step 4). You do not write this script; you just reference it.

> **Need server-side logic too?** You can also add serverless `actions` (small backend functions). They are optional and not required to render a UI, so we leave them out to keep this guide focused. If you add them later, declare an `actions:` folder here and a `runtimeManifest:` in `app.config.yaml`.

## Step 3 â&euro;" Set a stable extension id

Your extension needs a unique id that both frames share. Create `src/fusion-nav-organization-1/web-src/src/components/Constants.js`:

```js
module.exports = {
  extensionId: 'my-fusion-extension'
};
```

Use the same value everywhere your code refers to the extension id.

## Step 4 â&euro;" Register your widget

"Registration" is how the hidden background frame tells Fusion what your extension offers. You declare a `dashboard.getWidget()` method that returns your widget's title and the URL of its visible UI.

Create `src/fusion-nav-organization-1/web-src/src/components/ExtensionRegistration.js`.
The important part is the `register(...)` call:

```js
import { register } from "@adobe/uix-guest";
import metadata from "../../../../app-metadata.json";
import { extensionId } from "./Constants";

async function init() {
  await register({
    id: extensionId,
    metadata,
    methods: {
      dashboard: {
        getWidget() {
          return {
            id: extensionId,
            title: "My Fusion tool",        // shown on the Fusion nav button
            description: "What this tool does",
            url: "/index.html#/my-widget",  // route to your visible UI
            hideWidgetHeader: false          // false = Fusion shows the title
          };
        }
      }
    }
  });
}

init().catch(console.error);
```

Key points:

* **`title`** is the label Fusion puts on the navigation button. If `hideWidgetHeader` is `false`, Fusion also shows the title as a header above your UI.
* **`url`** is the route to your *visible* UI inside this same app. Here it is a hash route (`#/my-widget`) handled by your front-end router (set up on the next page). It must resolve to the component that renders your screen.
* **`metadata`** comes from `app-metadata.json`, which the `generate-metadata` hook creates for you at build time. Just import it as shown.
* The `dashboard.getWidget` method name is the agreed contract Fusion calls to discover your widget. Keep the `dashboard` namespace and `getWidget` name.

You now have the wiring. Next you build the actual screen and connect it to Fusion.

Next: [Build the UI â†'](./05-build-the-ui.md)
