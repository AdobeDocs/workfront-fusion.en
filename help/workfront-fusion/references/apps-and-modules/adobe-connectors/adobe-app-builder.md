---
title: Adobe App Builder module
description: The Adobe App Builder connector allows you to use custom functions in your scenarios.
author: Becky
feature: Workfront Fusion
exl-id: b9d7643e-febf-42e2-9ddc-8ec8eba98e7a
---
# Adobe App Builder module

You can create custom functions in the Functions area of Fusion. You then add these functions to your scenarios in the form of an Adobe App Builder module.

Because custom functions work through Adobe App Builder, your organization must have an Adobe App Builder license to use them.

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
   <td role="rowheader">Product</td> 
   <td>
   <p><ul><li>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li><li>You must have an Adobe App Builder license to use custom functions.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Adobe App Builder module

The only currently available Adobe App Builder module is Execute an action, which allows you to use a previously configured custom JavaScript function.

For instructions on configuring a custom function, see [Map data using custom functions](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

### Execute an action

This module executes a previously configured custom function.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Select the connection that contains the custom function that you want to run. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Select the custom function that you want to run.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parameters] </td> 
   <td>Enter the values for the function parameters. Available parameters are based on the parameters configured when the function was created.<p>If a parameter has a default value, you will not see it in the field, but can override it by entering or mapping a value into the field.</p></td> 
  </tr> 
   </tbody> 
</table>


