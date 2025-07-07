---
title: Adobe Experience Manager Assets modules
description: With the Adobe Experience Manager Assets connector for Adobe Workfront Fusion, you can create, upload, and update assets, and copy or move folders and assets.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
---
# Adobe Experience Manager Assets modules

With the Adobe Experience Manager Assets connector for Adobe Workfront Fusion, you can create, upload, and update assets, and copy or move folders and assets.

For a video introduction to the Adobe Experience Manager Assets connector, see:

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

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
   <p>Legacy: Workfront Fusion for Automation and Integration </p>
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

* You must have an Adobe Experience Manager Assets account to use these modules.
* You must set up Server-to-server flow in the Adobe Developer console.

   For instructions on setting up Server-to-server flow in the Adobe Developer console, see [Generating Access Tokens for Server Side APIs](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow).
* Your Adobe Experience Manager technical account must have write permissions.

   For instructions on adding write permissions to your Adobe Experience Manager technical account, see [Service credentials](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) in the Adobe Experience Manager documentation.

## Adobe Experience Manager Assets API information

The Adobe Experience Manager Assets connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## Connect Adobe Experience Manager Assets to  Workfront Fusion {#connect-adobe-experience-manager-assets-to-workfront-fusion}

To create a connection for your Adobe Experience Manager Assets modules:

1. Click Add next to the Connection box.

2. Select the type of connection that you are creating:

   * **AEM Assets as a Cloud Service**

      This configuration requires information from the Adobe Admin Console.

   * **AEM Assets Basic (Adobe Managed Services)**

      This configuration requires a username and password.

3. Fill in the fields for the type of connection that you are creating.

   For AEM Assets as a Cloud Service, see [Configure the connection for AEM Assets as a Cloud Service](#configure-the-connection-for-aem-assets-as-a-cloud-service).

   For AEM Assets Basic (Adobe Managed Services), see [Configure the connection for AEM Assets Basic](#configure-the-connection-for-aemassets-basic-adobe-managed-services).

4. Click **Continue** to save the connection and return to the module.


### Configure the connection for AEM Assets as a Cloud Service

>[!NOTE]
>
>* The information for these fields is generated as part of setting up Server-to-server flow on the Adobe Developer Console. You can find these values in the service credentials JSON file generated as part of that setup.
>
>   For instructions on setting up Server-to-server flow on the Adobe Developer Console, see [Generating Access Tokens for Server Side APIs](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow).
>
>* Your Adobe Experience Manager technical account must have write permissions.
>
>   For instructions on adding write permissions to your Adobe Experience Manager technical account, see [Service credentials](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) in the Adobe Experience Manager documentation.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">Connection name</td>
                  <td>
                      <p>Enter a name for this connection.</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">Instance URL without a trailing slash</td>
                  <td>Enter the URL for your Adobe Experience Manager instance. Do not include a slash <code>/</code> at the end of the URL.</td>
              </tr>
              <tr>
                  <td role="rowheader">Account details fill options</td>
                  <td>Select whether you want to provide JSON describing your account details, or if you want to enter details manually.</td>
              </tr>
              <tr>
                  <td role="rowheader">Technical account details in JSON format</td>
                  <td>If providing JSON, enter or paste the JSON describing your account details.</td>
              </tr>
              <tr>
                  <td role="rowheader">Client ID</td>
                  <td>If entering details manually, enter the Client ID generated in the Server-to-server setup.</td>
              </tr>
              <tr>
                  <td role="rowheader">Client Secret</td>
                  <td>If entering details manually, enter the Client Secret generated in the Server-to-server setup.</td>
              </tr>
              <tr>
                  <td role="rowheader">Technical account ID</td>
                  <td>If entering details manually, enter the ID of the technical account. This is the "id" field in the client credentials JSON file.</td>
              </tr>
              <tr>
                  <td role="rowheader">Org ID</td>
                  <td class="">If entering details manually, enter the ID of your organization. This is the "org" field in the client credentials JSON file.</td>
              </tr>
              <tr>
                  <td role="rowheader">Meta Scopes</td>
                  <td>Enter the Meta Scopes generated in the Server-to-server setup.</td>
              </tr>
              <tr>
                  <td role="rowheader">Private key</td>
                  <td>Enter the Private Key generated win the Server-to-server setup. To extract the private key, click Extract, then enter the file to extract and the password for the file.</td>
              </tr>
              <tr>
                  <td role="rowheader">Authentication URL</td>
                  <td>Enter authentication URL for this account.</td>
              </tr>
          </tbody>
      </table>


### Configure the connection for AEM Assets Basic (Adobe Managed Services)

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">Connection name</td>
                <td>
                    <p>Enter a name for this connection.</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">Instance URL without a trailing slash</td>
                <td>Enter the URL for your Adobe Experience Manager instance. Do not include a slash <code>/</code> at the end of the URL.</td>
            </tr>
            <tr>
                <td role="rowheader">Username</td>
                <td>Enter the username for the AEM Assets account that this connection uses.</td>
            </tr>
            <tr>
                <td role="rowheader">Password</td>
                <td>Enter the password for the AEM Assets account that this connection uses.</td>
            </tr>
        </tbody>
    </table>


## Adobe Experience Manager Assets modules and their fields

When you configure Adobe Experience Manager Assets modules,  Workfront Fusion displays the fields listed below. Along with these, additional Adobe Experience Manager Assets fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Files operations](#files-operations)
* [Other](#other)
* [Assets (Author API)](#assets-author-api)
* [Events (Author API)](#events-author-api)
* [Metadata (Author API)](#metadata-author-api)
* [Import (Author API)](#import-author-api)
* [Relations (Author API)](#relations-author-api)
* [Folders (Folders API)](#folders-folders-api)

### Files operations

* [Complete upload](#complete-upload)
* [Get presigned storage](#get-presigned-storage)
* [Initiate upload](#initiate-upload)
* [Upload an asset](#upload-an-asset)

#### Complete upload

This action module completes an initiated upload, after all parts of the file are uploaded.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">File name</td> 
   <td> <p>Enter or map a name for the uploaded file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Upload token</td> 
   <td>Enter or map the upload token for the binary, as provided by the initiation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">MIME type</td> 
   <td>Enter or map the MIME type for the completed file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Complete URI</td> 
   <td>Enter or map the complete URI for the file.</td> 
  </tr> 
 </tbody> 
</table>


#### Get presigned storage

This action module creates a temporary presigned URL to securely upload or download files from AEM without requiring direct credentials.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lookup typee</td> 
   <td> <p>Select whether you want to look up the asset by its path or its ID.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset</td> 
   <td>Select the path to the asset.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UDID</td> 
   <td>Enter or map the UDID for the asset.</td> 
  </tr> 
 </tbody> 
</table>

#### Initiate upload

This action module initiates an upload.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destination</td> 
   <td> <p>Select the folder where you want to upload a file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">File name</td> 
   <td> <p>Enter or map a name for the uploaded file</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Max file size</td> 
   <td>Enter or map the size, in bytes, of the uploaded file.</td> 
  </tr> 
 </tbody> 
</table>


#### Upload an asset

This action module uploads an asset to your Adobe Experience Manager Assets account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destination</td> 
   <td> <p>Select the folder where you want to upload an asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td>Enter or map the source file's name and data.</td> 
  </tr> 
 </tbody> 
</table>

### Other


* [Copy a folder or asset](#copy-a-folder-or-asset)
* [Create a record](#create-a-record)
* [Delete a folder, asset, or rendition](#delete-a-folder-asset-or-rendition)
* [Get a folder listing](#get-a-folder-listing)
* [Make a custom API call](#make-a-custom-api-call)
* [Move a folder or asset](#move-a-folder-or-asset)
* [Update a record](#update-a-record)



#### Copy a folder or asset

This action module copies a folder or asset to another location in your Adobe Experience Manager Assets account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> <p>Select whether you want to copy a folder or an asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Folder / Asset</td> 
   <td>Select or map the folder or asset that you want to copy.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destination path</td> 
   <td>Select or map the path to the location for the new folder or asset.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name of copied folder / asset</td> 
   <td>Enter a name for the new folder or asset. The folder name that displays in Adobe Experience Manager Assets is the same as the original name. The name entered here appears in the URL of the new folder or asset.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Copy children</td> 
   <td>If copying a folder, enable this option to copy any subfolders or assets within the folder.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overwrite</td> 
   <td>Enable this option to overwrite any folder or asset in the destination location that has the same name as the folder or asset being copied.</td> 
  </tr> 
 </tbody> 
</table>



#### Create a record

This action module creates a folder or an asset comment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Object type</td> 
   <td> <p>Select whether you want to create a folder or a comment on an asset.</p> 
    <ul> 
     <li> <p>Folder</p> <p>Fill in the following fields:</p> 
      <ul> 
       <li> <p>Name</p> <p>Enter a name for the folder. This name will appear in the file path, so it must not include spaces or other characters. </p> </li> 
       <li> <p>Title</p> <p>Enter a title for the folder, which can be displayed instead of the name.</p> </li> 
      </ul> </li> 
     <li> <p>Asset comment</p> <p>Fill in the following fields:</p> 
      <ul> 
       <li> <p>Asset selection</p> <p>Select or map the ID of the asset you want to add a comment to.</p> </li> 
       <li> <p>Comment</p> <p>Enter the text of the comment.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Delete a folder, asset, or rendition

This action module deletes a folder, asset, or rendition.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> <p>Select whether you want to delete a folder, asset, or rendition.</p> 
    <ul> 
     <li> <p>Folder</p> <p>Select the folder to delete by selecting the folders in its path.</p> </li> 
     <li> <p>Asset</p> <p>Select the asset by selecting the folders in its path, then the asset you want to delete.</p> </li> 
     <li> <p>Rendition</p> <p>Select the rendition by selecting the folders in its path.</p> <p>Enter or map the name of the rendition.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Get a folder listing

This action module retrieves a representation of an existing folder and of its child entities (folders or assets).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Folder</td> 
   <td>Select or map the folder that you want to retrieve. To add subfolders to the path, click the plus icon and select the subfolder.</td> 
  </tr> 
 </tbody> 
</table>

#### Make a custom API call

This action module makes a custom API call to the Adobe Experience Manager Assets API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL</p> </td> 
   <td> <p>Enter a path relative to your Adobe Experience Manager base URL.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Method</p> </td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Headers</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion adds authorization headers automatically.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Query String</td> 
   <td> <p>Enter the request query string. For Each Key/Value pair, click <b>Add item</b> and enter the Key and Value.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Body</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Move a folder or asset

This action module moves the asset or folder at the given path to a new location.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> <p>Select whether you want to move a folder or an asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Folder / Asset</td> 
   <td>Select or map the folder or asset that you want to move.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destination path</td> 
   <td>Select or map the path to the location that you want to move the folder or asset to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name of moved folder / asset</td> 
   <td>Enter a new name for the moved folder or asset. The folder name that displays in Adobe Experience Manager Assets is the same as the original name. The name entered here appears in the URL of the moved folder or asset.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overwrite</td> 
   <td>Enable this option to overwrite any folder or asset in the destination location that has the same name as the folder or asset being moved.</td> 
  </tr> 
 </tbody> 
</table>

#### Update a record

This action module updates an existing record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> <p>Select whether you want to delete asset metadata or an asset rendition.</p> 
    <ul> 
     <li> <p>Asset metadata</p> 
      <ul> 
       <li> <p>Select the asset that you want to update metadata for.</p> </li> 
       <li> <p>Enter the new title of the asset.</p> </li> 
      </ul> </li> 
     <li> <p>Asset rendition</p> 
      <ul> 
       <li> <p>Select the asset that you want to update the rendition for.</p> </li> 
       <li> <p>Select a source file from a previous module, or map the source file's name and data.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Assets (Author API)

* [Delete asset](#delete-asset)
* [Get job status](#get-job-status)

#### Delete asset

This action module deletes a single asset by its ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset ID</td> 
   <td> <p>Enter or map the ID of the asset that you want to delete.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Force</td> 
   <td>Enable this option to force the asset to delete, even if it is referenced.</td> 
  </tr> 
 </tbody> 
</table>

#### Get job status

This action module gets the current status of an async job.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Job ID</td> 
   <td> <p>Enter or map the ID of the job that you want to get the status for.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Events (Author API)

#### Watch events

This trigger module starts a scenario when an event occurs in AEM Assets.

The module contains a single field: Webhook. Select an existing webhook to use for these events, or create a new one.

To create a new webhook:

1. Click **Add** next to the Webhook field.
1. Fill in the following fields:

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">Webhook name</td>
        <td>Enter a name for this webhook.</td>
       </tr>
       <tr>
         <td role="rowheader">Connection</td>
        <td>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</td>
       </tr>
     </tbody>
   </table>

1. Click Save to save the webhook and return to the module.


### Metadata (Author API)

* [Get asset metadata](#get-asset-metadata)
* [Update asset metadata](#update-asset-metadata)

#### Get asset metadata

This action module retrieves metadata about the specified asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset ID</td> 
   <td> <p>Enter or map the ID of the asset that you want to get the metadata for.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Update asset metadata

This action module updates metadata for the specified asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset ID</td> 
   <td> <p>Enter or map the ID of the asset that you want to update the metadata for.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Updates</td> 
   <td> <p>For each metadata item that you want to update, click <b>Add item</b> and select the operation. Other fields in the Add item box depend on the operation selected.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Import (Author API)

* [Get import job results](#get-import-job-results)
* [Get import job status](#get-import-job-status)
* [Upload an asset from a URL](#upload-an-asset-from-a-url)

#### Get import job results

This action module retrieves results for the specified import job.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Import job ID</td> 
   <td> <p>Enter or map the ID of the job that you want to retrieve results for.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Get import job status

This action module retrieves the status of the specified import job.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Import job ID</td> 
   <td> <p>Enter or map the ID of the job that you want to retrieve the status of.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Upload an asset from a URL

This action module uploads a new asset by importing files from the specified URLs.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Title</td> 
   <td> <p>Enter or map a title for the asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Description</td> 
   <td> <p>Enter or map a description for the asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Subject</td> 
   <td> <p>Enter or map a subject for the asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Creator</td> 
   <td> <p>Enter or map the creator of the asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Expiration date</td> 
   <td> <p>Enter or map the experation date for the asset.</p><p>For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Custom metadata</td> 
   <td> <p>For each item of custom metadata that you want to add to the asset, click <b>Add item</b> and enter the metadata's name and value.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Folder path or ID</td> 
   <td> <p>Select whether you want to specify the destination folder by its path or ID, then select the path or enter the ID.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Files to import</td> 
   <td> <p>For each file that you want to import, click <b>Add item</> and fill in the details for the file. <code>Title</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"></td> 
   <td> <p></p> </td> 
  </tr> 
 </tbody> 
</table>

### Relations (Author API)

* [Create asset relations](#create-asset-relations)
* [Delete asset relation](#create-asset-relations)
* [Get asset relation types](#get-asset-relation-types)
* [Get asset relations](#get-asset-relations)

#### Create asset relations

This action module creates new asset relations for the selected asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset ID</td> 
   <td> <p>Enter or map the ID asset that you want to relate other assets to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Related assets</td> 
   <td> <p>For each asset that you want to relate to the selected asset, click <b>Add item</b> and enter or map the asset's ID and the relation type.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Delete asset relation

This action module delete an asset relation for an asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset ID</td> 
   <td> <p>Enter or map the ID asset that you want to delete a relation from.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Related assets</td> 
   <td> <p>Enter or map the type of relation that you want to delete.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Provide specific ID of the related asset to be deleted</td> 
   <td> <p>Check this box if you want to delete one specific relation. If this box is not checked, all relations of the selected type are deleted.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Related asset ID</td> 
   <td> <p>If you are deleting a specific relation, enter or map the ID of relation that you want to delete.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### Get asset relation types

This module lists the asset relation types that exist for the specified asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset ID</td> 
   <td> <p>Enter or map the ID asset that you want to list relation types for.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Get asset relations

This module lists the asset relations for the specified asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset ID</td> 
   <td> <p>Enter or map the ID asset that you want to list relations for.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Relation types</td> 
   <td> <p>Enter or map a comma-separaated list of the relation types that you want to list the relations for.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Folders (Folders API)

* [Create folders](#create-folders)
* [Delete a folder by ID](#delete-a-folder-by-id)
* [Delete folders by path](#delete-folders-by-path)
* [Get folders job results](#get-folders-job-results)
* [Get folders job status](#get-folders-job-status)
* [List folders](#list-folders)

#### Create folders

This action module creates a new folder in Adobe Experience Manager Assets.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Folders to create</td> 
   <td> <p>For each folder that you want to create, click <b>Add item</b> and enter the following information:</p>
   <ul>
   <li><b>New folder location</b><p>Select the path to the location where you want to create the new folder.</p></li>
       <li> <b>Name</b> <p>Enter a name for the folder. This name will appear in the file path, so it must not include spaces or other characters. </p> </li> 
       <li> <b>Title</b> <p>Enter a title for the folder, which can be displayed instead of the name.</p> </li> 
   </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Delete a folder by ID

This action module deletes the Adobe Experience Manager Assets folder with the specified ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Folder ID</td> 
   <td> Enter or map the ID of the folder that you want to delete.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Delete subfolders</td> 
   <td> Enable this option to delete the folder and all of its subfolders.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Force</td> 
   <td> Enable this option to force the folders to delete, even if it is referenced.</td>
  </tr> 
 </tbody> 
</table>

#### Delete folders by path

This action module deletes the Adobe Experience Manager Assets folders at the specified paths.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Folder Paths</td> 
   <td>For each folder that you want to delete, click <b>Add item</b> and select the folder's path.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Delete subfolders</td> 
   <td> Enable this option to delete the folder and all of its subfolders.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Force</td> 
   <td> Enable this option to force the asset to delete, even if it is referenced.</td>
  </tr> 
 </tbody> 
</table>

#### Get folders job results

This module retrieves the results of an async job created by the Adobe Experience Manager Assets folder API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Job ID</td> 
   <td> Enter or map the ID of the job that you want to retrieve results for.</td>
  </tr> 
 </tbody> 
</table>

#### Get folders job status

This module retrieves the status of an async job created by the Adobe Experience Manager Assets folder API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Job ID</td> 
   <td> Enter or map the ID of the job that you want to retrieve the status for.</td>
  </tr> 
 </tbody> 
</table>


#### List folders

This module lists subfolders of the specified folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Adobe Experience Manager Assets account to  Workfront Fusion, see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager Assets to  Workfront Fusion</a> in this article.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Folder path or ID</td> 
   <td> <p>Select whether you want to specify the destination folder by its path or ID, then select the path or enter the ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
i! I added a lot of modules to the AEM Assets connector and we need new documentation for them. The connector is available in the QA environment. Heres the added modules and a brief description of them, more info about them can be found in the Assets Author Api docs and the Folders Api docs. Im not fully confident that i kept all the best practices for naming things :sweat_smile:, i hope you can take a look at that as well. Let me know if theres anything i can tell about the modules and thanks again in advance!
Author API
Assets
Delete Asset
Deletes an asset when provided an Asset ID, There is a force parameter that when toggled will delete the folder regardless if it's referenced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get assets job status
Given an assets job ID will return the state that the job is currently in (PROCESSING, COMPLETED, etc.)
Events
AEM Assets events
The costumer can create a web hook in this module and register it in the Adobe admin console
Metadata
Get asset metadata
Given asset ID returns assets metadata.
Update asset metadata
Given asset ID, there are 6 patch operations that can be done with the metadata. The operations are visible in the module as well as the documentation.
Import
Get import job results
Given Job ID returns it's result.
Get import job status
Given Job ID returns its status.
Upload an asset from url
Takes global metadata which applies to all the assets and local ones which apply individually.In both it is also possible to specify custom metadata.
Also takes the folder path or folder ID to place the assets there and url-s of the assets.
Relations
Create asset relation
Given asset ID and a list of related asset ID as well as the relation types creates those relationships.
Delete asset relations
Given asset ID and relation type deletes all relations of that type. Can also specify a related asset to target only that.
 there is a checkbox that is checked by default and when unchecked reveals a field where the user can specify the related user ID.
Get asset relation types
Given asset ID returns all the relation types that the asset has.
Get asset relations
Given asset ID returns all relations. Can also specify a specific type of relation.
Folders API
Create folders
Given a list of folders with their path, name, title, creates them.
Delete a folder by ID
Given Folder ID deletes the folder. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Delete folders by path
Given a list of paths, deletes everything in them. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get folders job results
Given job ID returns its result.
Get folders job status
Given job ID returns its status.
List Folders
List folders under the given folder. In the module you can choose the root folder either by ID or by Path.
-->

