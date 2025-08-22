---
title: Image modules
description: Adobe Workfront Fusion Image modules allow you get information about a specific image (dimensions, type, and so on), convert an image to another file format, and directly change the size of the image.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
---
# Image modules

Adobe Workfront Fusion [!UICONTROL Image] modules allow you get information about a specific image (dimensions, type, and so on), convert an image to another file format, and directly change the size of the image.

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
   <p>No Workfront Fusion license requirement</p>
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

## [!UICONTROL Image] modules and their fields

When you are configuring this module, the following fields display. A bolded title in a module indicates a required field.

* [[!UICONTROL Convert a format]](#convert-a-format)
* [[!UICONTROL Extract metadata]](#extract-metadata)
* [[!UICONTROL Resize]](#resize)

### [!UICONTROL Convert a format] 

This transformer module changes the format of an image file. This module is compatible the following formats:

* PNG
* JPG
* GIF
* BMP

Both the source file and the output must be in one of these formats. For example, the [!UICONTROL Image] >[!UICONTROL Convert a format] module can transform a PNG file into a BMP file, or a BMP into a JPG.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output format]</td> 
   <td>Select the format that you want the module to convert the source file to. </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Extract metadata]

This transformer module returns basic information about a module.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Resize] 

This transformer module changes an image's height and width according to criteria you specify.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL I want to]</td> 
   <td>Select whether you want to maintain the height-width ratio or change the dimensions to a specified height and width.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL According to]</td> 
   <td> <p>Select how you want the module to determine the new size of the image. This field appears if you selected to maintain height-width ration in the I want to field. Other fields appear based on the selection in this field.</p> 
    <ul> 
     <li> <p>[!UICONTROL Maximum width]</p> <p>Reduces an image to a width you specify. Height is calculated automatically.</p> </li> 
     <li> <p>[!UICONTROL Maximum height]</p> <p>Reduces an image to a height you specify. Width is calculated automatically.</p> </li> 
     <li> <p>[!UICONTROL Maximum height or width]</p> <p>Reduces an image in a way that its height and width do not exceed the values you specify. Because this option maintains height-width ratio, one of the dimensions may be smaller than specified. For example, if height and width are both specified as 40, a 400x300 image will be reduced to 40X30.</p> </li> 
     <li> <p>[!UICONTROL Minimum width]</p> <p>Enlarges an image to a width you specify. Height is calculated automatically.</p> </li> 
     <li> <p>[!UICONTROL Minimum height]</p> <p>Enlarges an image to a height you specify. Width is calculated automatically.</p> </li> 
     <li> <p>[!UICONTROL Minimum height or width]</p> <p>Enlarges an image in a way that its height and width are not smaller than the values you specify. Because this option maintains height-width ratio, one of the dimensions may be larger than specified. For example, if height and width are both specified as 300, a 40x30 image will be enlarged to 400X300.</p> </li> 
     <li> <p>[!UICONTROL Percent]</p> <p>Changes the image size by a percentage based on the value you specify. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Width]</td> 
   <td>Enter or map the desired width of the resized image in pixels.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Height]</td> 
   <td>Enter or map the desired height of the resized image in pixels.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Change by percentage]</td> 
   <td>If you have chosen to change the image by percentage, enter or map the percentage that you want to change the image by.</td> 
  </tr> 
 </tbody> 
</table>

## Troubleshooting

### Action terminated with an error

 an action can terminate with an error because of one of the following causes :

* Received data is not in the JPG/GIF/PNG/BMP format
* The maximum width/height limit was exceeded while changing the image dimensions. The image size must not exceed 3840 px width and 2160 px height
* The maximum allowable size of an image was exceeded while changing the dimensions or format of the image.
