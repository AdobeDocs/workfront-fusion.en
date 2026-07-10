---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: fusion
navigation-topic: workfront-fusion-navigation-topic
title: "UI Extensibility overview"
description: Custom extensions in Workfront Fusion
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

# Custom UI extensions: article index

Fusion can display your own web UI inside its interface. You build a small web app, called an extension, publish it to Adobe, and it appears as a button in Fusion's navigation. When a user clicks it, your UI loads in the main area of Fusion and automatically receives information about who is signed in, which organization and team they are working in, and more.

This section of the fusion documentation walks you through the whole process, without assuming prior experience with Adobe App Builder or front-end frameworks. It also includes necessary code, along with explanations of that code.

## When to use this guide

Use this guide if you want to add a custom screen or tool to Fusion. You do not need to be an expert developer. You do need to be comfortable copying commands into a terminal and editing a few text files.

To create a custom UI extension, you will need an Adobe ID and access to an Adobe organization (the same kind of access you use to sign in to Fusion).

## What you will build

By the end of this guide you will have:

1. A free Adobe **App Builder** project. This is where your extension lives.
2. A small web app that renders your custom UI.
3. That web app connected to one of Fusion's extension points so it appears in the Fusion navigation.
4. Your UI reading live*context from Fusion, such as current user, organization, and team, and reacting when the user switches org or team.
5. The extension published so other users in your organization can see it.

<!--

## How it works, in one picture

```
  Fusion (the "Host")                         Your extension (the "Guest")
  â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;                         â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;â"&euro;
  Left navigation                             A web app hosted by Adobe
   â""â"&euro; Organization                            (App Builder + UI Extensibility)
       â""â"&euro; [Your extension button]  â"&euro;â"&euro; click â"&euro;â–¶ Fusion opens your UI in an iframe
                                              and sends it live context:
                                               * signed-in user
                                               * active organization
                                               * active team
                                               * Adobe IMS identifiers
```

Fusion is the **host**. Your extension is the **guest**. They run in separate browser frames and talk to each other through Adobe's **UI Extensibility SDK** (no custom networking required on your side).

-->

## Table of contents

Read the pages in order the first time. Later you can jump straight to the one you need.

| # | Page | What it covers |
| --- | ------ | ---------------- |
| 1 | [Overview and key concepts](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md) | The vocabulary , the architecture, and what each Fusion extension point is for. |
| 2 | [Set up your tools and Adobe account](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md) | Node.js, the Adobe I/O CLI, signing in, and creating your project in the Adobe Developer Console. |
| 3 | [Create the project and configure it for Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md) | Generate a generic App Builder project with the `aio` command line (not a product-specific template). Then, point your project at a Fusion extension point and register your widget. |
| 5 | [Build the UI](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md) | Render your custom screen and complete the connection ("handshake") with Fusion. |
| 6 | [The Fusion context reference](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md) | Every field Fusion sends you, what it means, and how to react to changes. |
| 7 | [Publish your extension](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md) | Build, deploy, and make your extension visible in Fusion. |
| 8 | [Troubleshooting](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md) | Fixes for the most common errors. |
| 9 | [Demo walkthrough](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-09-demo-walkthrough.md) | One linear, copy-paste script: scaffold from the generic Experience Cloud Shell template → retarget to Fusion → deploy to Stage → run in Fusion. Best for a live demo. |
| 10 | [Calling Workfront and Fusion APIs](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md) | Call backend APIs from your extension without hitting browser CORS, using a runtime-action proxy. Covers `require-adobe-auth`, Fusion v3 headers, and a worked example. |

## Availability note

Fusion currently exposes these extension points:

* `fusion/nav-organization/1` â&euro;" appears under the **Organization** section.
* `fusion/nav-team/1` â&euro;" appears under the **Team** section.

Before you can publish against one of these, the extension point must be onboarded for your Adobe organization. If your publish step fails saying the extension point "does not exist," see [Troubleshooting](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

## Official Adobe documentation

This guide is Fusion-specific. For the underlying platform, the canonical references are:

* [UI Extensibility overview](https://developer.adobe.com/uix/docs/)
* [UI Extension development flow](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [UI Extensions Management (publish / approve / revoke)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Adobe App Builder getting started](https://developer.adobe.com/app-builder/docs/getting_started/)
