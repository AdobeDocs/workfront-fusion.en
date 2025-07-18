---
title: Adobe Workfront Boards modules
description: You can use the Adobe Workfront Boards connector to automate your processes within Workfront Boards and connect it to third-party apps and services.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: dcc5044d-8fdf-4a74-b664-e965e714ce92
---
# [!DNL Adobe Workfront] Boards modules

>[!NOTE]
>
>The Boards Fusion connector is in a beta status. As a result, support for this connector is limited and may change due to future development of Boards. In addition, there may be changes to the GraphQL API without notice that could impact your Fusion connector process.

Adobe Workfront Boards are flexible tools that allow team collaboration by providing access to a shared board that contains columns and cards.

You can use the Adobe Workfront Boards modules to read or update records, make an API call to the Workfront Boards API, or trigger a scenario when an action occurs on a board.

<!--For general information on Workfront Boards, see [Boards overview](/help/quicksilver/agile/boards-overview.md).-->

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

You must have configured a board in Adobe Workfront before you can connect to it.

## Adobe Workfront Boards API information

The Adobe Workfront Boards connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.23.6</td> 
  </tr>
 </tbody> 
 </table>

## Create a connection to Workfront Boards

>[!NOTE]
>
>You can use a Workfront connection to connect to Workfront Boards, or you can create a separate Workfront Boards connection.

To create a Workfront Boards connection:

1. In any [!DNL Adobe Workfront Boards] module, click **[!UICONTROL Add]** next to the Connection box.

1. Fill in the following fields:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Enter a name for this connection.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Environment]</td>
          <td>Select whether you are connecting to a production or non-production environment.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Type]</td>
          <td>Select whether you care connecting to a service account or a personal account.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]<p>(Optional)</p></td>
          <td>Enter your [!DNL Adobe] [!UICONTROL Client ID]. This can be found in the [!UICONTROL Credentials details] section of the [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]<p>(Optional)</p></td>
          <td>Enter your [!DNL Adobe] [!UICONTROL Client Secret]. This can be found in the [!UICONTROL Credentials details] section of the [!DNL Adobe Developer Console].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Authentication URL]<p>(Optional)</p></td>
          <td>Enter the URL that your instance of Workfront will use to authenticate this connection. <p>The default value is <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host prefix]</td>
          <td>Enter your host prefix.<p>The default value is <code>origin-</code>.</p>
        </tr>
      </tbody>
    </table>
1. Click **[!UICONTROL Continue]** to save the connection and return to the module.

## Adobe Workfront Boards modules and their fields

When you configure Workfront Boards modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional Workfront Boards fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Cards](#cards)
* [Boards](#boards)
* [Columns](#columns)
* [Tags](#tags)
* [Comments](#comments)
* [Other](#other)

### Cards

* [Add checklist item](#add-checklist-item)
* [Add subtask](#add-subtask)
* [Create a card](#create-a-card)
* [Move a card](#move-a-card)
* [Read a card](#read-a-card)
* [Update a card](#update-a-card)

#### Add checklist item

This action module adds a checklist item to the specified card.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Enter or map the ID of the card you want to add a checklist item to.<p>You can find the card ID in the URL when viewing the card in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Checklist items]</td> 
   <td>For each checklist item you want to add, click Add item, enter the checklist item's name, and select whether the item has been completed.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Add subtask

This action module adds a subtask to a card in Boards. The card must be a connected card. The subtask is also added to the Workfront task that the card represents.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Parent card ID]</td> 
   <td>Enter or map the ID of the card you want to add a subtask to.<p>You can find the card ID in the URL when viewing the card in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Enter or map the ID of the board that contains the card you want to add a subtask to.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Enter or map a name for the new subtask.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Create a card

This action module creates a new card on a Workfront board.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Enter or map the ID of the board that you want to add a card to.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column ID]</td> 
   <td>Enter or map the ID of the column you want to add a subtask to.<p>You can find the column ID in the information that is returned from the Read a board module.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Enter or map a name for the new card.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Move a card

This action module moves a card to a different column on the same board.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Enter or map the ID of the card you want to move.<p>You can find the card ID in the URL when viewing the card in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Enter or map the ID of the board that contains the card you want to move.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination column ID]</td> 
   <td>Enter or map the ID of the column you want to move the card to.<p>You can find the column ID in the information that is returned from the Read a board module.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To index]</td> 
   <td>Enter or map the position that you want the card to have in the new column.<p>The top position in the column in index 0.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Read a card

This action module retrieves information about a specific card.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Enter or map the ID of the card you want to read.<p>You can find the card ID in the URL when viewing the card in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Enter or map the ID of the board that contains the card you want to read.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Update a card

This action module updates information for a card you specify.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Enter or map the ID of the card you want to update.<p>You can find the card ID in the URL when viewing the card in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Enter or map the ID of the board that contains the card you want to update.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Enter or map a new name for the card.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Enter or map a new description for the card.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Estimation]</td> 
   <td>Enter or map an estimation of the time needed to complete this card.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Due date]</td> 
   <td>Enter or map the due date for this card.</p>
   <p>For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p>
   </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Status]</td> 
   <td>Select a new status for the card.</p></td> 
  </tr> 
 </tbody> 
</table>

### Boards

* [Create a board](#create-a-board)
* [Read a board](#read-a-board)

#### Create a board

This action module creates a board in Workfront. You can specify the type of board you want to create.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board name]</td> 
   <td>Enter or map a name for the new board.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Template]</td> 
   <td>Select the template for the type of board you want to create.</td> 
  </tr> 
 </tbody> 
</table>

#### Read a board

This action module returns information about a single board, such as the board's cards, columns, tags, and members.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Enter or map the ID of the board that you want to retrieve information for.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
 </tbody> 
</table>

### Columns

* [Create a column](#create-a-column)
* [Search for a column](#search-for-a-column)
* [Update a column](#update-a-column)

#### Create a column

This action module creates a new column on the specified board.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Enter or map the ID of the board that you want to add a column to.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column ID]</td> 
   <td>Enter or map the ID of the column you want to update.<p>You can find the column ID in the information that is returned from the Read a board module.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column name]</td> 
   <td>Enter or map a new name for the column.</td> 
  </tr> 
 </tbody> 
</table>

#### Search for a column

This search module returns information about the column with the specified name.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Enter or map the ID of the board that contains the column you want to retrieve.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Name]</td> 
   <td>Enter or map the name of the column you want to retrieve.</td> 
  </tr> 
 </tbody> 
</table>

#### Update a column

This action module updates the name or WIP limit of the specified column.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Enter or map the ID of the board that contains the column you want to retrieve.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Name]</td> 
   <td>Enter or map the name of the column you want to retrieve.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL WIP Limit]</td> 
   <td>Enter or map a new WIP limit for the column.</td> 
  </tr> 
 </tbody> 
</table>

### Tags

* [Add a tag to a card](#add-a-tag-to-a-card)
* [Create a tag](#create-a-tag)

#### Add a tag to a card

This action module adds a tag to a card.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Enter or map the ID of the card you want to add a tag to.<p>You can find the card ID in the URL when viewing the card in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Enter or map the ID of the board that contains the card you want to add a tag to.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag ID]</td> 
   <td>Enter or map the ID of the tag you want to add.<p>You can find the tag ID in the information that is returned from the Read a board module.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Create a tag 

This action module creates a new tag and assigns it a color.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Enter or map the ID of the board that you want to create a tag for.<p>You can find the board ID in the URL when viewing the board in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag name]</td> 
   <td>Enter or map the a name for the new tag.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag Color]</td> 
   <td>Select the color for this tag.</td> 
  </tr> 
 </tbody> 
</table>

### Comments

* [Create a comment](#create-a-comment)
* [Read card comments](#read-card-comments)

#### Create a comment

This action module created a comment on the specified card.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Enter or map the ID of the card you want to add a comment to.<p>You can find the card ID in the URL when viewing the card in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Enter or map the text of the comment that you want to add.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Read card comments

This action module retrieves the comments from the specified card.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Enter or map the ID of the card you want to retrieve the comments for.<p>You can find the card ID in the URL when viewing the card in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Enter the maximum number of comments that you want the module to return in one execution cycle.</p></td> 
  </tr> 
 </tbody> 
</table>

### Other

#### Make a custom API call

This action module makes a custom call to the Workfront Boards API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Enter a path relative to<code> https://&lt;WORKFRONT_DOMAIN&gt;/boards-service/graphql?</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p><p>For most boards calls the method is POST. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object. This determines the content type of the request.</p> <p>For example,<code> { "Content-type":"application/json-stringify()"}</code></p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Add the query for the API call in the form of a standard JSON object.</p> <p>For Workfront Boards, this section is usually left empty.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Add the body content for the API call in the form of a JSON embedded Graphql </p> <p>Example:</p><p>This example updates a column name. You can include the <code>boardId</code> and <code>columnId</code> as GUIDs either hard coded or mapped from a previous module.<p><pre>{<br>  "query": "mutation { updateColumn(boardId: \"\", columnId: \"\", updateColumnInput: { name: \"\" }) { id name }}"<br>}</pre><p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


#### Make a custom GraphQL API call

This action module makes a custom GraphQL request to the Workfront Boards API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Select the method for this call. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Add the query for the API call in the form of a standard JSON object.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation name]</td> 
   <td> <p>Enter a name for this operation. This can make tracing and debugging the call easier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variables data source]</td> 
   <td> <p>Select whether the variables will be from a form or from a collection.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variables]</td> 
   <td> <p>For each variable that you want to add, click <b>Add item</b> and enter the variable's key and value.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
   </tr> 
 </tbody> 
</table>
