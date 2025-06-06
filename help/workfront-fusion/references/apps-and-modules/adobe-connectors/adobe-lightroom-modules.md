---
title: Adobe Lightroom modules
description: With the Adobe Lightroom modules, you can start an Adobe Workfront Fusion scenario based on events in your Adobe Lightroom account.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
---
# [!DNL Adobe Lightroom] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Adobe Lightroom], as well as connect it to multiple third-party applications and services. 

If you need instructions on creating a scenario, see the articles under [Create a scenario: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Before you can use the [!DNL Adobe Lightroom] connector, you must ensure that the following prerequisites are met:

* You must have an active [!DNL Adobe Lightroom] account.
* You must have an OAuth Web App configured in the Adobe Admin Console. For details see [Configure an OAuth application in the Adobe Admin Console](#configure-an-oauth-application-in-the-adobe-admin-console) in this article.

## Adobe Lightroom API information

The Adobe Lightroom connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td>https://lr.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.17.128</td> 
  </tr>
 </tbody> 
 </table>



## Create a connection to Adobe Lightroom

To connect to Adobe Lightroom, you must first configure an OAuth app in the Adobe Admin Console. After this app is configured, you can create connections from Workfront Fusion.

### Configure an OAuth application in the Adobe Admin Console

1. Begin configuring an OAuth Web App in the Adobe Admin Console.

   For instrtuctions, see [User Authentication Implementation Guide](https://developer.adobe.com/developer-console/docs/guides/authentication/UserAuthentication/implementation) in the Adobe developer documentation.
1. When configuring the OAuth Web App, enter the following values:

    <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>
          <ul>
            <li>AdobeID</li>
            <li>lr_partner_rendition_apis</li>
            <li>openid</li>
            <li>offline_access</li>
            <li>lr_partner_apis</li>
          </ul>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Redirect URI]</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Redirect URI pattern]</td>
        <td><code>https://app\.workfrontfusion\.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
      </tbody>
    </table>

### Create a connection to Adobe Lightroom from Workfront Fusion

To create a connection for your [!DNL Adobe Lightroom] modules:

1. In any Adobe Lightroom module, click **[!UICONTROL Add]** next to the Connection box.
    
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
        <td>Select whether you are connecting to a service account or a personal account.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Enter your [!UICONTROL Adobe] [!UICONTROL Client ID]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Enter your [!DNL Adobe] [!UICONTROL Client Secret]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console]</td>
        </tr>
      </tbody>
    </table>
    
1. Click **[!UICONTROL Continue]** to save the connection and return to the module.
    

## Adobe Lightroom modules and their fields

When you configure [!DNL Adobe Lightroom] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Adobe Lightroom] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Other](#other)
* [Assets](#assets)
* [Albums](#albums)

### Other

* [Health check](#health-check)
* [Retrieve user catalog metadata](#retrieve-user-catalog-metadata)

#### Health check

This action module retrieves a Lightroom server version ID, proving whether the Lightroom service is currently running.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>If you want to supply specific credentials to ensure that a specific server is running, click <b>Add item</b> and enter the credentials.</p><p>Authorization headers are added automatically.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Retrieve user catalog metadata

This action module retrieves metadata from a catalog in Adobe Lightroom. A catalog contains assets, albums, or other resources.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>If you want to supply specific credentials to ensure that you can access the correct user account, click Add item and enter the credentials.</p><p>Authorization headers are added automatically.</p>
      </td>
    </tr>
  </tbody>
</table>

### Assets

* [Create an asset original file](#create-an-asset-original-file)
* [Create an asset](#create-an-asset)
* [Create an asset external XMP develop setting file](#create-an-asset-external-xmp-develop-setting-file)
* [Generate renditions for an original file](#generate-renditions-for-an-original-file)
* [Get a catalog asset](#get-a-catalog-asset)
* [Get the latest asset external XMP develop setting](#get-the-latest-asset-external-xmp-develop-setting-file)
* [Get the latest asset rendition](#get-the-latest-asset-rendition)
* [Retrieve assets](#retrieve-assets)

#### Create an asset original file

This action module creates and uploads an original file for an asset.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains the asset.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Enter or map the ID of the asset that you want to create and upload a file for.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Enter or map the length of the content in bytes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Byte range]</td>
      <td>
        <p>Enter or map the byte range for the request, including first and last bytes and entity length as defined in RFC 2616. This information should be included only when the data is too large to be uploaded in a single call.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content type]</td>
      <td>
        <p>Select the content type for the new file.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Create an asset

This action module creates a new asset with initial metadata and import information.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog where the asset will be created.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Enter or map the ID of the new asset.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset type]</td>
      <td>
        <p>Select whether the asset is an image or a video.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user created]</td>
      <td>
        <p>Enter or map a date with the format <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user updated]</td>
      <td>
        <p>Enter or map a date with the format <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Date captured]</td>
      <td>
        <p>Enter or map the capture date of the asset with the format <code>YYYY-MM-DDT00:00:00-00:00</code>. This will be set by the server if the Date captured is set to <code>0000-00-00T00:00:00</code>. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File name]</td>
      <td>
        <p>Enter or map the file name of the asset that you are importing into Lightroom.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name of Device Imported On]</td>
      <td>
        <p>Enter or map the name of the device that imports the asset.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Account ID of User Who Imported]</td>
      <td>
        <p>Enter or map the ID of the user that imports the asset.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Import Timestamp]</td>
      <td>
        <p>Enter or map a date with the format <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Create an asset external XMP develop setting file

This action module supports two workflows: uploading the external XMP develop settings file for the asset, or creating an external XMP develop settings file by copying from another asset's external xmp develop setting file. 

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content Length in Bytes]</td>
      <td>
        <p>Enter or map the length of the content in bytes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Upload new or copy XMP/develop file]</td>
      <td>
        <p>Select whether you are uploading a new file, or copying a file from an existing asset.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog where you want to create the asset.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Enter or map the ID of the asset that you want to upload or copy a file to.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Link to XMP/develop file]</td>
      <td>
        <p>Enter or map a link to the file you want to upload or copy.</p><p>This file must be JSON if copying a file, or XML if uploading a file.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Generate renditions for an original file

This action module asynchronously generate renditions for an original file.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rendition Type(s) (semi-colon separated)]</td>
      <td>
        <p>Enter the rendition type for the rendition you want to create. If entering more than one type, separate them with a semicolon (;). <p>Possible types:</p><ul><li><code>fullsize</code></li><li><code>2560</code></li></ul></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Enter or map the length of the content in bytes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog where you want to generate the renditions.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Enter or map the ID of the asset that you want to create a rendition of a file for.</p>
      </td>
    </tr>
  </tbody>
</table> 

#### Get a catalog asset

This action module retrieves information about a single asset in a catalog. The catalog must be owned by the user whose credentials are represented in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains the asset.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Enter or map the ID of the asset that you want to retrieve information for.</p>
      </td>
    </tr>
  </tbody>
</table> 


#### Get the latest asset external XMP develop setting file

This action module retrieves the most recent asset external XMP setting file.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains the asset associated with the XMP develop setting file.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Enter or map the ID of the asset associated with the XMP develop setting file.</p>
      </td>
    </tr>
  </tbody>
</table> 

#### Get latest asset rendition

This action module retrieves the latest asset rendition of the specified type.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains the asset that you want to retrieve a rendition for.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Enter or map the ID of the asset that you want to retrieve a rendition for.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rendition type]</td>
      <td>
        <p>Select the type of rendition that you want to retrieve.</p>
      </td>
    </tr>
  </tbody>
</table> 

#### Retrieve assets

This action module retrieves assets owned by the by the user whose credentials are represented in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains the asset.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starting timestamp]</td>
      <td>
        <p>Enter or map a timestamp. The module returns records that have been updated after this time stamp.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Return assets captured before given time]</td>
      <td>
        <p>Enter a date with the format <code>YYYY-MM-DDT00:00:00</code>. The module returns results captured before this date.</p><p> This field cannot be used with the field <code>Return assets captured after given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Return assets captured after given time]</td>
      <td>
        <p>Enter a date with the format <code>YYYY-MM-DDT00:00:00</code>. The module returns results captured before this date.</p><p> This field cannot be used with the field <code>Return assets captured before given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned assets]</td>
      <td>
        <p>Enter the maximum number of records you want the module to return during each scenario execution cycle.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SHA256 Hash value of original file]</td>
      <td>
        <p>Enter or map the hash value of the original file. Assets with a matching hash are returned.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Hide assets that are inside stacks?"]</td>
      <td>
        <p>Select Yes to hide assets inside stacks (assets inside stacks are not returned). Select No to include assets inside stacks in results.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset subtype values]</td>
      <td>
        <p>Enter or map a semicolon-separated list of subtype values to return.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset IDs]</td>
      <td>
        <p>Enter or map up to 100 asset IDs, separated by commas.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Types of assets to exclude]</td>
      <td>
        <p>Select if you want to exclude complete or incomplete assets. To include all assets, leave this field blank.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Group values]</td>
      <td>
        <p>Enter or map a semicolon-separated list of group values.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name values]</td>
      <td>
        <p>Enter or map a semicolon-separated list of name values.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Favorite status]</td>
      <td>
        <p>Enter or map the favorite status that you want to return results for.</p>
      </td>
    </tr>
    </tr>
  </tbody>
</table> 

### Albums

* [Add assets to an album](#add-assets-to-an-album)
* [Create an album](#create-an-album)
* [Delete an album](#delete-an-album)
* [Get an album](#get-an-album)
* [List assets of an album](#list-assets-of-an-album)
* [Retrieve albums](#retrieve-albums)
* [Update an album](#update-album)

#### Add assets to an album

This action module adds one or more assets to the specified album. You can add up to 50 assets in one execution cycle.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains the album that you want to add assets to.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Enter or map the ID of the album that you want to add assets to.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Assets]</td>
      <td>
        <p>For each asset that you want to add to the album, click <b>Add item</b> and enter the following fields.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Enter or map the ID of the asset you want to add to the album</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Is this asset an album cover?]</td>
      <td>
        <p>Select whether you want this asset to be displayed as the image that represents the album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Order]</td>
      <td>
        <p>Specify the order of the asset.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Service Payload]</td>
      <td>
        <p>Enter or map any metadata you want to include with the asset. This must be a single text string with a maximum length of 1-24 characters.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Remote ID]</td>
      <td>
        <p>Enter an identifier for the asset.</p>
      </td>
    </tr>
  </tbody>
</table> 

#### Create an album

This action module creates a new album in Lightroom.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog where you want to create an album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Enter or map an ID for the new album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtype]</td>
      <td>
        <p>Select the subtype for the album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Service ID]</td>
      <td>
        <p>Enter the API key of the service that is creating the album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Date User Created]</td>
      <td>
        <p>Enter or map a date with the format <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Date User Updated]</td>
      <td>
        <p>Enter or map a date with the format <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album Name]</td>
      <td>
        <p>Enter or map a name for the new album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cover ID]</td>
      <td>
        <p>Enter or map the ID of an asset to use as the cover of this album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Parent ID]</td>
      <td>
        <p>Enter or map the ID of the parent for this album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Service Payload]</td>
      <td>
        <p>Enter or map album metadata as a string.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Remote ID]</td>
      <td>
        <p>Enter an identifier for the asset.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Created date]</td>
      <td>
        <p>Enter or map a date with the format <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Updated date]</td>
      <td>
        <p>Enter or map a date with the format <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Is the album deleted?]</td>
      <td>
        <p>Enable this option if the externally affiliated content was deleted.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL of location to edit affiliated content]</td>
      <td>
        <p>If there is a URL where users can edit content of this album, enter the URL here.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL of location to view affiliated content]</td>
      <td>
        <p>If there is a URL where users can view content of this album, enter the URL here.</p>
      </td>
    </tr>
  </tbody>
</table> 

#### Delete an album

This action module deletes an album.

The deleted album must have been created by the same client app that is now deleting it, and it must be of subtype `project` or `project_set`.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains album you want to delete.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Enter or map the ID of the album you want to delete.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Delete child albums?]</td>
      <td>
        <p>Select whether you want to delete child albums of the deleted album.</p>
      </td>
    </tr>
  </tbody>
</table> 

### Get an album

This action module retrieves the specified album.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains album you want to retrieve.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Enter or map the ID of the album you want to retrieve.</p>
      </td>
    </tr>
  </tbody>
</table> 

#### List assets of an album

This action module retrieves a list of assets in the specified album.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains the album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Enter or map the ID of the album for which you want to list assets.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Capture Assets Before Time]</td>
      <td>
        <p>Enter a date with the format <code>YYYY-MM-DDT00:00:00</code>. The module returns results captured before this date.</p><p> This field cannot be used with the field <code>Return assets captured after given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Capture Assets After Time]</td>
      <td>
        <p>Enter a date with the format <code>YYYY-MM-DDT00:00:00</code>. The module returns results captured before this date.</p><p> This field cannot be used with the field <code>Return assets captured before given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ending Asset Order Value]</td>
      <td>
        <p>Enter or map the order value of the ending asset.</p><p> This field can only be used with the field <code>Capture Assets After Time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starting Asset Order Value]</td>
      <td>
        <p>Enter or map the order value of the starting asset.</p><p> This field can only be used with the field <code>Capture Assets BEfore Time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Number of Assets to Return (1-500)]</td>
      <td>
        <p>Enter the maximum number of records you want the module to return during each scenario execution cycle. This number must be between 1-500.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Hide assets that are inside stacks?"]</td>
      <td>
        <p>Select Yes to hide assets inside stacks (assets inside stacks are not returned). Select No to include assets inside stacks in results.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtype Values (semi-colon separated)]</td>
      <td>
        <p>Enter or map a semicolon-separated list of subtype values to return.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Flag Values (semi-colon separated)]</td>
      <td>
        <p>Enter or map a semicolon-separated list of flag values to return.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Additional Data Fields to Include (semi-colon separated)]</td>
      <td>
        <p>If asset is included, all fields are included, otherwise, only id and self href link are returned.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Types of assets to exclude]</td>
      <td>
        <p>Select if you want to exclude complete or incomplete assets. To include all assets, leave this field blank.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset IDs]</td>
      <td>
        <p>Enter or map up to 100 asset IDs, separated by commas.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Filter out album assets based on presentation filters]</td>
      <td>
        <p>When this field is set to 'true', it filters out all the album assets based on the presentation filters set on the album. With this parameter, rejected assets always get filtered out irrespective of settings in presentation filters. Presentation filters are not applied when any value other than 'true' is set for album_filters. Default behavior is to display all assets. This parameter cannot be used along with flag parameter. </p>
      </td>
    </tr>
  </tbody>
</table> 

#### Retrieve albums

This action module retrieves a list of albums in the specified catalog.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains albums you want to retrieve.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtypes]</td>
      <td>
        <p>Enter or map a semicolon-separated list of subtype values to return.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name of album to precede current results]</td>
      <td>
        <p>If you are paginating your results, enter or map the name of the last album on the preceding page.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Number of Albums to Return]</td>
      <td>
        <p>Set the maximum number of assets that [!DNL Workfront Fusion] will return during one execution cycle. The default value for this field is 100.This module may return more albums than this limit if multiple albums at the limit boundary have the same <code>name_after</code> value.</p>
      </td>
    </tr>
  </tbody>
</table> 

#### Update album

This action module updates the specified album.

The updated album must have been created by the same client app that is now updating it, and it must be of subtype `project` or `project_set`.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Lightroom], see <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Create a connection to [!DNL Adobe Lightroom]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Enter or map the ID of the catalog that contains album you want to update.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Enter or map the ID of the album you want to update.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Other fields</td>
      <td>
      <td>For descriptions of other fields in this module, see <a href="#create-an-album" class="MCXref xref" >Create an album</a> in this article.</td>
      </td>
    </tr>
  </tbody>
</table>
