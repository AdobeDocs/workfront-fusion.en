---
title: Connect Adobe Workfront Fusion to Google Services using a custom OAuth client
description: You can use Adobe Workfront Fusion to connect to Google Services using a custom OAuth client. This procedure requires an existing Google account.
author: Becky
feature: Workfront Fusion
exl-id: 2f0bc289-4ecf-4a31-9d7b-641bbca6fc95
---
# Connect Adobe Workfront Fusion to Google Services using a custom OAuth client

You can use Adobe Workfront Fusion to connect to Google Services using a custom OAuth client. This procedure requires an existing Google account.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current: Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>Current: No Workfront Fusion license requirement</p>
   <p>Or</p>
   <p>Legacy: Any </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>Select or Prime Workfront Plan: Your organization must purchase Adobe Workfront Fusion.</li><li>Ultimate Workfront Plan: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

You need an existing Google account to make this connection.

## Connect Fusion to Google services using a custom OAuth client

To create this connection, you must create and configure a project on Google Cloud platform, and then configure the connection in Fusion based on that project.

>[!NOTE]
>
>This procedure is intended for:
>
>* Personal use (`@gmail.com` and `@googlemail.com` users)
>* Internal use (Google Workspace users that prefer to use a custom OAuth client)

* [Create a project on Google Cloud Platform](#create-a-project-on-google-cloud-platform)
* [Configure OAuth consent settings](#configure-oauth-consent-settings) 
* [Create OAuth credentials](#create-oauth-credentials)
* [Connect to Google in Workfront Fusion](#connect-to-google-in-workfront-fusion)

### Create a project on Google Cloud Platform 

To create a project on Google Cloud Platform:

1. Begin creating a project on Google Cloud Platform.

   For instructions, see [Create a Google Cloud project](https://developers.google.com/workspace/guides/create-project) in the Google documentation.
1. When enabling APIs, you must enable Google Drive API as well as the API of all Google apps you want to use (such as Google Sheets API).
1. Finish creating the project.
1. Continue to the section [Configure OAuth consent settings](#configure-oauth-consent-settings) in this article.

### Configure OAuth consent settings 

1. Begin configuring OAuth for your project

   For instructions, see [Configure the OAuth consent screen and choose scopes](https://developers.google.com/workspace/guides/configure-oauth-consent) in the Google documentation.
1. Select **External**, then click **Create**.

   >[!NOTE]
   >
   >You will not be charged when selecting this option. For more information, see Google's information about exceptions to verification requirements.

1. Fill the required fields as follows:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>App name</p> </td> 
      <td> <p>Enter the name of the app asking for consent.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Example: </b></span></span>Adobe Workfront Fusion </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">User support email</td> 
      <td>Enter an email address for users to contact you with questions about their consent when connecting to this app.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Email addresses</td> 
      <td>Enter one or more email addresses that Google can use to notify you about any changes to your project.</td> 
     </tr> 
    </tbody> 
   </table>

1. Under Authorized domains, click **Add domain**, and enter `workfrontfusion.com`.
1. Add the following scopes:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Service/API</th> 
      <th>Required scopes</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td> <p>Gmail</p> </td> 
      <td> <p>https://mail.google.com/</p> <p>https://www.googleapis.com/auth/gmail.labels</p> <p>https://www.googleapis.com/auth/gmail.send</p> <p>https://www.googleapis.com/auth/gmail.readonly</p> <p>https://www.googleapis.com/auth/gmail.compose</p> <p>https://www.googleapis.com/auth/gmail.insert</p> <p>https://www.googleapis.com/auth/gmail.modify</p> <p>https://www.googleapis.com/auth/gmail.metadata</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Google Drive</p> </td> 
      <td> <p>https://www.googleapis.com/auth/drive</p> <p>https://www.googleapis.com/auth/drive.readonly</p> </td> 
     </tr> 
    </tbody> 
   </table>

   You may need to expand the list or go to the next page of the list to see them all.

1. (Optional) Add any test users to the project.
1. Examine your information for accuracy, then click **Back to dashboard**.

   >[!NOTE]
   >
   >You don't need to submit your consent screen and application for verification by Google.

1. Continue to [Create OAuth Credentials](#create-oauth-credentials).

### Create OAuth Credentials 

1. Begin creating OAuth cliet ID credentials.

   For instructions, see [Create access credentials](https://developers.google.com/workspace/guides/create-credentials) in the Google documentation.

   >[!NOTE]
   >
   >If this is not the first API or service (Gmail or Google Drive) you have enabled, you don't have to create new credentials.

1. Fill the required fields as follows:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Application type</td> 
      <td> <p> Web application</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Name</td> 
      <td>Workfront Fusion </td> 
     </tr> 
    </tbody> 
   </table>

1. Under Authorized redirect URIs,  enter **one** of the following:

   * For Gmail or Google Drive: `https://app.workfrontfusion.com/oauth/cb/google-restricted`

   * For other Google apps: `https://app.workfrontfusion.com/oauth/cb/google`

1. Click **Create**.

   The Client ID and Client Secret display.

1. Copy the Client ID and Client Secret to a secure location. You will use them to make a connection in Workfront Fusion.
1. Continue to [Connect to Google in Workfront Fusion](#connect-to-google-in-workfront-fusion).

### Connect to Google in Workfront Fusion 

The process of creating a connection to Google differs depending on whether you are using a module from a Google service(such as Google Sheets or Google Docs), or if you are connecting to Google via the HTTP >Make an OAuth2.0 request module.

* [Connect to Google in a Google service](#connect-to-google-in-a-google-service)
* [Connect to Google in the HTTP > Make an OAuth2.0 request module](#connect-to-google-in-the-http--make-an-oauth20-request-module)

#### Connect to Google in a Google service

1. In Workfront Fusion, locate the Google module that you need to create a connection for.
1. Click **Create a connection**, then click **Show advanced settings**.
1. Fill in the Connection name, Environment, and Type fields as applicable.
1. Enter the Client ID and Client Secret you retrieved in [Create OAuth Credentials](#create-oauth-credentials) in the respective fields, then click **Continue**.

1. Sign in with your Google account.

   The **This app isn't verified** window displays. Note that the "app" mentioned in the window title is the OAuth client that you created above.

1. Click **Advanced**, then click **Go to Workfront Fusion (unsafe)** to allow access using your custom OAuth client.

1. Click **Allow** to grant Workfront Fusion permission.
1. In the window that appears, click **Allow** again to confirm your choices.

   The connection to the desired Google service using a custom OAuth client is established.

#### Connect to Google in the HTTP > Make an OAuth2.0 request module {#connect-to-google-in-the-http--make-an-oauth20-request-module}

For instructions on connecting to Google in the HTTP > Make an OAuth2.0 request module, see [Instructions for creating a connection to Google in the HTTP > Make an OAuth 2.0 request module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module) in the article HTTP > Make an OAuth 2.0 request module.

## Possible error message:[403 Access Not Configured]

If the `403 Access Not Configured` error message displays, you must enable the corresponding API in your Google Cloud Platform. To enable the API, follow the steps in the section [Create a project on Google Cloud Platform](#create-a-project-on-google-cloud-platform) in this article.
