---
title: Google Forms modules
description: The [!DNL Adobe Workfront Fusion Google Forms] modules allow you to monitor, select, add, update or delete responses on your Google Forms.
author: Becky
feature: Workfront Fusion
exl-id: dc017957-c0f8-4206-916f-21ccda346fb9
---
# [!DNL Google Forms] modules

The [!DNL Adobe Workfront Fusion] [!DNL Google Forms] modules allow you to monitor, select, add, update or delete responses on your [!DNL Google Forms].

In order to use [!DNL Google Docs] with [!DNL Adobe Workfront Fusion], it is necessary to have a [!DNL Google] account. If you don't have a [!DNL Google] account yet, you can create one at the [!DNL Google] Account help page.

For instructions on creating a scenario, see the articles under [Create scenarios: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

To use [!DNL Google Forms] modules, you must have a [!DNL Google] account.

## Google Forms API information

The Google Forms connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## Creating a Spreadsheet from the Form

To work with your form responses, you must first create the response spreadsheet.

1. Open your form.
1. Go to the **[!UICONTROL Responses]** tab.
1. Click the **[!UICONTROL Create Spreadsheet]** icon ![Spreadsheet icon](/help/workfront-fusion/references/apps-and-modules/assets/spreadsheet-icon.png).

1. Select whether you want to create a new spreadsheet or an existing spreadsheet
1. Click **[!UICONTROL Create]**.

## [!DNL Google Forms] modules and their fields

When you configure [!DNL Google Forms] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Google Forms] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Actions](#actions)
* [Searches](#searches)

### Triggers 

#### [!UICONTROL Watch Responses]

Watches the form for new responses.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Google] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Select the spreadsheet that contains the responses from the form that you want to watch for new responses.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Select the sheet that contains the form responses.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row with headers]</td> 
   <td>Specify the header row of the table. The default row is <code>A1:Z1</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>Specify how you want the values to be rendered in the output.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong> </p> <p>Values are calculated and formatted in the reply according to the cell's formatting. Formatting is based on the spreadsheet's locale, not the requesting user's locale. For example, if <code>A1</code> is <code>1. 23</code> and <code>A2 </code>is <code>=A1</code> and formatted as currency, then <code>A2</code> returns <code>$1. 23</code> .</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>Values are calculated, but not formatted in the reply. For example, if <code>A1</code> is <code>1. 23</code> and <code>A2 </code>is <code>=A1</code> and formatted as currency, then <code>A2</code> returns the number <code>1. 23</code> .</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>Values are not calculated. The reply includes the formulas. For example, if <code>A1</code> is <code>1. 23</code> and <code>A2 </code>is <code>=A1</code> and formatted as currency, then <code>A2</code> returns <code>=A1</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Date and time render option]</td> 
   <td>Select how you want dates, times, and duration to be represented in the output. This field is ignored if [!UICONTROL Value Render Option] is set to [!UICONTROL Formatted Value].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p> Set the maximum number of responses that [!DNL Workfront Fusion] works with during one cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions 

* [[!UICONTROL Add a Response]](#add-a-response)
* [[!UICONTROL Delete a Response]](#delete-a-response)
* [[!UICONTROL Update a Response]](#update-a-response)

#### [!UICONTROL Add a Response] 

This module appends a new response to the bottom of the form's spreadsheet.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Google] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Select the spreadsheet that contains the sheet where you want to add a response.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Select the sheet that contains the form responses.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Enter the desired values to the sheet columns. Columns are available based on the sheet.</p> <p>For the [!UICONTROL Timestamp] column, use the following value:</p><pre>formatDate(now;DD/MM/YYYY HH:mm;UTC)</pre> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> The values that the user enters are not parsed and are stored as-is. </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>The values are parsed as if the user typed them into the UI. Numbers remain numbers, but strings may be converted to numbers, dates, or other formats following the same rules that are applied when entering text into a cell via the [!DNL Google Sheets] UI.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Insert data option]</td> 
   <td> <p>Specify how existing data is changed when new data is input. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>The new data overwrites existing data in the areas where it is written. Adding data to the end of the sheet inserts new rows or columns so the data can be written.</p> </li> 
     <li> <p><strong>[!UICONTROL Insert rows]</strong></p> <p>Rows are inserted for the new data.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Response]

This module deletes a selected response.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Google] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Select the spreadsheet that contains the sheet where you want to delete a response.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Select the sheet that contains the form responses.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>Enter or map the number of the row you want to delete.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Response]

This module updates the selected response.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Google] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Select the spreadsheet that contains the sheet where you want to update a response.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Select the sheet that contains the form responses.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>Enter or map the number of the row you want to update.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Enter the new values for the desired columns. Columns are available based on the sheet.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> The values that the user enters are not parsed and are stored as-is. </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>The values are parsed as if the user typed them into the UI. Numbers remain numbers, but strings may be converted to numbers, dates, or other formats following the same rules that are applied when entering text into a cell via the [!DNL Google Sheets] UI.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Searches 

* [[!UICONTROL Search Responses]](#search-responses)
* [[!UICONTROL Search Responses (Advanced])](#search-responses-advanced)

#### [!UICONTROL Search Responses] 

This module returns responses matching the given criteria.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
    <td>Connection</td>
   <td> <p>For instructions about connecting your [!DNL Google] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>Select the form you want to search in.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Sheet] </td>
   <td> <p>Select the sheet that contains the form responses.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Column range]</td>
   <td> <p> Select the column range you want to search.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Define the filter you want to search responses responses by.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Sort Order] </td>
   <td> <p>Select whether to sort returned responses in ascending or descending order.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Order By]</td>
   <td> <p> Select the column you want to order returned responses by.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>Specify how you want the values to be rendered in the output.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong></p> <p>Values are calculated and formatted in the reply according to the cell's formatting. Formatting is based on the spreadsheet's locale, not the requesting user's locale. For example, if <code>A1</code> is <code>1. 23</code> and <code>A2 </code>is <code>=A1</code> and formatted as currency, then <code>A2</code> returns <code>$1. 23</code> .</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>Values are calculated, but not formatted in the reply. For example, if <code>A1</code> is <code>1. 23</code> and <code>A2 </code>is <code>=A1</code> and formatted as currency, then <code>A2</code> returns the number <code>1. 23</code> .</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>Values are not calculated. The reply includes the formulas. For example, if <code>A1</code> is <code>1. 23</code> and <code>A2 </code>is <code>=A1</code> and formatted as currency, then <code>A2</code> returns <code>=A1</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Date and time render option]</td>
    <td>Select how you want dates, times, and duration to be represented in the output. This field is ignored if [!UICONTROL Value Render] Option is set to Formatted Value. </td>
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Maximum number of returned responses]</td>
   <td> <p> Set the maximum number of responses that [!DNL Workfront Fusion] returns during one cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Responses (Advanced)] 

This module performs a search using the [[!DNL Google Charts Query Language]](https://developers.google.com/chart/interactive/docs/querylanguage). This module does not return a row number.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
   <td> <p>For instructions about connecting your [!DNL Google] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>Select the spreadsheet that contains the sheet you want to search.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Sheet]</td>
   <td> <p> Select the sheet that contains the form responses.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Define the search query using the <a href="https://developers.google.com/chart/interactive/docs/querylanguage">[!DNL Google Charts Query Language]</a>.</p> <p>Example: <code>select * where C = "John"</code> retrieves all values for the row where the C column is "John".</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Maximum number of returned rows]</td>
   <td> <p> Set the maximum number of responses that [!DNL Workfront Fusion] returns during one cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>
