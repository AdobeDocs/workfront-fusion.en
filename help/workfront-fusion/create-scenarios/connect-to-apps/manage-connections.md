---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: connections-annd-webhooks
title: Manage connections
description: For most apps, it is necessary to create a connection, through which [!DNL Adobe Workfront Fusion] can communicate with the given third-party service according to the settings of the specific scenario.
author: Becky
feature: Workfront Fusion
exl-id: 2d5cf083-9893-45e8-8f7d-0f8f5a74eef3
---
# Manage connections

<!--affected by unified shell-->

<!--audited: Nov 2024-->

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
   <td role="rowheader">[!DNL Adobe Workfront] plan</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] license</td> 
   <td> <p>New: [!UICONTROL Standard]</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] license**</td> 
   <td>
   <p>Current: No [!DNL Workfront Fusion] license requirement.</p>
   <p>Or</p>
   <p>Legacy: Any </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan: [!DNL Workfront Fusion] is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

<!--For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md).-->

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## View and manage connections

You can manage all connections from the Connections area. 

>[!NOTE]
>
>Connections are owned by teams. If you cannot find the connection you are looking for, check that you are viewing the correct team.
>
>To select a new team:
>
>* Click the team name in the left navigation and select a new team.
>
>    Or
>
>* Click Team overview in the left navigation, then click the dropdown arrow next to the team name near the top of the page. Select a new team.

1. To open the Connections area, click **Connections** ![Connections icon](assets/connections-icon.png) in the left navigation.
1. Locate the connection you want to manage, then perform one or more of the following steps in the line for that connection.
1. (Optional) Assign an environment and connection type by clicking the **Environment** and **Type** dropdowns and selecting an option.
1. (Optional) To view which permissions were given to Workfront Fusion for the connection, click the View icon ![View connection permissions](assets/view-connection-permissions.png) for that connection.
1. (Optional) To rename a connection, highlight the connection name and type the new name.
1. (Optional) To reauthorize a connection, click **Reauthorize**.
1. (Optional) To delete a connection, click **Delete**, then click **Really?**.
1. (Optional) To verify that the connection to the service was established successfully, click **Verify**.

## Renew a connection

[!DNL Workfront Fusion] usually obtains access rights to a given service for an unlimited period of time. Some applications require the access permission to be renewed after a certain period of time. In these cases, [!DNL Workfront Fusion] notifies you via email shortly before its access rights expire.

To renew a connection:

1. To open the Connections area, click **Connections** ![Connections icon](assets/connections-icon.png) in the left navigation.
1. Locate the connection you want to renew.
1. In the line for that connection, click the **[!UICONTROL Reauthorize]** button in the **[!UICONTROL Connections]** area.

## Resources

* For more information on connection metadata, such as environment and type, see [Connection metadata](/help/workfront-fusion/references/connections/connection-metadata.md).




