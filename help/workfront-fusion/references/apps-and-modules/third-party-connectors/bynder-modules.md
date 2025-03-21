---
title: Bynder modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Bynder], as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 0a45f8a7-12cc-41cc-9135-92f4779afac0
---
# [!DNL Bynder] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Bynder], as well as connect it to multiple third-party applications and services.

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

To use [!DNL Bynder] modules, you must have a [!DNL Bynder] account.

## Bynder API information

The Bynder connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API version</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.25.21</td> 
  </tr>
 </tbody> 
 </table>

## Connect [!DNL Bynder] to Workfront Fusion  {#connect-bynder-to-workfront-fusion}

>[!NOTE]
>
>Bynder uses the Authorization code / refresh token grant type. This is the only grant type that the Fusion Bynder connector uses.

* [Create a connection to [!DNL Bynder] from [!DNL Workfront Fusion]](#create-a-connection-to-bynder-from-workfront-fusion)
* [Generate a [!UICONTROL Client ID] and [!UICONTROL Client Secret] in [!DNL Bynder] (Optional)](#generate-a-client-id-and-client-secret-in-bynder-optional)

### Create a connection to [!DNL Bynder] from [!DNL Workfront Fusion]

You can create a connection from [!DNL Workfront Fusion] to your [!DNL Bynder] account directly from inside a [!DNL Bynder] module.

1. In any [!DNL Bynder] module, click **[!UICONTROL Add]** next to the [!UICONTROL Connection] field.
1. Select the [!DNL Bynder] domain that you want to connect to.
1. (Optional) Click **[!UICONTROL Advanced settings]**, then enter your [!UICONTROL Client ID] and [!UICONTROL Client Secret].

   For instructions on generating the Client ID and Client Secret, see [Generate a Client ID and Client Secret in [!DNL Bynder] (Optional)](#generate-a-client-id-and-client-secret-in-bynder-optional) in this article.

1. In the [!UICONTROL login] window, enter your username (email address) and password.
1. Click **[!UICONTROL Continue]** to create the connection and go back to the module.

### Generate a [!UICONTROL Client ID] and [!UICONTROL Client Secret] in [!DNL Bynder] (Optional) 

If you want to create a connection using the Client ID and Client Secret, you can generate them from your [!DNL Bynder] account. The Client ID and Client Secret are generated when you create an app in [!DNL Bynder].

For instructions for creating an app in [!DNL Bynder], see [Oauth 2.0 Apps](https://developer-docs.bynder.com/api/authentication-oauth2-oauth-apps/) in the [!DNL Bynder] documentation.

>[!NOTE]
>
>* When creating the app in [!DNL Bynder], enter the following as the `redirect uri`:
>
>   * US cluster: `https://app.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * EU cluster: `https://app-eu.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * Azure cluster: `https://app-az.workfrontfusion.com/oauth/cb/workfront-bynder`
>* Bynder uses the Authorization code / refresh token grant type. This is the only grant type that the Fusion Bynder connector uses.

## [!DNL Bynder] modules and their fields

When you configure [!DNL Bynder] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Bynder] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Searches](#searches)
* [Triggers](#triggers)

### Actions

* [[!UICONTROL Add a tag to assets]](#add-a-tag-to-assets)
* [[!UICONTROL Add assets to a collection]](#add-assets-to-a-collection)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download asset]](#download-asset)
* [[!UICONTROL Read asset metadata]](#read-asset-metadata)
* [[!UICONTROL Remove a tag] from assets](#remove-a-tag-from-assets)
* [[!UICONTROL Remove assets from collection]](#remove-assets-from-collection)
* [[!UICONTROL Update asset metadata]](#update-asset-metadata)
* [[!UICONTROL Upload asset]](#upload-asset)

#### [!UICONTROL Add a tag to assets] 

This action module adds a tag to one or more assets

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>Enter or map the ID of the tag that you want to add to assets.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>For each asset you want to tag, click <strong>[!UICONTROL Add item]</strong>, then enter or map the asset ID.</p> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL Add assets to a collection] 

This action module adds one or more assets to a collection.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Enter or map the ID of the collection where you want to add assets.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>For each asset you want to add to the collection, click <strong>[!UICONTROL Add item]</strong>, then enter or map the asset ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call] 

This action module lets you make a custom authenticated call to the [!DNL Bynder] API. This way, you can create a data flow automation that can't be accomplished by the other [!DNL Bynder] modules.

When you are configuring this module, the following fields display.

The module returns a status code, along with the headers and body of the API call.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Enter a path relative to <code>https://{your-bynder-domain}/api/{api-version}/</code>.</td> 
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

#### [!UICONTROL Download asset]

This action module downloads a single asset.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Enter or map the ID of the asset you want to download.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset version]</td> 
   <td> <p>Enter or map the version of the asset that you want to download. To download the latest version of the asset, leave the field empty.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read asset metadata]

This action module reads the metadata of an asset.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Enter or map the ID of the asset that you want to retrieve metadata for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a tag from assets]

This action module removes a tag from one or more assets

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>Enter or map the ID of the tag that you want to remove from assets.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>For each asset you want to remove a tag from, click <strong>[!UICONTROL Add item]</strong>, then enter or map the asset ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assets from collection] 

This action module removes one or more assets from a collection.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Enter or map the ID of the collection where you want to remove assets.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>For each asset you want to remove from the collection, click <strong>[!UICONTROL Add item]</strong>, then enter or map the asset ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update asset metadata]

This action module updates the metadata of an existing asset.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Enter or map the ID of the asset that you want to update metadata for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Select the fields that you want to enter information for, then enter or map the information that you want to update the metadata with into those fields. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metaproperties]</p> </td> 
   <td>Select the options that you want to update, then enter or map the information into those properties. Metaproperties are information about the asset that do not represent specific fields in the asset.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload asset]

This action module uploads a single asset.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save as]</td> 
   <td> <p>Select how you want to save the file you are uploading.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL New asset]</strong> </p> <p>Select the fields and metaproperties that you want to enter information for, then enter the information into those fields.</p> <p>Enter or map the ID of the Brand you want to use for the uploaded asset.</p> </li> 
     <li> <p><strong>[!UICONTROL New asset version]</strong> </p> <p>Enter the ID of the asset that you are uploading a new version for.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asynchronous file upload]</td> 
   <td>Enable this option when uploading large files. This prevents large files from blocking scenario execution.</td> 
  </tr> 
 </tbody> 
</table>

### Searches 

* [[!UICONTROL List record]](#list-record)
* [[!UICONTROL Search Assets]](#search-assets)

#### [!UICONTROL List record] 

This search module retrieves all items of a specific type.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of record you want to list.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Read all collections]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read information about all tags]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read all assets of a collection]</strong> </p> <p>Enter or map the ID of the collection that you want to list assets of.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the module's output.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of assets you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Assets]

This search module searches for assets base on criteria you supply.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td> <p>Enter the search criteria. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Field]</strong> </p> <p>Select the field that you want to use in your search</p> </li> 
     <li> <p><strong>[!UICONTROL Logical Operator]</strong> </p> <p>Select the operator that you want to use in your search.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter or map the value to look for in the selected field. The value type should be the same as the data type of the selected field. </p> <p>For more information on data types, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Item data types</a>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Select whether you want to return the first matching asset or all matching assets.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Select the field that you want to sort by.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort Direction]</td> 
   <td> <p>Select whether you want to sort ascending or descending.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the module's output.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of assets you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Triggers 

#### [!UICONTROL Watch assets]

This trigger module starts a scenario when an asset is created or updated.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>For instructions about connecting your [!DNL Bynder] account to [!DNL Workfront Fusion], see <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connect [!DNL Bynder] to [!DNL Workfront Fusion] </a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">Event type</td>
    <td>Select whether you want to start the scenario when a new asset is created or when an existing asset is updated.</td>
  </tr> 
  <tr>
     <td role="rowheader">[!UICONTROL Collections]</td>
   <td> <p>Select the collection that you want to watch for new assets. To watch all collections, leave this field empty.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">Outputs</td>
    <td>Select the fields that you want to include in the output.</td>
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Limit]</td>

<td> <p>Enter the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>
