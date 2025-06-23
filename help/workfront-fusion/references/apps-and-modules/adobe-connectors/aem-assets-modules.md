---
title: Adobe Experience Manager Assets modules
description: With the [!DNL Adobe Experience Manager Assets] connector for [!DNL Adobe Workfront Fusion], you can create, upload, and update assets, and copy or move folders and assets.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
---
# [!DNL Adobe Experience Manager Assets] modules

With the [!DNL Adobe Experience Manager Assets] connector for [!DNL Adobe Workfront Fusion], you can create, upload, and update assets, and copy or move folders and assets.

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

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

* You must have an [!DNL Adobe Experience Manager Assets] account to use these modules.
* You must set up [!UICONTROL Server-to-server] flow in the [!DNL Adobe Developer console].

   For instructions on setting up [!UICONTROL Server-to-server] flow in the [!DNL Adobe Developer console], see [Generating Access Tokens for Server Side APIs](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow).
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

## Connect [!DNL Adobe Experience Manager Assets] to [!DNL Workfront Fusion] {#connect-adobe-experience-manager-assets-to-workfront-fusion}

To create a connection for your [!DNL Adobe Experience Manager Assets] modules:

1. Click [!UICONTROL Add] next to the [!UICONTROL Connection] box.

2. Select the type of connection that you are creating:

   * **[!DNL AEM Assets as a Cloud Service]**

      This configuration requires information from the [!DNL Adobe Admin Console].

   * **[!DNL AEM Assets Basic] ([!DNL Adobe Managed Services])**

      This configuration requires a username and password.

3. Fill in the fields for the type of connection that you are creating.

   For [!DNL AEM Assets as a Cloud Service], see [Configure the connection for [!DNL AEM Assets as a Cloud Service]](#configure-the-connection-for-aem-assets-as-a-cloud-service).

   For [!UICONTROL AEM Assets Basic] ([!DNL Adobe Managed Services]), see [Configure the connection for [!UICONTROL AEM Assets Basic]](#configure-the-connection-for-aemassets-basic-adobe-managed-services).

4. Click **[!UICONTROL Continue]** to save the connection and return to the module.


### Configure the connection for [!DNL AEM Assets as a Cloud Service]

>[!NOTE]
>
>* The information for these fields is generated as part of setting up [!UICONTROL Server-to-server] flow on the [!DNL Adobe Developer Console]. You can find these values in the service credentials JSON file generated as part of that setup.
>
>   For instructions on setting up [!UICONTROL Server-to-server] flow on the [!UICONTROL Adobe Developer Console], see [Generating Access Tokens for Server Side APIs](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow).
>
>* Your Adobe Experience Manager technical account must have write permissions.
>
>   For instructions on adding write permissions to your Adobe Experience Manager technical account, see [Service credentials](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) in the Adobe Experience Manager documentation.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">[!UICONTROL Connection name]</td>
                  <td>
                      <p>Enter a name for this connection.</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Instance URL without a trailing slash]</td>
                  <td>Enter the URL for your [!DNL Adobe Experience Manager] instance. Do not include a slash <code>/</code> at the end of the URL.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Account details fill options]</td>
                  <td>Select whether you want to provide JSON describing your account details, or if you want to enter details manually.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Technical account details in JSON format]</td>
                  <td>If providing JSON, enter or paste the JSON describing your account details.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Client ID]</td>
                  <td>If entering details manually, enter the Client ID generated in the [!UICONTROL Server-to-server] setup.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Client Secret]</td>
                  <td>If entering details manually, enter the Client Secret generated in the [!UICONTROL Server-to-server] setup.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Technical account ID]</td>
                  <td>If entering details manually, enter the ID of the technical account. This is the "[!UICONTROL id]" field in the client credentials JSON file.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Org ID]</td>
                  <td class="">If entering details manually, enter the ID of your organization. This is the "[!UICONTROL org]" field in the client credentials JSON file.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Meta Scopes]</td>
                  <td>Enter the Meta Scopes generated in the [!UICONTROL Server-to-server] setup.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Private key]</td>
                  <td>Enter the Private Key generated win the [!UICONTROL Server-to-server] setup. To extract the private key, click [!UICONTROL Extract], then enter the file to extract and the password for the file.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Authentication URL]</td>
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
                <td role="rowheader">[!UICONTROL Connection name]</td>
                <td>
                    <p>Enter a name for this connection.</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Instance URL without a trailing slash]</td>
                <td>Enter the URL for your [!DNL Adobe Experience Manager] instance. Do not include a slash <code>/</code> at the end of the URL.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Username]</td>
                <td>Enter the username for the [!DNL AEM Assets] account that this connection uses.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Password]</td>
                <td>Enter the password for the [!DNL AEM Assets] account that this connection uses.</td>
            </tr>
        </tbody>
    </table>


## [!DNL Adobe Experience Manager Assets] modules and their fields

When you configure [!DNL Adobe Experience Manager Essentials] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Adobe Experience Manager Essentials] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Files operations]()
* [Other]()
* [Assets (Author API)]()
* [Events (Author API)]()
* [Metadata (Author API)]()
* [Import (Author API)]()
* [Relations (Author API)]()
* [Folders (Folders API)]()

### Files operations



#### [!UICONTROL Upload an asset]

This action module uploads an asset to your [!DNL Adobe Experience Manager Assets] account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Adobe Experience Manager Assets] account to [!DNL Workfront Fusion], see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect [!DNL Adobe Experience Manager Assets] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination]</td> 
   <td> <p>Select the folder where you want to upload an asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Enter or map the source file's name and data.</td> 
  </tr> 
 </tbody> 
</table>

### Other





#### [!UICONTROL Copy a folder or asset]

This action module copies a folder or asset to another location in your Adobe Experience Manager Assets account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Adobe Experience Manager Assets] account to [!DNL Workfront Fusion], see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect [!DNL Adobe Experience Manager Assets] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Select whether you want to copy a folder or an asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Asset]</td> 
   <td>Select or map the folder or asset that you want to copy.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination path]</td> 
   <td>Select or map the path to the location for the new folder or asset.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of copied folder] / [!UICONTROL asset]</td> 
   <td>Enter a name for the new folder or asset. The folder name that displays in [!DNL Adobe Experience Manager Assets] is the same as the original name. The name entered here appears in the URL of the new folder or asset.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy children]</td> 
   <td>If copying a folder, enable this option to copy any subfolders or assets within the folder.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Enable this option to overwrite any folder or asset in the destination location that has the same name as the folder or asset being copied.</td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Create a record]

This action module creates a folder or an asset comment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Adobe Experience Manager Assets] account to [!DNL Workfront Fusion], see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect [!DNL Adobe Experience Manager Assets] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object type]</td> 
   <td> <p>Select whether you want to create a folder or a comment on an asset.</p> 
    <ul> 
     <li> <p>[!UICONTROL Folder]</p> <p>Fill in the following fields:</p> 
      <ul> 
       <li> <p>[!UICONTROL Name]</p> <p>Enter a name for the folder. This name will appear in the file path, so it must not include spaces or other characters. </p> </li> 
       <li> <p>[!UICONTROL Title]</p> <p>Enter a title for the folder, which can be displayed instead of the name.</p> </li> 
      </ul> </li> 
     <li> <p>[!UICONTROL Asset comment]</p> <p>Fill in the following fields:</p> 
      <ul> 
       <li> <p>[!UICONTROL Asset selection]</p> <p>Select or map the ID of the asset you want to add a comment to.</p> </li> 
       <li> <p>[!UICONTROL Comment]</p> <p>Enter the text of the comment.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder, asset, or rendition]

This action module deletes a folder, asset, or rendition.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Adobe Experience Manager Assets] account to [!DNL Workfront Fusion], see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect [!DNL Adobe Experience Manager Assets] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Select whether you want to delete a folder, asset, or rendition.</p> 
    <ul> 
     <li> <p>[!UICONTROL Folder]</p> <p>Select the folder to delete by selecting the folders in its path.</p> </li> 
     <li> <p>[!UICONTROL Asset] </p> <p>Select the asset by selecting the folders in its path, then the asset you want to delete.</p> </li> 
     <li> <p>[!UICONTROL Rendition]</p> <p>Select the rendition by selecting the folders in its path.</p> <p>Enter or map the name of the rendition.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a folder listing]

This action module retrieves a representation of an existing folder and of its child entities (folders or assets).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Adobe Experience Manager Assets] account to [!DNL Workfront Fusion], see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect [!DNL Adobe Experience Manager Assets] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Select or map the folder that you want to retrieve. To add subfolders to the path, click the plus icon and select the subfolder.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make a custom API call]

This action module makes a custom API call to the [!DNL Adobe Experience Manager Assets] API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Adobe Experience Manager Assets] account to [!DNL Workfront Fusion], see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect [!DNL Adobe Experience Manager Assets] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Enter a path relative to your [!DNL Adobe Experience Manager] base URL.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] adds authorization headers automatically.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Enter the request query string. For Each Key/Value pair, click <b>[!UICONTROL Add item]</b> and enter the [!UICONTROL Key] and [!UICONTROL Value].</p> </td> 
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

#### [!UICONTROL Move a folder or asset]

This action module moves the asset or folder at the given path to a new location.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Adobe Experience Manager Assets] account to [!DNL Workfront Fusion], see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect [!DNL Adobe Experience Manager Assets] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Select whether you want to move a folder or an asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Asset]</td> 
   <td>Select or map the folder or asset that you want to move.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination path]</td> 
   <td>Select or map the path to the location that you want to move the folder or asset to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of moved folder] / [!UICONTROL asset]</td> 
   <td>Enter a new name for the moved folder or asset. The folder name that displays in [!DNL Adobe Experience Manager Assets] is the same as the original name. The name entered here appears in the URL of the moved folder or asset.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Enable this option to overwrite any folder or asset in the destination location that has the same name as the folder or asset being moved.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

This action module updates an existing record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Adobe Experience Manager Assets] account to [!DNL Workfront Fusion], see <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connect [!DNL Adobe Experience Manager Assets] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Select whether you want to delete asset metadata or an asset rendition.</p> 
    <ul> 
     <li> <p>[!UICONTROL Asset metadata]</p> 
      <ul> 
       <li> <p>Select the asset that you want to update metadata for.</p> </li> 
       <li> <p>Enter the new title of the asset.</p> </li> 
      </ul> </li> 
     <li> <p>[!UICONTROL Asset rendition]</p> 
      <ul> 
       <li> <p>Select the asset that you want to update the rendition for.</p> </li> 
       <li> <p>Select a source file from a previous module, or map the source file's name and data.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Assets (Author API)



### Events (Author API)



### Metadata (Author API)



### Import (Author API)



### Relations (Author API)



### Folders (Folders API)






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

