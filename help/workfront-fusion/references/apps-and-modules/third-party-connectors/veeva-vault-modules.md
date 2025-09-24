---
title: Veeva Vault modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use [!UICONTROL Veeva Vault], as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
---
# [!DNL Veeva Vault] modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use [!UICONTROL Veeva Vault], as well as connect it to multiple third-party applications and services.

For instructions on creating a scenario, see the articles under [Create scenarios: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

## Access requirements

<!--UPDATE THIS-->

+++ Expand to view access requirements for the functionality in this article.

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

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

To use [!UICONTROL Veeva Vault] modules, you must have a [!UICONTROL Veeva Vault] account.

## Veeva Vault modules and their fields

When you configure [!DNL Veeva Vault] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Veeva Vault] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions]()
* [Searches]()

### Actions

#### Create multiple documents

This module creates multiple documents or templates using a CSV file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Veeva Vault] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to create templates or documents</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>File data</p> </td> 
   <td> <p>Map the CSV file that will be used to create the documents.</td> 
  </tr> 
 </tbody> 
</table>

#### Create single document

This module creates a single document, binder, or template.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Veeva Vault] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to create a document, bunder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Select fields</p> </td> 
   <td> <p>Select the fields that you want to enter data for, then enter the data into those fields.</td> 
  </tr> 
 </tbody> 
</table>

#### Delete single document

This module deletes a single document, binder, or template.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Veeva Vault] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to delete a document, bunder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document ID / Binder ID / Template name</p> </td> 
   <td> <p>Select the fields that you want to enter data for, then enter the data into those fields.</td> 
  </tr> 
 </tbody> 
</table>


#### Export documents

This module exports documents you specify, including sources, renditions, and text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!UICONTROL Veeva Vault] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to delete a document, bunder, or template.</p> </td> 
  </tr> 
  <tr> <!--Becky start here-->
   <td role="rowheader"><p></p> </td> 
   <td> <p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p></p> </td> 
   <td> <p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p></p> </td> 
   <td> <p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p></p> </td> 
   <td> <p></td> 
  </tr> 
 </tbody> 
</table>

#### Get single document

#### Initiate user action

#### Make a custom API call

#### Retrieve document export results

#### Update multiple documents

#### Update single document

#### VQL query

### Searches

#### List documents

#### List objects

#### Read logs

