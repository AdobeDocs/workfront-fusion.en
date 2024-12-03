---
title: Call the MS Graph REST API via the Adobe Workfront Fusion HTTP &gt; Make an OAuth 2.0 request module
description: Call the MS Graph REST API via the Adobe Workfront Fusion HTTP &gt; Make an OAuth 2.0 request module
author: Becky
feature: Workfront Fusion
exl-id: adae390d-8b9e-4dab-8551-605e50af5a1e
---
# Call the MS Graph REST API via the Adobe Workfront Fusion HTTP > Make an OAuth 2.0 request module

Many Microsoft web services are accessed through the Microsoft Graph API. You can create a connection to the Microsoft Graph API, by using the Workfront Fusion HTTP > Make an OAuth 2.0 request module.

## Access requirements

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront plan</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current: Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>Current: No Workfront Fusion license requirement.</p>
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

For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Register Workfront Fusion in the Microsoft Application Registration Portal 

To create a connection to the Microsoft Graph REST API, you must first register Adobe Workfront Fusion.

1. Begin registering a new application as described in [Register your app](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) in the Microsoft documentation.

   As part of the registration, Microsoft requires the following information:

   <table style="table-layout:auto">
      <tr>
        <td>Application name</td>
        <td>Enter a name for the application, such as "My Workfront Fusion application."</td>
      </tr>
      <tr>
        <td>Redirect URL</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/oauth2</code></td>
      </tr>
    </table>

1. When you have completed the app registration, make note of the Application ID.

   >[!IMPORTANT]
   >
   >You will need the Application ID to set up your connection in Workfront Fusion.

1. Generate a Cliebt Secret. Make note of this secret.

   For instructions, see [Register your app](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) in the Microsoft documentation.

   >[!IMPORTANT]
   >
   >You will need the Client Secret to set up your connection in Workfront Fusion.

1. Configure the permissions for your application.

   For specifics on locating and configuring these fields, see the "Configure permissions for Microsoft Graph" section in [Get access without a user](https://docs.microsoft.com/en-us/graph/auth-v2-service) in the Microsoft documentation.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">What type of permissions does your application require?</td> 
      <td>Select <code>Delegated permissions</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Select permissions</td> 
      <td> <p>Select the following permissions:</p> 
       <ul> 
        <li> <p><code>offline_access</code> </p> </li> 
        <li> <p><code>openid</code> </p> </li> 
        <li> <p>Any other permissions required by your integrations (Example: <code>User.Read</code>)</p> </li> 
       </ul> <p><b>Important</b>: You will need the selected permissions to set up your connection in Workfront Fusion.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Continue to [Configure your MS Graph API connection in Workfront Fusion](#configure-your-ms-graph-api-connection-in-workfront-fusion).

## Configure your MS Graph API connection in Workfront Fusion 

After you register Workfront Fusion as discussed in [Register Workfront Fusion in the Microsoft Application Registration Portal](#register-workfront-fusion-in-the-microsoft-application-registration-portal), you can configure your connection in the HTTP > Make an Oauth 2.0 request module.

1. Add an HTTP > Make an OAuth 2.0 call module to your scenario.
1. Click **Add** next to the connection field.
1. Configure the connection fields as follows:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Connection name</td> 
      <td>Enter a name for the connection.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Environment</p> </td> 
      <td>Select whether you are connecting to a production or non-production account. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Type</p> </td> 
      <td>Select whether you are connecting to a service account or a personal account. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Flow type</p> </td> 
      <td>Select <code>Authorization Code</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Authorize URI</td> 
      <td>Enter <code>https://login.microsoftonline.com/common/oauth2/v2.0/authorize</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token URI</td> 
      <td>Enter <code>https://login.microsoftonline.com/common/oauth2/v2.0/token</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Scope</td> 
      <td> <p>Enter the permissions that you selected in step 4 of <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Register Workfront Fusion in the Microsoft Application Registration Portal</a>.</p> <p>For each scope, click <b>Add</b> and type in the permission.</p> <p>Example: <code>offline_access</code>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Scope separator</td> 
      <td>Select <code>SPACE</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Client ID</td> 
      <td>Enter the Application ID from step 2 in <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Register Workfront Fusion in the Microsoft Application Registration Portal</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Client Secret</td> 
      <td>Enter the Client  Secret that you generated in step 3 in <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Register Workfront Fusion in the Microsoft Application Registration Portal</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Authorize parameters</td> 
      <td> <p>Add the following Authorize parameters. For each parameter you are adding, click <b>Add item</b> and enter the following: </p> 
       <ul> 
        <li> <p>Key:<code> response_mode</code> Value: <code>query</code></p> </li> 
        <li> <p>Key: <code>prompt </code>Value: <code>consent</code></p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Access token parameters</td> 
      <td>You do not need to enter anything into this field.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Refresh token parameters</td> 
      <td> 
       <ol> 
        <li value="1"> <p>Click <b>Add item</b>.</p> </li> 
        <li value="2"> <p>In the <b>Key</b> field, enter <code>scope</code>.</p> </li> 
        <li value="3"> <p>In the <b>Value</b> field, enter all of the scopes that you entered into the scope field, separated by spaces.</p> <p>Example: <code>offline_access openid User.Read</code></p> </li> 
       </ol> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Custom Headers</td> 
      <td>You do not need to enter anything into this field.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token Placement</td> 
      <td><code>In the header</code> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Continue**.
1. In the window that appears, click **Accept** to complete the connection and return to the module.
