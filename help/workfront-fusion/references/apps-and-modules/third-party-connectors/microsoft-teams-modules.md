---
title: Microsoft Teams modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use Teams, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: d21eafad-9c67-4f42-b718-0aa4223846e6
---
# [!DNL Microsoft Teams] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Teams], as well as connect it to multiple third-party applications and services.

For instructions on creating a scenario, see the articles under [Create scenarios: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

## Prerequisites

To use Microsoft Teams modules, you must have a Microsoft Teams account able to perform the action in the module.

## Connecting the [!DNL Teams] service to [!DNL Workfront Fusion]

For instructions about connecting your [!DNL Teams] account to [!UICONTROL Workfront Fusion], see [Create a connection to [!UICONTROL Adobe Workfront Fusion] - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Some Microsoft apps use the same connection, which is tied to individual user permissions. Therefore, when creating a connection, the permissions consent screen displays any permissions that were previously granted to this user's connection, in addition to any new permissions needed for the current application. 
>
>For example, if a user has "Read table" permissions granted via the Excel connector and then creates a connection in the Outlook connector to read emails, the permissions consent screen will show both the already granted "Read table" permission and the newly required "Write email" permission.

## [!DNL Microsoft Teams] modules and their fields

When you configure [!DNL Teams] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Teams] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Team](#team)
* [Channel]()
* [Message]()
* [Member]()
* [Online meeting]()
* [Other]()

### Team

* [Create a team from a group](#create-a-team-from-a-group)
* [Create an office 365 group]()
* [Delete a team or group]()
* [Get a team]()
* [List all teams and groups]()
* [List joined teams]()
* [Update a team]()

#### Create a team from a group

This action module creates a team from an existingMicrosoft Office 365 group and configures settings for the new team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Group ID</td> 
   <td> <p>Select the group that you want to create a team from.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Allow members to create and update channels</td> 
   <td>Select whether you want to allow members to create and update channels.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow members to delete channels</td> 
   <td>Select whether you want to allow members to delete channels.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow members to add and remove apps</td> 
   <td>Select whether you want to allow members to add and remove apps.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow members to create, update, and  remove tabs</td> 
   <td>Select whether you want to allow members to create, update, and  remove tabs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow members to create and remove connectors</td> 
   <td>Select whether you want to allow members to create and remove connectors.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow users to edit their messages</td> 
   <td>Select whether you want to allow users to edit their messages.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow users to delete their messages</td> 
   <td>Select whether you want to allow users to delete their messages.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow owners to delete messages</td> 
   <td>Select whether you want to allow owners to delete any message.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow @team mentions</td> 
   <td>Select whether you want to allow @team mentions.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow @channel mentions</td> 
   <td>Select whether you want to allow @channel mentions.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">field name</td> 
   <td>Select whether you want to allow members to .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">field name</td> 
   <td>Select whether you want to allow members to .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">field name</td> 
   <td>Select whether you want to allow members to .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">field name</td> 
   <td>Select whether you want to allow members to .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">field name</td> 
   <td>Select whether you want to allow members to .</td> 
  </tr> 
 </tbody> 
</table>








