---
title: Mapping overview
description: Mapping is the process of assigning a module's outputs, structured into items, to another module's input fields.
author: Becky
feature: Workfront Fusion
---
# Mapping overview

Mapping is the process of assigning a module's outputs to another module's input fields.

The operation of a module produces zero, one, or more bundles as its output. A bundle consists of one or more items.

You can map these items to fields in later modules.

When you click a field where you can insert a value outputted from a preceding module in a scenario, the mapping panel displays. Here, you can select the item that you want to map. A mapping can include one or more of the following:

* A single item
* Multiple items
* Static text
* Functions

>[!BEGINSHADEBOX]

**Examples**:

Single item

![](assets/map-single.png)

Multiple items with text

![](assets/map-multiple-with-text.png)

Function with multiple items and text

![](assets/map-formula-with-text.png)


>[!ENDSHADEBOX]


For instructions on mapping, see the articles under [Map data](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md).

<!--## Access requirements

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] plan*</td> 
   <td> <p>[!DNL Pro] or higher</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] license*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] license**</td> 
   <td>
   <p>Current license requirement: No [!DNL Workfront Fusion] license requirement.</p>
   <p>Or</p>
   <p>Legacy license requirement: [!UICONTROL [!DNL Workfront Fusion] for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Current product requirement: If you have the [!UICONTROL Select] or [!UICONTROL Prime] [!DNL Adobe Workfront] Plan, your organization must purchase [!DNL Adobe Workfront Fusion] as well as [!DNL Adobe Workfront] to use functionality described in this article. [!DNL Workfront Fusion] is included in the [!UICONTROL Ultimate] [!DNL Workfront] plan.</p>
   <p>Or</p>
   <p>Legacy product requirement: Your organization must purchase [!DNL Adobe Workfront Fusion] as well as [!DNL Adobe Workfront] to use functionality described in this article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

To find out what plan, license type, or access you have, contact your [!DNL Workfront] administrator.

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->


>[!NOTE]
>
>The outputs from modules wrapped between an [!UICONTROL Iterator] and [!UICONTROL Aggregator] are not accessible beyond the [!UICONTROL Aggregator] module.

## The mapping panel

When you click into a field where you can map data, the mapping panel opens.

The first tab ![](assets/toolbar-icon-functions-you-map-from-other-modules.png) displays the items that you can map from other modules.

The other tabs include functions, operators, and keywords that you can use to create formulas. These are sorted into different tabs based on the type of data they handle.

For more information on function tabs, see [Function overview](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md).

For more information on mapping items using functions, see [Map items using functions](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

## Collections

Items can contain multiple values of various types. These are collection-type items.

Collection-type bundles display `(Collection)` next to the bundle label in the module output. 

![](assets/collection.png)

In most cases, you map the collection's elements instead of mapping the item that represents the whole collection.

To locate a collection's element in the mapping panel, click the arrow next to the collection.

![](assets/collection-dropdown.png)

For more information about collections, see [Item data types](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

For instructions on mapping collections, see [Map an item](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md#map-an-item) in the article Map information from one module to another.

## Arrays

Items can contain multiple values of the same type. These are array-type items.

Array-type bundles display `(Array)` next to the bundle label in the module output.

In the mapping panel, arrays display with square bracksts. You can identify an array type item by the square brackets at the end of the item's label. To locate specific array element in the mapping panel, click the arrow next to the array.

![](assets/array.png)

For information and instructions about mapping arrays and array elements, see [Map arrays and array elements](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).
