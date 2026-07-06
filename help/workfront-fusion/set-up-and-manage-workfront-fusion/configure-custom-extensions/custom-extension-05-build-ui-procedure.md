---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: fusion
navigation-topic: workfront-fusion-navigation-topic
title: Build the custom extension UI
description:  Build the custom extension UI
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

# Build the custom extension UI

>[!NOTE]
>
>This article assumes some familiarity with software development tools. 

This procedure describes how to build the screen users actually see, and complete the **connection ("handshake")** with Fusion. 

During this process, it is important to recallthat your extension runs in two frames: the hidden **registration** frame and the visible **UI** frame.

For information on frames in relation to custom extensions, see [Frames included in a UI Extension](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension).

For instructions on building the registration frame, see [Create a project for UI Extensibility](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).

## Route between the two frames

Both frames load the same `index.html`; a small front-end router decides which component to show based on the URL. 

1. Set up the routes in `web-src/src/components/App.js`. The essential part is:

   ```jsx
   import { HashRouter as Router, Routes, Route } from "react-router-dom";
   import ExtensionRegistration from "./ExtensionRegistration";
   import DashboardWidget from "./DashboardWidget";
   
   export default function App() {
     return (
       <Router>
         <Routes>
           {/* Background frame: registers the extension with Fusion */}
           <Route index element={<ExtensionRegistration />} />
           <Route path="index.html" element={<ExtensionRegistration />} />
   
           {/* Visible frame: the URL you returned from getWidget() */}
           <Route path="my-widget" element={<DashboardWidget />} />
         </Routes>
       </Router>
     );
   }
   ```

   These routes map to previous configuration as follows:

   * The default route (`index`) renders **`ExtensionRegistration`**, the hidden frame that calls `register(...)`.
   * The `my-widget` route renders **`DashboardWidget`**, your visible UI. This matches the `url: "/index.html#/my-widget"` you returned from `getWidget()` in [the previous page](./04-configure-for-fusion.md).

   >[!NOTE]
   >
   > **The routes and the `getWidget` url must agree.** If you change the route name, change the `url` too, or Fusion will load a blank page.

1. Continue to [Complete the handshake with `attach`](#complete-the-handshake-with-attach).

## Complete the handshake with `attach`

This is the single most important line in your visible UI. When Fusion opens your UI frame, it waits for that frame to "check in." Your code checks in by calling `attach({ id })`. 

**If this is omitted, Fusion times out** with an error such as *"awaiting initial message from target iframe."*

1. Add the following to `web-src/src/components/DashboardWidget.js`:

   ```jsx
   import { useEffect, useState } from "react";
   import { attach } from "@adobe/uix-guest";
   import { extensionId } from "./Constants";
   
   export default function DashboardWidget() {
     const [connection, setConnection] = useState(null);
   
     useEffect(() => {
       // Tell Fusion this UI frame is ready. Required.
       attach({ id: extensionId })
         .then(setConnection)
         .catch((e) => console.error("attach failed", e));
     }, []);
   
     if (!connection) {
       return <p>Connecting to Fusionâ&euro;¦</p>;
     }
   
     return <h2>Hello from my Fusion extension!</h2>;
   }
   ```

   This code does the following:

<!--Becky start here-->

* `attach({ id })` returns a **connection object** once Fusion responds. Store it; you will use it in the next step to read the context Fusion sends.
* Until the connection resolves, show a short "Connectingâ&euro;¦" message.
* Use the **same `extensionId`** you set in `Constants.js`.

At this point you have a working extension: it registers, attaches, and shows a message. Everything after this is about using the data Fusion gives you.

## Step 3 â&euro;" Read the context Fusion shares

Once attached, the connection exposes a **shared context** with information about the current user, organization, and team. Read individual values with `connection.sharedContext.get("<key>")`:

```jsx
const orgId = connection.sharedContext.get("imsOrgId");
const organization = connection.sharedContext.get("organization"); // full Fusion org
const user = connection.sharedContext.get("user");                 // full Fusion user
```

A complete, reactive example that also updates when the user switches org or team:

```jsx
import { useEffect, useState } from "react";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

function readContext(source) {
  // sharedContext behaves like a Map (.get); the change event gives a plain object.
  const get =
    typeof source.get === "function" ? (k) => source.get(k) : (k) => source[k];
  return Object.fromEntries(KEYS.map((k) => [k, get(k)]));
}

export default function DashboardWidget() {
  const [context, setContext] = useState(null);

  useEffect(() => {
    let cleanup = () => {};
    attach({ id: extensionId })
      .then((connection) => {
        // 1) initial values
        setContext(readContext(connection.sharedContext));

        // 2) react to org/team/user changes pushed by Fusion
        const onChange = (event) =>
          setContext(readContext(event?.detail?.context ?? connection.sharedContext));
        connection.addEventListener("contextchange", onChange);
        cleanup = () => connection.removeEventListener?.("contextchange", onChange);
      })
      .catch((e) => console.error("attach failed", e));
    return () => cleanup();
  }, []);

  if (!context) return <p>Connecting to Fusionâ&euro;¦</p>;

  return (
    <div>
      <h2>{context.organization?.name ?? "No organization"}</h2>
      <p>Signed in as {context.user?.name} ({context.user?.email})</p>
      <p>IMS org: {context.imsOrgId}</p>
    </div>
  );
}
```

The two things to remember:

1. **Read initial values** from `connection.sharedContext.get(key)` right after `attach`.
2. **Subscribe to `contextchange`** to stay in sync. Fusion fires this event whenever the active organization, team, or user changes. The new values arrive on `event.detail.context`.

The full list of keys and what each contains is the next page.

Next: [The Fusion context reference â†'](./06-fusion-context-reference.md)
