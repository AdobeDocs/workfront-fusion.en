---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: fusion
navigation-topic: workfront-fusion-navigation-topic
title: The Fusion context reference
description:  The Fusion context reference
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
# Publish your extension

Your extension runs in Fusion only after it is **built**, **deployed** to Adobe, and (for general availability) **approved** for your organization. The procedures on this page show how publish your extension and how to verify the result.

This information has been adapted from Adobe's official documentation and applies specifically to Workfront Fusion.

For the general Adobe information, see [UI Extension development flow](https://developer.adobe.com/uix/docs/guides/development-flow/) and [UI Extensions Management](https://developer.adobe.com/uix/docs/guides/publication/) in the Adobe documentation.

## Stage and Production

Stage and Production are two separate environments. Use Stage for testing, then Release the extension to Production when you want to make it visible to your organization.

* **Stage** is for development and testing. A plain `aio app deploy` to the Stage workspace is enough for Fusion to discover your extension while you iterate. No approval is required.
* **Production** is for releasing to all users. It additionally requires an **approval request** submitted from the Production workspace, after which the extension is registered in the Adobe App Registry and surfaced across the organization.

The Stage environment workflow is as follows:

1. Build the extension and deploy it to Stage.
1. Fusion discovers the extension from the stage workspace. You can now test it.

The Production environment workflow is as follows:

1. Build the extension and deploy it to stage.
1. Submit an Approval request from the Production workspace.
1. After approval, the extension is added to the Adobe App registry and is visible to your whole organization.

>[!NOTE]
>
> **Roles:** creating and deploying needs the **Developer** role; submitting the approval request to publish needs a **System Administrator** role. 
>For more information, see:
> * [Set up UI Extension tools and account](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md) 
> * [How to Get Access](https://developer.adobe.com/uix/docs/guides/get-access/) in the Adobe documentation.
<!--Becky start here-->
---

## Part A — Test on Stage

### Step 1 — Select the Stage workspace

```sh
aio console where                  # shows current org / project / workspace
aio console workspace select       # choose Stage
```

### Step 2 — Build

```sh
aio app build
```

This compiles your front-end and runs the metadata hook (which generates `app-metadata.json`). Fix any reported errors before continuing.

### Step 3 — Deploy

```sh
aio app deploy
```

`deploy` does two things:

1. **Hosts your UI** on Adobe's content delivery network, at a URL like `https://<project>-stage.adobeio-static.net`. The CLI prints this **extension endpoint URL** when it finishes. This is the URL Fusion loads in its iframe.
2. **Registers your extension's endpoints** for the extension point (`fusion/nav-organization/1`) in the Stage workspace, which is what lets Fusion discover it.

> **If deploy fails with "Extension point 'fusion/nav-organization/1' does not exist" (error 1060):** the Fusion extension point is not enabled for your organization yet. This is an onboarding step, not a mistake in your code. See [Troubleshooting](./08-troubleshooting.md#error-1060-extension-point-does-not-exist).

### Step 4 — Verify in Fusion

1. Sign in to Fusion with an account in the **same organization** you deployed to.
2. Open the section that matches your extension point:
   - `fusion/nav-organization/1` → the **Organization** area of the left navigation.
   - `fusion/nav-team/1` → the **Team** area (select a team first).
3. You should see a button with the **title** you set in `getWidget()`. Click it; your UI loads and receives the [Fusion context](./06-fusion-context-reference.md).

If the button does not appear or the panel shows an error, see [Troubleshooting](./08-troubleshooting.md).

> You can also preview the extension locally with `aio app run` before deploying. See Adobe's [Local Preview of UI Extensions](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/).

---

## Part B — Release on Production

When your extension works on Stage and you are ready for all users.

### Step 1 — Switch to the Production workspace

```sh
aio console workspace select       # choose Production
```

When the CLI asks about the `.env` file, choose **Merge** so you keep your environment variables.

### Step 2 — Build and deploy to Production

```sh
aio app build
aio app deploy
```

### Step 3 — Submit the approval request

Publishing is an **approval request submitted from the Production workspace**:

1. Open the [Adobe Developer Console](https://developer.adobe.com/console), select your **Organization**, open your **Project**, and switch to the **Production** workspace.
2. Submit your app for **approval / publishing** (this requires the **System Administrator** role).
3. After approval, your extension is added to the **Adobe App Registry** and becomes available across [Adobe Experience Cloud](https://experience.adobe.com), including Fusion, for your organization.

The full publication UI and states are documented in Adobe's [UI Extensions Management](https://developer.adobe.com/uix/docs/guides/publication/) guide.

---

## Updating your extension later

To ship changes, repeat **build → deploy** in the appropriate workspace (and, for Production, re-submit for approval if required). Users pick up the new version the next time they open your extension; there is nothing for them to install.

## Removing (revoking) your extension

Removing an extension is done by **revoking** it in Adobe Exchange:

1. Log in to **Adobe Exchange**.
2. Go to **Manage > App Builder Apps**.
3. Click **Revoke** next to the extension you want to remove, and confirm.

After revoking, the extension shows a *revoked* status in the Extension Manager. To remove it completely, delete the project in the Developer Console (a project **cannot** be deleted until its extension is revoked).

For Stage-only test deployments you can also tear down the deployment with:

```sh
aio app undeploy
```

---

## Official references

- [UI Extension development flow](https://developer.adobe.com/uix/docs/guides/development-flow/)
- [UI Extensions Management (publish / approve / revoke)](https://developer.adobe.com/uix/docs/guides/publication/)
- [Create a Project in Developer Console](https://developer.adobe.com/uix/docs/guides/creating-project-in-dev-console/)
- [How to Get Access (roles)](https://developer.adobe.com/uix/docs/guides/get-access/)
- [Local preview of UI Extensions](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/)

Next: [Troubleshooting →](./08-troubleshooting.md)
