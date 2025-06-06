---
title: Adobe Photoshop modules
description: With the Adobe Photoshop modules, you can start an Adobe Workfront Fusion scenario based on events in your Adobe Photoshop account, create, read, or update agreements and other records, search for records using criteria you set, and upload documents.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
---
# [!DNL Adobe Photoshop] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Adobe Photoshop], as well as connect it to multiple third-party applications and services. 


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

Before you can use the [!DNL Adobe Photoshop] connector, you must ensure that the following prerequisites are met:

* You must have an active [!DNL Adobe Photoshop] account.
* You must have a Firefly Services license.
* You must have a Client ID and Client Secret. You can acquire these from the Adobe Developer Console.

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

When you configure [!DNL Adobe Photoshop] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Adobe Photoshop] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Apply PSD edits](#apply-psd-edits)
* [Auto color correct an image](#auto-color-correct-an-image)
* [Convert image format](#convert-image-format)
* [Create a mask](#create-a-mask)
* [Create a new PSD](#create-a-new-psd)
* [Edit text layers](#edit-text-layers)
* [Edit text layers (Legacy)](#edit-text-layers-legacy)
* [Execute an action JSON](#execute-an-action-json)
* [Execute Depth Blur](#execute-depth-blur)
* [Execute Photoshop actions](#execute-photoshop-actions)
* [Execute Product Crop](#execute-product-crop)
* [Get layer info](#get-layer-info)
* [Make a custom API call](#make-a-custom-api-call)
* [Remove background](#remove-background)
* [Replace a Smart Object](#replace-a-smart-object)
* [Replace a Smart Object (Legacy)](#replace-a-smart-object-legacy)
* [Resize an image](#resize-an-image)
* [Watermark an image](#watermark-an-image)

### Apply PSD edits

This action module applies a variety of document and layer level edits. 

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
   <td> For each layer you want to add, click Add item and and fill in the layer details. <p>For details about layer options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_applyPsdEdits/">Apply PSD Edits</a> in the Adobe Photoshop documentation.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>For each edited file you want to create, click Add item and enter the storage, location, and type as listed in this table.</p>
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

### Auto color correct an image

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

### Convert image format

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
        <p>For each converted file you want to create, click Add item and enter the storage, location, and type as listed in this table.</p>
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

### Create a mask

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

### Create a new PSD

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
   <td> For each layer you want to add, click Add item and and fill in the layer details. <p>For details about layer options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_createPsd/">Create PSD</a> in the Adobe Photoshop documentation.  </td> 
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
        <p>For each file you want to create, click Add item and enter the storage, location, and type as listed in this table.</p>
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
        <p><p>For details about output options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_createPsd/">Create PSD</a> in the Adobe Photoshop documentation.  </p>
      </td>
    </tr>
    </tbody>
</table>

### Edit text layers

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
   <td> <p>For each text layer that you want to edit, click <b>Add item</b> and enter the layer options.<p>For details about layer options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_editText/">Edit text</a> in the Adobe Photoshop documentation.</p>  </td>     </tr>
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

### Edit text layers (Legacy)

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
   <td> <p>For details about layer options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_editText/">Edit text layer</a> in the Adobe Photoshop documentation.</p>  </td>     </tr>
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


### Execute an action JSON

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
        <p>For each file you want to create, click Add item and enter the storage, location, type, and overwrite option as listed in this table.</p>
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

### Execute Depth Blur

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
        <p>For details about other Depth Blur options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_depthBlur/">Execute Depth Blur </a>in the Adobe Photoshop API documentation.</p>
      </td>
    </tr>
  </tbody>
</table>

### Execute Photoshop Actions

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
        <p>For details about other Depth Blur options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_depthBlur/">Execute Depth Blur </a>in the Adobe Photoshop API documentation.</p>
      </td>
    </tr>
  </tbody>
</table>

### Execute Product Crop

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
        <p>For details about other Depth Blur options, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_depthBlur/">Execute Depth Blur </a>in the Adobe Photoshop API documentation.</p>
      </td>
    </tr>
  </tbody>
</table>

### Get layer info

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

### Make a custom API call

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
        <p>[!DNL Workfront Fusion] adds authorization headers automatically.</p>
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

### Remove background

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

### Replace a smart object

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
   <td>For each layer you want to add to the Smart Object, click Add item and Enter the object's name or ID, the file service where the Smart Object is stored, and the the URL or path of the layer.<p>For descriptions of the advanced settings in this area, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_replaceSmartObject/">Replace a Smart Object</a> in the Photoshop API documentation </td> 
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

### Replace a smart object (Legacy)

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
   <td>For each layer you want to add to the Smart Object, click Add item and Enter the object's name or ID, the file service where the Smart Object is stored, and the the URL or path of the layer.<p>For descriptions of the advanced settings in this area, see <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_replaceSmartObject/">Replace a Smart Object</a> in the Photoshop API documentation </td> 
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

### Resize an image

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
        <p>For each converted file you want to create, click Add item and enter the storage, location, and other options as listed in this table.</p>
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

### Watermark an image

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
