Readme

# Build a custom UI extension for Adobe Workfront Fusion

Fusion can display **your own web UI** inside its interface. You build a small web app (an "extension"), publish it to Adobe, and it shows up as a button in Fusion's navigation. When a user clicks it, your UI loads in the main area of Fusion and automatically receives information about who is signed in, which organization and team they are working in, and more.

This guide walks you through the whole process, from zero to a published extension, **without assuming prior experience** with Adobe App Builder or front-end frameworks. Where a step needs code, we explain what each piece does.

## Who this guide is for

* People who want to add a custom screen or tool to Fusion.
* You do **not** need to be an expert developer. You do need to be comfortable copying commands into a terminal and editing a few text files.
* You will need an Adobe ID and access to an Adobe organization (the same kind of access you use to sign in to Fusion).

## What you will build

By the end of this guide you will have:

1. A free Adobe **App Builder** project (this is where your extension lives).
2. A small web app that renders your custom UI.
3. That web app connected to one of Fusion's **extension points** so it appears in the Fusion navigation.
4. Your UI reading live **context** from Fusion (current user, organization, team) and reacting when the user switches org or team.
5. The extension **published** so other users in your organization can see it.

## How it works, in one picture

```
  Fusion (the "Host")                         Your extension (the "Guest")
  â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€                         â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€
  Left navigation                             A web app hosted by Adobe
   â””â”€ Organization                            (App Builder + UI Extensibility)
       â””â”€ [Your extension button]  â”€â”€ click â”€â–¶ Fusion opens your UI in an iframe
                                              and sends it live context:
                                               * signed-in user
                                               * active organization
                                               * active team
                                               * Adobe IMS identifiers
```

Fusion is the **host**. Your extension is the **guest**. They run in separate browser frames and talk to each other through Adobe's **UI Extensibility SDK** (no custom networking required on your side).

## Table of contents

Read the pages in order the first time. Later you can jump straight to the one you need.

| # | Page | What it covers |
|---|------|----------------|
| 1 | [Overview & key concepts](./01-overview.md) | The vocabulary (host, guest, extension point), the architecture, and what each Fusion extension point is for. |
| 2 | [Set up your tools & Adobe account](./02-setup.md) | Node.js, the Adobe I/O CLI, signing in, and creating your project in the Adobe Developer Console. |
| 3 | [Create the project](./03-create-project.md) | Generate a generic App Builder project with the `aio` command line (not a product-specific template). |
| 4 | [Configure it for Fusion](./04-configure-for-fusion.md) | Point your project at a Fusion extension point and register your widget. |
| 5 | [Build the UI](./05-build-the-ui.md) | Render your custom screen and complete the connection ("handshake") with Fusion. |
| 6 | [The Fusion context reference](./06-fusion-context-reference.md) | Every field Fusion sends you, what it means, and how to react to changes. |
| 7 | [Publish your extension](./07-publish.md) | Build, deploy, and make your extension visible in Fusion. |
| 8 | [Troubleshooting](./08-troubleshooting.md) | Fixes for the most common errors. |

## Availability note

Fusion currently exposes these extension points:

* `fusion/nav-organization/1` â€” appears under the **Organization** section.
* `fusion/nav-team/1` â€” appears under the **Team** section.

Before you can publish against one of these, the extension point must be enabled ("onboarded") for your Adobe organization. If your publish step fails saying the extension point "does not exist," see [Troubleshooting](./08-troubleshooting.md).

## Official Adobe documentation

This guide is Fusion-specific. For the underlying platform, the canonical references are:

* [UI Extensibility overview](https://developer.adobe.com/uix/docs/)
* [UI Extension development flow](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [UI Extensions Management (publish / approve / revoke)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Adobe App Builder getting started](https://developer.adobe.com/app-builder/docs/getting_started/)
