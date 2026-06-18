---
title: Adobe Photoshop modules
description: With the Adobe Photoshop modules, you can start an Adobe Workfront Fusion scenario based on events in your Adobe Photoshop account, create, read, or update agreements and other records, search for records using criteria you set, and upload documents.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
TQID: https://experienceleague.adobe.com/RratZmko93V0LMxJ6qTy6cNvRqgPNvNgHTflRngE6BI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# [!DNL Adobe Photoshop] modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use [!DNL Adobe Photoshop], as well as connect it to multiple third-party applications and services. 

If you need instructions on creating a scenario, see the articles under [Create a scenario: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

>[!IMPORTANT]
>
>Adobe Photoshop has deprecated some elements of its API, which Fusion uses to perform actions in Photoshop. 
>
>**Therefore, some of the existing Photoshop modules will not work after July 30, 2026.**
>
>We recommend updating any scenarios that use these modules to the updated modules as soon as possible. 
>
>For a list of affected modules, see [Adobe Photoshop API deprecation updates](#adobe-photoshop-api-deprecation-updates).
>
>For an explanation of how API changes affect Workfront Fusion, see [Overview of APIs in Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md).

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any Adobe Workfront Workflow package and any Adobe Workfront Automation and Integration package</p><p>Workfront Ultimate</p><p>Workfront Prime and Select packages, with an additional purchase of Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront licenses</td> 
   <td> <p>Standard</p><p>Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license</td> 
   <td>
   <p>Operation-based: No Workfront Fusion license requirement</p>
   <p>Connector-based (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

Before you can use the [!DNL Adobe Photoshop] connector, you must ensure that the following prerequisites are met:

* You must have an active [!DNL Adobe Photoshop] account.
* You must have a Firefly Services license.
* You must have a Client ID and Client Secret. You can acquire these from the Adobe Developer Console.

## Adobe Photoshop API deprecation updates

Adobe Photoshop has deprecated some elements of its API, which Fusion uses to perform actions in Photoshop. 

**Therefore, some of the existing Photoshop modules will not work after July 30, 2026.**

This table documents which modules have been affected by this deprecation, and which module you should update to.

|Deprecated legacy module|Update to new module|
|---|---|
|Apply PSD edits|Create or edit a composite|
|Convert image format|Create or edit a composite|
|Create a composite|Create or edit a composite|
|Create a new PSD|Create or edit a composite|
|Create renditions|Create or edit a composite|
|Edit text layers|Execute Photoshop actions, scripts, and transformations|
|Edit text layers 2|Execute Photoshop actions, scripts, and transformations|
|Execute an action JSON|Execute Photoshop actions, scripts, and transformations|
|Execute depth blur|(Not available)|
|Execute Photoshop actions|Execute Photoshop actions, scripts, and transformations|
|Execute product crop|Execute Photoshop actions, scripts, and transformations|
|Get layer info|Generate a manifest|
|Resize an image|Create or edit a composite|
|Replace Smart Object|Create or edit a composite|
|Replace Smart Object 2|Create or edit a composite|
|Rotate an image|Execute Photoshop actions, scripts, and transformations|
|Watermark an image|Create or edit a composite|

## Adobe Photoshop API information

The Adobe Photoshop connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td>https://image.adobe.io/pie/psdService</td> 
  </tr>
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.12.31</td> 
  </tr>
 </tbody> 
 </table>

## Create a connection to [!DNL Adobe Photoshop]

To create a connection for your [!DNL Adobe Photoshop] modules:

1. In any module, click **[!UICONTROL Add]** next to the Connection box.
    
1. Fill in the following fields:
    
    <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Select whether you want to use a JWT connection or a server-to-server connection.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Enter a name for this connection.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Enter your [!UICONTROL Adobe] [!UICONTROL Client ID]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Enter your [!DNL Adobe] [!UICONTROL Client Secret]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>If you are using a JWT connection, enter your [!DNL Adobe] [!UICONTROL Technical account ID]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>If you are using a JWT connection, enter your [!DNL Adobe] [!UICONTROL Organization ID]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>If you are using a JWT connection, enter the private key that was generated when your credentials were created in the [!DNL Adobe Developer Console]. </p>
          <p>To extract your private key or certificate:</p>
          <ol>
            <li value="1">
              <p>Click <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Select the type of file you are extracting.</p>
            </li>
            <li value="3">
              <p>Select the file that contains the private key or certificate.</p>
            </li>
            <li value="4">
              <p>Enter the password for the file.</p>
            </li>
            <li value="5">
              <p>Click <b>Save</b> to extract the file and return to the connection setup.</p>
            </li>
          </ol>
        </td>
        </tr>
      </tbody>
    </table>
    
1. Click **[!UICONTROL Continue]** to save the connection and return to the module.
    
## [!DNL Adobe Photoshop] modules and their fields

When you configure [!DNL Adobe Photoshop] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Adobe Photoshop] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Actions

* [Convert HEX to RGB]()
* [Create an artboard](#create-an-artboard)
* [Create or edit a composite](#create-or-edit-a-composite)
* [Edit an image with various adjustments](#edit-an-image-with-various-adjustments)
* [Execute Photoshop actions, scripts, and transformations](#execute-photoshop-actions-scripts-and-transformations)
* [Generate a manifest](#generate-a-manifest)
* [Remove background](#remove-background)

#### Create an artboard

This module creates a new artboard in Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Images]</td>
      <td>
        <p>For each image that you want to add to this artboard, click <b>Add item</b> and enter the image's source type and location.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Artboard spacing]</p>
      </td>
   <td>Enter or map the spacing, in pixels, that you want to have between each artboard.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each converted file you want to create, click Add item and enter the storage, location, and other options as listed.</p>
      </td>
    </tr>
    </tbody>
</table>

#### Create or edit a composite

This module creates or edits a composite in Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Images]</td>
      <td>
        <p>For each image that you want to add to this artboard, click <b>Add item</b> and enter the image's source type and location.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Width]</p>
      </td>
   <td>If you are creating an image, enter the image width in pixels.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Height]</td>
      <td>
        <p>If you are creating an image, enter the image height in pixels.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Mode]</td>
      <td>
        <p>Select the color mode for this image.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fill]</td>
      <td>
        <p>Select the type of fill for the background layer.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>
        <p>Enter or map a name for the new image.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Pixel scale factor]</td>
      <td>
        <p>Enter or map the pixel scale factor. This must be a number between 0.1 and 1.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Resolution]</td>
      <td>
        <p>In the <b>Value</b> field, enter the value of the resolution in density units (pixels per inch). The default value is 72.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Profile Type]</td>
      <td>
        <p>If you want to override the default color profile, select a profile type and enter details as listed.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Crop > Top / Left / Bottom / Right]</td>
      <td>
        <p>Enter the bounds that you want to crop the image to.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Hide]</td>
      <td>
        <p>Select yes to hide pixels outside of crop bounds. IF set to false, pixels outside of crop bounds are deleted. The default is false.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Resize > Width]</td>
      <td>
        <p>Select the unit that you want to use for the width, then select the value that represents the width that you want. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Resize > Height]</td>
      <td>
        <p>Select the unit that you want to use for the height, then select the value that represents the height that you want. </p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Resolution]</td>
      <td>
        <p>Select the unit that you want to use for the resolution, then select the value that represents the resolution that you want.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Resample]</td>
      <td>
        <p>Select the resampling method to use when resizing.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Constrain proportions]</td>
      <td>
        <p>Select Yes to maintain the aspect ratio between width and height. Select No to allow independent adjustment of width and height.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Rasterize]</td>
      <td>
        <p>Select whether you want to rasterize the image.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Scale styles]</td>
      <td>
        <p>Select whether you want to apply scaling to styles when you resize the image.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Trim upon]</td>
      <td>
        <p>Select whether you want to trim upon transparent pixels.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Layers]</td>
      <td>
        <p>For each later you want to add, click <b>Add item</b> and enter layer details. </p><p>For details, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/createComposite">Create or edit a composite</a> in the Adobe documentation.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Default font PostScript name]</td>
      <td>
        <p>Enter or map the PostScript name of the default font that you want to use.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Missing font strategy]</td>
      <td>
        <p>Select whether you want the creation or edit to fail or to use the default font if a font is not available.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Additional fonts]</td>
      <td>
        <p>For each font that you want to add, click <b>Add item</b> and enter the font's source URL. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each edited file you want to create, click Add item and enter the output details. </p><p>For details see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/createComposite">Create or edit a composite</a> in the Adobe documentation.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Maximum number of results]</td>
      <td>
        <p>Enter or map the maximum number of results that you want the module to work with during one execution cycle.</p>
      </td>
      </tr>
      </tbody>
</table>

#### Edit an image with various adjustments

This module makes Lightroom-style adjustments to an image.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Images]</td>
      <td>
        <p>Enter or map the image's source type and location.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Other fields]</p>
      </td>
   <td><p>For details see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/edit">Edit an image with various adjustments</a> in the Adobe documentation.</p></td> 
    </tr>
    </tbody>
</table>

#### Execute Photoshop actions, scripts, and transformations

This module executes actions, scripts, and transformations available in the Firefly Photoshop API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Images]</td>
      <td>
        <p>Enter or map the image's source type and location.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Actions]</p>
      </td>
   <td><p>For each action that you want to add, click <b>Add item</b> and enter the action's source, URL, and name.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL UXP source]</p>
      </td>
   <td><p>If you are using a UXP script, select whether you are providing a URL or inline content, then enter or map the URL or content.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Additional contents]</p>
      </td>
   <td><p>Add up to 25 files referenced from the action or UXP.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each edited file you want to create, click Add item and enter the format, destination, and output pattern.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Maximum number of results]</td>
      <td>
        <p>Enter or map the maximum number of results that you want the module to work with during one execution cycle.</p>
      </td>
      </tr>
    </tbody>
</table>

#### Generate a manifest

This module generates a PSD manifest for the given input image.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Source]</td>
      <td>
        <p>Enter or map the image's source type and location.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each edited file you want to create, click Add item and enter the destination details.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Include layer thumbnails]</p>
      </td>
   <td><p>Select Yes if you want to module to generate a thumbnail rendition for each layer in the manifest.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum thumbnail depth]</p>
      </td>
   <td><p>Enter or map the maximum depth for thumbnail renditions. For no maximum depth, enter <code>0</code>.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Layer thumbnail format]</p>
      </td>
   <td><p>Select whether you want the thumbnails to be in JPEG or PNG format.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Extract Smart Object data]</td>
      <td>
        <p>Select whether to extract embedded smart objects and include a presigned URL in the manifest.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Trim to transparency]</td>
      <td>
        <p>Select whether to trim each layer thumbnail to remove transparent pixels.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of results]</td>
      <td>
        <p>Enter or map the maximum number of results that you want the module to work with during one execution cycle.</p>
      </td>
      </tr>
    </tbody>
</table> 

#### Remove background

This action module identifies the main subject of your image and removes the background. 

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Select the file service where the file you want to remove the background from is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to remove the background from. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the new file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the new file will be stored.  This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists. This applies only to files in Adobe storage.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Color space]</p>
      </td>
   <td>Select whether the output image uses RGB or RGBA color. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Mask format]</p>
      </td>
   <td>Select whether the edges of the image should be soft (feathered) or binary. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Optimize]</p>
      </td>
   <td>Select Performance to optimize for speed, or Batch to allow wait time. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Post process]</p>
      </td>
   <td>Select whether to enable post processing.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>Default is 4.0</td> 
    </tr> 
    </tbody>
</table>
 

### Legacy

* [Apply PSD edits (Legacy)](#apply-psd-edits-legacy)
* [Auto color correct an image (Legacy)](#auto-color-correct-an-image-legacy)
* [Convert image format (Legacy)](#convert-image-format-legacy)
* [Create a mask (Legacy)](#create-a-mask-legacy)
* [Create a new PSD (Legacy)](#create-a-new-psd-legacy)
* [Create renditions (Legacy)]()
* [Edit text layers (Legacy)](#edit-text-layers-legacy)
* [Edit text layers 2 (Legacy)](#edit-text-layers-2-legacy)
* [Execute an action JSON (Legacy)](#execute-an-action-json-legacy)
* [Execute Depth Blur (Legacy)](#execute-depth-blur-legacy)
* [Execute Photoshop actions (Legacy)](#execute-photoshop-actions-legacy)
* [Execute Product Crop (Legacy)](#execute-product-crop-legacy)
* [Get layer info (Legacy)](#get-layer-info-legacy)
* [Make a custom API call (Legacy)](#make-a-custom-api-call-legacy)
* [Remove background (Legacy)](#remove-background-legacy)
* [Replace a Smart Object (Legacy)](#replace-a-smart-object-legacy)
* [Replace a Smart Object 2 (Legacy)](#replace-a-smart-object-2-legacy)
* [Resize an image (Legacy)](#resize-an-image-legacy)
* [Watermark an image (Legacy)](#watermark-an-image-legacy)

#### Apply PSD edits (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Create or edit a composite](#create-or-edit-a-composite) module.

This action module applies a variety of document and layer level edits. 

This module supports large files. For more information on large files, see [Working with large files](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Select the file service where the file you want to edit is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to edit. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Image size) Height]</p>
      </td>
      <td> Enter or map the height of the image in pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Image size) Width]</p>
      </td>
      <td> Enter or map the width of the image in pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Canvas size) Top]</p>
      </td>
   <td> Enter or map, in pixels, the y coordinate of the document's upper-left corner. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Canvas size) Bottom]</p>
      </td>
   <td> Enter or map, in pixels, the y coordinate of the document's lower-right corner. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Canvas size) Left]</p>
      </td>
   <td> Enter or map, in pixels, the x coordinate of the document's upper-left corner. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Canvas size) Right]</p>
      </td>
   <td> Enter or map, in pixels, the x coordinate of the document's lower-right corner. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document) Trim]</p>
      </td>
   <td> Select Transparent pixels to base the trim on transparent pixels in the image. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Default font]</p>
      </td>
   <td> Enter the full postscript name of the font to be used as the global default for the document. This font will be used for any text layer which has a missing font and no other font has been specifically provided for that layer. If this font is missing, the option specified in Manage missing fonts will take effect. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> For each font that the document needs, click Add item and enter the font's storage location and file location. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Manage missing fonts]</p>
      </td>
   <td> Select the action to take if there are one or more missing fonts in the document. <ul><li><code>fail</code>: The job will not succeed and the status will be set to failed, with the details of the error provided in the details section in the status.</li><li><code>useDefault</code>: The job will succeed, and all the missing fonts will be replaced with ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Layers]</p>
      </td>
   <td> For each layer you want to add, click Add item and and fill in the layer details. <p>For details about layer options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/modifyDocumentAsync">Apply PSD Edits</a> in the Adobe Photoshop documentation.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each edited file you want to create, click Add item and enter the storage, location, and type as listed.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the new file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the new file will be stored. This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Select the file type that you want to convert the file to. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists. This applies only to files in Adobe storage.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Trim to Canvas]</p>
      </td>
   <td>Select whether the renditions must be of Canvas size. True trims the renditions to Canvas size, while False makes the renditions layer Size</td> 
    </tr>
    </tbody>
</table>

#### Auto color correct an image (Legacy)

This action module auto color corrects the specified image.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Select the file service where the file you want to color correct is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to color correct. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the new file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the new file will be stored. This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Select the file type that you want to convert the file to. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists. This applies only to files in Adobe storage.</p>
      </td>
    </tr>
    </tbody>
</table>

#### Convert image format (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Create or edit a composite](#create-or-edit-a-composite) module.

This action module converts a file to JPEG, PNG, PSD or TIFF.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Select the file service where the file you want to remove the background from is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to remove the background from. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each converted file you want to create, click Add item and enter the storage, location, and type as listed.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the new file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the new file will be stored. This is only necessary if you have not chosen Fusion internal storage for the output storage. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Select the file type that you want to convert the file to. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists. This applies only to files in Adobe storage.</p>
      </td>
    </tr>
    </tbody>
</table>

#### Create a mask (Legacy)

This action module returns a PNG file with a mask applied around the subject.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Select the file service where the file you want to create a mask from is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to create a mask from. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the mask file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the mask file will be stored. This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists. This applies only to files in Adobe storage.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Color space]</p>
      </td>
   <td>Select whether the output image uses RGB or RGBA color. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Mask format]</p>
      </td>
   <td>Select whether the mask should be soft (feathered) or binary. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Optimize]</p>
      </td>
   <td>Select Performance to optimize for speed, or Batch to allow wait time. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Post process]</p>
      </td>
   <td>Select whether to enable post processing.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>Default is 4.0</td> 
    </tr> 
    </tbody>
</table>

#### Create a new PSD (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Create or edit a composite](#create-or-edit-a-composite) module.

This action module creates a new PSD with optional layers, and generates renditions or saves as a PSD.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Image size) Height]</p>
      </td>
      <td> Enter or map the height of the image in pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Image size) Width]</p>
      </td>
      <td> Enter or map the width of the image in pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document) Resolution]</p>
      </td>
   <td> Enter or map, in pixels per inch, the resolution for the image. This must be between 72 and 300. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document) Mode]</p>
      </td>
   <td> Select the mode for the image. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document) Fill]</p>
      </td>
   <td> Select whether you want the fill for the background layer to be transparent, white, or the background color of the image. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document) Depth]</p>
      </td>
   <td> Select the bit depth of the image. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Layers]</p>
      </td>
   <td> For each layer you want to add, click Add item and and fill in the layer details. <p>For details about layer options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync">Create PSD</a> in the Adobe Photoshop documentation.  </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Global font]</p>
      </td>
   <td> Enter the full postscript name of the font to be used as the global default for the document. This font will be used for any text layer which has a missing font and no other font has been specifically provided for that layer. If this font is missing, the option specified in Manage missing fonts will take effect. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> For each font that the document needs, click Add item and enter the font's storage location and file location. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Manage missing fonts]</p>
      </td>
   <td> Select the action to take if there are one or more missing fonts in the document. <ul><li><code>fail</code>: The job will not succeed and the status will be set to failed, with the details of the error provided in the details section in the status.</li><li><code>useDefault</code>: The job will succeed, and all the missing fonts will be replaced with ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each file you want to create, click Add item and enter the storage, location, and type as listed.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the new file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the new file will be stored. This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Select the file type that you want to convert the file to. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Other fields]</td>
      <td>
        <p><p>For details about output options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync">Create PSD</a> in the Adobe Photoshop documentation.  </p>
      </td>
    </tr>
    </tbody>
</table>

#### Edit text layers (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Execute Photoshop actions, scripts, and transformations](#execute-photoshop-actions-scripts-and-transformations) module.

This action module edits text layers on a Photoshop file. You can enter separate edit details for multiple layers in the same file.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Select the file service where the file you want to edit is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to edit. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Manage missing fonts]</td>
      <td>
        <p>Select the action to take if there are one or more missing fonts in the document. If the font is not provided, the module uses the default font.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default font]  </td>
      <td>
        <p>Enter the full postscript name of the font to be used as the global default for the document. This font will be used for any text layer which has a missing font and no other font has been specifically provided for that layer. If this font is missing, the option specified in Manage missing fonts will take effect.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> Enter the font's storage location and file location. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Layers]</td>
   <td> <p>For each text layer that you want to edit, click <b>Add item</b> and enter the layer options.<p>For details about layer options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync">Edit text</a> in the Adobe Photoshop documentation.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the edited file to be stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the edited file will be stored. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Select the file type for the edited file. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Edit text layers 2 (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Execute Photoshop actions, scripts, and transformations](#execute-photoshop-actions-scripts-and-transformations) module.

This action module edits a text layer on a Photoshop file.

To edit multiple layers, use the [Edit text layers](#edit-text-layers) module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Select the file service where the file you want to edit is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to edit. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Manage missing fonts]</td>
      <td>
        <p>Select the action to take if there are one or more missing fonts in the document. If the font is not provided, the module uses the default font.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default font]  </td>
      <td>
        <p>Enter the full postscript name of the font to be used as the global default for the document. This font will be used for any text layer which has a missing font and no other font has been specifically provided for that layer. If this font is missing, the option specified in Manage missing fonts will take effect.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> Enter the font's storage location and file location. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Layers]</td>
   <td> <p>For details about layer options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync">Edit text layer</a> in the Adobe Photoshop documentation.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output file storage]</td>
      <td>
        <p>Select the file service where the you want the edited file to be stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the edited file to be stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the edited file will be stored. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Select the file type for the edited file. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists.</p>
      </td>
    </tr>
  </tbody>
</table>


#### Execute an action JSON (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Execute Photoshop actions, scripts, and transformations](#execute-photoshop-actions-scripts-and-transformations) module.

This action module executes Photoshop actions using JSON commands.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Select the file service where the file you want to edit is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to edit. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Action JSON]</td>
      <td>
        <p>Enter the JSON command for the action you want to take.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fonts / Patterns / Brushes / Additional images]</td>
      <td>
        <p>For each font, pattern, brush, or additional image that you want to use in this action, click Add item and enter the item's storage and file location.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Font / Pattern / Brush file URL]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to use. </td> 
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each file you want to create, click Add item and enter the storage, location, type, and overwrite option as listed.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Storage]</td>
      <td>
        <p>Select the file service where the you want the edited file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) File URL]</p>
      </td>
   <td> Enter or map the URL or path of where the edited file will be stored.  This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> Select the file type for the edited file. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists.</p>
      </td>
    </tr>
      </tbody>
</table>

#### Execute Depth Blur (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.

This action module executes Depth Blur on the selected file.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Select the file service where the file you want to edit is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to edit. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Storage]</td>
      <td>
        <p>Select the file service where the you want the edited file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) File URL]</p>
      </td>
   <td> Enter or map the URL or path of where the edited file will be stored.  This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> Select the file type for the edited file. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Other fields]</td>
      <td>
        <p>For details about other Depth Blur options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Execute Depth Blur </a>in the Adobe Photoshop API documentation.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Execute Photoshop Actions (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Execute Photoshop actions, scripts, and transformations](#execute-photoshop-actions-scripts-and-transformations) module.

This action module executes a Photoshop action on the selected image.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Select the file service where the file you want to edit is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to edit. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Actions file storage]</td>
      <td>
        <p>Select the file service where actions file is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Actions file URL]</p>
      </td>
   <td> Enter or map the URL or path of the actions file. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Action name]</p>
      </td>
   <td> If you only want to execute a particular action, you may specify which action to play from the ActionSet. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Font / Pattern / Brush storage]</td>
      <td>
        <p>Select the file service where the file you want to use is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Font / Pattern / Brush file URL]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to use. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Storage]</td>
      <td>
        <p>Select the file service where the you want the edited file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) File URL]</p>
      </td>
   <td> Enter or map the URL or path of where the edited file will be stored.  This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> Select the file type for the edited file. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Other fields]</td>
      <td>
        <p>For details about other Depth Blur options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Execute Depth Blur </a>in the Adobe Photoshop API documentation.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Execute Product Crop (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Execute Photoshop actions, scripts, and transformations](#execute-photoshop-actions-scripts-and-transformations) module.

This action module executes Product Crop on the selected image.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Select the file service where the file you want to crop is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to crop. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Unit]</p>
      </td>
   <td> Select whether you want to describe the height and width adjustment in pixels or as a percent. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Width]</p>
      </td>
   <td> Enter or map amount of width padding you want to add. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Height]</p>
      </td>
   <td> Enter or map amount of height padding you want to add. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Storage]</td>
      <td>
        <p>Select the file service where the you want the edited file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) File URL]</p>
      </td>
   <td> Enter or map the URL or path of where the edited file will be stored.  This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> Select the file type for the edited file. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Other fields]</td>
      <td>
        <p>For details about other Depth Blur options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Execute Depth Blur </a>in the Adobe Photoshop API documentation.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Get layer info (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Generate a manifest](#generate-a-manifest) module.

This action module retrieves layer information from the specified PSD file.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Select the file service where the file you want to retrieve layer information from is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to retrieve layer information from. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Thumbnails]</p>
      </td>
   <td> Select the type of file that you want the thumbnails to be. Thumbnails are small previews for any renderable layer.</td> 
    </tr>
  </tbody>
</table>

#### Make a custom API call

This action module makes a custom call to the Photoshop API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Enter a path relative to <code>https://image.adobe.io/pie/psdService</code>. Example: <code>/photoshopActions</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Add the headers of the request in the form of a standard JSON object.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion adds authorization headers automatically.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Enter the request query string.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### Replace a smart object (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Create or edit a composite](#create-or-edit-a-composite) module.

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Create or edit a composite](#create-or-edit-a-composite) module.

This action module replaces a Smart Object within a PSD layer, and generates new renditions.

This module uses Smart Object API version 2.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Select the file service where the Smart Object is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Enter or map the URL or path of the Smart Object. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Layers]</p>
      </td>
   <td>For each layer you want to add to the Smart Object, click Add item and Enter the object's name or ID, the file service where the Smart Object is stored, and the the URL or path of the layer.<p>For descriptions of the advanced settings in this area, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync">Replace a Smart Object</a> in the Photoshop API documentation </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resize image during place]</p>
      </td>
   <td> Select whether you want to resize the image.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each new rendition you want the module to produce, click Add item and fill in the following fields. You can have a maximum of 25 output files.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the new file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the new file will be stored.  This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> Select the file type for the edited file. </td> 
    </tr>
     </tbody>
</table>

#### Replace a smart object 2 (Legacy)

This action module replaces a Smart Object within a PSD layer, and generates new renditions.

This module uses the legacy version of Smart Objects.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Select the file service where the Smart Object is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Enter or map the URL or path of the Smart Object. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Layers]</p>
      </td>
   <td>For each layer you want to add to the Smart Object, click Add item and Enter the object's name or ID, the file service where the Smart Object is stored, and the the URL or path of the layer.<p>For descriptions of the advanced settings in this area, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync">Replace a Smart Object</a> in the Photoshop API documentation </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each new rendition you want the module to produce, click Add item and fill in the following fields. You can have a maximum of 25 output files.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the new file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the new file will be stored.  This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Width]</p>
      </td>
   <td> The width, in pixels, of the output file. The module will preserve the original aspect ratio. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists. This applies only to files in Adobe storage.</p>
      </td>
    </tbody>
</table>

#### Resize an image (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Create or edit a composite](#create-or-edit-a-composite) module.

This action resizes an image, using the same aspect ratio.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Storage]</td>
      <td>
        <p>Select the file service where the file you want to resize is stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL File location]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to resize.  This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each converted file you want to create, click Add item and enter the storage, location, and other options as listed.</p>
      </td>
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Storage]</td>
      <td>
        <p>Select the file service where the you want the new file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL File location]</p>
      </td>
   <td> Enter or map the URL or path of where the new file will be stored.  This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Width]</p>
      </td>
   <td> The width, in pixels, of the output file. The module will preserve the original aspect ratio. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Max width]</p>
      </td>
   <td>When width is 0, Max with can be provided to get the size. Max width takes precedence with it is smaller than the document width.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists. This applies only to files in Adobe storage.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Trim to canvas]</p>
      </td>
   <td>Select Yes to trim the renditions to Canvas size, or No to make the renditions Layer Size.</td> 
    </tr>
    </tbody>
</table>

#### Watermark an image (Legacy)

>[!NOTE]
>
>This module has been deprecated, and will no longer work after July 30, 2026.
>Update this module to the [Create or edit a composite](#create-or-edit-a-composite) module.

This action module adds a watermark to the selected image.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Photoshop], see <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Create a connection to [!DNL Adobe Photoshop]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Base > Input) Storage]</td>
      <td>
        <p>Select the file service where the file you want to add a watermark to is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Base > Input) File location]</p>
      </td>
   <td> Enter or map the URL or path of the file that you want to add a watermark to. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Watermark > Input) Storage]</td>
      <td>
        <p>Select the file service where the watermark you want to add is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Watermark > Input) Storage]</td>
      <td>
        <p>Select the file service where the watermark you want to add is stored.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark > Bounds) Height]</p>
      </td>
   <td>Enter or map the desired height of the watermark in pixels.</td> 
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark > Bounds) Width]</p>
      </td>
   <td> Enter or map the desired width of the watermark in pixels. </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark > Bounds) Left]</p>
      </td>
   <td> Enter or map the distance in pixels from the left side of the image that the watermark should be.</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark > Bounds) Top]</p>
      </td>
   <td> Enter or map the distance in pixels from the top of the image that the watermark should be.</td> 
    </tr>  
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Select the file service where the you want the watermarked file to be stored.</p><p>Selecting Fusion internal storage makes the file available for later modules, but does not make the file available outside of the scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Enter or map the URL or path of where the watermarked file will be stored. This is only necessary if you have not chosen Fusion internal storage for the output storage.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Select the file type that you want to convert the file to. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Width]</p>
      </td>
   <td> The width, in pixels, of the output file. The module will preserve the original aspect ratio. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Select whether the newly edited file will overwrite any output file that already exists. This applies only to files in Adobe storage.</p>
      </td>
    </tbody>
</table>
