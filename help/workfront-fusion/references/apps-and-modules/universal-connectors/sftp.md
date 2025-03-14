---
title: SFTP modules
description: The [!DNL Adobe Workfront Fusion SFTP] modules allow you to monitor file changes in a selected folder/subfolder, upload new files to the desired folder, modify, or delete existing files that are already in a folder, or change file permissions.
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
---
# SFTP modules

The [!DNL Adobe Workfront Fusion] SF[!UICONTROL ]TP modules allow you to monitor file changes in a selected folder/subfolder, upload new files to the desired folder, modify, or delete existing files that are already in a folder, or change file permissions.

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

In order to use SFTP with [!DNL Workfront Fusion], it is necessary to have an SFTP account (such as [!DNL GoDaddy] web hosting).

## Connect SFTP to [!DNL Workfront Fusion] {#connect-sftp-to-workfront-fusion}

To connect your SFTP account to [!DNL Workfront Fusion] you need create a connection that specifies the target Host and the SFTP credentials (user name and password or user name and key).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection name]</td> 
   <td> <p> Enter the name for your SFTP connection.</p> </td> 
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
   <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
   <td> <p>Enter the host name of the SFTP server you want to connect.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Port] </td> 
   <td> <p>Enter the SFTP server port. For example, 22.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Auth type]</p> </td> 
   <td> <p>Select the authorization method you want to use for connecting to the SFTP server.</p> 
    <ul> 
     <li><strong>[!UICONTROL User name and password]</strong>: Enter your credentials.</li> 
     <li> <p><strong>[!UICONTROL User name and key]</strong>: Enter your user name and the private key/certificate</p> <p>Upload the private key to use the client-side authorization or upload your certificate (P12 or PFX file) if you want to use TLS using your self-signed certificate. If you're using the client-side certificate authorization, you can enter your CA certificate here.</p> <p>[!DNL Workfront Fusion] does not retain or store any data (files, passwords) you provide here. File and password are only used to extract a private key/certificate.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Key exchange algorithms] </td> 
   <td> <p>You can enter a set of algorithms for key exchange. The module prioritizes algorithms based on the order they were added. For each algorithm you want to add, click <b>Add item</b> and select the algorithm.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ciphers] </td> 
   <td> <p>You can enter a set of ciphers for key exchange. The module prioritizes ciphers based on the order they were added. For each cipher you want to add, click <b>Add item</b> and select the cipher.</p> </td> 
  </tr> 
 </tbody> 
</table>

After entering the connection information, click **[!UICONTROL Continue]** to establish a connection.

## [!UICONTROL SFTP] modules and their fields

When you configure [!UICONTROL SFTP] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!UICONTROL SFTP] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Triggers

* [Watch Files in a Folder](#watch-files-in-a-folder)
* [Watch Subfolders in a Folder](#watch-subfolders-in-a-folder)

#### [!UICONTROL Watch Files in a Folder]

Returns files with details when a file is created or changed in a specified folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Enter the folder you want to watch. You can specify an absolute path such as <code>/home/user/</code>, or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>Buffer Size [B]</td> 
   <td> <p> Enter the buffer size in bytes. The value defines the size of transferred chunks from the server. Some servers may cause problems or corrupt files when the value is too high.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Subfolders in a Folder]

Returns folders with details when a folder is created or changed in a specified folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Enter or map the folder you want to watch. You can specify an absolute path such as <code>/home/user/</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [Create a folder](#create-a-folderr)
* [Delete a file](#delete-a-file)
* [Delete a folder](#delete-a-folder)
* [Get a file](#get-a-file)
* [Get files](#get-files)
* [List a folder's content](#list-a-folders-content)
* [Move a file](#move-a-file)
* [Rename a file](#rename-a-file)
* [Update file permissions](#update-file-permissions)
* [Upload a file](#upload-a-file)

#### [!UICONTROL Create a folder]

This action module creates a new folder in the specified location.

>[!NOTE]
>
>If the folder already exists, the module will throw an error. To continue the flow uninterrupted, attach an error handler route to the module to catch the error and employ the [!UICONTROL Resume] directive to continue the flow. For information about attaching an error handler route, see [Error handling in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md). For information about the error handler route, see [Directives for error handling in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Specify an existing folder as the storage location for the new folder. You can specify an absolute path such as <code>/home/user/file.txt</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder Name]</td> 
   <td> <p> Enter the folder name.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Set the desired folder permissions. Use chmod parameters. For example, <code>777</code> or <code>-rwxrwxrwx</code>.</p> <p>These permissions must match the pattern <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>For more information about chmod, see the <a href="https://ss64.com/bash/chmod.html">chmod documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a file]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Enter the path to the file you want to delete. You can specify an absolute path such as <code>/home/user/file.txt</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Folder Path]</td> 
   <td> <p> Specify the path to the folder you want to delete. You can specify an absolute path such as <code>/home/user/</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

This module retrieves file details, including a file's data.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> Enter the buffer size in bytes. The value defines the size of transferred chunks from the server. Some servers may cause problems or corrupt files when the value is too high.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path] </td> 
   <td> <p>Enter the path to the file. You can specify an absolute path such as <code>/home/user/file.txt</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get files]

This module returns files from a specified folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> Enter the buffer size in bytes. The value defines the size of transferred chunks from the server. Some servers may cause problems or corrupt files when the value is too high.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Enter or map the folder that contains the files or folders you want to list. You can specify an absolute path such as <code>/home/user/</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Enter or map the search term. For example, if you want to search for files with the file extension .txt, enter <code>.txt</code>.You can also enter or map the name of the file you want to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> Select whether you want to sort results by the file name, size, last access date, or last modified date.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order]</td> 
   <td> <p> Select whether the result should be returned in ascending or descending order.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>Enable this option to ensure that this module does not stop the scenario if it returns no results.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List a folder's content]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>Select whether you want to retrieve files, folders, or both.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Enter or map the folder that contains the files or folders you want to list. You can specify an absolute path such as <code>/home/user/</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Enter or map the search term. For example, if you want to search for files with the file extension .txt, enter <code>.txt</code>.You can also enter or map the name of the file you want to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> Select whether you want to sort results by file name, size, last access date, or last modified date.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order] </td> 
   <td> <p>Select whether the result should be returned in ascending or descending order.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>Enable this option to ensure that this module does not stop the scenario if it returns no results.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Enter the path to the file you want to move. You can specify an absolute path such as <code>/home/user/file.txt</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New Folder]</td> 
   <td> <p> Enter the path to the file's new location. You can specify an absolute path such as <code>/home/user/</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rename a File]

Renames a file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Enter the path to the file you want to rename. You can specify an absolute path such as <code>/home/user/file.txt</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New file name]</td> 
   <td> <p> Enter the new name for the file, including the file extension.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update file permissions]

Allows you to change permissions of the file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Enter the path to the file you want to move. You can specify an absolute path such as <code>/home/user/file.txt</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Set the desired file permissions. Use chmod parameters. For example, <code>777</code> or <code>-rwxrwxrwx</code>.</p> <p>These permissions must match the pattern <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>For more information about chmod, see the <a href="https://ss64.com/bash/chmod.html">chmod documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

This module allows you to upload a file to the SFTP server.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your SFTP account to [!DNL Workfront Fusion], see <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connect SFTP to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Specify an existing folder as the storage location for the file. You can specify an absolute path such as <code>/home/user/</code>. Or you can specify a relative path pointing to a specific folder of the logged in user, such as <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td> <p> Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Set the desired permissions for the file or folder. Use chmod parameters. For example, <code>777</code> or <code>-rwxrwxrwx</code>.</p> <p>These permissions must match the pattern <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>For more information about chmod, see the <a href="https://ss64.com/bash/chmod.html">chmod documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
