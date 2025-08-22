---
title: Microsoft OneDrive for Business modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use [!DNL Microsoft OneDrive for Business], as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 657bea46-064e-4333-8e86-81678bb1c3bd
---
# [!DNL Microsoft OneDrive for Business] modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use [!DNL Microsoft OneDrive for Business], as well as connect it to multiple third-party applications and services.

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

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

To use [!DNL Microsoft OneDrive for Business] with Adobe Workfront Fusion, you will need a [!DNL Microsoft] account.

## Connecting the [!DNL Microsoft OneDrive for Business] service to Workfront Fusion

For instructions about connecting your [!DNL Microsoft OneDrive for Business] account to [!UICONTROL Workfront Fusion], see [Create a connection to [!UICONTROL Adobe Workfront Fusion] - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Some Microsoft apps use the same connection, which is tied to individual user permissions. Therefore, when creating a connection, the permissions consent screen displays any permissions that were previously granted to this user's connection, in addition to any new permissions needed for the current application. 
>
>For example, if a user has "Read table" permissions granted via the Excel connector and then creates a connection in the Outlook connector to read emails, the permissions consent screen will show both the already granted "Read table" permission and the newly required "Write email" permission.

## [!DNL Microsoft OneDrive for Business] modules and their fields

When you configure [!DNL Microsoft OneDrive for Business] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Microsoft OneDrive for Business] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Actions](#actions)

### Triggers

* [[!UICONTROL Watch files]](#watch-files)
* [[!UICONTROL Watch folders]](#watch-folders)

#### [!UICONTROL Watch files]

This trigger module activates when a new file is added or updated in a folder being watched.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Drive ID]</p> </td> 
   <td> <p>Select the drive that you want to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p> Select the folder that you want to watch. Within a scenario, you can only monitor one folder.</p> <p>Tip: To watch multiple folders, create an independent scenario for each of them.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL I want to watch]</p> </td> 
   <td> <p>Select whether you want to watch new files and all changes, or new files only.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned rows]</td> 
   <td> <p> Set the maximum number of results that you want the module to return during one cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch folders]

This trigger module activates when a new folder is added to the folder being watched.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Drive ID]</p> </td> 
   <td> <p>Select the drive that you want to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p> Select the folder that you want to watch. Within a scenario, you can only monitor one folder.</p> <p>Tip: To keep track of multiple folders, create an independent scenario for each of them.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL I want to watch]</p> </td> 
   <td> <p>Select whether you want to watch new folders and all changes, or new folders only.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned rows]</td> 
   <td> <p> Set the maximum number of results that you want the module to return during one cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Create a folder]](#create-a-folder)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Delete a folder]](#delete-a-folder)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Get a sharing link]](#get-a-sharing-link)
* [[!UICONTROL Upload a file]](#upload-a-file)

#### [!UICONTROL Create a folder]

Creates a folder inside the specified parent folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><strong>[!UICONTROL Connection]</strong> </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Drive ID]</strong> </td> 
   <td> <p>Select the drive where you want to create a new folder.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Folder]</strong> </td> 
   <td> <p>Select the folder that you want to create a new folder in.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Folder name]</strong> </td> 
   <td>Enter or map a name for the new folder.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a file]

This action module moves the specified file to the recycle bin.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Select the drive you want to delete a file from.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p>Enter the ID of the file you want to delete. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Select the drive you want to delete a file from.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td> <p>Enter or map the ID of the folder you want to delete. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

This action module retrieves the file with the given ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Select the drive you want to retrieve a file from.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p>Enter the ID of the file you want to retrieve. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a sharing link]

This module retrieves a link that you can share to give access to the specified file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Select the drive you want to upload a file to.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enter]</td> 
   <td> <p>Select whether you want to choose a file by using the File ID or the File path. Enter the File ID or path in the field that appears.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permission type]</p> </td> 
   <td> <p>Select whether you want people who receive the link to have read/write permissions or read only.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Scope]</td> 
   <td> <p> Select whether you want the file to be accessible by anyone who has the link or accessible to members of your organization only.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

This action module uploads a binary or text file to a specified folder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Select the drive you want to upload a file to.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Select the folder within the drive.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL If the file with the same name exists]</td> 
   <td> <p> Select what you want to do if a file with the same name as the file you are trying up upload already exists.</p> 
    <ul> 
     <li>[!UICONTROL Replace the existing file]</li> 
     <li>[!UICONTROL Rename the new file]</li> 
     <li>[!UICONTROL End with an error]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
