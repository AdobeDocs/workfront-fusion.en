---
title: Workfront Fusion modules
description: With the Workfront Fusion connector, you can manage your own Fusion organization from within a scenario, including records, hooks, scenarios, and connections.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# Workfront Fusion modules

With the Workfront Fusion connector, you can manage your own Fusion organization from within a scenario. Unlike other connectors, which connect Fusion to a third-party app or service, this connector lets a scenario call Fusion's own API, similar to how the Adobe Workfront connector lets a scenario manage Workfront.

For instructions on creating a scenario, see the articles under [Create scenarios: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Connect Workfront Fusion to Workfront Fusion

1. In any Workfront Fusion module, click **[!UICONTROL Add]** next to the Connection field.
1. Fill in the following fields:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection type]</td> 
      <td>Select the type of connection you want to create.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name]</td> 
      <td>Enter a name for the connection.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID]</td> 
      <td>Enter your [!DNL Adobe] [!UICONTROL Client ID]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td>Enter your [!DNL Adobe] [!UICONTROL Client Secret]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Organization ID]</td> 
      <td>Enter your [!DNL Adobe] IMS Organization ID.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Region]</td> 
      <td>Select the Fusion region for this connection.</td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.

## Workfront Fusion modules and their fields

When you configure Workfront Fusion modules, Workfront Fusion displays the fields listed below. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Export](#export)
* [Misc](#misc)

### Actions

* [Clone a record](#clone-a-record)
* [Create a record](#create-a-record)
* [Delete a record](#delete-a-record)
* [List records](#list-records)
* [Read a record](#read-a-record)
* [Update a record](#update-a-record)

#### Clone a record

This module makes a copy of the specified record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> Select the type of record that you want to clone. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Scenario ID</td> 
   <td> Enter or map the ID of the scenario that you want to clone. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name</td> 
   <td> Enter or map a name for the new scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### Create a record

This module creates a record with the specified data.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> Select the type of record that you want to create. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team ID</td> 
   <td> Enter or map the ID of the team that will own this record. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name</td> 
   <td> Enter or map a name for the new record.</td> 
  </tr> 
 </tbody> 
</table>

#### Delete a record

This module deletes a specified record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> Select the type of record that you want to delete. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Other fields</td> 
   <td>Enter values for any other fields. Available fields depend on the selected record type. </td> 
  </tr> 
 </tbody> 
</table>

#### List records

This module returns a paged list of records using cursor-based paging and property filters.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td>Select the type of record that you want to return a list of.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Property</td> 
   <td>For each property filter that you want to return results for, click <b>Add item</b> and enter the field, operator, and value that you want to filter for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Start</td> 
   <td>Enter the location where you want to start the returned results. This is used for pagination.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of records that you want the module to return for each execution cycle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Order by</td> 
   <td>Select the field that you want to order results by.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direction</td> 
   <td>Select whether you want to order results ascending or descending.</td> 
  </tr> 
 </tbody> 
</table>

#### Read a record

This module retrieves the specified record

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> Select the type of record that you want to delete. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Other fields</td> 
   <td>Enter values for any other fields. Available fields depend on the selected record type. </td> 
  </tr> 
 </tbody> 
</table>

#### Update a record

Updates a specified record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> Select the type of record that you want to update. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name</td> 
   <td> Enter or map a new name for the record.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td> Enter or map the ID of the record that you want to update. </td> 
  </tr> 
 </tbody> 
</table>

### Export

#### Export activity logs

This module exports activity logs.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">File type</td> 
   <td>Select the file format that you want to export logs into.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Property</td> 
   <td>For each property filter that you want to return results for, click <b>Add item</b> and enter the field, operator, and value that you want to filter for. You can also filter by whether or not the field exists.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Start</td> 
   <td>Enter the location where you want to start the returned results. This is used for pagination.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of records that you want the module to return for each execution cycle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Order by</td> 
   <td>Select the field that you want to order results by.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direction</td> 
   <td>Select whether you want to order results ascending or descending.</td> 
  </tr> 
 </tbody> 
</table>

### Misc

* [Get queue statistics for a hook](#get-queue-statistics-for-a-hook)
* [Get record dependencies](#get-record-dependencies)
* [List scenarios for a connection](#list-scenarios-for-a-connection)
* [List the Fusion regions and organizations](#list-the-fusion-regions-and-organizations)

#### Get queue statistics for a hook

This module returns queue statistics for the specified hook: the number of events currently queued, the queue limit, and whether the hook is enabled.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  <tr> 
   <td role="rowheader">Hook ID</td> 
   <td> Enter or map the ID of the hook that you want to return details for.</td> 
  </tr> 
 </tbody> 
</table>

#### Get record dependencies

This module gets the dependencies of the record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> Select the type of record that you want to retrieve dependencies for. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Scenario ID</td> 
   <td> Enter or map the ID of the record that you want to retrieve dependencies for. </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### List scenarios for a connection

This module returns a paginated list of scenarios that reference the given connection.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Connection ID</td> 
   <td>Enter or map the ID of the connection that you want to return scenarios for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Property</td> 
   <td>For each property filter that you want to return results for, click <b>Add item</b> and enter the field, operator, and value that you want to filter for. You can also filter by whether or not the field exists.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Start</td> 
   <td>Enter the location where you want to start the returned results. This is used for pagination.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of records that you want the module to return for each execution cycle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Order by</td> 
   <td>Select the field that you want to order results by.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direction</td> 
   <td>Select whether you want to order results ascending or descending.</td> 
  </tr> 
 </tbody> 
</table>

#### List the Fusion regions and organizations

This module returns the region and organization ID for every Fusion organization the connection can access, based on the credentials and access in the IMS user profile of the credentials used in the connection.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Workfront Fusion to Workfront Fusion, see <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connect Workfront Fusion to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
 </tbody> 
</table>





