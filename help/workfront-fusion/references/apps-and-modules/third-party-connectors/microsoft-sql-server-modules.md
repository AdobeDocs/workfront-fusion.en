---
title: Microsoft SQL Server modules
description: You can use Adobe Workfront Fusion to connect to Microsoft SQL Server.
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
---
# [!DNL Microsoft SQL Server] modules

You can use Adobe Workfront Fusion to connect to [!UICONTROL Microsoft SQL Server].

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any Adobe Workfront Workflow package and any Adobe Workfront Automation and Integration package</p><p>Workfront Ultimate</p><p>Workfront Prime and Select packages, with an additional purchase of Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront licenses</td> 
   <td> <p>Standard</p><p>Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license</td> 
   <td>
   <p>Operation-based: No Workfront Fusion license requirement</p>
   <p>Connector-based (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Connecting the [!DNL Microsoft SQL Server] service to Workfront Fusion

For instructions about connecting your [!DNL Microsoft SQL Server] account to [!UICONTROL Workfront Fusion], see [Create a connection to [!UICONTROL Adobe Workfront Fusion] - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Some Microsoft apps use the same connection, which is tied to individual user permissions. Therefore, when creating a connection, the permissions consent screen displays any permissions that were previously granted to this user's connection, in addition to any new permissions needed for the current application. 
>
>For example, if a user has "Read table" permissions granted via the Excel connector and then creates a connection in the Outlook connector to read emails, the permissions consent screen will show both the already granted "Read table" permission and the newly required "Write email" permission.

## Using [!DNL Microsoft SQL Server] modules

You can execute your custom logic directly on your database server through stored procedures. Adobe Workfront Fusion loads interface of input/output parameters and recordset dynamically so each parameter or value can be mapped individually. Before you start configuring your scenario, make sure the account you're using to connect to your database has read access to `INFORMATION_SCHEMA.ROUTINES` and `INFORMATION_SCHEMA.PARAMETERS` views.

When [!DNL Fusion] establishes the connection to the [!DNL SQL server] destination, the [!DNL Fusion] user identifies the Host (the domain name or IP address where the server is hosted) and the port. [!DNL Fusion] can connect to any available host and port.

For information about specific IP addresses used by Workfront Fusion, see [IP Addresses for accessing Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

To learn more about creating a stored procedure, see the [!DNL Microsoft SQL Server] documentation.

>[!NOTE]
>
>Workfront Fusion doesn't support multiple recordsets. Only the first one is processed.

## Troubleshooting error [!UICONTROL ER_LOCK_WAIT_TIMEOUT: Lock wait timeout exceeded; try restarting transaction]

This error occurs when you modify the same data using multiple modules. It is caused by SQL transactions.

When any SQL module is executed, it starts a transaction. The transaction is finished after the scenario is fully executed.

If another module tries to access the same data, it has to wait until the previous transaction is finished. Since the first transaction will be finished after the scenario is finished, the second transaction can never begin.

### Solution:

Turn on Auto-commit. Auto-commit finishes (commits) every transaction immediately after the module execution is done.

1. Click the [!UICONTROL Scenario settings] icon ![Scenario settings icon](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png)at the bottom of the screen.
1. Click the **[!UICONTROL Auto commit]** checkbox.
1. Click **[!UICONTROL OK]** to save the scenario settings.
