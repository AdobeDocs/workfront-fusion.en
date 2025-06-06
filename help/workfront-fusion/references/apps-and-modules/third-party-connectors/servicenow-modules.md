---
title: ServiceNow modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL ServiceNow], as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
---
# [!DNL ServiceNow] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL ServiceNow], as well as connect it to multiple third-party applications and services.

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

To use [!DNL ServiceNow] modules, you must have a [!DNL ServiceNow] account.

## ServiceNow API information

The ServiceNow connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td>https://&#123;&#123;connection.instance&#125;&#125;/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## Connect [!DNL ServiceNow] to [!DNL Workfront Fusion]

To create a connection for your [!DNL ServiceNow] modules:

1. Click **[!UICONTROL Add]** next to the [!UICONTROL Connection] box when you begin configuring the first [!DNL ServiceNow] module.
1. Enter the following:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Enter a name for the new [!DNL ServiceNow] connection.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td>Select whether you are connecting to a production or non-production environment.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>Select whether you are connecting to a service account or a personal account. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Username]</p> </td> 
      <td>Enter your [!DNL ServiceNow] username.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>Enter your ServiceNow password.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Instance]</p> </td> 
      <td> <p>Enter the address of your [!DNL ServiceNow] account without <code>https://</code> (usually <code>&lt;company>.service-now.com</code>).</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Continue** to save the connection and return to the module.

   <!--Markdown placeholder-->

## [!UICONTROL ServiceNow] modules and their fields

When you configure [!DNL ServiceNow] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL ServiceNow] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* If a custom record is selected in a "[!UICONTROL Record type]" field, it may take some time to load the custom fields.
>
>* If there are no custom records, the "Record type" field dropdown will be empty.

### Triggers

#### [!UICONTROL Watch records]

This trigger module activates a scenario when a record is created or updated.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your ServiceNow account to [!DNL Workfront Fusion], see <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connect [!DNL ServiceNow] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Select whether the table you want to watch is a custom table or a standard table.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Select the type of record that you want to watch.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Select the type of values that you want to display.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Select the fields that you want the module to output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Select whether you want to watch new records or updated records.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Deactivate a User]](#deactivate-a-user)
* [[!UICONTROL Delete a record]](#delete-a-record)
* [[!UICONTROL Download an attachment]](#download-an-attachment)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Upload an attachment]](#upload-an-attachment)
* [[!UICONTROL Update a record]](#update-a-record)

#### [!UICONTROL Create a record]

This action module creates a new [!DNL ServiceNow] record.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your ServiceNow account to [!DNL Workfront Fusion], see <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connect [!DNL ServiceNow] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Select whether you want to create a record in a custom table or a standard table.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Select the type of [!DNL ServiceNow] record that you want the module to create. You can then fill in the available fields for this record type.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

This action module lets you make a custom authenticated call to the [!DNL ServiceNow] API. This way, you can create a data flow automation that can't be accomplished by the other [!DNL ServiceNow] modules.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your ServiceNow account to [!DNL Workfront Fusion], see <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connect [!DNL ServiceNow] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Relative URL]</td> 
   <td> Enter a path relative to <code>https://&ltinstance_url&gt/api/</code>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Add the query for the API call in the form of a standard JSON object.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Deactivate a User]

This action module deactivates a user in [!DNL ServiceNow] by using the system ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your ServiceNow account to [!DNL Workfront Fusion], see <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connect [!DNL ServiceNow] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User System ID]</td> 
   <td> Enter or map the unique [!DNL ServiceNow] ID of the user that you want the module to deactivate.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a record]

This action module deletes an incident or a user.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your ServiceNow account to [!DNL Workfront Fusion], see <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connect [!DNL ServiceNow] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Select whether you want to delete an incident or a user.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>Enter or map the unique [!DNL ServiceNow] ID of the record that you want the module to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download an attachment]

This action module downloads an attachment in a [!DNL ServiceNow] record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your ServiceNow account to [!DNL Workfront Fusion], see <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connect [!DNL ServiceNow] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment System ID]</td> 
   <td> Enter or map the unique [!DNL ServiceNow] ID of the attachment that you want the module to download.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

This action module reads a [!DNL ServiceNow] record by using the system ID.

The module returns any standard fields associated with the record, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your ServiceNow account to [!DNL Workfront Fusion], see <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connect [!DNL ServiceNow] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>Enter or map the unique [!DNL ServiceNow] ID of the record that you want the module to read.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Select whether the record you want to read is in a custom table or a standard table.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Select the type of [!DNL ServiceNow] record that you want the module to read.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Select the type of values that you want to display.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Select the fields that you want the module to output.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

This action module creates a new [!DNL ServiceNow] record.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your ServiceNow account to [!DNL Workfront Fusion], see <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connect [!DNL ServiceNow] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>Enter or map the unique [!DNL ServiceNow] ID of the record that you want the module to update.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Select whether the record want to update is in a custom table or a standard table.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Select the type of [!DNL ServiceNow] record that you want the module to update. You can then fill in the available fields for this record type.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an attachment]

This action module uploads an attachment to a [!DNL ServiceNow] record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your ServiceNow account to [!DNL Workfront Fusion], see <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connect [!DNL ServiceNow] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table name]</td> 
   <td>Enter or map the name of the table where you want to upload the attachment.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>Enter or map the unique [!DNL ServiceNow] ID of the item where you want to upload the attachment.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Searches

#### [!UICONTROL Search for records]

This module searches for records using criteria you select.

The module returns any standard fields associated with the record, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your ServiceNow account to [!DNL Workfront Fusion], see <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connect [!DNL ServiceNow] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Select whether the table you want to search is a custom table or a standard table.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Select the type of record that you want to search for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Select whether you want the module to return all records that match the criteria, or only the first record to match it. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal count of records]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search type]</td> 
   <td> <p>Select what type of search you want the module to execute</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Advanced query]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Query]</p> <p>Enter the custom search query. For information on [!DNL ServiceNow] custom search queries, see the <a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">ServiceNow query documentation</a>.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Simple]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Criteria]</p> <p>Enter the criteria by which you want the module to search. </li> 
       <li> <p>[!UICONTROL Sort by]</p> <p>Indicate which field you want the module to sort results by, and whether they should be sorted ascending or descending.</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Select the type of values that you want to display.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Select the fields that you want the module to output.</td> 
  </tr> 
 </tbody> 
</table>
