---
title: Trello modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use Trello, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 5df5cd2b-ad4c-4a02-9d0c-7cee35232f93
---
# [!UICONTROL Trello] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!UICONTROL Trello], as well as connect it to multiple third-party applications and services.

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

To use [!DNL Trello] modules, you must have a [!UICONTROL Trello] account.

## Trello API information

The Trello connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td> https://api.trello.com/1</td>
  </tr> 
  <tr> 
   <td role="rowheader">API version</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v4.12.37</td> 
  </tr>
 </tbody> 
 </table>

## Connect [!UICONTROL Trello] to [!DNL Workfront Fusion]

For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see [Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!UICONTROL Trello] modules and their fields

When you configure [!UICONTROL Trello] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!UICONTROL Trello] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Boards](#boards)
* [Lists](#lists)
* [Cards](#cards)
* [Members](#members)
* [Checklists](#checklists)
* [Labels](#labels)
* [Comments](#comments)

### Boards 

+++ **[!UICONTROL Archive or Unarchive a Board]**

This action module closes (archives) or re-opens (unarchives) a board that you specify.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Enter or map the ID of the board you want to close or re-open.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> Select whether you want to close (archive) or re-open (unarchive) the board.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assign a Member to a Board]**

This action module assigns a member to a board that you specify .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Select the board where you want to add a member.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email address]</td> 
   <td> <p> Enter or map the email address of the member you want to add to the board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Member type]</p> </td> 
   <td> <p>Select the type of member that you want the new member to be.</p> 
    <ul> 
     <li><strong>[!UICONTROL Admin]</strong>: A board administrator can perform any board action on the board.</li> 
     <li><strong>[!UICONTROL Normal]</strong>: A normal member is simply a member of the board.</li> 
     <li><strong>[!UICONTROL Observer]</strong>: An observer is a member with read-only access to the board. <br>Observers are only available to teams with [!UICONTROL Trello Business Class].</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Full name]</td> 
   <td> <p> Enter or map the full name of the user you want to add to the board.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Board]**

This action module creates a new board with the selected settings.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Enter or map a name for the new board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Enter or map the board description if needed.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>Enter or map the ID of the organization. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>Boards have different voting and commenting rules for each permission level. For example, if your board is [!UICONTROL Private] and you set the voting and commenting rules as [!UICONTROL All], you receive an error. </p> <p>Voting and commenting is limited to the following groups for each permission level:</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      Members, Members and Observers</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      Members, Members and Observers, Organization Members</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      Members, Members and Observers, Organization Members, All</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>Select an option to specify who can vote on this board. See the [!UICONTROL Permission level] field for voting limitations on permission levels.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>Select an option to specify who can comment on cards for this board. See the [!UICONTROL Permission level] field for commenting limitations on permission levels.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Invitations]</p> </td> 
   <td> <p>Select who can invite other people to this board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Self-join]</p> </td> 
   <td> <p>Select whether team members can join the board themselves or they have to be invited.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default labels]</p> </td> 
   <td> <p>Select whether to use the default set of labels for the new board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default lists]</p> </td> 
   <td> <p>Select whether to add the default set of lists to the board ([!UICONTROL To Do], [!UICONTROL Doing], [!UICONTROL Done]).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board source ID]</p> </td> 
   <td> <p>Select or map the ID of the board that you want to copy into the new board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card Covers]</p> </td> 
   <td> <p>Select <strong>[!UICONTROL Yes]</strong> if you want to enable card covers for the board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Background]</p> </td> 
   <td> <p>Select the color of the background or the custom background.</p> <p>Note: Custom backgrounds are available only to [!UICONTROL Trello Gold and Business Class] subscribers.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background ID]</td> 
   <td> <p> If you have selected to use a custom background in the [!UICONTROL Background] field, enter or map the ID of the background you want to use.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>Select between two modes of card aging. </p> 
    <ul> 
     <li><strong>[!UICONTROL Pirate mode]</strong>: Cards will tear, yellow, and crack like an old pirate map as they age.</li> 
     <li><strong>[!UICONTROL Regular mode ]</strong>: Cards become progressively more transparent as they age. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Board]**

This action module edits the settings of an existing board.

>[!SUCCESS]
>
><table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>Enter or map the unique [!UICONTROL Trello] ID of the board that you want the module to create. You can retrieve the Board ID using another module, such as the Watch Boards module</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/watch-boards.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p> Enter or map a new name for the board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New description]</td> 
   <td> <p> Enter or map a new board description.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>Enter or map the unique [!UICONTROL Trello] ID of the board that you want the module to edit.  </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>Select an option to specify whether the user that owns the connection used by this module is subscribed to the board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>Boards have different voting and commenting rules for each permission level. For example: if your board is [!UICONTROL Private] and you set the voting and commenting rules as [!UICONTROL All], you receive an error. </p> <p>Voting and commenting is limited to the following groups for each permission level:</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      Members, Members and Observers</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      Members, Members and Observers, Organization Members</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      Members, Members and Observers, Organization Members, All</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>Select an option to specify who can vote on this board. See the [!UICONTROL Permission level] field for voting limitations on permission levels.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>Select an option to specify who can comment on cards for this board. See the [!UICONTROL Permission level] field for commenting limitations on permission levels.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Invitations] </td> 
   <td> <p>Select who can invite people to this board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-join]</td> 
   <td> <p> Select whether team members can join the board themselves or they have to be invited.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card covers]</td> 
   <td> <p> Select whether card covers should be displayed on this board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background] </td> 
   <td> <p>Select the color of the background or the custom background.</p> <p>Note: Custom backgrounds are available only to [!UICONTROL Trello Gold and Business Class] subscribers.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background ID]</td> 
   <td> <p> If you have selected to use a custom background in the [!UICONTROL Background] field, enter or map the ID of the background you want to use.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>Select between two modes of card aging. </p> 
    <ul> 
     <li><strong>[!UICONTROL Pirate mode]</strong>: Cards will tear, yellow, and crack like an old pirate map as they age.</li> 
     <li><strong>[!UICONTROL Regular mode]</strong>: Cards become progressively more transparent as they age. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar feed enabled]</td> 
   <td> <p> Select whether the calendar feed is enabled or not.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL &lt;Color> label name]</td> 
   <td> <p> Assign a name to the desired color label.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>Select an option to indicate whether you want to archive (close) the board. </p> </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **[!UICONTROL Get a Board]**

This action module retrieves a board's details.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>Enter or map the ID of the board you want to retrieve information about.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!DNL Search for Boards]**

This search module retrieves information about a board that you specify.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Enter or map the name (or a part of the name) of the board that you want to get information about.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned boards]</td> 
   <td> <p> Enter the maximum number of boards [!DNL Workfront Fusion] will return during one execution cycle. This value must be less than or equal to 1000.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Partial] </p> </td> 
   <td> <p>By default, this module searches member content for exact matches of each word in your query. When [!UICONTROL Partial] is enabled, the module looks for content that starts with any word in your query.</p> <p> For example If you are using the word "development" to look for a board titled "My Development Status Report," by default you would need to search for the entire word. If you have [!UICONTROL Partial] enabled, you would be able to search for "dev" but not "velopment."</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Boards] </td> 
   <td> <p>Enter "mine," or map a comma-separated list of board IDs.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

This action module removes a member from a board.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Enter (map or select) the ID of the board you want to remove the user from.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Member] </td> 
   <td> <p>Select the member you want to remove from the board.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch Boards]**

This trigger module begins a scenario when a new board is added.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Enter or map the maximum number of boards you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Lists

+++ **[!UICONTROL Create a List]**

This action module creates a list on a board that you specify .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Enter or map the ID of the board where you want to create a list.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Enter or map a name for the new list.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Select whether you want to add the list to the top or append it to the bottom of the card.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy list]</td> 
   <td> <p> If you are copying a list, select how you want to enter the ID of the list you want to copy.</p> 
    <ul> 
     <li> <p><strong>Enter manually</strong> </p> <p>In the <strong>[!UICONTROL List ID]</strong> field, enter or map the ID of the list you want to copy.<br></p> </li> 
     <li> <p><strong>Select</strong> </p> <p>Select the board that contains the list you want to copy, then select the list.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a List]**

This action module edits an existing list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td> <p> Enter or map the ID of the list you want to update.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Enter or map a new name for the list.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Map or select the board where you want to move the list.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Select whether you want to add the list to the top or append it to the bottom of the card.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribed]</td> 
   <td> <p>Enable this option if you want to subscribe the active member to the list.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a List]**

This action module retrieves details about a specific list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL List ID]</p> </td> 
   <td> <p>Enter or map the ID of the list you want to retrieve information about.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch cards moved to a list]**

This trigger module activates when a card is moved to a specific list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board]</td> 
   <td>Select the board that contains the list that you want to watch for cards.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List]</td> 
   <td>Select the list that you want to watch for cards.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Cards

+++ **[!UICONTROL Add an Attachment]**

This action module adds an attachment to the selected card.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Select how you want to enter the ID of the card you want to add an attachment to.</p> 
    <ul> 
     <li> <p><strong>Enter manually</strong> </p> <p>In the <strong>[!UICONTROL Card ID]</strong> field, enter or map the ID of the card you want to add an attachment to.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card you want to add an attachment to, then select the list that contains the card, then select the card.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment type]</p> </td> 
   <td> <p>Select whether you want to upload the file directly or provide a URL to the file.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Select a source file from a previous module, or map the source file's name and data.</p> </li> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Enter the URL to the file, and provide a name for the attachment.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archive or Unarchive a Card]**

This action module archives or sends a card back to the board.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card ID]</td> 
   <td> <p> Enter or map the ID of the card you want to archive or send back to the board.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> Select whether you want to close the card (archive) or send it back to the board (unarchive).</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a card]**

This action module creates a card in a selected list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a list ID]</td> 
   <td> <p> Select how you want to enter the ID of the list where you want to add a card.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL List ID]</strong> field, enter or map the ID of the list where you want to add a card.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the list where you want to add a card, then select the list.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>For each label that you want to add to the card, click <b>Add item</b> and enter the ID of the label.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members]</td> 
   <td>For each member that you want to add to the card, click <b>Add item</b> and enter the ID of the member. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Enter a name for the new card.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Description]</p> </td> 
   <td> <p>Enter the description for the card.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Select whether you want to add the card to the top or append the card to the bottom of the list.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> Enter a due date for the card. For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Enable this option to mark the card as complete on the due date.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td> <p>Enter or map the URL of a file that you want to add as an attachment to the card.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Source file]</p> </td> 
   <td> <p>Enter or map information for a file you to want to add as an attachment to the card. Select a file from a previous module, or map the file's name and data</p> 
     <p>Note: There is a 10 MB file upload limit per attachment. However, [!UICONTROL Business Class] and [!UICONTROL Trello Gold] members have a 250 MB file upload limit per attachment.</p> 
     </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy card]</td> 
   <td> <p> If you are creating a new card as a copy of an existing card, select how you want to enter the ID of the card you want to copy.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Card ID]</strong> field, enter or map the ID of the card you want to copy.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card you want to copy, then select the list that contains the card, then select the card.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Card]**

This action module edits an existing card.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Card ID]</td> 
   <td> <p> Select how you want to enter the ID of the card you want to edit.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Card ID]</strong> field, enter or map the ID of the card you want to edit.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card you want to edit, then select the list that contains the card, then select the card.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p>Enter or map a new name for the card.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New description]</p> </td> 
   <td> <p>Enter or map a new description for the card.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Move a card]</p> </td> 
   <td> <p>Select the board or the board and list where you want to move the card.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>For each label that you want to add to the card, click <b>Add item</b> and enter the ID of the label.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Select whether you want to add the card to the top or [!UICONTROL append] the card to the bottom of the list.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> Enter a due date for the card. For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Enable this option to mark the card as complete on the due date.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members] </td> 
   <td> <p>For each member that you want to add to the card, click <b>Add item</b> and enter or map the member's ID.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment cover ID]</p> </td> 
   <td> <p>Enter or map the ID of the image attachment that you want the card to use as its cover.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>Select whether the member should be subscribed to the card.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>Select an option to indicate whether you want to archive (close) the card. </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Card]**

This action module retrieves a selected card's details.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p>Enter the ID of the board that contains the card that you want to retrieve details about. This allows you to see names of the board's custom fields.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Select how you want to enter the ID of the card you want to retrieve details about.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Card ID]</strong> field, enter or map the ID of the card you want to retrieve details about.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card you want to retrieve details about, then select the list that contains the card, then select the card.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search for Cards]**

This action module returns cards that match the search query.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board] </td> 
   <td> <p>Select the boards you want to search through. If no board is selected, all boards will be searched.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Query]</p> </td> 
   <td> <p>Enter the search query. You can refine your search using the following search operators:</p> 
    <ul> 
     <li><code><strong>-operator</strong></code> <p>You can add "-" to any operator to do a negative search, such as <code>[!UICONTROL -has:members]</code> to search for cards without any members assigned.</p> </li> 
     <li><code><strong>@name</strong></code> <p>Returns cards assigned to a member. You can also use <code>member:</code>. Use <code>@me</code> to include only your cards.</p> </li> 
     <li><code><strong>#label</strong></code> <p>Returns labeled cards. You can also use <code>label:</code>. For example, <code>label:"FIX IT"</code> will return cards with the label named "FIX IT".</p> </li> 
     <li><code><strong>board:id</strong></code> <p>Returns cards within a specific board. For example, <code>board:Trello</code> will return cards on boards with [!UICONTROL Trello] in the board name.</p> </li> 
     <li><code><strong>list:name</strong></code> <p>Returns cards within the list named "name".</p> </li> 
     <li><code><strong>has:attachments</strong></code> <p>Returns cards with attachments. The <code>has</code>: operator can also be used with other attributes, such as <code>has:description</code>, <code>has:cover</code>, <code>has:members</code>, or <code>has:stickers</code>.</p> </li> 
     <li><code><strong>due:day</strong></code> <p>Returns cards due within 24 hours. The <code>due:</code> operator can also be used with other timeframes, such as <code>due:week</code>, <code>due:month</code>, or <code>due:overdue</code>. You can also search for a specific day range. For example, adding <code>due:14</code> to search includes cards due in the next 14 days.</p> </li> 
     <li><code><strong>created:day</strong></code> <p>Returns cards created in the last 24 hours. The<code> created:</code> operator can also be used with other timeframes such as <code>created:week</code> or <code>created:month</code>. You can also search for a specific day range. For example, adding <code>created:14</code> to the search includes cards created in the last 14 days.</p> </li> 
     <li><code><strong>edited:day</strong></code> <p>Returns cards edited in the last 24 hours. The <code>edited:</code> operator can also be used with other timeframes, such as <code>edited:week</code> or <code>edited:month</code>. You can also search for a specific day range. For example, adding <code>edited:21</code> to the search includes cards edited in the last 21 days.</p> </li> 
     <li><code><strong>description:</strong>, <strong>checklist:</strong>, <strong>comment:</strong>, and <strong>name:</strong></code> <p>Returns cards matching the text of card descriptions, checklists, comments, or names. For example, <code>comment:"FIX IT"</code> will return cards with "FIX IT" in a comment.</p> </li> 
     <li><code><strong>is:open</strong> and <strong>is:archived</strong></code> <p>Returns cards that are open or archived. If neither is specified, [!UICONTROL Trello] returns both types.</p> </li> 
     <li><code><strong>is:starred</strong> </code> <p>Only includes cards on starred boards.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned cards]</td> 
   <td> <p> Enter or map the maximum number of cards you want [!DNL Workfront Fusion] to return during one execution cycle. This value must be less than or equal to 1000.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>By default, this module searches member content for exact matches of each word in your query. When [!UICONTROL Partial] is enabled, the module looks for content that starts with any word in your query.</p> <p> For example If you are using the word "development" to look for a board titled "My Development Status Report," by default you would need to search for the entire word. If you have [!UICONTROL Partial] enabled, you would be able to search for "dev" but not "velopment."</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cards] </td> 
   <td> <p>To search specific cards, click <b>Add item</b> and add the card's ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch cards]**

This trigger module starts a scenario when a new card is added.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Select the location you want to watch for cards.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards]</strong> </li> 
     <li> <p><strong>Cards on specific board</strong> </p> <p>Select the board that you want to watch for cards</p> </li> 
     <li> <p><strong>[!UICONTROL Cards on specific list]</strong> </p> <p>Select the board that contains the list you want to watch for cards, then select the list.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Members

+++ **[!UICONTROL Add a Member to a Card]**

This action module adds the specified member to the specified card.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter card ID and member ID]</p> </td> 
   <td> <p>Choose how you want to enter the card ID and the member ID.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Card ID]</strong> and the <strong>[!UICONTROL Member ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card you want to add a member to, then select the list that contains the card, the card itself, and the member that you want to add to the card.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assign a Member to a Board]**

See "[!UICONTROL Assign a Member to a Board]" under [Boards](#boards).

+++

+++ **[!UICONTROL Search for Members]**

This action module retrieves information about [!UICONTROL Trello] members.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Enter the name or username of the user you want to find.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>By default, this module searches member content for exact matches of each word in your query. When [!UICONTROL Partial] is enabled, the module looks for content that starts with any word in your query.</p> <p> For example If you are using the word "development" to look for a board titled "My Development Status Report," by default you would need to search for the entire word. If you have [!UICONTROL Partial] enabled, you would be able to search for "dev" but not "velopment."</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned members]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

See "[!UICONTROL Unassign a Member from a Board]" under [Boards](#boards).

+++

### Checklists

+++ **[!UICONTROL Create a Checklist]**

This action module creates a checklist on the selected card.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Select how you want to enter the ID of the card where you want to add a checklist.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Card ID]</strong> field, enter or map the ID of the card where you want to add a checklist.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card where you want to add a checklist, then select the list that contains the card, then select the card.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Enter or map a name for the checklist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Select whether you want to add the checklist to the top or append the checklist to the bottom of the card.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter checklist ID]</p> </td> 
   <td> <p>If you are creating the checklist by copying an existing checklist, enter or map the ID of a source checklist that you want to copy into the new one.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Checklist Item]**

This action module adds an item to a specific checklist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter checklist ID]</td> 
   <td> <p> If you are creating a new checklist by copying an existing checklist, select how you want to enter the ID of the checklist where you want to add an item.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Checklist ID]</strong> field, enter or map the ID of the card where you want to add a checklist.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card where you want to add a checklist, then select the list that contains the card, then select the card, then select the checklist.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>Enter or map a name for the new item.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Select whether you want to add the item to the top or [!UICONTROL append] to the bottom of the checklist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Checked]</p> </td> 
   <td> <p>Enable this option if you want to add the item as already checked.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Checklist Item]**

This action module edits an existing checklist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Card ID and Checklist Item ID]</td> 
   <td> <p> Select how you want to enter the ID of the card and checklist where you want to edit an item.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Checklist ID]</strong> field, enter or map the ID of the card where you want to add a checklist.</p> <p>In the <strong>[!UICONTROL Checklist Item ID]</strong> field, enter or map the ID of the checklist.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card where you want to add a checklist, then select the list that contains the card, then select the card, then select the checklist.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Checklist ID]</td> 
   <td>Select or map the checklist that you want to move the checklist item to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>Enter or map a name for the new item.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Select whether you want to add the item to the top or append to the bottom of the checklist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL State]</p> </td> 
   <td> <p>Select whether the checklist item is complete or incomplete.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Labels

+++ **[!UICONTROL Add a Label to a Card]**

This action module adds a label to a selected card.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Select how you want to enter the ID of the card where you want to add a checklist.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Card ID]</strong> field, enter or map the ID of the card where you want to add a checklist. In the<strong>[!UICONTROL Label ID]</strong> field, enter or map the ID of the label that you want to add.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card where you want to add a checklist, then select the list that contains the card, then select the card. </p> <p>Select the label that you want to add to the card.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Comments 

+++ **[!UICONTROL Create a Comment in a Card]**

This action module adds a comment to a selected card.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Select how you want to enter the ID of the card where you want to add a comment.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Card ID]</strong> field, enter or map the ID of the card where you want to add a comment.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card where you want to add a comment, then select the list that contains the card, then select the card.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment] </td> 
   <td> <p>Enter or map the comment that you want to add to the selected card.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Comments in a Card]**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Select how you want to enter the ID of the card where you want to add a comment.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Card ID]</strong> field, enter or map the ID of the card where you want to add a comment.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Select the board that contains the card where you want to add a comment, then select the list that contains the card, then select the card.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td> 
   <td> <p> Enter the maximum number of comments [!DNL Workfront Fusion] will return during one execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since] </td> 
   <td> <p>Set the start date of the period in which the comment was created. For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before] </td> 
   <td> <p>Set the end date of the period in which the comment was created. For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch Comments]**

This trigger module starts a scenario when a comment is added.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Trello] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Select the location you want to watch for comments.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards] everywhere</strong> </li> 
     <li> <p><strong>[!UICONTROL Board]</strong> </p> <p>Select the board that you want to watch for comments</p> </li> 
     <li> <p><strong>[!UICONTROL List]</strong> </p> <p>Select the board that contains the list you want to watch for comments, then select the list.</p> </li> 
     <li><strong>[!UICONTROL Card]</strong> </li> 
     <li>Select the board that contains the card you want to watch for comments, then select the list that contains the card, then select the card.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Enter or map the maximum number of comments you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

## [!UICONTROL Trello] Object IDs

* [How to find the ID or the shortlink of a card in [!DNL Trello]](#how-to-find-the-id-or-the-shortlink-of-a-card-in-trello)
* [How to find IDs of other objects in [!DNL Trello]](#how-to-find-ids-of-other-objects-in-trello)

### How to find the ID or the shortlink of a card in [!DNL Trello] 

If you want to edit a card or create a new comment, you need to know the ID of the card or its shortlink. You can get this information from the output of the [!UICONTROL New Card] trigger. The shortlink for a card can also be obtained by opening the card and clicking on the [!UICONTROL Share] button. The shortlink can be found in the [!UICONTROL Link to this card] box, at the end of the URL after `https://trello.com/c/`.

![Share and more](/help/workfront-fusion/references/apps-and-modules/assets/share-and-more-350x575.png)

### How to find IDs of other objects in [!DNL Trello] 

Board, list and comment IDs can only be obtained using triggers. The [!DNL `trello.com`] website does not show these IDs.
