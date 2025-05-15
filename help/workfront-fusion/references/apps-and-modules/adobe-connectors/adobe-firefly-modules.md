---
title: Adobe Firefly modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Adobe Firefly], as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
---
# [!DNL Adobe Firefly] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Adobe Firefly], as well as connect it to multiple third-party applications and services. 

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

Before you can use the [!DNL Adobe Firefly] connector, you must ensure that the following prerequisites are met:

* You must have an active [!DNL Adobe Firefly] account.

## Adobe Firefly API information

The Adobe Firefly connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.4.24</td> 
  </tr>
 </tbody> 
 </table>

## Create a connection to [!DNL Adobe Firefly]

To create a connection for your [!DNL Adobe Firefly] modules:

1. In any module, click **[!UICONTROL Add]** next to the Connection box.
    
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
        <td>Enter your [!UICONTROL Adobe] [!UICONTROL Client ID]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Enter your [!DNL Adobe] [!UICONTROL Client Secret]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console].</td>
        </tr>
      </tbody>
    </table>
    
1. Click **[!UICONTROL Continue]** to save the connection and return to the module.
    
## [!DNL Adobe Firefly] modules and their fields

When you configure [!DNL Adobe Firefly] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Adobe Firefly] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Expand an image

This action module expands an image, optionally with content from a prompt you provide.

This module works with the Firefly API V3 Async. The previous version of this module has been deprecated and will be removed in the near future.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Campaign], see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to [!DNL Adobe Firefly]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Enter or map a prompt for the content with which you want to expand the image. If no prompt is provided, the image will be expanded with content matching the original image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Enter a number between 1-4. The module will generate this number of expanded image variations.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source]</td> 
   <td>Select how you are providing the source file:<ul><li><p><b>File</b></p><p>Select a source file from a previous module, or map the source file's Reference image file name and reference image file.</p></li><li><p><b>Presigned URL</b></p><p>Enter or map the URL of the source image.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expanded image format]</td> 
   <td>Select the file format that the expanded image will be saved as.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand by]</td> 
   <td>  <p>Select whether you want to expand the image by using image placement or by using a mask.</p> 
   <ul>
   <li><b>Placement</b><p>Enter the horizontal and vertial alignment, and the inset of the placed image from the edges.</p></li>
   <li><b>Mask</b><p>Select the source file for the mask, and whether the mask should be inverted.</p></li>
   </ul>
</td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Select the height and width that you want the expanded image to be.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>For each image that the module will generate, click <b>Add item</b> and enter or map an integer. You can use this same seed in another Expand an image module to generate a similar image with different styles. The number of seeds you add must be equal to the Number of variations field.</td> 
  </tr> 
 </tbody> 
</table>

### Expand an image (deprecated)

This module has been deprecated and will be removed in the near future. Use the Expand an image module instead.

### Fill an image

This action module fills the masked area of an image, optionally with content from a prompt you provide.

This module works with the Firefly API V3 Async. The previous version of this module has been deprecated and will be removed in the near future.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Campaign], see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to [!DNL Adobe Firefly]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image > Source]</td> 
   <td>Select how you are providing the image source file:<ul><li><p><b>File</b></p><p>Select a source file from a previous module, or map the source file's Reference image file name and reference image file.</p></li><li><p><b>Presigned URL</b></p><p>Enter or map the URL of the source image.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mask > Source]</td> 
   <td>Select how you are providing the mask source file:<ul><li><p><b>File</b></p><p>Select a source file from a previous module, or map the source file's Reference image file name and reference image file.</p></li><li><p><b>Presigned URL</b></p><p>Enter or map the URL of the source image.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Enter or map a prompt for the content with which you want to fill the image. If no prompt is provided, the image will be filled with content matching the original image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Enter a number between 1-4. The module will generate this number of filled image variations.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filled image format]</td> 
   <td>Select the file format that the filled image will be saved as.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>For each image that the module will generate, click <b>Add item</b> and enter or map an integer. You can use this same seed in another Expand an image module to generate a similar image with different styles. The number of seeds you add must be equal to the Number of variations field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Select the size that you want the filled image to be.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>If a locale is provided, the module generates content more relevant to the specified locale. <p>Locale must be provided in ISO 639-1 language code and ISO 3166-1 region.</p><p> Example: <code>en-US</code></p></td> 
  </tr> 
 </tbody> 
</table>

### Fill an image (deprecated)

This module has been deprecated and will be removed in the near future. Use the Fill an image module instead.

### Generate an image

This action module generates and image based on a prompt you provide. You can also provide an optional reference image, and the generated image will match the style of the reference image.

This module works with the Firefly API V3 Async. The previous version of this module has been deprecated and will be removed in the near future.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Campaign], see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to [!DNL Adobe Firefly]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Enter or map a prompt for the image you want to generate. More detail in the prompt will allow you more control over what appears in the image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model version]</td> 
   <td>Select the Firefly model version that you want to use to generate the image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Enter a number between 1-4. The module will generate this number of image variations.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Select the file format that the expanded image will be saved as. If you select default, the file format will be JPEG if no reference image is provided. If a reference image is provided, the file format of the generated image will be the same as the reference image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Image reference]</td> 
    <td>Select how you are providing the source file for the new image's structure:<ul><li><p><b>File</b></p><p>Select a source file from a previous module, or map the source file's Reference image file name and reference image file.</p></li><li><p><b>Presigned URL</b></p><p>Enter or map the URL of the source image.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Strength]</td> 
    <td>Enter a number between 0 and 100 to control how strictly Firefly follows the source image's structure. Higher numbers mean that Firefly follows the image more strictly.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Image reference]</td> 
    <td>Select how you are providing the source file for the new image's style:<ul><li><p><b>File</b></p><p>Select a source file from a previous module, or map the source file's Reference image file name and reference image file.</p></li><li><p><b>Presigned URL</b></p><p>Enter or map the URL of the source image.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Strength]</td> 
    <td>Enter a number between 0 and 100 to control how strictly Firefly follows the source image's style. Higher numbers mean that Firefly follows the image more strictly.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Presets]</td> 
   <td>If you want to use a preset style, click Add item and enter or map the style that you want to use.<p>For a list of preset styles, see <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Image Model Styles</a> in the Adobe developer documentation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Negative prompt]</td> 
   <td>Enter or map the words that you want to avoid in the generated content. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content class]</td> 
   <td>Select whether you want the generated image to be more like a photo, or more like created art. <ul><li><b>Photo</b><p>Enter values for the Aperture, Shutter speed (in seconds), and field of view (in millimeters).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]</td> 
   <td>For each image that the module will generate, click <b>Add item</b> and enter or map an integer. You can use this same seed in another Expand an image module to generate a similar image with different styles. The number of seeds you add must be equal to the Number of variations field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Select the size that you want the generated image to be.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Visual intensity]</td> 
   <td>Enter or map an integer that represents the overall intensity of the photo's existing visual characteristics. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>If a locale is provided, the module generates content more relevant to the specified locale. <p>Locale must be provided in ISO 639-1 language code and ISO 3166-1 region.</p><p> Example: <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tileable]</td> 
   <td>Enable this option to generate an image that can be repeated infinitely in every direction.</td> 
  </tr> 
 </tbody> 
</table>

### Generate an image (deprecated)

This module has been deprecated and will be removed in the near future. Use the Generate an image module instead.

### Generate an object composite

This action module combines images generated by Firefly to create an image composite.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Campaign], see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to [!DNL Adobe Firefly]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Enter or map a prompt for the image you want to generate. More detail in the prompt will allow you more control over what appears in the image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Enter a number between 1-4. The module will generate this number of image variations.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content classs]</td> 
   <td>Select whether you want the generated image to be more like a photo or like art.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image > Source]</td> 
    <td>Select how you are providing the source file for the new image's structure:<ul><li><p><b>File</b></p><p>Select a source file from a previous module, or map the source file's Reference image file name and reference image file.</p></li><li><p><b>Presigned URL</b></p><p>Enter or map the URL of the source image.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Select the file format that the expanded image will be saved as. If you select default, the file format will be JPEG if no reference image is provided. If a reference image is provided, the file format of the generated image will be the same as the reference image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Image reference]</td> 
    <td>Select how you are providing the source file for the new image's style:<ul><li><p><b>File</b></p><p>Select a source file from a previous module, or map the source file's Reference image file name and reference image file.</p></li><li><p><b>Presigned URL</b></p><p>Enter or map the URL of the source image.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Strength]</td> 
    <td>Enter a number between 0 and 100 to control how strictly Firefly follows the source image's style. Higher numbers mean that Firefly follows the image more strictly.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Presets]</td> 
   <td>If you want to use a preset style, click Add item and enter or map the style that you want to use.<p>For a list of preset styles, see <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Image Model Styles</a> in the Adobe developer documentation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Select the size that you want the generated composite to be. </td> 
  </tr> 
 </tbody> 
</table>

### Generate similar images

This action module generates images similar to the source image you specify.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Campaign], see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to [!DNL Adobe Firefly]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Enter a number between 1-4. The module will generate this number of image variations.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model version]</td> 
   <td>Select the Firefly model version that you want to use to generate the images.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Select the file format that the expanded image will be saved as. If you select default, the file format will be JPEG if no reference image is provided. If a reference image is provided, the file format of the generated image will be the same as the reference image.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Image > Source]</td> 
    <td>Select how you are providing the source file for the new image's structure:<ul><li><p><b>File</b></p><p>Select a source file from a previous module, or map the source file's Reference image file name and reference image file.</p></li><li><p><b>Presigned URL</b></p><p>Enter or map the URL of the source image.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Image reference]</td> 
    <td>Select how you are providing the source file for the new image's style:<ul><li><p><b>File</b></p><p>Select a source file from a previous module, or map the source file's Reference image file name and reference image file.</p></li><li><p><b>Presigned URL</b></p><p>Enter or map the URL of the source image.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Select the size that you want the generated composite to be. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>For each image that the module will generate, click <b>Add item</b> and enter or map an integer. You can use this same seed in another Expand an image module to generate a similar image with different styles. The number of seeds you add must be equal to the Number of variations field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tileable]</td> 
   <td>Enable this option to generate an image that can be repeated infinitely in every direction.</td> 
  </tr> 
 </tbody> 
</table>


### Make a custom API call

This action module makes a custom call to the Firefly API.

For specific available APIs, see [Adobe Firefly API](https://developer.adobe.com/firefly-services/docs/firefly-api/) in the Adobe Developer documentation.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Firefly], see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to [!DNL Adobe Firefly]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Enter a path relative to <code>https://firefly-api.adobe.io/</code>.</p>
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
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

