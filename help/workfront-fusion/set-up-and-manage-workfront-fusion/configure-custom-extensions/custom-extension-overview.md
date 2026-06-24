# 1. Overview & key concepts

This page explains the words and ideas used throughout the guide. Skim it once;
you will refer back to it.

## The big idea: Host and Guest

Fusion can show UI that it did not build itself. To make that safe, your UI runs
in its own isolated browser frame (an `<iframe>`), completely separate from
Fusion's code. The two sides communicate by passing messages.

- **Host** — the application that *contains* the extension. Here, that is
  **Fusion**. The host decides where extensions can appear and what data it will
  share with them.
- **Guest** — *your* extension. It is a small web application that the host
  loads into an iframe.

You never modify Fusion. You only build and publish a guest. Fusion discovers
your guest automatically once it is published.

## The technology underneath

Your guest is built with two Adobe technologies. You do not need to master them,
but it helps to know the names:

- **Adobe App Builder** — a free hosting and tooling platform for small web apps
  and serverless actions. Your extension is an App Builder app. App Builder
  gives you a place to host your UI (on Adobe's `*.adobeio-static.net` content
  delivery network) and a command line tool called `aio` to create, build, and
  publish it.
- **Adobe UI Extensibility SDK (UIX)** — the libraries that let the host and
  guest talk. You will use one package, `@adobe/uix-guest`, on your side. Fusion
  uses the matching `@adobe/uix-host` package on its side.

```
   ┌──────────────────────────── Browser ─────────────────────────────┐
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

## What is an "extension point"?

An **extension point** is a named "slot" in the host where a guest is allowed to
appear. Fusion defines its slots; you choose which one to plug into.

An extension point name has three parts: `service/name/version`.

Fusion offers these extension points:

| Extension point | Where your UI appears in Fusion | Use it when… |
|-----------------|---------------------------------|--------------|
| `fusion/nav-organization/1` | Under the **Organization** section of the left navigation. | Your tool is about the whole organization. |
| `fusion/nav-team/1` | Under the **Team** section of the left navigation (shown when a team is selected). | Your tool is about a specific team. |

- `fusion` is the **service** (the product, Fusion).
- `nav-organization` / `nav-team` is the **name** (the specific slot).
- `1` is the **version**.

One extension can implement one or both extension points. Most extensions start
with just one.

> **What happens visually:** Fusion adds a button with your extension's title to
> the matching navigation section. Clicking it opens a dedicated page in Fusion's
> main content area and loads your UI there.

## The two iframes: registration vs. your visible UI

This trips up most newcomers, so read it carefully.

When Fusion loads your guest, your extension actually runs in **two** frames:

1. **The registration frame (invisible).** Runs first, in the background. Its
   only job is to *tell Fusion what your extension offers* — for example, "I
   have a dashboard widget; here is its title and the URL of its UI." It does
   this by calling `register(...)`. It renders no visible UI.
2. **The UI frame (visible).** This is the page Fusion shows to the user. It
   must announce itself to the host by calling `attach(...)`. If it never calls
   `attach`, Fusion waits and eventually times out with an error.

```
  Fusion clicks your nav button
        │
        ▼
  1) loads your REGISTRATION frame (hidden)
        │   register({ methods: { dashboard: { getWidget() {...} } } })
        │   getWidget() returns the URL of your visible UI
        ▼
  2) loads your UI frame (visible) at that URL
        │   attach({ id })   ◀── REQUIRED, or Fusion times out
        ▼
  Fusion sends context, your UI renders
```

You will write both frames in [Build the UI](./05-build-the-ui.md). For now,
just remember: **the visible page must call `attach`.**

## What data you get from Fusion

Once attached, Fusion shares a **context** object with your guest. It contains:

- The signed-in **user** (Fusion profile plus Adobe IMS user id).
- The active **organization** (full Fusion organization record plus the Adobe
  IMS organization id).
- The active **team** (when applicable).
- The Adobe **IMS access token** (so you can call Adobe or Fusion APIs on the
  user's behalf, if you need to).

Fusion also **pushes updates**: if the user switches organization or team while
your UI is open, Fusion sends the new context and your UI can react instantly.

The complete list of fields is in
[The Fusion context reference](./06-fusion-context-reference.md).

## The end-to-end journey

Here is everything you will do, mapped to the remaining pages:

1. Install tools and create an Adobe project — [page 2](./02-setup.md).
2. Generate a blank App Builder project — [page 3](./03-create-project.md).
3. Point it at a Fusion extension point and register your widget —
   [page 4](./04-configure-for-fusion.md).
4. Build the UI and connect to Fusion — [page 5](./05-build-the-ui.md).
5. Use the context Fusion sends — [page 6](./06-fusion-context-reference.md).
6. Publish so Fusion can find it — [page 7](./07-publish.md).

Next: [Set up your tools & Adobe account →](./02-setup.md)