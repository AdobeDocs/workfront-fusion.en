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

>[!IMPORTANT]
>
>BECKY CHECK ME: This article is a skeleton, created from a screenshot of the module picker. The introduction, Connect section, and the fields for each module below all need to be confirmed with engineering before this is published.

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

>[!IMPORTANT]
>
>BECKY CHECK ME: Confirm the connection type and fields for this connector. The steps below are a placeholder.

1. In any Workfront Fusion module, click **[!UICONTROL Add]** next to the Connection field.
1. Fill in the required fields.
1. Click **[!UICONTROL Continue]** to save the connection and return to the module.

## Workfront Fusion modules and their fields

When you configure Workfront Fusion modules, Workfront Fusion displays the fields listed below. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Export](#export)
* [Misc](#misc)
* [Uncategorized](#uncategorized)

### Actions

* [Create a record](#create-a-record)
* [Delete a record](#delete-a-record)
* [List records](#list-records)
* [Read a record](#read-a-record)
* [Update a record](#update-a-record)

#### Create a record

Creates a specified record.

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

#### Delete a record

Deletes a specified record.

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

#### List records

Returns a paged list of records using cursor-based paging and property filters.

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

#### Read a record

Gets a specified record.

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
 </tbody> 
</table>

### Export

#### Export activity logs

Exports activity logs.

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

### Misc

* [Get queue statistics for a hook](#get-queue-statistics-for-a-hook)
* [List scenarios for a connection](#list-scenarios-for-a-connection)
* [List the Fusion regions and organizations](#list-the-fusion-regions-and-organizations)

#### Get queue statistics for a hook

Returns queue statistics for the specified hook: the number of events currently queued, the queue limit, and whether the hook is enabled.

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

#### List scenarios for a connection

Returns a paginated list of scenarios that reference the given connection.

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

#### List the Fusion regions and organizations

Returns `{ region, organizationId }` for every Fusion organization the caller can access, read from the caller's IMS profile.

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

### Uncategorized

* [Clone a record](#clone-a-record)
* [Get record dependencies](#get-record-dependencies)

#### Clone a record

Creates a copy of the record.

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

#### Get record dependencies

Get the dependencies of the record.

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
