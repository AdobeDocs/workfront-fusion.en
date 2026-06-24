# 3. Create the project

In this step you generate a **generic** App Builder project with the `aio`
command line. "Generic" means we do **not** start from a product-specific
template (such as the AEM template). Starting generic keeps the project simple
and lets us wire it to Fusion ourselves in the next page, which is the part you
most want to understand.

## Step 1 — Pick a folder and run `aio app init`

Open a terminal, move to the folder where you keep projects, and run:

```sh
aio app init my-fusion-extension --standalone-app
```

- `my-fusion-extension` is the folder/app name. Choose anything you like
  (lowercase, hyphens, no spaces).
- `--standalone-app` tells the CLI to create a **plain application skeleton**
  instead of asking you to pick a product template. This is the key to avoiding
  the AEM (or any other) template.

The command will:

1. Ask you to **select your Organization** (if you belong to more than one).
2. Ask you to **select or create a Project** — choose **Create new project** and
   accept the suggested name, or pick an existing empty project.
3. Set up the **Stage** and **Production** workspaces automatically.
4. Generate files into the `my-fusion-extension` folder and run `npm install`.

> **If you prefer the interactive menu:** run `aio app init my-fusion-extension`
> (without `--standalone-app`). When it asks **"What templates do you want to
> search for?"** or shows a checklist of templates, **do not** select a
> product template like *AEM*. Choose the option to create a **standalone
> application** / **"All extension points → none"**. The goal is an empty
> skeleton you control.

## Step 2 — Look at what was created

Move into the folder:

```sh
cd my-fusion-extension
```

You will see a structure similar to this (some files omitted):

```
my-fusion-extension/
├── app.config.yaml        ← main configuration (you will edit this)
├── package.json           ← dependencies and scripts
├── src/                   ← your source code
└── web-src/  or  src/.../web-src/   ← front-end files (HTML/JS)
```

The two files you care about most are:

- **`app.config.yaml`** — the central configuration. In the next page you add an
  `extensions:` section here that connects your app to a Fusion extension point.
- **`package.json`** — lists the libraries your app uses. You will add the
  Adobe UI Extensibility guest library here.

> Don't worry if your generated layout differs slightly between CLI versions.
> The next page tells you exactly which files to create and what to put in them,
> so you can match the expected structure regardless of the starting point.

## Step 3 — Add the libraries you need

Your extension needs two libraries:

- **`@adobe/uix-guest`** — lets your app talk to Fusion (the host).
- **`@adobe/react-spectrum`** — Adobe's React UI components, so your screen
  matches Adobe's look and feel. (Optional, but recommended; you can use plain
  HTML instead.)

Install them:

```sh
npm install @adobe/uix-guest @adobe/react-spectrum
```

If your generated project does not already include React, also install it:

```sh
npm install react react-dom react-router-dom
```

## Step 4 — Confirm the project builds

Before changing anything, make sure the empty project builds:

```sh
aio app build
```

If this completes without errors, your tools and project are healthy. You are
ready to connect it to Fusion.

> **Build fails?** The most common cause is an unsupported Node.js version. Run
> `node --version` and make sure it is 18 or 20 (see
> [Set up your tools](./02-setup.md)). For other errors, see
> [Troubleshooting](./08-troubleshooting.md).

Next: [Configure it for Fusion →](./04-configure-for-fusion.md)

# 4. Configure it for Fusion

This page connects your generic project to Fusion. You will:

1. Create a folder for your extension.
2. Tell App Builder about a Fusion **extension point** (in `app.config.yaml`).
3. Describe your extension's pieces (in `ext.config.yaml`).
4. **Register** your widget so Fusion knows its title and where its UI lives.

We use `fusion/nav-organization/1` throughout. To target the Team section
instead, swap in `fusion/nav-team/1` everywhere. To support both, repeat the
pattern for each.

## The folder layout you are aiming for

Create your files so the project looks like this:

```
my-fusion-extension/
├── app.config.yaml
└── src/
    └── fusion-nav-organization-1/          ← one folder per extension point
        ├── ext.config.yaml
        └── web-src/
            └── src/
                └── components/
                    ├── App.js
                    ├── ExtensionRegistration.js
                    ├── DashboardWidget.js
                    └── Constants.js
```

Naming the folder after the extension point (`fusion-nav-organization-1`) keeps
things obvious, but the exact name is up to you, as long as it matches what you
reference in `app.config.yaml`.

## Step 1 — Declare the extension point in `app.config.yaml`

Open `app.config.yaml` and make its contents look like this:

```yaml
extensions:
  fusion/nav-organization/1:
    $include: src/fusion-nav-organization-1/ext.config.yaml
```

What this says:

- `extensions:` — this app implements one or more extension points.
- `fusion/nav-organization/1` — the Fusion slot you are plugging into. **The
  name must match exactly**, including the `1` version.
- `$include:` — points to a second config file (next step) that describes this
  extension's contents. Keeping it in a separate file keeps `app.config.yaml`
  clean and lets you add more extension points later.

> **Targeting both sections?** List both, each with its own folder:
>
> ```yaml
> extensions:
>   fusion/nav-organization/1:
>     $include: src/fusion-nav-organization-1/ext.config.yaml
>   fusion/nav-team/1:
>     $include: src/fusion-nav-team-1/ext.config.yaml
> ```

## Step 2 — Describe the extension in `ext.config.yaml`

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

- **`operations.view`** — declares that your extension provides a **view** (a
  visible UI), served from `index.html`. This is what makes your extension show
  a screen rather than run only in the background.
- **`web: web-src`** — the folder that holds your front-end files. App Builder
  builds everything under here and hosts it on Adobe's CDN.
- **`hooks`** — small commands that run automatically at build/run time. The
  `generate-metadata.js` script ships with `@adobe/uix-guest`; it produces an
  `app-metadata.json` file that your registration code needs (see Step 4). You
  do not write this script; you just reference it.

> **Need server-side logic too?** You can also add serverless `actions` (small
> backend functions). They are optional and not required to render a UI, so we
> leave them out to keep this guide focused. If you add them later, declare an
> `actions:` folder here and a `runtimeManifest:` in `app.config.yaml`.

## Step 3 — Set a stable extension id

Your extension needs a unique id that both frames share. Create
`src/fusion-nav-organization-1/web-src/src/components/Constants.js`:

```js
module.exports = {
  extensionId: 'my-fusion-extension'
};
```

Use the same value everywhere your code refers to the extension id.

## Step 4 — Register your widget

"Registration" is how the hidden background frame tells Fusion what your
extension offers. You declare a `dashboard.getWidget()` method that returns your
widget's title and the URL of its visible UI.

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

- **`title`** is the label Fusion puts on the navigation button. If
  `hideWidgetHeader` is `false`, Fusion also shows the title as a header above
  your UI.
- **`url`** is the route to your *visible* UI inside this same app. Here it is a
  hash route (`#/my-widget`) handled by your front-end router (set up on the
  next page). It must resolve to the component that renders your screen.
- **`metadata`** comes from `app-metadata.json`, which the `generate-metadata`
  hook creates for you at build time. Just import it as shown.
- The `dashboard.getWidget` method name is the agreed contract Fusion calls to
  discover your widget. Keep the `dashboard` namespace and `getWidget` name.

You now have the wiring. Next you build the actual screen and connect it to
Fusion.

Next: [Build the UI →](./05-build-the-ui.md)