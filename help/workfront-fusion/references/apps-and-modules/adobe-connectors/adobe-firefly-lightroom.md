---
title: Adobe Firefly modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Adobe Firefly Lightroom, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
---
# Adobe Firefly Lightroom modules

<!--add to tocs-->

In an Adobe Workfront Fusion scenario, you can automate workflows that use Adobe Firefly Lightroom, as well as connect it to multiple third-party applications and services. 

If you need instructions on creating a scenario, see the articles under [Create a scenario: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

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

Before you can use the Adobe Firefly Lightroom connector, you must ensure that the following prerequisites are met:

* You must have an active Adobe Firefly Lightroom account.

## Create a connection to Adobe Firefly Lightroom

To create a connection for your Adobe Firefly Lightroom modules:

1. In any module, click **[!UICONTROL Add]** next to the Connection box.
    
1. Fill in the following fields:
    
    <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Connection name</td>
        <td>
          <p>Enter a name for this connection.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Environment</td>
        <td>Select whether you are connecting to a production or non-production environment.</td>
        </tr>
        <tr>
        <td role="rowheader">Type</td>
        <td>Select whether you are connecting to a service account or a personal account.</td>
        </tr>
        <tr>
        <td role="rowheader">Client ID</td>
        <td>Enter your Adobe Client ID. This can be found in the Credentials details section of the Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Client Secret</td>
        <td>Enter your Adobe Client Secret. This can be found in the Credentials details section of the Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>
    
1. Click **[!UICONTROL Continue]** to save the connection and return to the module.


## Adobe Firefly Lightroom modules and their fields

When you configure Adobe Firefly Lightroom modules, Workfront Fusion displays the fields listed below. Along with these, additional Adobe Firefly Lightroom fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Add XMP to image](#add-xmp-to-image)
* [Apply Lightroom edits](#apply-lightroom-edits)
* [Apply Lightroom presets](#apply-lightroom-presets)
* [Auto-straighten](#auto-straighten)
* [Auto-tone](#auto-tone)


### Add XMP to image

This module applies an XMP-based Lightroom preset to an image.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly Lightroom, see <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Create a connection to Adobe Firefly Lightroom</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image URL</td> 
   <td>Enter or map a presigned URL that represents the image you want to apply XMP to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Storage type</td> 
   <td>Select the type of storage that the image is stored in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">XMP content</td> 
   <td>Enter or map the text of the XMP content that you want to add to the image. This should be an XML string.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Orientation</td> 
    <td>Enter or map the EXIF orientation to apply to the image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output storage</td> 
    <td>Select where you want the output file to be stored. <p>Fusion internal storage does not store the image outside of the scenario, but allows other modules in the scenario to access the image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output type</td> 
   <td>Select the file type for the output file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overwrite</td> 
   <td>Select yes if you want to allow the module to overwrite output if it already exists. This applies only to Adobe cloud storage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Quality</td> 
   <td>Enter or map the quality of the output image. 1 is the lowest quality, and 12 is the highest. This applies only to JPEG files.</td> 
  </tr> 
 </tbody> 
</table>

### Apply Lightroom edits

This module applies one or more Lightroom edits to an image. Edits include exposure, contrast, sharpness, and saturation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly Lightroom, see <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Create a connection to Adobe Firefly Lightroom</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image URL</td> 
   <td>Enter or map a presigned URL that represents the image you want to apply XMP to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Storage type</td> 
   <td>Select the type of storage that the image is stored in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Edit options</td> 
   <td>Set any edit options that you want to apply to the image.<p>For details on options, see <a href="https://developer.adobe.com/firefly-services/docs/lightroom/api/#operation/applyEdits">Apply Lightroom Edits</a> in the Adobe Firefly Lightroom API documentation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output storage</td> 
    <td>Select where you want the output file to be stored. <p>Fusion internal storage does not store the image outside of the scenario, but allows other modules in the scenario to access the image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output type</td> 
   <td>Select the file type for the output file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overwrite</td> 
   <td>Select yes if you want to allow the module to overwrite output if it already exists. This applies only to Adobe cloud storage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Quality</td> 
   <td>Enter or map the quality of the output image. 1 is the lowest quality, and 12 is the highest. This applies only to JPEG files.</td> 
  </tr> 
 </tbody> 
</table>

### Apply Lightroom presets

This module applies one or more XMP Lightroom presets to the given image, by using the given preset XMP files.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly Lightroom, see <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Create a connection to Adobe Firefly Lightroom</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image URL</td> 
   <td>Enter or map a presigned URL that represents the image you want to apply XMP to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Storage type</td> 
   <td>Select the type of storage that the image is stored in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Presets</td> 
   <td>For each preset that you want to apply, click <b>Add item</b>, enter the preset's presigned URL, and select its storage type.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output storage</td> 
    <td>Select where you want the output file to be stored. <p>Fusion internal storage does not store the image outside of the scenario, but allows other modules in the scenario to access the image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output type</td> 
   <td>Select the file type for the output file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overwrite</td> 
   <td>Select yes if you want to allow the module to overwrite output if it already exists. This applies only to Adobe cloud storage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Quality</td> 
   <td>Enter or map the quality of the output image. 1 is the lowest quality, and 12 is the highest. This applies only to JPEG files.</td> 
  </tr> 
 </tbody> 
</table>

### Auto-straighten

This module auto-straightens an image by applying the Auto Upright transformation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly Lightroom, see <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Create a connection to Adobe Firefly Lightroom</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image URL</td> 
   <td>Enter or map a presigned URL that represents the image you want to apply XMP to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Storage type</td> 
   <td>Select the type of storage that the image is stored in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Upright mode</td> 
   <td>Select the type of Upright mode that you want to use. If you do not set a value, an appropriate mode will be provided automatically.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Constrain Crop</td> 
   <td>Select whether the straightened image should be cropped to remove all blank edges.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">Output sorage</td> 
    <td>Select where you want the output file to be stored. <p>Fusion internal storage does not store the image outside of the scenario, but allows other modules in the scenario to access the image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output type</td> 
   <td>Select the file type for the output file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overwrite</td> 
   <td>Select yes if you want to allow the module to overwrite output if it already exists. This applies only to Adobe cloud storage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Quality</td> 
   <td>Enter or map the quality of the output image. 1 is the lowest quality, and 12 is the highest. This applies only to JPEG files.</td> 
  </tr> 
 </tbody> 
</table>


### Auto-tone

This module automatically corrects exposure, contrast, sharpness, and saturation on an image.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly Lightroom, see <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Create a connection to Adobe Firefly Lightroom</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image URL</td> 
   <td>Enter or map a presigned URL that represents the image you want to apply XMP to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Storage type</td> 
   <td>Select the type of storage that the image is stored in.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Output storage</td> 
    <td>Select where you want the output file to be stored. <p>Fusion internal storage does not store the image outside of the scenario, but allows other modules in the scenario to access the image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output type</td> 
   <td>Select the file type for the output file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overwrite</td> 
   <td>Select yes if you want to allow the module to overwrite output if it already exists. This applies only to Adobe cloud storage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Quality</td> 
   <td>Enter or map the quality of the output image. 1 is the lowest quality, and 12 is the highest. This applies only to JPEG files.</td> 
  </tr> 
 </tbody> 
</table>


