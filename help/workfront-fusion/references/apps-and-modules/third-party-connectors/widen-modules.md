---
title: Widen modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!UICONTROL Widen], as well as connect it to multiple third-party applications and services.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 11376e58-a44b-4766-85dc-e2421b0112de
---
# [!DNL Widen] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!UICONTROL Widen], as well as connect it to multiple third-party applications and services.

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

To use [!UICONTROL Widen] modules, you must have a [!UICONTROL Widen] account.

## Widen API information

The Widen connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API version</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.10.11</td> 
  </tr>
 </tbody> 
 </table>

## Connect [!DNL Widen] to [!DNL Workfront Fusion]  {#connect-widen-to-workfront-fusion}

You can create a connection to your [!DNL Widen] account directly from inside a [!DNL Widen] module.

1. In any [!DNL Widen] module, click **[!UICONTROL Add]** next to the [!UICONTROL Connection] field.
1. Select the environment and type of account you are connecting to. This is for information only, and appears in the Connections area of Fusion.
1. Select the [!DNL Widen] domain that you want to connect to.
1. Enter the token for your [!DNL Widen] account. For instructions on locating this token, see the [[!DNL Widen] API FAQs](https://community.widen.com/collective/s/article/API-FAQs).
1. Click **[!UICONTROL Continue]** to create the connection and go back to the module.

## [!DNL Widen] modules and their fields

When you configure [!DNL Widen] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Widen] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger modules](#trigger-modules)
* [Action Modules](#action-modules)
* [Search Modules](#search-modules)

### Trigger modules

#### [!UICONTROL Watch assets]

This trigger module starts a scenario when an asset is created or updated.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>For instructions about connecting your [!DNL Widen] account to [!DNL Workfront Fusion], see <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connect [!DNL Widen] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p>Select whether you want to watch new assets or updated assets.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Select the properties that you want to include in the module output in addition to the asset fields.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Select the fields that you want to include in the module output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of assets you want the module to work with during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Action Modules

* [[!UICONTROL Add assets to collections]](#add-assets-to-collections)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download File]](#download-file)
* [[!UICONTROL Read asset info]](#read-asset-info)
* [[!UICONTROL Remove assets from collection]](#remove-assets-from-collection)
* [[!UICONTROL Update asset metadata]](#update-asset-metadata)
* [[!UICONTROL Upload a file]](#upload-a-file)

#### [!UICONTROL Add assets to collections]

This action module adds one or more assets to collections.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>For instructions about connecting your [!DNL Widen] account to [!DNL Workfront Fusion], see <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connect [!DNL Widen] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collections ID]</td> 
   <td>For each collection that you want to add the assets to, click <strong>[Collections ID]</strong> and enter or map the [!UICONTROL Collection ID].</li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> For each asset that you want to add to a collection, click <strong>[!UICONTROL Assets ID]</strong> and enter or map the Asset ID.</p> </li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of assets you want the module to work with during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

This action module lets you make a custom authenticated call to the [!DNL Widen] API. This way, you can create a data flow automation that can't be accomplished by the other [!DNL Widen] modules.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Widen] account to [!DNL Workfront Fusion], see <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connect [!DNL Widen] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Select whether you want to use the latest version of the [!DNL Widen] API, or Version 1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Enter or map the URL for your API call.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP request methods</a>.</p> </td> 
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
 </tbody> 
</table>

#### [!UICONTROL Download File]

This action module downloads an asset from your [!DNL Widen] account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>For instructions about connecting your [!DNL Widen] account to [!DNL Workfront Fusion], see <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connect [!DNL Widen] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Enter or map the ID of the asset you want to download.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read asset info]

This action module retrieves an individual asset by its unique ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>For instructions about connecting your [!DNL Widen] account to [!DNL Workfront Fusion], see <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connect [!DNL Widen] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Enter or map the ID of the asset you want to read information for.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Select the properties that you want to include in the module output in addition to the asset fields.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Select the fields that you want to include in the module output.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assets from collection]

This action module removes one or more assets from collections.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>For instructions about connecting your [!DNL Widen] account to [!DNL Workfront Fusion], see <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connect [!DNL Widen] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collections ID]</td> 
   <td>For each collection that you want to remove assets from, click <strong>[Collections ID]</strong> and enter or map the [!UICONTROL Collection ID].</li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> For each asset that you want to remove from a collection, click <strong>[!UICONTROL Assets ID]</strong> and enter or map the Asset ID.</p> </li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of assets you want the module to work with during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update asset metadata]

This action module updates the metadata fields of an asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>For instructions about connecting your [!DNL Widen] account to [!DNL Workfront Fusion], see <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connect [!DNL Widen] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Enter or map the ID of the asset where you want to update metadata.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata type]</td> 
   <td> <p>Select the metadata type for the metadata you want to update.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Select the metadata fields that you want to update. For each field, enter the new value for the field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of assets you want the module to work with during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

This action module uploads a file into your [!DNL Widen] account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>For instructions about connecting your [!DNL Widen] account to [!DNL Workfront Fusion], see <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connect [!DNL Widen] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Profile]</td> 
   <td> <p>Select the upload profile that you want the module to use.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Method]</td> 
   <td> <p>Select how you want to upload the file.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL From File]</strong> </p> <p>Select or map the source file from a previous module.</p> </li> 
     <li> <p><strong>[!UICONTROL By URL]</strong> </p> <p>Enter or map the URL of the file that you want to upload.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Enter or map a name for the uploaded file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata Type]</td> 
   <td>Select the metadata type for the file you want to upload.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Select the metadata fields that you want to include in the file upload. For each field, enter the [!UICONTROL value] for the field.</td> 
  </tr> 
 </tbody> 
</table>

### Search Modules

* [[!UICONTROL Read collection assets]](#read-collection-assets)
* [[!UICONTROL Search assets]](#search-assets)

#### [!UICONTROL Read collection assets]

This action module retrieves a list of assets within a collection.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>For instructions about connecting your [!DNL Widen] account to [!DNL Workfront Fusion], see <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connect [!DNL Widen] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Enter or map the ID of the collection that contains the assets you want to read.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td>Enter or map the number of the first item you want to list. This is a way to paginate the records.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort By]</td> 
   <td> <p>Select the property by which you want to sort the assets. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>Select whether you want to sort assets ascending or descending.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Select the fields that you want to include in the module output.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search assets]

This search module retrieves a list of assets that match the specific search criteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>For instructions about connecting your [!DNL Widen] account to [!DNL Workfront Fusion], see <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connect [!DNL Widen] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search query]</td> 
   <td> <p>Enter the criteria by which you want to search assets.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort By]</td> 
   <td> <p>Select how you want to sort the assets. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>Select whether you want to sort assets ascending or descending.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include deleted]</td> 
   <td>Enable this option to include deleted assets in the search.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Include archived]</p> </td> 
   <td> <p>Enable this option to include archived assets in the search.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search document text]</td> 
   <td>Enable this option to include document text in your search, or set to false to include only assets for which the title matches the search criteria.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Offset]</td> 
   <td>Enter or map the number of the first item you want to retrieve details for. This is a way to paginate the records.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scroll]</td> 
   <td>Enable this option to allow scrolling.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Select the properties that you want to include in the module output in addition to the asset fields.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Select the fields that you want to include in the module output.</td> 
  </tr> 
 </tbody> 
</table>
