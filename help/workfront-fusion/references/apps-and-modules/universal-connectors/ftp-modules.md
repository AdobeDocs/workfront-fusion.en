---
title: FTP modules
description: FTP modules let you monitor file changes in a selected folder, upload new files to the desired folder, and modify or delete existing files that are already in a folder.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
---
# FTP modules

FTP modules let you monitor file changes in a selected folder, upload new files to the desired folder, and modify or delete existing files that are already in a folder.

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

In order to use FTP modules, you must have an account with an FTP service.

## Create a connection in an FTP module {#create-a-connection}

1. In any FTP module, click **Add** next to the connection box.
1. Fill in the following fields.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Connection name]</td> 
      <td> <p> Enter the name for your FTP connection.</p> </td> 
     </tr> 
     <tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td> <p>Select whther you are using a production or non-production environment.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Type]</p> </td> 
      <td> <p>Select whether you are using a service account or a personal account.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Host] </td> 
      <td> <p>Enter the FTP server hostname. Example: <code>myftp123.server.com</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Port] </td> 
      <td> <p>Enter the FTP server port number. Example: <code>21</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL User name] </td> 
      <td> <p>Enter your FTP account user name.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Password] </td> 
      <td> <p>Enter your FTP account password.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Use a secure connection (TLS)</p> </td> 
      <td> <p>Select whether you want to use a secure connection.</p> <ul><li><p><b>[!UICONTROL No]</b></p> <p>The connection is not secured.</p></li><li> <p><b>Explicit encryption</b> or <b>Implicit encryption</b></p> <p>The connection is secured using SSL.</p> </td> 
     </tr> 
    <tr> 
   <td> <p>[!UICONTROL Reject unauthorized certificates]</p> </td> 
   <td> <p>Enable this option to verify the FTP server certificate. If the verification fails, the connection will not be created. To pass the verification, the certificate must meet one of the following criteria:</p> 
    <ul> 
     <li>be signed by a Root Certificate Authority</a></li> 
     <li>be signed by an Intermediate Certificate Authority. In this case all the Intermediate Certificates should be installed on the FTP server.</li> 
     <li>be a Self-Signed Certificate supplied in the [!UICONTROL Self-signed certificate] field (see below)</li> </ul>
     <p>If this option is disabled, the FTP server certificate is not verified. We strongly advise against disabling the option as it renders the connection insecure and poses a serious security risk.</p></td>
    </tr> 
    <tr> 
     <td> <p>[!UICONTROL Self-signed certificate]</p> </td> 
     <td> <p>Click the <b>[!UICONTROL Extract]</b> button to open the upload dialog.</p> <p>Upload the certificate to use the TLS with your self-signed certificate. [!DNL Workfront Fusion] does not retain or store any data you provide, such as files and passwords. File and password are used only to extract the certificate.</p> </td> 
    </tr> 
   </tbody> 
   </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.

## FTP modules and their fields

* [Triggers](#triggers)
* [Actions](#actions)

### Triggers 

#### [!UICONTROL Watch files]

[!UICONTROL Watch files] is the only trigger module for FTP. It monitors the file content of the selected folder. The trigger is executed when a new file is added tp the specified folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on establishing a connection to the FTP account, see <a href="#create-a-connection" class="MCXref xref">[!UICONTROL Create a connection] in an FTP module</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Folder]</p> </td> 
   <td> <p>Select the folder you want to watch.</p> <p><b>Note:</b> Only one folder per scenario is allowed. Subfolders are ignored.</p> <p><b>Tip:</b> To watch multiple folders, create a separate scenario for each of them.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files] </td> 
   <td> <p>Set the maximum number of results that you want the module to work with during one cycle. If the value is set too high, the connection may be interrupted on the side of the FTP server. [!DNL Workfront Fusion] has no influence on this. We recommend that you set a lower value and either define a higher value for the maximum number of cycles or run the scenario more frequently.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Change permissions]](#change-permissions)
* [[!UICONTROL Create a folder]](#create-a-folder)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Delete a folder]](#delete-a-folder)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL List of files in a folder]](#list-of-files-in-a-folder)
* [[!UICONTROL Move a file or folder]](#move-a-file-or-folder)
* [[!UICONTROL Upload] a file](#upload-a-file)

#### [!UICONTROL Change permissions]

This action module changes permission settings of a file or folder.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>For instructions on establishing a connection to the FTP account, see <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in an FTP module</a> in this article.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Change permission settings of]</td>
            <td>
               <p>Select whether you want to change settings for a file or folder.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL File path]</td>
            <td>Enter or map the file path to the folder or file.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Permissions]</td>
            <td>
               <p>Set the desired file or folder permissions. Use the chmod parameters. For example: <code>777 </code>or <code>-rwxrwxrwx</code>.</p>
               <p>Permissions must match the pattern <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code>.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Create a folder]

This action module creates a new folder.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>For instructions on establishing a connection to the FTP account, see <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in an FTP module</a> in this article.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Folder path]</td>
            <td>Enter or map the file path to the new folder.</td>
         </tr>
         <tr>
            <td>[!UICONTROL New folder name]</td>
            <td>
               <p>Enter or map a name for the new folder.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Delete a file]

This action module deletes a file from the specified folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
            <td>For instructions on establishing a connection to the FTP account, see <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in an FTP module</a> in this article.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Select the FTP folder you want to delete a file from.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td> <p> Enter the filename, including file name extension. Example: <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

This action module permanently deletes the specified folder.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>For instructions on establishing a connection to the FTP account, see <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in an FTP module</a> in this article.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Folder]</td>
            <td>
               <p>Select the FTP folder you want to delete a file from.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Get a file]

This action module retrieves a file from the FTP server.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on establishing a connection to the FTP account, see <a href="#creating-the-ftp-connection" class="MCXref xref">Creating the FTP Connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File path]</td> 
   <td> <p> Enter the path of the file you want to get.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List of files in a folder] 

This action module retrieves file and/or folder information.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on establishing a connection to the FTP account, see <a href="#creating-the-ftp-connection" class="MCXref xref">Creating the FTP Connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Select the FTP folder you want to search in.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>Select whether you want to retrieve information about files or folders, or both.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Enter the search term. If no search term is entered, all files or folders from the specified folder will be retrieved.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p>Enter or map the maximum number of results that you want the module to work with during one cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a file or folder]

This action module moves a file or folder to a different location.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>For instructions on establishing a connection to the FTP account, see <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in an FTP module</a> in this article.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Old file path]</td>
            <td>
               <p>Enter the path that you want to move the file from. Example: <code>/folder1/document.txt</code>.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL New file path]</td>
            <td>
               <p>Enter the path that you want to move the file to. Example: <code>/folder2/document.txt</code>.</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL Upload a file]

Uploads a file to the FTP server.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>For instructions on establishing a connection to the FTP account, see <a href="#creating-the-ftp-connection" class="MCXref xref">Creating the FTP Connection</a> in this article.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Select the FTP folder you want to upload the file to.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file] </td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Append to an already existing file]</td> 
   <td> <p>If this option is enabled and the file already exists on the FTP server, the contents of the file are appended to the existing file. If this option is not enabled, the content of the file will be overwritten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create folders if don't exist] </td> 
   <td> <p>If this option is enabled and the folder you have entered to the Folder field does not exist on the FTP server, the module creates the folder</p> </td> 
  </tr> 
 </tbody> 
</table>

## Troubleshooting {#troubleshooting}

If you are experiencing issues with the FTP app either during the connection creation or during a module's operation, try to use one of the popular FTP clients, and try to perform the same action (for example, create a connection or list files in a folder). with the FTP client. If you are experiencing the same issues also with the FTP client, the reason might be a misconfiguration of the FTP server.
