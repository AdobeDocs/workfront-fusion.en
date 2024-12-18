---
title: Math variables
description: The following math variables are available in the [!DNL Adobe Workfront Fusion mapping] panel.
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
---
# Math variables

## Access requirements

You must have the following access to use the functionality in this article:

<table style="table-layout:auto"> 
 <col>  
 <col>  
 <tbody>  
  <tr>  
   <td role="rowheader">[!DNL Adobe Workfront] package</td>  
   <td> <p>Any</p> </td>  
  </tr>  
  <tr data-mc-conditions="">  
   <td role="rowheader">[!DNL Adobe Workfront] license</td>  
   <td> <p>New: [!UICONTROL Standard]</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p> </td>  
  </tr>  
  <tr>  
   <td role="rowheader">[!DNL Adobe Workfront Fusion] license**</td>  
   <td> 
   <p>Current: No [!DNL Workfront Fusion] license requirement.</p> 
   <p>Or</p> 
   <p>Legacy: Any </p> 
   </td>  
  </tr>  
  <tr>  
   <td role="rowheader">Product</td>  
   <td> 
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] Plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] is included.</li></ul> 
   <p>Or</p> 
   <p>Current: Your organization must purchase [!DNL Adobe Workfront Fusion].</p> 
   </td>  
  </tr> 
 </tbody>  
</table>  

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md). 

For information about Adobe Workfront Fusion licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## pi

Represents the mathematical symbol $\pi$.

## [!UICONTROL random]

Returns a floating-point pseudo-random number in the range [`0`,`1`] (inclusive of `0`, but not `1`).

Use the following formula to generate an integer pseudo-random number in the range [`min`,`max`] (inclusive of both `min` and `max`):

![](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
