---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe Storage modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you to create and manage projects in the Adobe Admin Console.
author: Becky
feature: Workfront Fusion
exl-id: 78ee905f-4713-44a4-bffb-c64cdb3665c2
---
# Adobe Storage modules

In an [!DNL Adobe Workfront Fusion] scenario, you can create and manage projects in the Adobe Admin Console. 

If you need instructions on creating a scenario, see the articles under [Create a scenario: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current:  Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>Current: No Workfront Fusion license requirement</p>
   <p>Or</p>
   <p>Legacy: Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>Select or Prime Workfront package: Your organization must purchase Adobe Workfront Fusion.</li><li>Ultimate Workfront package: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Create a connection to Adobe Storage

Creating a connection to Adobe Storage requires some configuration in the Adobe Developer Console as well as in Fusion.

### Configure the project in the Adobe Developer Console

You must add the API to your project in the Adobe Developer Console.

1. Open your project in the Adobe Developer Console.
1. Click **Add to project**, and select **API**.
1. From the list of available APIs, select **Adobe Cloud Platform and Collaboration API**.
1. On the Select authentication type screen, select **OAuth Server-to-Server** and click **Next**.
1. Add a name for the crendential.
1. Click **Next**, then click **Save configured API**.
1. Make note of the provided credentials, which you will use when configuring the connection in Workfront Fusion.
1. Continue to [Make your technical account an admin in the Adobe Admin Console](#make-your-technical-account-an-admin-in-the-adobe-admin-console).

### Make your technical account an admin in the Adobe Admin Console

From the Adobe Admin Console page, select the Products tab in the top navigation bar, and then select Workfront Fusion

1. Locate and copy the email address of the technical account user in your organization.
1. If a list displays, select the link at the top.
1. This is your Production instance where your users work.
1. In the list that displays, with the Product Profiles tab selected, click the name of the Workfront Product Profile link.

   This list includes all users that are already assigned to your Production instance of Workfront.

1. Select the **Admins** tab above the list of users.
1. Select **Add Admin**.
1. In the Add product profile administrators box, enter the email addresses of the technical account, then select **Save**.

   The technical account is made an administrator.

1. Continue to [Create the connection in Workfront Fusion](#create-the-connection-in-workfront-fusion).

### Create the connection in Workfront Fusion

To create a connection for your [!DNL Adobe Storage] modules:

1. In any module, click **[!UICONTROL Add]** next to the Connection box.
    
1. Fill in the following fields:
    
    <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>Select <code>Server to server</code>.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Enter a name for this connection.</p>
        </td>
        </tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Enter your [!UICONTROL Adobe] [!UICONTROL Client ID]. This can be found in the [!UICONTROL Credential details] section of the project in the [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Enter your [!DNL Adobe] [!UICONTROL Client Secret]. This can be found in the [!UICONTROL Credential details] section of the project in the [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS Organization ID]</td>
        <td>Enter or map your Adobe IMS Organization ID. This is a string with the form <code> 123abc@AdobeOrg</code>, where the section before the @ is a hexadecimal number. You can find this value as part of the URL path for your organization in the Adobe Admin Console, or in the Adobe.IO console for your user management integration.</td>
        </tr>
      </tbody>
    </table>
    
1. Click **[!UICONTROL Continue]** to save the connection and return to the module.

## Adobe Storage modules and their fields

When you configure Adobe User Management modules, Workfront Fusion displays the fields listed below. Along with these, additional Adobe User Management fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [ESM stores](#esm-stores)
* [Invitations](#invitations)
* [Other](#other)

### ESM stores

* [Create an ESM store](#create-an-esm-store)
* [Delete an ESM store](#delete-an-esm-store)
* [Discard an ESM store](#discard-an-esm-store)
* [Restore an ESM store](#restore-an-esm-store)

#### Create an ESM store

This action module sets up a new Enterprise Storage Management (ESM) store to organize and manage business-critical assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Storage, see <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Create a connection to Adobe Storage</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Project name</td> 
   <td>Enter or map a name for the new project.</td> 
  </tr> 
 </tbody> 
</table>

#### Delete an ESM store

This action module permanently removes an existing ESM store and all its associated data. This action cannot be undone.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Storage, see <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Create a connection to Adobe Storage</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Store ID</td> 
   <td>Enter or map the ID of the store you want to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### Discard an ESM store

This action module marks an EMS store for deletion, allowing for a grace period before permanent removal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Storage, see <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Create a connection to Adobe Storage</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Store ID</td> 
   <td>Enter or map the ID of the store you want to discard.</td> 
  </tr> 
 </tbody> 
</table>

#### Restore an ESM store

This action module recovers a previously deleted ESM store and restores access to its data and configurations.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Storage, see <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Create a connection to Adobe Storage</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Store ID</td> 
   <td>Enter or map the ID of the store you want to restore.</td> 
  </tr> 
 </tbody> 
</table>

### Invitations

#### Invite user

This action module sends an invitation grant a new user access to a specific ESM store, enabling collaboration and file management.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Storage, see <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Create a connection to Adobe Storage</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Email address</td> 
   <td>Enter or map the email address of the user that you want to invite to the store.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset ID</td> 
   <td>Enter or map the ID of the asset that you want to invite the user to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Role</td> 
   <td>Select the role that you want the newly invited user to have for the asset.<ul><li>Owner</li><li>Editor</li><li>Viewer</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Can comment</td> 
   <td>Enable this option to allow the user to comment on the asset.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Can share</td> 
   <td>Enable this option to allow the user to share the asset with other user.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Acceptance required</td> 
   <td>Enable this option to ensure that the user must accept the invitation before they can collaborate on the asset.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Use mounts</td> 
   <td>Enable this option if a mount point to the resource must be created for the invitee. The Acceptance required option must be enabled to enable this option.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Notification type</td> 
   <td>Enter or map the Adobe notification type that you want to use to notify the user about the invitation. If this is left empty, the notification type is based on the asset's mimetype.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Template name</td> 
   <td>Enter or map the Adobe Post Office ID of the template you want to use for the invitation email.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Locale</td> 
   <td>Enter the locale of the user in the form of a language code and country code. <p>Example: <code>en-us</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">External</td> 
   <td>Set this option to true if you want to send notifications using a system external to the Adobe Invitations Service. External notification is supported only when acceptance is not required.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset type</td> 
   <td>Enter or map the type of asset.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Message</td> 
   <td>Enter or map a message to include in the invitation email.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Target URL</td> 
   <td>Enter or map the URL that the invitee can use to view the asset.</td> 
  </tr> 
 </tbody> 
</table>

### Other

#### Make a custom API call

This action module makes a custom HTTP request to the Adobe Storage API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
   <td>For instructions on creating a connection to Adobe Storage, see <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Create a connection to Adobe Storage</a> in this article.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>Enter a path relative to <code>https://ccprojects.adobe.io/api/v3/.</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Method</p>
      </td>
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">Headers</td>
      <td>
        <p>Add the headers of the request in the form of a standard JSON object.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] adds authorization headers and x-api-key headers automatically.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Query String  </td>
      <td>
        <p>Enter the request query string.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Body</td>
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
