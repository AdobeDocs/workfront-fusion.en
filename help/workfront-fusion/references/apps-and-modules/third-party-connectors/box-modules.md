---
title: Box modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Box, as well as connect it to multiple third-party applications and services. monitors a specified folder to check for file changes, to modify and delete existing files, or to upload new files to a folder.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
---
# Box modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use [!DNL Box], as well as connect it to multiple third-party applications and services. monitors a specified folder to check for file changes, to modify and delete existing files, or to upload new files to a folder.

For instructions on creating a scenario, see the articles under [Create scenarios: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

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

To use [!DNL Box] modules, you must have a [!DNL Box] account.

## Box API information

The Box connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API version</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box] modules and their fields

When you configure [!DNL Box] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Box] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Actions](#actions)
* [Searches](#searches)

### Triggers

* [[!UICONTROL New File Event]](#new-file-event)
* [New Folder Event](#new-folder-event)
* [[!UICONTROL Watch Files]](#watch-files)

#### [!UICONTROL New File Event] 

This instant trigger module starts a scenario when a the selected action occurs on a file..

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Select the webhook that you want to use to watch outgoing messages, or add a webhook. </p><p>To add a webhook, click <strong>[!UICONTROL Add]</strong> and enter the webhook's name and connection, the file that you want to watch, and the triggers that you want to watch for.</p> <p> For instructions about connecting your [!UICONTROL Box] account to [!UICONTROL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Connect to a service - Basic instructions</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### New Folder Event

This instant trigger module starts a scenario when the selection action occurs in the folder.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Select the webhook that you want to use to watch outgoing messages, or add a webhook. </p><p>To add a webhook, click <strong>[!UICONTROL Add]</strong> and enter the webhook's name and connection, the folder that you want to watch, and the triggers that you want to watch for.</p> <p> For instructions about connecting your [!UICONTROL Box] account to [!UICONTROL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Connect to a service - Basic instructions</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Files] 

This trigger module starts a scenario when a new file is added or an existing file is updated in a folder being watched.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">Watch in folder</td> 
   <td> <p>Select the folder you want to watch. A scenario can watch a single folder.</p> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Watch</td> 
   <td> <p>Select the type of files you want to watch.</p> 
    <ul> 
     <li> <p><strong>Only new files</strong> </p> <p>The scenario will start when a new file is added.</p> </li> 
     <li> <p><strong>New files and all changes</strong> </p> <p>The scenario starts when a file is added, or when file content or a file attribute (such as its name) is modified.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Maximum number of downloaded files</p> </td> 
   <td> <p>Enter the highest number of files you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

<!--* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Upload] a file](#upload-a-file)-->
* [Create a Folder](#create-a-folder)
* [Get a Folder](#get-a-folder)
* [Get Folder Metadata](#get-folder-metadata)
* [Make an API Call](#make-an-api-call)
* [Update Folder Metadata](#update-folder-metadata)

<!--#### [!UICONTROL Delete a file] 

This action module deletes a file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

This action module downloads a file.

You specify the ID of the file.

>[!NOTE]
>
>This module is useful for providing files to subsequent modules.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to retrieve.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a file] 

This action module updates a file.

You specify the ID of the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to update.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file] 

This action module uploads a file.

You specify the file. You can also provide a new filename for the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Select the folder where you want to upload the file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If this module is not successful, consider the following:
>
>* The size of the file might exceed the maximum file size limit for your [!DNL Box] plan, or you may have used all of your [!DNL Box] account's storage quota. To get more storage space, delete existing files from [!DNL Box] or upgrade your [!DNL Box] account.
>* [!DNL Box] does not upload more than one files with the same name to a single folder. If the destination folder contains a file with the same name as the file being uploaded, the scenario run terminates with an error. To avoid this, rename the file. If you want to update the file, use the **[!UICONTROL Update a file]** module.-->

#### Create a Folder

This action module creates a new empty folder inside the specified parent folder.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td> <p>Enter or map a name for the new folder.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder]</td> 
   <td> <p>Select the folder where you want to create the new folder.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder Upload Email Access]</td> 
   <td> <p>When this parameter has been set, users can email files to the email address that has been automatically created for this folder. The collaborators options allows only registered emails for collaborators.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Synchronization State]</td> 
   <td> <p>Specifies whether a folder should be synced to a user's device or not. This is used by Box Sync (discontinued) and is not used by Box Drive.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Get a Folder

This action module retrieves details for a folder, including the first 100 entries in the folder.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Select the folder that you want to retrieve details for.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Get Folder Metadata

This action module retrieves folder metadata by folder ID.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> <p>Select the scope that you want to use for this metadata retrieval.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Select the folder that you want to retrieve metadata for.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Make an API Call

This action module makes a custom call to the Box API.



<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to Workfront Fusion, see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to Workfront Fusion </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Enter a path relative to <code>https://api.box.com</code>. <p>Example: <code>/2.0/users/me</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion adds the authorization headers for you.</p> </td> 
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
 </tbody> 
</table>

#### Update Folder Metadata

This action module creates or updates the metadata of a folder.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> <p>Select the scope that you want to use for this metadata update.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Select the folder that you want to update metadata for.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Searches

#### Search for Content

This search module searches for items that are available to the user or to the emtire enterprise.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Enter or map the string to search for. This query is matched against item names, descriptions, text content of files, and various other fields of the different item types.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> <p>Select whether you are searching for content associated with the user whose credentials are used for the connection used in this module, or searching for content associated with the entire enterprise.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Select whether you are searching for files, folders, or web links.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort]</td> 
   <td> <p>Select whether you want to sort by relevance or by modified date.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trash Content]</td> 
   <td> <p>Select whether you want to search trashed content or content that hasn't been trashed.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder IDs]</td> 
   <td> <p>To search in a specific folder, for each folder you want to search, click <b>Add item</b> and enter the ID of the folder. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created From]</td> 
   <td> <p>To search for assets created in a certain date range, enter the earliest date in the range.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created to]</td> 
   <td> <p>To search for assets created in a certain date range, enter the latest date in the range.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Updated From]</td> 
   <td> <p>To search for assets updated in a certain date range, enter the earliest date in the range.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Updated to]</td> 
   <td> <p>To search for assets updated in a certain date range, enter the latest date in the range.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>For each attribute that you want to return in the module's response, click <b>Add item</b> and enter the field.</p><p>This can be used to request fields that are not normally returned in a standard response. Be aware that specifying this parameter will have the effect that none of the standard fields are returned in the response unless explicitly specified. </p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Extensions]</td> 
   <td> <p>To limit the search to specific file extensions, enter a comma-separated list of file extensions.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size From]</td> 
   <td> <p>To search for assets in a specific size range, enter the small end of the range, in bytes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size To]</td> 
   <td> <p>To search for assets in a specific size range, enter the large end of the range, in bytes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner User ID]</td> 
   <td> <p>To search for assets owned by specific users, enter a comma-separated list of owner IDs.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of results that you want the module to return in each execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>


