---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: fusion
navigation-topic: workfront-fusion-navigation-topic
title: Publish your custom extension
description: Publish your custom extension
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
# Publish your custom extension

>[!NOTE]
>
>This article assumes some familiarity with software development tools. 

Your extension runs in Fusion only after it is **built**, **deployed** to Adobe, and **approved** for your organization. The procedures on this page show how to publish your extension and how to verify the result.

This information is adapted from Adobe's official documentation and applies specifically to Workfront Fusion. For the general Adobe information, see [UI Extension development flow](https://developer.adobe.com/uix/docs/guides/development-flow/) and [UI Extensions Management](https://developer.adobe.com/uix/docs/guides/publication/) in the Adobe documentation.

## Workspaces

Every App Builder project has a **Stage** and a **Production** workspace. Think of them as environments:

* **Stage** is for development and testing. You deploy here while you iterate. No approval is required, and the result is visible only through the Stage testing switch described below (or local preview).
* **Production** is for releasing to everyone. After you deploy to Production, you submit an **approval request**, and once it is approved the extension is registered in the Adobe App Registry and shown to your whole organization.

>[!NOTE]
>
> **Roles:** creating and deploying needs the **Developer** role; submitting the approval request to publish needs a **System Administrator** role. 
>For more information, see:
>
> * [Set up UI Extension tools and account](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md) 
> * [How to Get Access](https://developer.adobe.com/uix/docs/guides/get-access/) in the Adobe documentation.

By default, Fusion shows only **published** extensions. These are extensions you have deployed to the **Production** workspace and then submitted for **approval**. This is the safe default, so a work-in-progress deploy never appears to your whole organization by accident.

A deploy to the **Stage** workspace is not published, so it does not appear in Fusion on its own. You have two ways to try an extension before you publish it:

* **Preview it locally** with `aio app run` (see [Local preview of UI extensions](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/) in the Adobe documentation). Nothing is deployed, and only you see it.
* **Load it from Stage inside Fusion** by turning on a per-user testing switch in your Fusion profile. This is described in [Test a Stage build in Fusion](#test-a-stage-build-in-fusion) in this article.

## Test a Stage build in Fusion

Use this flow to see a Stage deploy inside Fusion before you publish it.

### Step 1: Select the Stage workspace

```sh
aio console where                  # shows current org / project / workspace
aio console workspace select       # choose Stage
```

### Step 2: Build

```sh
aio app build
```

This compiles your front-end and runs the metadata hook (which generates `app-metadata.json`). Fix any reported errors before continuing.

### Step 3: Deploy

```sh
aio app deploy
```

`deploy` does two things:

* **Hosts your UI** on Adobe's content delivery network, at a URL like `https://<project>-stage.adobeio-static.net`. The CLI prints this **extension endpoint URL** when it finishes. This is the URL Fusion loads in its iframe.
* **Registers your extension's endpoints** for the extension point (`fusion/nav-organization/1`) in the Stage workspace.

>[!TIP]
>
> **If deploy fails with "Extension point 'fusion/nav-organization/1' does not exist" (error 1060):** the Fusion extension point is not enabled for your organization yet. This is an onboarding step, not a mistake in your code. 
>For more information, see [Extension point does not exist](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md#error-1060-extension-point-does-not-exist) in the troubleshooting article.

### Step 4: Turn on Stage testing in your Fusion profile

Fusion loads Stage extensions only when you opt in, per user:

1. Sign in to Fusion with an account in the **same organization** you deployed to.
1. Open the user avatar menu in the top corner and go to **Product Settings** > **Fusion Profile** > **Preferences**.
1. Turn on the **Stage extensions** switch.

   Fusion prompts you to reload.
1. Confirm the reload.

After the reload, Fusion loads extensions from the Stage workspace instead of the published set, and labels each one **(Stage)** in the navigation so you can tell them apart.

This switch is a personal testing setting stored in your browser, not an organization setting. Turn it off (and reload) to go back to the published extensions. Because it is stored locally, it does not follow you to another browser or machine.

### Step 5: Verify in Fusion

1. Open the section that matches your extension point:
   * `fusion/nav-organization/1` → the **Organization** area of the left navigation.
   * `fusion/nav-team/1` → the **Team** area (select a team first).

   A button with the title you set in `getWidget()` appears, marked **(Stage)**.
1. Click the button that appeared.

Your UI loads and receives the [Fusion context](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

If the button does not appear or the panel shows an error, see [Troubleshooting](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

## Release on Production

When your extension works on Stage and you are ready for all users:

### Step 1: Switch to the Production workspace

```sh
aio console workspace select       # choose Production
```

When the CLI prompts about the `.env` file, select **Merge** so you keep your environment variables.

### Step 2: Build and deploy to Production

```sh
aio app build
aio app deploy
```

### Step 3: Submit the approval request

Publishing is an **approval request submitted from the Production workspace**:

1. Open the [Adobe Developer Console](https://developer.adobe.com/console), select your **Organization**, open your **Project**, and switch to the **Production** workspace.
1. Submit your app for **approval / publishing** (this requires the **System Administrator** role).
1. After approval, your extension is added to the **Adobe App Registry** and becomes available across [Adobe Experience Cloud](https://experience.adobe.com), including Fusion, for your organization.

For detailed instructions, see [UI Extensions Management](https://developer.adobe.com/uix/docs/guides/publication/) in the Adobe Developer documentation.

## Status and updates

A few behaviors are worth knowing so you can tell "still working on it" apart from "something is wrong":

* **Deployed to Production is not the same as visible.** `aio app deploy` to Production uploads your app, but it does not make the extension appear. It appears only after the approval request is submitted and approved. If you deployed to Production and still do not see it in Fusion, the usual reason is that it is not approved yet.
* **Code-only updates do not need a new approval.** If your extension is already published and you only change its code (the UI or the runtime actions), redeploy to the same URL with:

   ```sh
   aio app deploy --force-deploy
   ```

   Users get the new version the next time they open the extension. There is nothing for them to install. You only need to submit a new approval request when you change the **registration** itself, for example adding a new extension point or changing what `getWidget()` advertises.
* **A revoked or retracted extension  disappears.** If an extension is revoked by you or retracted, it stops appearing in Fusion with no error message. If a previously working extension vanishes for everyone, check whether it was revoked before searching for a code problem.

## Remove (revoke) an extension

Removing a published extension is done by **revoking** it in Adobe Exchange:

1. Sign in to **Adobe Exchange**.
1. Go to **Manage** > **App Builder Apps**.
1. Select **Revoke** next to the extension you want to remove, and confirm.

After revoking, the extension shows a *revoked* status in the Extension Manager and no longer appears in Fusion. To remove it completely, delete the project in the Developer Console. A project cannot be deleted until its extension is revoked.

For a Stage-only test deployment, you can remove the deployment with:

```sh
aio app undeploy
```

## Additional resources

The following resources are available in the Adobe documentation:

* [UI Extension development flow](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [UI Extensions Management (publish / approve / revoke)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Create a Project in Developer Console](https://developer.adobe.com/uix/docs/guides/creating-project-in-dev-console/)
* [How to Get Access (roles)](https://developer.adobe.com/uix/docs/guides/get-access/)
* [Local preview of UI Extensions](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/)
