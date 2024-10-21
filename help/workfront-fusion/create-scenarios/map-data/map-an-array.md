---
title: Map arrays and array elements
description: You can map an array or individual array elements to a module field in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
---
# Map arrays and array elements

<!--EDIT ME-->

An array is a special type of item that can contain the following:

* One or more text values (simple array)
* One or more collections of the same type (complex array)

>[!INFO]
>
>**Example:** The [!UICONTROL Watch emails] module returns an array of attachments for every email. Every attachment represents a collection that may contain a name, content, size, and so on.

For more information, see [Item data types in [!DNL Adobe Workfront Fusion]](../../workfront-fusion/mapping/item-data-types.md).

## Access requirements

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

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).

## Map an array

1. Click the button located in the target field.

   >[!INFO]
   >
   >  **Example:** For the example above, you would click the [!UICONTROL Add an attachment] button for an email.
   >
   >![](assets/add-an-attachment-button-350x152.jpg)

1. In the box that displays, enter the item.

   The panel allows you to map fields in the same way as with any other type of item. If you do not want to fill in each item separately, but want to map another array into the target field, use the [!UICONTROL Map] button. In this case, make sure that both arrays (the source array and the target array) have the same structure.

   You can add any number of items to an array.

You can divide an array into individual bundles using an iterator. Fore more information, see [[!UICONTROL Iterator] module in [!DNL Adobe Workfront Fusion]](../../workfront-fusion/modules/iterator-module.md).



## Map array elements


### Map array elements by number

Array elements display as a number in square brackets after the array name.

![](assets/map-array-1st-element.png)

The number in the square brackets is an index that determines which element of the array will be used. It is set to 1 by default, which represents the first element of the array.

To map a different element, click on the square brackets and enter the index of the element you want to map. 

>[!NOTE]
>
>Array indexing in Workfront Fusion starts from 1. 

![](assets/access-another-element.png)

### Map an array's element with a given key

Some arrays contain collections with key-value items such as metadata, attributes, and so on. To use one of these values, you can look up an element by its given key value and obtain the corresponding value from the value item. We recommend using a formula employing a combination of the `map()` and `get()` functions.

The following is a detailed breakdown of the formula:

1. The first parameter of the `map()` function is the whole array item.
1. The second parameter is the raw name of the value item. To obtain the raw name, hover over the item in the [!UICONTROL mapping] panel:

   ![](assets/obtain-raw-name-350x124.png)

   >[!NOTE]
   >
   >All parameters are case sensitive. Even though in this particular example the item's label differs from its raw name only in capitalization, it is necessary to use the raw name, which is all lowercase value in contrast to the label Value.

1. The 3rd parameter is the raw name of the key item:

   ![](assets/3rd-parameter-350x166.png)

1. The 4th parameter is the given key value.

Because the `map()` function returns an array (as there could be more elements with the given key value), it is necessary to apply the `get()` function to get its first element:

* The 1st parameter of the `get()` function is the result of the `map()` function.

* The 2nd parameter is the element's index - one.

For more information about the `map()` function, see [Array functions](../../workfront-fusion/functions/array-functions.md).

For more information about the `get()` function, see [General functions](../../workfront-fusion/functions/general-functions.md).

>[!BEGINSHADEBOX]

The following example shows the output of the [!DNL Jira] App.

![](assets/output-of-jira-app-350x100.png)

In this example, we get a file name from an array of attachments for the specific attachment with an ID of 10108.

The output from [!DNL Jira] looks like this:

![](assets/output-from-jira-350x261.png)

>[!ENDSHADEBOX]

## Converting elements to a series of bundles

Arrays can be converted to a series of bundles using the [!UICONTROL Iterator] module. For more information, see [[!UICONTROL Iterator] module](../../workfront-fusion/modules/iterator-module.md).

![](assets/series-of-bundles-350x169.png)