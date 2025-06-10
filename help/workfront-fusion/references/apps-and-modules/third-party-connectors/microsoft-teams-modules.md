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

## Connecting the [!DNL Teams] service to Workfront Fusion

For instructions about connecting your [!DNL Teams] account to [!UICONTROL Workfront Fusion], see [Create a connection to [!UICONTROL Adobe Workfront Fusion] - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Some Microsoft apps use the same connection, which is tied to individual user permissions. Therefore, when creating a connection, the permissions consent screen displays any permissions that were previously granted to this user's connection, in addition to any new permissions needed for the current application. 
>
>For example, if a user has "Read table" permissions granted via the Excel connector and then creates a connection in the Outlook connector to read emails, the permissions consent screen will show both the already granted "Read table" permission and the newly required "Write email" permission.

## [!DNL Microsoft Teams] modules and their fields

When you configure [!DNL Teams] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Teams] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Team](#team)
* [Channel](#channel)
* [Message](#message)
* [Member](#member)
* [Online meeting](#online-meeting)
* [Other](#other)

### Team

* [Create a Team from a Group](#create-a-team-from-a-group)
* [Create an Office 365 Group](#create-an-office-365-group)
* [Delete a Team or Group](#delete-a-team-or-group)
* [Get a Team](#get-a-team)
* [List all Teams and Groups](#list-all-teams-and-Groups)
* [List joined Teams](#list-joined-teams)
* [Update a Team](#update-a-team)
* [Watch Teams](#watch-teams)

#### Create a Team from a Group

This action module creates a Team from an existing Microsoft Office 365 Group and configures settings for the new team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Group ID</td> 
   <td> <p>Select the Group that you want to create a Team from.</p> 
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
   <td role="rowheader">Allow Giphy</td> 
   <td>Select whether you want to allow Giphy use for this Team.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow stickers and memes</td> 
   <td>Select whether you want to allow users to include stickers and memes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow custom memes</td> 
   <td>Select whether you want to allow users to include custom memes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow guests to create and update channels</td> 
   <td>Select whether you want to allow guests to create and update channels.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allow guests to delete channels</td> 
   <td>Select whether you want to allow guests to delete channels.</td> 
  </tr> 
 </tbody> 
</table>

#### Create an Office 365 Group

This action module creates a Group in Microsoft Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Display name</td> 
   <td> <p>Enter or map the name that this Group displays in its address book.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias for Group</td> 
   <td>Enter or map the email alias for this Group. You can include lowercase letters, numbers, and underscores. For the Office 365 Group type, this will be the Group's email alias ([Alias]@[Your Domain].onmicrosoft.com). For Security Group type, the alias functions as a nickname.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Group type</td> 
   <td>Enable <b>Unified</b> if you are creating an Office 365 Group.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Description</td> 
   <td>Enter or map a description for this Group.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Security enabled</td> 
   <td>Enable this option if you want the Group to be security enabled.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Owners</td> 
   <td>Select the owners for this Group.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Members</td> 
   <td>Select the members for this Group.</td> 
  </tr> 
 </tbody> 
</table>

#### Delete a Team or Group

This action module deletes the specified Team or Group.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Group ID</td> 
   <td> <p>Enter or map the ID of the Group you want to delete.</p> 
   </tr> 
 </tbody> 
</table>

#### Get a Team

This module retrieves properties and relationships for the specified Microsoft Team or Office 365 Group.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Group ID</td> 
   <td> <p>Enter or map the ID of the Group you want to retrieve details for.</p> 
   </tr> 
 </tbody> 
</table>

#### List all Teams and Groups

This module lists all Microsoft Teams and Office 365 Groups associated with the organization. You can filter to return only results that meet criteria you specify.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>You can set a filter to return only Teams and Groups that meet criteria you select.</p> <p>For each filter, enter the field you want the filter to evaluate, the operator, and the value that you want the filter to allow. You can use more than one filter by adding AND or OR rules.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximum number of returned results</td> 
   <td>Set the maximum number of Teams or Groups Workfront Fusion will return during one execution cycle.</td> 
  </tr> 
 </tbody> 
</table>


#### List joined Teams

This action module lists the teams that have been joined by the user associated with the connection used in this module.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>Maximum number of returned results</td> 
   <td>Set the maximum number of Teams or Groups Workfront Fusion will return during one execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

#### Update a Team

This action module updates the properties of the specified Microsoft Team or Office 365 Group.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Display name</td> 
   <td> <p>Enter or map the name that this Group displays in its address book.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias for Group</td> 
   <td>Enter or map the email alias for this Group. You can include lowercase letters, numbers, and underscores. For the Office 365 Group type, this will be the Group's email alias ([Alias]@[Your Domain].onmicrosoft.com). For Security Group type, the alias functions as a nickname.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Description</td> 
   <td>Enter or map a description for this Group.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Security enabled</td> 
   <td>Enable this option if you want the Group to be security enabled.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Visibility</td> 
   <td>Specify the visibility of the Office 365 Group.</td> 
  </tr> 
 </tbody> 
</table>

#### Watch Teams

This trigger module starts a scenario when a Team or Group is created or updated.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>You can set a filter to watch for only Teams and Groups that meet criteria you select.</p> <p>For each filter, enter the field you want the filter to evaluate, the operator, and the value that you want the filter to allow. You can use more than one filter by adding AND or OR rules.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximum number of returned results</td> 
   <td>Set the maximum number of Teams or Groups Workfront Fusion will return during one execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

### Channel

#### Create a channel

This action module creates a new channel for the specified team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team ID</td> 
   <td> <p>Select the Microsoft Team that you want to create a channel for.</p> </td> 
   </tr> 
  <tr> 
   <td>Channel name</td> 
   <td>Enter or map a name for the new channel.</td> 
  </tr> 
  <tr> 
   <td>Descriptione</td> 
   <td>Enter or map a description for the new channel.</td> 
  </tr> 
 </tbody> 
</table>

#### Delete a channel

This action module deletes the specified channel from a Microsoft Team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team ID</td> 
   <td> <p>Enter or map the ID of the Microsoft Team that you want to delete a channel from.</p> </td> 
   </tr> 
  <tr> 
   <td>Channel ID</td> 
   <td>Enter or map the ID of the channel you want to delete.</td> 
  </tr> 
  </tbody> 
</table>

#### Get a channel

This module retrieves the properties and relationships of a channel.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team ID</td> 
   <td> <p>Enter or map the ID of the Microsoft Team that owns the channel you want to retrieve details for.</p> </td> 
   </tr> 
  <tr> 
   <td>Channel ID</td> 
   <td>Enter or map the ID of the channel you want to retrieve details for.</td> 
  </tr> 
  </tbody> 
</table>

#### List channels

This modules lists channels owned by the specified Microsoft Team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team ID</td> 
   <td> <p>Select the Microsoft Team that you want to list channels for.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximum number of returned results</td> 
   <td>Set the maximum number of channels Workfront Fusion will return during one execution cycle.</td> 
  </tr> 
  </tbody> 
</table>

#### Update a channel

This action module updates the description of the specified channel.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team ID</td> 
   <td> <p>Select the Microsoft Team that owns the channel you want to update.</p> </td> 
   </tr> 
  <tr> 
   <td>Channel name</td> 
   <td>Enter or map the name of the channel that you want to update.</td> 
  </tr> 
  <tr> 
   <td>Description</td> 
   <td>Enter or map the new description for the channel.</td> 
  </tr> 
 </tbody> 
</table>

### Message

#### Reply to a channel message

#### Send a message

#### Watch messages

#### Watch messages (deprecated)

#### Watch new replies

### Member

#### Add a memner

#### Add a member to a Group

### Online meeting

#### Create an online meeting

#### Delete an online meeting

#### Get an online meeting

#### Update an online meeting

### Other

#### Get a user's presence

#### Make an API call

#### Search users







