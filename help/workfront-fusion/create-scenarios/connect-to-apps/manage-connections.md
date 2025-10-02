---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: connections-annd-webhooks
title: Manage connections
description: For most apps, it is necessary to create a connection, through which Adobe Workfront Fusion can communicate with the given third-party service according to the settings of the specific scenario.
author: Becky
feature: Workfront Fusion
exl-id: 26d7caad-8e12-4f04-ac7c-f71686c90ee6
---
# Manage connections

A connection represents the authorization and permissions that Fusion uses to access the application. You can create one or more connections for each application, and can use the same connection in multiple modules or scenarios. 

You can manage these connections in the Connections area.

For more information on connections, see [Connection overview](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

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
   <td> <p>New: Standard</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p> </td> 
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
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] Workfront plan: Your organization must purchase Adobe Workfront Fusion.</li><li>[!UICONTROL Ultimate] Workfront plan: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## View and manage connections

You can manage all connections from the Connections area. 

>[!NOTE]
>
>Connections are owned by teams. If you cannot find the connection you are looking for, check that you are viewing the correct team.
>
>To select a new team, click the team name in the left navigation and select a new team.

1. To open the Connections area, click **Connections** ![Connections icon](assets/connections-icon.png) in the left navigation.
1. Locate the connection you want to manage, then perform one or more of the following steps in the line for that connection.
1. (Optional) Assign an environment and connection type by clicking the **Environment** and **Type** dropdowns and selecting an option.
1. (Optional) To view which permissions were given to Workfront Fusion for the connection, click the View icon ![View connection permissions](assets/view-connection-permissions.png) for that connection.
1. (Optional) To rename a connection, highlight the connection name and type the new name.
1. (Optional) To reauthorize a connection, check the checkbox next to the connection, then click **Reauthorize** near the bottom of the screen.
1. (Optional) To delete a connection, check the checkbox next to the connection, click **Delete** near the bottom of the screen, then click **Really?**.
1. (Optional) To verify that the connection to the service was established successfully, check the checkbox next to the connection, then click **Verify** near the bottom of the screen.
1. (Optional) To view active scenarios that use this connection, check the checkbox next to the connection, then click **Fetch Active Scenarios**. You can then click a scenario in the Active scenarios list to go to that scenario.

## Renew a connection

Workfront Fusion usually obtains access rights to a given service for an unlimited period of time. Some applications require the access permission to be renewed after a certain period of time. In these cases, Workfront Fusion notifies you via email shortly before its access rights expire.

To renew a connection:

1. To open the Connections area, click **Connections** ![Connections icon](assets/connections-icon.png) in the left navigation.
1. Locate the connection you want to renew.
1. In the line for that connection, check the checkbox next to the connection, then click **Reauthorize** near the bottom of the screen.

## Resources

* For more information on connection metadata, such as environment and type, see [Connection metadata](/help/workfront-fusion/references/connections/connection-metadata.md).
