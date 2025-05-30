---
title: JSON modules
description: The Adobe Workfront Fusion JSON app provides modules to process data in JSON format so that Adobe Workfront Fusion can further work with the data content, or create new JSON content.
author: Becky
feature: Workfront Fusion
exl-id: f8b281c5-bb63-4412-98c5-d82f45f8eafc
---
# [!UICONTROL JSON] modules

The [!DNL Adobe Workfront Fusion] [!UICONTROL JSON] app provides modules to process data in JSON format so that [!DNL Adobe Workfront Fusion] can further work with the data content, or create new JSON content.

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

## Considerations when parsing JSON

* [Data structure](#data-structure) 
* [Collection vs. Array](#collection-vs-array)

### Data structure

The Data structure describes how the JSON data is organized and enables the mapping of individual JSON items to other modules in your scenario. If you don't provide the Data structure, you may manually execute the module and [!DNL Workfront Fusion] will build the structure from the provided JSON:

1. Add the [!UICONTROL Parse JSON] module to a scenario.
1. In the **[!UICONTROL JSON String]** field, enter the JSON from which you want to build a data structure.
1. Do not connect other modules to the [!UICONTROL Parse JSON] module yet. Because [!DNL Workfront Fusion] does not yet know the structure of the JSON data, it is not yet possible to map data from the [!UICONTROL Parse JSON] module to other modules in your scenario.
1. Manually run the scenario. This allows the [!UICONTROL Parse JSON] module to identify the JSON structure from the JSON you have provided.
1. You can now connect following modules. The items from the Parse JSON module are now available for mapping.

For more information, see [Data structures in [!UICONTROL Adobe Workfront Fusion]](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

### Collection vs. Array

If the JSON string field contains a collection `{ ... }`, The output is a single bundle containing the items of the collection.

>[!BEGINSHADEBOX]

**Example:**

```
{
    "name" : "Peter",

    "ID" : 1>}
```


![JSON collection](/help/workfront-fusion/references/apps-and-modules/assets/json-collection.png)

>[!ENDSHADEBOX]

If the JSON string field contains an array `[ ... ]`, the output is a series of bundles. each bundle contains one element of the array.

>[!BEGINSHADEBOX]

**Example:** 

```
[
  {
    "name" : "Peter",
    "ID" : 1
  },

  {
    "name" : "Mike",
    "ID" : 2
  }
]
```

![JSON array](/help/workfront-fusion/references/apps-and-modules/assets/json-array.png)

>[!ENDSHADEBOX]

## [!UICONTROL JSON] modules and their fields

When you configure [!DNL JSON] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional JSON fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Convert JSON to XML](#convert-json-to-xml) 
* [Parse JSON](#parse-json) 
* [Create JSON](#create-json) 
* [Transform JSON](#transform-json)

### Aggregators

#### [!UICONTROL Aggregate to JSON]

This aggregator module aggregates output from a previous module into JSON. 

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module] </td> 
   <td> <p>Select the module that outputs the data that you want to aggregate to JSON.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data structure]</td> 
   <td> <p>Select the data structure that you want to use to create JSON. The data structure determines what other fields are available in this module. For more information, see <a href="#data-structure" class="MCXref xref">Data structure</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Indentation]</td> 
   <td> <p> Select whether you want to indent the JSON using tabs, two spaces, or four spaces.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by]</td> 
   <td>Define an expression that you want to group the aggregated output by. This expression can contain one or more mapped items. The aggregated data is then separated into groups using this expression's value. Each group outputs as a separate bundle with a key (the evaluated expression) and a value (the aggregated text). You can use the key as a filter in subsequent modules.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Enable this option to stop the scenario when there are no results.</td> 
  </tr> 
 </tbody> 
</table>

### Transformers

* [Convert JSON to XML](#convert-json-to-xml) 
* [Create JSON](#create-json) 
* [Parse JSON](#parse-json) 
* [Transform JSON](#transform-json)

#### [!UICONTROL Convert JSON to XML]

This action module converts a JSON string to XML.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON string] </td> 
   <td> <p>Enter or map the JSON that you want to convert into XML.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create JSON]

This action module creates JSON from a data structure.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Data structure</td> 
   <td> <p>Select the data structure that you want to use to create JSON. For more information, see <a href="#data-structure" class="MCXref xref">Data structure</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Indentation</td> 
   <td> <p>Select the indentation you want to use for this JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Parse JSON]

This action module parses a JSON string into a data structure, which allows you to access the data inside the JSON string.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data structure]</td> 
   <td> <p>Select the data structure that you want to use to create JSON. For more information, see <a href="#data-structure" class="MCXref xref">Data structure</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON string] </td> 
   <td> <p>Enter or map the JSON that you want to parse.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Transform JSON]

This action module transforms an object into a json string.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Indentation</td> 
   <td> <p>Select the indentation you want to use for this JSON.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object]</td> 
   <td> <p>Enter or map the object that you want to transform into JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Transforming data records to JSON

>[!BEGINSHADEBOX]

**Example:** The following example shows how to transform data records from [!DNL Google Sheets] to JSON format:

1. Place the [!DNL Google Sheets] > [!UICONTROL Select rows] module in your scenario to fetch the data. Set up the module to retrieve rows from your [!DNL Google] spreadsheet. Set the&#x200B;**[!UICONTROL Maximum number of returned rows]** to a small number, but larger than one for testing purposes (Example, three). Execute the [!DNL Google Sheets] module by right-clicking it and choosing "**[!UICONTROL Run this module only]**." Verify the output of the module.

1. Connect the [!UICONTROL Array Aggregator] module after the [!DNL Google Sheets] module. In the module's setup choose the [!DNL Google Sheets] module in the **[!UICONTROL Source node]** field. Leave the other fields as they are for the moment.

1. Connect [!UICONTROL JSON] > [!UICONTROL Create JSON] module after the [!UICONTROL Array Aggregator] module. The module's setup requires a Data structure that describes the JSON format. Click **[!UICONTROL Add]** to open the Data structure setup. The easiest way to create this Data structure is to generate it automatically from a JSON sample. Click **[!UICONTROL Generator]** and paste your JSON sample to the **[!UICONTROL Sample data]** field:

     **Example:** 

     ```
     {
     "books": [
     {
     "id": "ID",
     "title": "Title",
     "author": "Author"
     }
     ]
     }
     ```

1. Click **[!UICONTROL Save]**. The [!UICONTROL Specification] field in the Data structure now contains the generated structure.
1. Change the name of your Data structure to something more specific and click **[!UICONTROL Save]**. A field corresponding to the root array attribute appears as a mappable field in the JSON module's setup.

1. Click the **[!UICONTROL Map]** button next to the field and map the `Array[]` item from the Array aggregator output to it.

1. Click **[!UICONTROL OK]** to close the [!UICONTROL JSON] module's setup.

1. Open the setup of the [!UICONTROL Array Aggregator] module. Change the **[!UICONTROL Target structure]** from [!UICONTROL Custom] to the [!UICONTROL JSON] module's field corresponding to the root array attribute. Map items from the [!DNL Google Sheets] module to the appropriate fields.

1. Click **[!UICONTROL OK]** to close the [!UICONTROL Array Aggregator] module's setup.

1. Run the scenario.

     The [!UICONTROL JSON] module outputs the correct JSON format. 

1. Open the setup of the [!DNL Google Sheets] module and increase the [!UICONTROL Maximum number of returned rows] number to be larger than the number of rows in your spreadsheet to process all the data.

>[!ENDSHADEBOX]

## Troubleshooting

### Cannot map data from the [!UICONTROL Parse JSON] module

Make sure that the JSON content is properly mapped into the [!UICONTROL Parse JSON] module and that the data structure is correctly defined. For more information, see [Transforming data records to JSON](#transforming-data-records-to-json) in this article.

### Module fails when using conditional statements in JSON

When using conditional statements such as `if` in your JSON, put the quotation marks outside of the conditional statement.

>[!BEGINSHADEBOX]

**Example:**  

![Quotes in JSON](/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png)

>[!ENDSHADEBOX]
