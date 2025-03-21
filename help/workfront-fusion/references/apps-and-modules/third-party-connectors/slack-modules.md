---
title: Slack modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use Slack, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: c9c68a4c-f592-42d1-b15f-a525b9aa3944
---
# [!DNL Slack] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Slack], as well as connect it to multiple third-party applications and services.

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

To use [!DNL Slack] modules, you must have a [!DNL Slack] account.

## Slack API information

The Slack connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td>&#123;&#123;ifempty(parameters.domain, 'https://slack.com/api/')&#125;&#125;</td> 
  </tr>
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v4.0.15</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Slack] modules and their fields

When you configure [!DNL Slack] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Slack] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Messages](#messages)
* [Conversations](#channels)
* [Other](#other)

### Messages

* [Create a Message](#create-a-message)
* [Delete a message](#delete-a-message)
* [Get a Private Channel Message](#get-a-private-channel-message)
* [Get a Public Channel Message](#get-a-public-channel-message)
* [Update a Message](#update-a-message)
* [Watch Private Channel Messages](#watch-private-channel-messages)
* [Watch Public Channel Messages](#watch-public-channel-messages)

### [!UICONTROL Create a Message]

This action module creates a new message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choose how you want to select the channel where you want to create a message.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Channel ID or name]</strong> field, enter or map the Channel ID or name of the channel where you want to post the message.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the type of channel, then select the channel.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>Enter the text content of the message you want to create.</p> <p>Note: For detailed information about text formatting, see <a href="https://api.slack.com/reference/surfaces/formatting">Formatting text for app surfaces</a> in the [!DNL Slack] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL As user]</td> 
   <td>Enable this option to post the message as the user that owns the credentials used by the connection for this module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thread message ID (time stamp)]</td> 
   <td>If the new message is a reply, enter the time stamp of the message you want to reply to. Do not enter the time stamp of a message that is already a reply.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reply broadcast]</td> 
   <td> <p>Select <strong>[!UICONTROL Yes]</strong> if both of the following apply:</p> 
    <ul> 
     <li> <p>The new message is a reply to another message</p> </li> 
     <li> <p>You want the new message to be visible to everyone in the channel</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachments]</td> 
   <td>For each item that you want to attach to the message, click <b>Add item</b> and fill in the item's details.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Icon emoji]</td> 
   <td>Enter or map the emoji to use as the icon for this message, in the format <code>:icon-name:</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Icon URL]</td> 
   <td>Enter or map the URL of the image to use as the icon for this message. </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Link names]</p> </td> 
   <td> <p>Enable this option to allow names and channels to use <code>@username</code> or <code>#channel</code> format. </p> <p>For more information, see <a href="https://api.slack.com/docs/formatting">Formatting text for app surfaces</a> in the [!DNL Slack] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse message text]</p> </td> 
   <td> <p>Enable this option to allow automatic parsing. </p> <p>For more information, see <a href="https://api.slack.com/docs/formatting">Formatting text for app surfaces</a> in the [!DNL Slack] documentation.</p> <p>Note: If you used [!UICONTROL Link names] or [!UICONTROL Parse message text] options in the original message, you should specify them when running the [!UICONTROL Update a Message] module as well.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Use markdown]</p> </td> 
   <td> <p>Enable this option to allow [!DNL Slack] to use markdown in the text.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Unfurl primarily text-based content]</p> </td> 
   <td> <p>Enable this option to allow unfurling of primarily text-based content. </p> <p>For more information about unfurling in [!DNL Slack], see <a href="https://api.slack.com/reference/messaging/link-unfurling">Unfurling links in messages</a> in the [!DNL Slack] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Unfurl media content]</p> </td> 
   <td> <p>Enable this option to allow unfurling of media content. </p> <p>For more information about unfurling in [!DNL Slack], see <a href="https://api.slack.com/reference/messaging/link-unfurling">Unfurling links in messages</a> in the [!DNL Slack] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User name]</td> 
   <td>Specify the user name used to post the message. If no user name is specified, the name "Bot" is used.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Message]

This action module deletes a specified message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Enter or map the Channel ID.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Enter or map the time stamp of the message you want to delete.</p> <p>Note: The time stamp can be retrieved using another module, such as the Watch Private Channel Module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Private Channel Message]

This action module retrieves the details of a message from a selected channel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Enter (map) the Channel ID.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Message ID (Time stamp)]</p> </td> 
   <td> <p> Enter or map the message time stamp of the message you want to retrieve information about.</p> <p>Note: The time stamp can be retrieved using another module, such as the [!UICONTROL Watch Public Channel] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Public Channel Message]**

This action module returns a message with a given ID from a specified public channel..

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Enter or map the Channel ID.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (Time stamp)]</td> 
   <td> <p> Enter or map the message time stamp of the message you want to retrieve information about.</p> <p>Note: The time stamp can be retrieved using another module, such as the [!UICONTROL Watch Public Channel] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Message]

This action module allows you to edit an existing message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choose how you want to select the message you want to .</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Channel ID or name]</strong> field, enter or map the Channel ID or of the channel that contains the message, then enter the <strong>[!UICONTROL Time Stamp (Message ID)]</strong> of the message. .</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the type of channel, then select the channel, then select the message.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>Enter the new text content of the message you want to update.</p> <p>For more information, see <a href="https://api.slack.com/docs/formatting">Formatting text for app surfaces</a> in the [!DNL Slack] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blocks]</td> 
   <td>Blocks are reusable components that you can use to customize and organize your messages. For more information on blocks, see <a href="https://api.slack.com/block-kit">Block Kit</a> in the [!DNL Slack] documentation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Link names]</p> </td> 
   <td> <p>Enable this option to allow names and channels to use <code>@username</code> or <code>#channel</code> format. </p> <p>For more information, see <a href="https://api.slack.com/docs/formatting">Formatting text for app surfaces</a> in the [!DNL Slack] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse message text]</p> </td> 
   <td> <p>Enable this option to allow automatic parsing. </p> <p> For more information, see <a href="https://api.slack.com/docs/formatting">Formatting text for app surfaces</a> in the [!DNL Slack] documentation.</p> <p>Note: If you used [!UICONTROL Link names] or [!UICONTROL Parse message text] options in the original message, you should specify them when running the Update a Message module as well.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Watch Private Channel Messages]

This trigger module starts the scenario when a new message is added to a private channel (group).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Select the private channel you want to watch for new messages.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Set the maximum number of messages [!DNL Workfront Fusion] will return during one execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Public Channel Messages]

This trigger module starts the scenario when a new message is added to a public channel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Select the public channel you want to watch for new messages.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Set the maximum number of messages [!DNL Workfront Fusion] will return during one execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Conversations

* [Get a Channel](#get-a-channel)
* [List Channels](#list-channels)
* [List Members in Channel](#list-members-in-channel)

#### [!UICONTROL Get a Channel]

This action module returns information about a workspace channel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Enter or map the ID of the channel that you want to retrieve information about.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </td> 
  </tr> 
 </tbody> 

#### [!UICONTROL List Channels]

This search module returns a list of all channels in a workspace.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Exclude archived]</p> </td> 
   <td> <p>Select [!UICONTROL Yes] to exclude archived channels in results.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Select the type(s) of channels you want to retrieve.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Set the maximum number of channels [!DNL Workfront Fusion] will return during one execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL List Members in Channel]

This search module returns a list of users in the selected channel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Select the type of channel that contains the list of members you want to list.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private Channel]</td> 
   <td>Select the channel that you want to list members of.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Set the maximum number of members [!DNL Workfront Fusion] will return during one execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Other 

#### [!UICONTROL Make an API Call]

This action module lets you make a custom authenticated call to the [!DNL Slack] API. This way, you can create a data flow automation that can't be accomplished by the other [!DNL Slack] modules.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Enter a path relative to <code>https://slack.com/api/</code>. Example: <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] adds the authorization headers for you.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Add the query for the API call in the form of a standard JSON object.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Base URL]</td> 
   <td>Select the base URL that you want to use for the API call.</td> 
  </tr> 
 </tbody> 
</table>

## Terminology

The following terminology may be useful when configuring [!DNL Slack] modules:

* **DM**: [!UICONTROL Direct Message]
* **IM**: [!UICONTROL Instant Message]
* **Private Channel**: formerly [!UICONTROL Group]
* **Direct Message**: formerly [!UICONTROL IM]
* **Channel**: [!UICONTROL Conversation] in the API documentation, [!UICONTROL channel] in the [!DNL Slack] app.
