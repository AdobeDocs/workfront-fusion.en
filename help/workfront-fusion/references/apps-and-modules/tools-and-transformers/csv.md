---
title: CSV
description: The Adobe Workfront Fusion CSV modules let you create CSV files and parse CSV text from a received text value or a file.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
---
# CSV

The Adobe Workfront Fusion [!UICONTROL CSV] modules let you create CSV files and parse CSV text from a received text value or a file.

Because this is a transformer, these modules do not require a connection.

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

## [!UICONTROL Create CSV]

The [!UICONTROL Create CSV] Aggregator lets you create a csv text from received text values.

For more information on aggregators, see [Aggregator module](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Select the module that outputs the fields that you want to use to create the CSV.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Aggregated Fields]</td>
        <td>Select the fields you want to aggregate from the list of available fields.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Include headers in the first row]</td>
        <td>Select this option to include the headers in the result.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Group by]</td>
        <td>Enter the filter to group the results. For example, enter a date.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Stop processing after an empty aggregation]</td>
        <td>Select this option to stop the scenario when there are no results.</td>
    </tr>
</table>

## [!UICONTROL Create CSV (advanced)]

The [!UICONTROL Create CSV (advanced)] Aggregator lets you create a CSV text from received text values. It employs a data structure that defines the CSV columns in the resulting CSV file. Once defined, the columns appear as fields in the CSV module setup, and can be mapped to later module in the scenario.

For more information on aggregators, see [Aggregator module](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
        <td>Select the module that outputs the fields that you want to use to create the CSV.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>Select the data structure to aggregate the fields in the way you want. After defining the data structure, you can map the items to the corresponding fields.</p> <p>For more information, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Data structures</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include headers in the first row] </td> 
   <td>Select this option to include the headers in the result. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by] </td> 
   <td>Enter the filter to group the results. For example, enter a date. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation] </td> 
   <td>Select this option to stop the scenario when there are no results. </td> 
  </tr> 
 </tbody> 
</table>


>[!BEGINSHADEBOX]

**Example**:

This example shows how to export Google contacts to a CSV file with two columns called "Full Name" and "Email". The output bundle from the [!UICONTROL Google Contacts] > [!UICONTROL Get contacts from a group] module has the following structure. The email addresses are stored inside the <code>[!UICONTROL Emails[]]</code> item, which is an array of collections, each collection containing two items: <code>Label</code> and <code>Email</code>.
![Transforming](/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png)

The simple [!DNL Create CSV] module, offers a list of checkboxes corresponding to a bundle's top-level items. If you attempt to select <code>Full name</code> and <code>Emails</code> items, the [!UICONTROL Create CSV] module produces the following output, which may not be what you want:

```
"emails","fullName"
"[object Object]","Shon Winer"
"[object Object]","Lizeth Fulmore"
"[object Object]","Hilario Gullatt"
"[object Object]","Abby Eisenbarth"
```

Because the item <code>Full Name</code> is of simple type Text, it is exported as expected. The item <code>Emails</code>, which is of a complex type Array of Collections, is exported as [object Object], which is how Collections and Arrays are transformed to text by default. 

For more information, see [Item data types](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).


To export content of the <code>Email </code>item of the first collection of the <code>Emails[]</code> array instead, You must use the [!UICONTROL Create CSV (advanced)] module. This module allows you to define individual columns of your CSV file and map items to them, including the nested ones.

1. Insert the module [!UICONTROL Create CSV (advanced)] in a scenario.
1. Click the <strong>[!UICONTROL Add]</strong> button next to the [!UICONTROL Data structure] field to create a new data structure.
1. Enter a name for the data structure and click <strong>[!UICONTROL Add item]</strong> to add the individual columns. To export two columns: "Full Name" and "Email", the resulting Data structure would look like this:

   ![Google Contacts output](/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png)

1. After you have defined the data structure, fields corresponding to each individual column appear in the configuration of the [!UICONTROL Create CSV (advanced)] module so you can map the items. Take the first item from the <code>[!UICONTROL Emails[]]</code> array and map its item <code>Email </code>to the field/column Email:

   ![Create CSV Advanced module](/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png)

1. Execute the scenario. Because the item <code>Emails[1]: Email</code> mapped to column "Email" is of simple type Text, it exports correctly.

```
"Full Name","Email"
"Shon Winer","Shon@Winer.com"
"Lizeth Fulmore","Lizeth@Fulmore.com"
"Hilario Gullatt","Hilario@Gullatt.com"
"Abby Eisenbarth","Abby@Eisenbarth.com"
```

>[!ENDSHADEBOX]

## [!UICONTROL Parse CSV]

The [!UICONTROL Parse CSV] transformer lets you parse CSV text from a received text value or a file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of columns]</td> 
   <td>Specify the number of columns in the CSV file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV contains headers]</td> 
   <td> <p>Select this option if the first row of the CSV text contains headers.</p> <p>Note: The module does not use these headers to label the columns in the output. Instead, this field ensures that the headers are not included in the output data.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL delimiterType]</td> 
   <td> <p>Select the delimiter for the CSV file. The delimiter is the text character that indicates the boundary between separate values or fields.</p> 
    <ul> 
     <li>[!UICONTROL Comma]</li> 
     <li>[!UICONTROL Tab]</li> 
     <li> <p>[!UICONTROL Other]</p> <p>If you select [!UICONTROL Other], enter the delimiter character that the CSV file is using to separate values. You must enter exactly one character.<br></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve quotes inside unquoted field]</td> 
   <td>Enable this option to preserve quotes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV]</td> 
   <td>Enter or map the CSV file that you want to parse.<p>Note: <p>If your data comes in binary form (typically from a file), you must use the `toString()` function to convert the binary data to [!UICONTROL String]:</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png"></p></p></td> 
  </tr> 
 </tbody> 
</table>
