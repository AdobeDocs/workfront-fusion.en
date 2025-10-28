---
title: Veeva Vault modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Veeva Vault, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
---
# Veeva Vault modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use Veeva Vault, as well as connect it to multiple third-party applications and services.

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
   <td role="rowheader">Adobe Workfront Fusion license</td> 
   <td>
   <p>Operation-based: No Workfront Fusion license requirement</p>
   <p>Connector-based (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

To use Veeva Vault modules, you must have a Veeva Vault account.

## Veeva Vault modules and their fields

When you configure Veeva Vault modules, Workfront Fusion displays the fields listed below. Along with these, additional Veeva Vault fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Document

* [Create a single document](#create-a-single-document)
* [Create multiple documents](#create-multiple-documents)
* [Delete a single document](#delete-a-single-document)
* [Export documents](#export-documents)
* [Get a single document](#get-a-single-document)
* [Initiate user action](#initiate-user-action)
* [List documents](#list-documents)
* [Retrieve document export results](#retrieve-document-export-results)
* [Update multiple documents](#update-multiple-documents)
* [Update a single document](#update-a-single-document)

#### Create a single document

This module creates a single document, binder, or template.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to create a document, binder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Select fields</p> </td> 
   <td> <p>Select the fields that you want to enter data for, then enter the data into those fields.</td> 
  </tr> 
 </tbody> 
</table>

#### Create multiple documents

This module creates multiple documents or templates using a CSV file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
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

#### Delete a single document

This module deletes a single document, binder, or template.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to delete a document, binder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document ID / Binder ID / Template name</p> </td> 
   <td> <p>Select the fields that you want to delete.</td> 
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
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to delete a document, binder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Source</p> </td> 
   <td> <p>Enable this option to include source files in the export.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Renditions</p> </td> 
   <td> <p>Enable this option to include renditions files in the export.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>All versions</p> </td> 
   <td> <p>Enable this option to include all versions of the document files in the export.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Text</p> </td> 
   <td> <p>Enable this option to include source document text in the export.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Get a single document

This module retrieves metadata for a single document, binder, or template.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to retrieve data for a document, binder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document ID / Binder ID / Template name</p> </td> 
   <td> <p>Select the fields that you want to retrieve data for.</td> 
  </tr> 
 </tbody> 
</table>

#### Initiate user action

This module initiates actions on documents and binder, such as sending a document for review or changing its state.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to perform an action on a document or a binder.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document / Binder</p> </td> 
   <td> <p>Select the document or binder that you want to perform the action on.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document version/ Binder version</p> </td> 
   <td> <p>Select the document or binder that you want to perform the action on.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Action</p> </td> 
   <td> <p>Select the action to perform on the document or binder.</td> 
  </tr> 
 </tbody> 
</table>

#### List documents

This module lists all documents of the selected type.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to list documents, binders, or templates.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

#### Retrieve document export results

This module returns the results of a previously requested document export.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Job ID</p> </td> 
   <td> <p>Enter or map the ID of the job that you want to return results for. </p> </td> 
  </tr> 
  </tbody> 
</table>

#### Update multiple documents

This module updates multiple documents or templates using a CSV file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
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

#### Update a single document

This module updates a single document, binder, or template.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to create a document, document version, binder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID / Name</p> </td> 
   <td> <p>If you are updating a template, enter a new name for the template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>New template Name</p> </td> 
   <td> <p>Enter or map the ID or name of the object that you want to update.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>Select fields</p> </td> 
   <td> <p>Select the fields that you want to enter data for, then enter the data into those fields.</td> 
  </tr> 
 </tbody> 
</table>

### Object



#### List objects

This module retrieves all Vault objects in the authenticated Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Retrieve localized labels</p> </td> 
   <td> <p>Select Yes to retrieve localized (translated) strings for the label and label_plural object fields.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

### Other

* [Make a custom API call](#make-a-custom-api-call)
* [Make a VQL query](#make-a-vql-query)
* [Read logs](#read-logs)

#### Make a custom API call

This action module makes a custom call to the Veeva Vault API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Enter a path relative to <code>baseurl/api/v</code>.  For example: <code>/objects/documents</code>. Do not include <code>baseurl/api/v/</code>, as it is already included.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Method</td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Headers</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion adds the authorization headers for you.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Query String</td> 
   <td> <p>Add the query for the API call in the form of a standard JSON object.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Body</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Make a VQL query

This module makes a query using Vault Query Language (VQL).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
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

#### Read logs

This module returns data from audit trails

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Audit type</p> </td> 
   <td> <p>Select the audit type that you want to retrieve data for.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Start date</p> </td> 
   <td> <p>Enter or map the start date for the audits that you want to retrieve.</p><p>For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>End date</p> </td> 
   <td> <p>Enter or map the end date for the audits that you want to retrieve.</p><p>For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Result URL </p> </td> 
   <td> <p>Select CSV if you want to get URL to download a CSV of the result.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>


