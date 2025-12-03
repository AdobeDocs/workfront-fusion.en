---
filename: adobe-indesign-modules
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe InDesign modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Adobe InDesign, as well as connect it to multiple third-party applications and services. 
author: Becky
---

# Adobe InDesign Modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use Adobe InDesign, as well as connect it to multiple third-party applications and services. 


If you need instructions on creating a scenario, see [Create a scenario](../../workfront-fusion/scenarios/create-a-scenario.md).

For information about modules, see [Modules in Adobe Workfront Fusion](../../workfront-fusion/modules/modules.md).

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

Before you can use the Adobe InDesign connector, you must have an active Adobe InDesign account.

## Create a connection to Adobe InDesign

To create a connection for your Adobe InDesign modules:

1. In any Adobe InDesign module, click **Add** next to the Connection box.
    
1. Fill in the following fields:
      
    <table style="table-layout:auto"> 
      <col>
      </col>
      <col>
      </col>
      <tbody>
        <tr>
          <td role="rowheader">Connection name</td>
          <td>
            <p>Enter a name for this connection.</p>
          </td>
        </tr>
      <tr>
        <td role="rowheader">Environment</td>
        <td>
          <p>Select whether are connecting to a production or non-production environment.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Type</td>
        <td>
          <p>Select whether you are connecting to a service account or a personal account.</p>
        </td>
      </tr>
        <tr>
          <td role="rowheader">Client ID</td>
          <td>Enter your Adobe Client ID. This can be found in the Credentials details section of the Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Client Secret</td>
          <td>Enter your Adobe Client Secret. This can be found in the Credentials details section of the Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">IMS Organization ID</td>
          <td>Enter your Adobe Organization ID. This can be found in the Credentials details section of the Adobe Developer Console</td>
        </tr>
      </tbody>
    </table>
1. Click **Continue** to save the connection and return to the module.

## InDesign modules and their fields

When you configure Adobe InDesign modules, Workfront Fusion displays the fields listed below. Along with these, additional Adobe InDesign fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another in Adobe Workfront Fusion](../../workfront-fusion/mapping/map-information-between-modules.md).

![](assets/map-toggle-350x74.png)

### Actions

#### Create rendition

This action module creates and returns a JPEG, PNG, or PDF rendition of a specific InDesign document. For the structure of `StatusCompletedRespons/output/data` refer to `RenditionOutputData`. Also for the list of possible error codes in FailedEvent refer to `RenditionFailedData`.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe InDesign, see <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Create a connection to Adobe InDesign</a> in this article.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Type</p>
      </td>
      <td>Select the file type of the rendition you want to create. 
      <ul><li>JPEG</li><li>PNG</li><li>PDF</li></ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>For each asset that you want to add to the rendition:<ol><li>Click <b>Add item</b>.</li><li>Select or map the source of the asset.</li><li>Enter a destination. The destination is  a path relative to a temporary base directory (working directory) where the resource is downloaded. This identifies the assets within the parameters. It cannot go up using '..' or '/'. There should be a valid file name.</td>
    </tr>
    <tr>
      <td role="rowheader">Target document</td>
      <td>Enter or map the document that will be processed and rendered. Currently, only one document at a time is supported.</td>
    </tr>
    <tr>
      <td role="rowheader">Other fields</td>
   <td>For other fields, see information included in the module.</td>     </tr>
  </tbody>
</table>

#### Make a custom API call

This module makes a custom API call to the Adobe InDesign API

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe InDesign, see <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Create a connection to Adobe InDesign</a> in this article.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Path</p>
      </td>
      <td>
        <p>Enter a path relative to <code>https://indesign.adobe.io/v3</code>.</p><p> Example: <code>/create-rendition</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Method</p>
      </td>
      <td>
        <p>Select the HTTP request method you need to configure the API call. For more information, see [HTTP request methods](/help/workfront-fusion/references/modules/http-request-methods.md).</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Headers</td>
      <td>
        <p>Add the headers of the request in the form of a standard JSON object.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion adds authorization headers automatically.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Query String  </td>
      <td>
        <p>Enter the request query string.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Body</td>
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### Custom Script Execution Request

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe InDesign, see <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Create a connection to Adobe InDesign</a> in this article.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Script ID</p>
      </td>
      <td>Enter or map the ID of the custom script.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>For each asset that you want submit an executionr request for, <ol><li>Click <b>Add item</b>.</li><li>Select or map the source of the asset.</li><li>Enter a destination. The destination is  a path relative to a temporary base directory (working directory) where the resource is downloaded. This identifies the assets within the parameters. It cannot go up using '..' or '/'. There should be a valid file name.</td>
    </tr>
    <tr>
      <td role="rowheader">Other fields</td>
   <td>For other fields, see information included in the module.</td>     </tr>
  </tbody>
</table>

#### Delete a Custom Script

### Searches

#### Get Custom Script Details

### Uncategorized

#### Data merge

#### Get data merge tags

#### Get document information

#### Remap links

#### List custom scripts









