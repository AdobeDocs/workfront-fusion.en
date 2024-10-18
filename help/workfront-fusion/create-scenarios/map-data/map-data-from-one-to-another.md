---
title: Map information from one module to another
description: Mapping is the process of assigning a module's outputs, structured into items, to another module's input fields.
author: Becky
feature: Workfront Fusion
---
# Map information from one module to another

Mapping is the process of assigning a module's outputs to another module's input fields.

The mapping panel displays when you click a field where you can insert a value outputted from a preceding module in a scenario. 

You can also create a formula using any combination of functions and mapped items from the mapping panel with static text that you type. These elements can be nested inside each other.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan</td> 
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

<!--<!--For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md).-->-->

<!--<!--For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->-->

+++

## Map an item

After you have created a sequence of modules by linking two or more of them, each module can process values of items outputted by the modules that precede it.

To assign output items to a module's input fields:

1. Click on the module that should process the output of the preceding module or modules.
1. In the Module settings panel that displays, click a field where you want to use the value of an item outputted from a preceding module.

   The mapping panel opens.

1. (Optional) To search for a particular field in the mapping panel, click the mapping panel search bar and type in the term you want to search for. Click the field when it appears in the list.

   Search results contain the search term and are not case sensitive.
1. Click an item from the mapping panel to insert it into the field.

<!--For more information, see [Configure a module's settings in [!DNL Adobe Workfront Fusion]](../../workfront-fusion/modules/configure-a-modules-settings.md).-->

