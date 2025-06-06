---
title: Create a connection - Basic instructions
description: Many [!DNL Adobe Workfront Fusion] connectors do not require custom configuration when creating a connection. This article describes the default connection creation process.
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
---
# Create a connection - Basic instructions

Many [!DNL Adobe Workfront Fusion] connectors do not require custom configuration when creating a connection. This article describes the default connection creation process.

>[!NOTE]
>
>
>If Adobe Workfront Fusion doesn't offer an app for the web service you would like to use in your scenario, you can connect to the web service using [!DNL Workfront Fusion] HTTP and Webhooks modules, as explained in the following articles:
>
>* [Connect Adobe Workfront Fusion to a web service that uses API token authorization](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [Configure a webhook for a web service without a connector](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

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

## Create a connection

To create a connection to a given application, you must be in a module for that application. For example, to create a connection to Workfront, you must be in a Workfront module.

To create a connection inside a [!DNL Workfront Fusion] module:

1. In any module for the given application, click **[!UICONTROL Add]** next to the [!UICONTROL Connection] box to open the **[!UICONTROL Create a connection]** panel.
1. (Optional) Change the default **[!UICONTROL Connection name]**.
1. In the Environment field, select whether this is a production or non-production environment. 
1. In the Type field, select whether this is a service or personal account.
1. (Conditional) If the app requires advanced connection settings, such as an ID, key, or [!UICONTROL secret], enter that information.

   You ay need to click **[!UICONTROL Show advanced settings]** to display the fields where you can enter this kind of information.

1. Click **[!UICONTROL Continue]**.
1. In the sign-in window that displays, enter your credentials to log in to the app if you haven't already done so.
1. (Conditional) If an **[!UICONTROL Allow]** button displays, examine the actions that the connector will be able to take, then click the button to connect the app to [!DNL Workfront Fusion].

   >[!NOTE]
   >
   >* The Environment and Type fields are for information only and do not change the functionality of the connection. This information appears in the Connections area of Fusion, allowing you to determine which connection to use for a given use case in your organization.
   >* Some Microsoft apps use the same connection, which is tied to individual user permissions. Therefore, when creating a connection, the permissions consent screen displays any permissions that were previously granted to this user's connection, in addition to any new permissions needed for the current application. 
   >
   >   For example, if a user has "Read table" permissions granted via the Excel connector and then creates a connection in the Outlook connector to read emails, the permissions consent screen will show both the already granted "Read table" permission and the newly required "Write email" permission.
