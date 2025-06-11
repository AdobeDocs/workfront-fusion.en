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

* [Create a channel](#create-a-channel)
* [Delete a channel](#delete-a-channel)
* [Get a channel](#get-a-channel)
* [List channels](#list-channels)
* [Update a channel](#update-a-channel)

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

* [Reply to a channel message](#reply-to-a-channel-message)
* [Send a message](#send-a-message)
* [Watch messages](#watch-messages)
* [Watch new replies](#watch-new-replies)

#### Reply to a channel message

This action module creates a reply to a message in the specified channel.

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
   <td> <p>Select the Microsoft Team that owns the channel that contains the message you want to reply to.</p> </td> 
   </tr> 
  <tr> 
   <td>Channel ID</td> 
   <td>Select the channel that contains the message you want to reply to.</td> 
  </tr> 
  <tr> 
   <td>Message ID</td> 
   <td>Enter or map the ID of the message you want to reply to.</td> 
  </tr> 
  <tr> 
   <td>Content type</td> 
   <td>Select whether you want to send the message in plain text or HTML format.</td> 
  </tr> 
  <tr> 
   <td>Reply message</td> 
   <td>Enter or map the body of the reply message you want to send.</td> 
  </tr> 
 </tbody> 
</table>

#### Send a message

This action module sends a message to a team's channel or to a chat.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Message type/td> 
   <td> <p>Select whether you are sending a channel message or a chat message.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Team ID</td> 
   <td> <p>If you are sending a message to a channel, enter or map the ID of the Microsoft Team that owns the channel that you want to send a message to.</p> </td> 
   </tr> 
  <tr> 
   <td>Channel ID</td> 
   <td>If you are sending a message to a channel, enter or map the ID of the channel that you want to send a message to.</td> 
  </tr> 
  <tr> 
   <td>Create a new chat</td> 
   <td>If you are sending a chat message, select whether you want to create a new chat.
   <ul><li><b>Yes</b><p>Select whether you want a one-on-one chat or a group chat, and select the member that you want to include in the chat. You must select the user associated with the connection this module uses, and a one-on-one chat must contain only that user and one other user.</p><p>If you are creating a group chat, you can set a topic in the Topic field.</p>
   <li><b>No</b><p>Enter or map the ID of the team that owns the channel you want to send a message to, then enter or map the ID of the channel.</td> 
  </tr> 
  <tr> 
   <td>Message</td> 
   <td>Enter or map the body of the  message you want to send.</td> 
  </tr> 
  <tr> 
   <td>Content type</td> 
   <td>Select whether you want to send the message in plain text or HTML format.</td> 
  </tr> 
 </tbody> 
</table>

#### Watch messages

This trigger module starts a scenario when a message is sent to a team's channel or to a chat.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type of messages to watch</td> 
   <td> <p>Select whether you want to watch channel messages or chat messages.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Team ID</td> 
   <td> <p>If you are watching channel messages, select the Microsoft Team that owns the channel that you watch for messages.</p> </td> 
   </tr> 
  <tr> 
   <td>Channel ID</td> 
   <td>If you are watching channel messages, select the channel that you want to watch for messages.</td> 
  </tr> 
  <tr> 
   <td>Chat ID</td> 
   <td>If you are watching chat messages, select the chat that you want to watch for messages.</td> 
  </tr> 
  <tr> 
   <td>Maximum number of returned messages</td> 
   <td>Set the maximum number of messages Workfront Fusion will return during one execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

#### Watch messages (deprecated)

<!--Check on this-->

#### Watch new replies

This trigger module starts a scenario when a new reply is received by the specified message.

This module is not available for Personal accounts.

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
   <td> <p>Select the Microsoft Team that owns the channel that you watch for replies.</p> </td> 
   </tr> 
  <tr> 
   <td>Channel ID</td> 
   <td>Select the channel that you want to watch for replies.</td> 
  </tr> 
  <tr> 
   <td>Message ID</td> 
   <td>Select the chat that you want to watch for replies.</td> 
  </tr> 
  <tr> 
   <td>Maximum number of returned replies</td> 
   <td>Set the maximum number of replies Workfront Fusion will return during one execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

### Member

* [Add a member](#add-a-member)
* [Add a member to a group](#add-a-member-to-a-group)

#### Add a member

This action module adds a member to Microsoft Teams.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Member name</td> 
   <td> <p>Enter or map the name of the member that you want to add to Microsoft Teams.</p> </td> 
   </tr> 
  <tr> 
   <td>Password</td> 
   <td>Enter or map the password for the member.</td> 
  </tr> 
 </tbody> 
</table>

#### Add a member to a Group

This action module adds a member to an Office 365 Group.

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
   <td> <p>Select the group that you want to add a member to.</p> </td> 
   </tr> 
  <tr> 
   <td>Member ID</td> 
   <td>Select the member that you want to add to the group.</td> 
  </tr> 
 </tbody> 
</table>

### Online meeting

#### Create an online meeting

This action module creates a standalone meeting that is not associated with an event on the user's calendar. This meeting will not appear on the user's calendar.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Subject</td> 
   <td>Enter or map a subject for this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Start date and time</td> 
   <td>Enter or map the date and time that you want the meeting to start. For a list of supported date formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">End date and time</td> 
   <td>Enter or map the date and time that you want the meeting to end. For a list of supported date formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Allowed Presenters</td> 
   <td>Select the group that is allowed to present in this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Attendiees</td> 
   <td>For each attendee that you want to add to the meeting, click <b>Add item</b> and select the attendee's name and role.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Allow attendees to enable their cameras</td> 
   <td>Select whether you want to allow attendees to enable their own cameras.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Allow attendees to enable their microphones</td> 
   <td>Select whether you want to allow attendees to enable their own microphones.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Allow meeting chat</td> 
   <td>Select whether you want the meeting chat to be enabled, disabled, or limited to the duration of the meeting call</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Allow Teams reactions</td> 
   <td>Select whether you want to enable Teams reactions for this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Thread ID</td> 
   <td>Enter or map the ID of a thread associated with this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Message ID</td> 
   <td>Enter or map the ID of a message associated with this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Reply chain message ID</td> 
   <td>Enter or map the ID of the reply chain associated with this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Announce entry and exit</td> 
   <td>Select whether you want the meeting to announce when attendees enter or exit.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Scope</td> 
   <td>Select the group of attendees that can bypass waiting in the lobby. These attendees will join the meeting directly.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Enable dial-in users to bypass lobby</td> 
   <td>Select whether to enable dial-in users to bypass the lobby.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Record automatically</td> 
   <td>Select whether you want to record the meeting automatically.</td> 
   </tr> 
   </tbody> 
</table>

#### Delete an online meeting

This action module deletes the online meeting with the specified ID.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Meeting ID</td> 
   <td> <p>Enter or map the ID of the meeting that you want to delete.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Get an online meeting

This action module retrieves details of the online meeting with the specified ID.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Meeting ID</td> 
   <td> <p>Enter or map the ID of the meeting that you want to retrieve details for.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Update an online meeting

This action module updates the online meeting withthe specified ID.



<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Microsoft Teams account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Meeting ID</td> 
   <td>Enter or map the ID of the meeting that you want to update.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Subject</td> 
   <td>Enter or map a subject for this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Start date and time</td> 
   <td>Enter or map the date and time that you want the meeting to start. For a list of supported date formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">End date and time</td> 
   <td>Enter or map the date and time that you want the meeting to end. For a list of supported date formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Allowed Presenters</td> 
   <td>Select the group that is allowed to present in this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Attendiees</td> 
   <td>For each attendee that you want to add to the meeting, click <b>Add item</b> and select the attendee's name and role.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Allow attendees to enable their cameras</td> 
   <td>Select whether you want to allow attendees to enable their own cameras.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Allow attendees to enable their microphones</td> 
   <td>Select whether you want to allow attendees to enable their own microphones.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Allow meeting chat</td> 
   <td>Select whether you want the meeting chat to be enabled, disabled, or limited to the duration of the meeting call</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Allow Teams reactions</td> 
   <td>Select whether you want to enable Teams reactions for this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Thread ID</td> 
   <td>Enter or map the ID of a thread associated with this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Message ID</td> 
   <td>Enter or map the ID of a message associated with this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Reply chain message ID</td> 
   <td>Enter or map the ID of the reply chain associated with this meeting.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Announce entry and exit</td> 
   <td>Select whether you want the meeting to announce when attendees enter or exit.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Scope</td> 
   <td>Select the group of attendees that can bypass waiting in the lobby. These attendees will join the meeting directly.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Enable dial-in users to bypass lobby</td> 
   <td>Select whether to enable dial-in users to bypass the lobby.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Record automatically</td> 
   <td>Select whether you want to record the meeting automatically.</td> 
   </tr> 
   </tbody> 
</table>

### Other

#### Get a user's presence

#### Make an API call

#### Search users







