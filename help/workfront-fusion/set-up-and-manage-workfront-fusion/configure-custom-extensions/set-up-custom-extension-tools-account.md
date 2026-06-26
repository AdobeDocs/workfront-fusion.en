---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: fusion
navigation-topic: workfront-fusion-navigation-topic
title: Set up UI Extension tools and account
description: Set up UI Extension tools and account
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

# Set up UI Extension tools and account

Before you can create a UI Extension for Workfront Fusion, you must set up your tools and account. This only needs to be done once.

>[!NOTE]
>
>This article assumes some familiarity with software development tools. 

<!--Access requirements-->

## Prerequisites

To set up your UI Extensibility tools and account, you need the following:

* **An Adobe ID** with access to an Adobe organization. This is the account you use to sign in to Fusion. 
* **Developer access to App Builder.** Your organization administrator may need to grant you the **Developer** role and add you to a **Product Profile** that includes App Builder. If commands later fail with "you are not a developer" or you cannot see your organization, ask your Adobe org administrator to add you.
* **A System Administrator** <!--Adobe? Fusion?--> (possibly someone else on your team) for the final release step. Creating and deploying needs only the Developer role, but **submitting an extension for approval/publishing requires the System Administrator role**. 

   For more information on Adobe access levels, see
  [How to Get Access](https://developer.adobe.com/uix/docs/guides/get-access/) in the Adobe documentation.

* **A computer where you can install software** and run terminal commands (macOS, Windows, or Linux).

## Install Node.js

The Adobe tooling runs on **Node.js**. You must install the **LTS** version (18 or 20).

1. Go to <https://nodejs.org> and download the **LTS** installer.
1. Run the installer and accept the defaults.
1. Confirm it worked by opening a terminal and running:

   ```sh
   node --version
   npm --version
   ```

   You should see version numbers (for example `v20.17.0` and `10.x`). 
   
1. (Conditional) If `node` is not found, close and reopen your terminal, or restart your computer.

1. Continue to [Install the Adobe I/O CLI (`aio`)](#install-the-adobe-io-cli-aio).

>[!TIP]
>
>* If you work with multiple Node versions, a version manager such as `nvm` is convenient, but it is optional. 
>* The Adobe CLI requires Node 18 or newer. very new, non-LTS versions can occasionally cause issues, so we recommend using LTS.

## Install the Adobe I/O CLI (`aio`)

The command-line tool that you use to create, build, and publish your extension is called `aio`.

To install it globally: 

1. Use the following `npm` command on your command line.

   ```sh
   npm install -g @adobe/aio-cli
   ```

1. Confirm that it installed by using the following command:

   ```sh
   aio --version
   ```

   You should see something like `@adobe/aio-cli/11.x.x`.

1. Continue to [Sign in to Adobe](#sign-in-to-adobe).

>[!NOTE]
>
> If you see a permissions error on macOS/Linux, do **not** use `sudo`. Instead, fix npm's global folder permissions, or use a Node version manager that installs into your home directory.

## Sign in to Adobe

1. Connect the CLI to your Adobe account with the following command:

   ```sh
   aio login
   ```

1. In the browser window that opens, sign in with your Adobe ID and approve access. 

1. After sign-in is successful, close the browser tab and return to the terminal.

1. (Optional) To sign out later, (for example to switch accounts), use the command: `aio logout`.
1. Continue to [Confirm your active organization](#confirm-your-active-organization).

## Confirm your active organization

Check which organization the CLI is pointed at:

   ```sh
   aio console org list      # see organizations you can use
   aio console where         # see your currently selected org/project/workspace
```

If you belong to several organizations, select the correct one:

   ```sh
   aio console org select
   ```

You are now ready to create the project.
