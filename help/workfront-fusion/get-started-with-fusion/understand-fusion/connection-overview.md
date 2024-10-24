---
title: Connection overview
description: For most apps, it is necessary to create a connection, through which [!DNL Adobe Workfront Fusion] can communicate with the given third-party service according to the settings of the specific scenario.
author: Becky
feature: Workfront Fusion
---
# Connection overview

Workfront Fusion requires a connection for most applications.  It uses this connection to communicate with the given third-party service.

For example, if you want to create a scenario that retrieves information from [!DNL Workfront], you must grant permission for [!DNL Workfront Fusion] to access your [!DNL Workfront] account.

A connection represents the authorization and permissions that Fusion uses to access the application. You can create one or more connections for each application used in your scenarios, and can use the same connection in multiple modules or scenarios. 

Most connections are used only for a single application. For example, a [!DNL Workfront] connection cannot be used in a [!UICONTROL Salesforce] module. Some [!DNL Adobe] applications can share connections. <!--For details, see the articles for those applications, listed in [Apps and their modules](/help/quicksilver/workfront-fusion/apps-and-their-modules/apps-and-their-modules.md). -->

Connections are owned by teams. All members of a team have access to the team's connections, and users outside of a team do not have access to the team's connections.

## Access rights

For every connection, [!DNL Workfront Fusion] requires only those access rights that are necessary to successfully complete a given scenario. For example, if you create a scenario to download a document from [!DNL Workfront], [!DNL Workfront Fusion] does not ask for permission to create a new project. Later, if you find that you need to create a project, you can update the connection or create a new one that can create projects.

Not all services allow you to limit access to specific tasks. In these cases, [!DNL Workfront Fusion] must require full access rights. <!--For more information on how to restrict [!DNL Workfront Fusion] access to your account registered to those services, see the application-specific documentation listed in [Apps and their modules](/help/quicksilver/workfront-fusion/apps-and-their-modules/apps-and-their-modules.md).-->

<!--
## Access requirements

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
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] Plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->
