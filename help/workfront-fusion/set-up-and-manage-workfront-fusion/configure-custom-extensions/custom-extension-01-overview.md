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
# UI Extensibility overview

UI Extensibility allows you to bring your custom logic and UI (user interface) into Adobe Workfront Fusion. By using Adobe App Builder, you can modify your organization's Workfront Fusion experience to better meet the needs of the organization, while still relying on the core functionality of Fusion.

This article gives an overview of UI Extensibility and how your custom extension communicates with Workfront Fusion. 

## Extension structure 

* [Hosts and Guests](#hosts-and-guests)
* [The technology underneath](#the-technology-underneath)

### Hosts and Guests

Fusion can display UI that was not created by the Workfront Fusion team. To ensure that these UI changes do not affect the core functionality of Fusion, the UI runs in its own isolated browser frame (an `<iframe>`), completely separate from Fusion's code.

* **Host**: The application that *contains* the extension. Here, that is **Fusion**. The host decides where extensions can appear and what data it will share with them.
* **Guest**: *Your* extension. It is a small web application that the host loads into an iframe.

When creating a UI Extension, you do not modify Fusion. You build and publish a guest, which Fusion can use after the guest is published.

### The technology underneath

Your guest is built with two Adobe technologies:

* **Adobe App Builder**: A free hosting and tooling platform for small web apps and serverless actions. Your extension is an App Builder app. App Builder gives you a place to host your UI (on Adobe's `*.adobeio-static.net` content delivery network) and a command line tool called `aio` to create, build, and publish it.
* **Adobe UI Extensibility SDK (UIX)**: The libraries that let the host and guest talk. You will use one package, `@adobe/uix-guest`, on your side. Fusion uses the matching `@adobe/uix-host` package on its side.

<!--

```
   ┌────────── Browser ─────────────────────────────┐
   │                                                                   │
   │   Fusion (Host)                      Your extension (Guest)       │
   │   ────────────                       ─────────────────────        │
   │   @adobe/uix-host   ◀── messages ──▶  @adobe/uix-guest            │
   │        │                                    │                     │
   │   renders an iframe ───────────────▶  your React/HTML UI          │
   │                                                                   │
   └───────────────────────────────────────────────────────────────────┘

   Your UI files are hosted by Adobe App Builder at
   https://<your-app>.adobeio-static.net
```

-->

## Extension points

An extension point is a named "slot" in the host where a guest is allowed to appear. Fusion defines its slots, and you choose which one the guest will use.

An extension point name has three parts: `service/name/version`.

Fusion offers the following extension points:

| Extension point | Where your UI appears in Fusion | When to use it |
| --- | --- | ---- |
| `fusion/nav-organization/1` | Under the **Organization** section of the left navigation. | Your tool is about the whole organization. |
| `fusion/nav-team/1` | Under the **Team** section of the left navigation (shown when a team is selected). | Your tool is about a specific team. |

* `fusion` is the **service** (the product, Fusion).
* `nav-organization` / `nav-team` is the **name** (the specific slot).
* `1` is the **version**.

One extension can implement one or both extension points. Most extensions use one point.

Based on which extension point is selected, Fusion adds a button with the extension's title to the matching navigation section. Clicking it opens a dedicated page in Fusion's main content area and loads your UI there.

## Frames included in a UI Extension

>[!IMPORTANT]
>
>This section discusses an aspect of UI Extensions that may cause confusion. We recommend reading it carefully.

When Fusion loads your guest, your extension runs in **two** frames:

1. **The registration frame (invisible).** Runs first, in the background.The registration frame tells Fusion what your extension offers. For example, it may indicate that it has a dashboard widget, and send the widget's title and the URL of its UI.. The registration frame does this by calling `register(...)`. It renders no visible UI.
2. **The UI frame (visible).** This is the page Fusion shows to the user. It must announce itself to the host by calling `attach(...)`. If it never calls `attach`, Fusion waits and eventually times out with an error.

>[!BEGINSHADEBOX]

This example shows the flow when a user clicks the extension button.

1. The button is clicked.
1. Fusion loads your REGISTRATION frame (hidden).

   ```
   register({ methods: { dashboard: { getWidget() {...} } } })
   ```

   `getWidget()` returns the URL of your visible UI
1. Fusion loads your UI frame (visible) at that URL.

   ```
   attach({ id }) 
   ```
   
   This is required, or Fusion times out
1. Fusion sends context, and your UI renders.

>[!ENDSHADEBOX]

Both frames are written when you build the UI. The important thing is to remember that the visible page **must** call `attach`.

For more information on building the UI, see [Build the custom extension UI](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).

## Context from Fusion

After the extension is attached, Fusion shares a `context` object with your guest. It contains:

* **User**: The signed-in user's Fusion profile and Adobe IMS user ID.
* **Organization**: The active organization's full Fusion organization record and the Adobe IMS organization ID.
* **Team**: The active team, when applicable.
* **Adobe IMS access token**: This calls Adobe or Fusion APIs on the user's behalf, if necessary.

Fusion also pushes updates. For example, if the user switches organization or team while your UI is open, Fusion sends the new context so your UI can react instantly.

For the complete list of context fields, see [The Fusion context reference](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

## Creating a UI Extension

To create a UI Extension, follow these steps:

1. [Install tools and create an Adobe project](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
1. [Generate a blank App Builder project, point it at a Fusion extension point and register your widget](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).
1. [Build the UI and connect to Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).
1. [Use the context Fusion sends](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).
1. [Publish so Fusion can find it](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. (Optional) [Call Workfront/Fusion APIs for real data without CORS](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).

To begin the process, go to [Set up your tools and Adobe account](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).


