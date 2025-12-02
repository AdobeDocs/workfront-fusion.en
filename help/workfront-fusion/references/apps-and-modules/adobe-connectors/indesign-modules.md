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

You must have the following access to use the functionality in this article:

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Adobe Workfront plan*</td>
      <td>
        <p>Pro or higher</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Adobe Workfront license*</td>
      <td>
        <p>Plan, Work</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Adobe Workfront Fusion license**</td>
      <td >
        <p>Workfront Fusion for Work Automation and Integration</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Product</td>
      <td>Your organization must purchase Adobe Workfront Fusion as well as Adobe Workfront to use functionality described in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">Access level configurations*</td>
      <td>
        <p>You must be a Workfront Fusion administrator for your organization.</p>
        <p>You must be a Workfront Fusion administrator for your team.</p>
      </td>
    </tr>
  </tbody>
</table>


&#42;To find out what plan, license type, or access you have, contact your Workfront administrator.

&#42;&#42;For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md)

## Prerequisites

Before you can use the Adobe InDesign connector, you must ensure that the following prerequisites are met:

*   You must have an active Adobe InDesign account.

## Create a connection to Adobe InDesign

To create a connection for your Adobe InDesign modules:

1.  In any Adobe InDesign module, click **Add** next to the Connection box.
    
1.  Fill in the following fields:
      
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
          <td role="rowheader">Client ID</td>
          <td>Enter your Adobe Client ID. This can be found in the Credentials details section of the Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Client Secret</td>
          <td>Enter your Adobe Client Secret. This can be found in the Credentials details section of the Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Technical account ID</td>
          <td>Enter your Adobe Technical account ID. This can be found in the Credentials details section of the Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Organization ID</td>
          <td>Enter your Adobe Organization ID. This can be found in the Credentials details section of the Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Private key</td>
          <td>
            <p>Enter the private key that was generated when your credentials were created in the Adobe Developer Console. </p>
            <p>To extract your private key or certificate:</p>
            <ol>
              <li value="1">
                <p>Click <b>Extract</b>.</p>
              </li>
              <li value="2">
                <p>Select the type of file you are extracting.</p>
              </li>
              <li value="3">
                <p>Select the file that contains the private key or certificate.</p>
              </li>
              <li value="4">
                <p>Enter the password for the file.</p>
              </li>
              <li value="5">
                <p>Click <b>Save</b> to extract the file and return to the connection setup.</p>
              </li>
            </ol>
          </td>
        </tr>
      </tbody>
    </table>
1. Click **Continue** to save the connection and return to the module.

## InDesign modules and their fields

>[!NOTE]
>
>The Adobe InDesign API is continuing to evolve. As updates are released to the API, the Workfront Fusion Adobe InDesign connector will also be updated.

When you configure Adobe InDesign modules, Workfront Fusion displays the fields listed below. Along with these, additional Adobe InDesign fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another in Adobe Workfront Fusion](../../workfront-fusion/mapping/map-information-between-modules.md).

![](assets/map-toggle-350x74.png)

### Copy Collab

This action module retrieves data for a copy collaboration workflow.

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
        <p>Assets</p>
      </td>
      <td>For each asset that you want to add to the rendition:<ol><li>Click <b>Add item</b>.</li><li>Select or map the source of the asset.</li><li>Enter a destination. The destination is  a path relative to a temporary base directory (working directory) where the resource is downloaded. This identifies the assets within the parameters. It cannot go up using '..' or '/'. There should be a valid file name.</td>
    </tr>
    <tr>
      <td role="rowheader">Target document</td>
      <td>The target document is an InDesign document that contains placeholders for data, as well as any other material or text that remain the same in every rendition of the document.</td>
    </tr>
    <tr>
      <td role="rowheader">Other fields</td>
   <td>For other fields, see information included in the module.</td>     </tr>
  </tbody>
</table>


### Create Rendition

This action module creates and returns a JPEG, PNG, or PDF rendition of a specific InDesign document. For the structure of StatusCompletedRespons/output/data refer to RenditionOutputData. Also for the list of possible error codes in FailedEvent refer to RenditionFailedData.

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
      <td>The target document is an InDesign document that contains placeholders for data, as well as any other material or text that remain the same in every rendition of the document.</td>
    </tr>
    <tr>
      <td role="rowheader">Other fields</td>
   <td>For other fields, see information included in the module.</td>     </tr>
  </tbody>
</table>


### Make a custom API call

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
        <p>Enter a path relative to <code>https://indesign.adobe.io/api</code>.</p><p> Example: <code>/v1/capability/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Method</p>
      </td>
      <td>
        <p>Select the HTTP request method you need to configure the API call. For more information, see HTTP request methods.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Headers</td>
      <td>
        <p>Add the headers of the request in the form of a standard JSON object.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion adds authorization headers and x-api-key headers automatically.</p>
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

### Submit Capability

This action module submits a capability bundle, and returns the URL for the posting execution request.

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
      <td>
        <p>Select whether you want to submit a custom capability, or submit an execution request.</p>
        <ul><li><p><b>Custom</b></p><p>Enter or select the ID of the IMS organization that you are submitting this capability for, then select the source file from a previous module, or map the source file's name and data.</p></li><li><p><b>Execution request</b></p><p>For descriptions of fields, see the information included in the module.</p></li></ul>
      </td>
    </tr>
  </tbody>
</table>


### Get status

This action module retrieves the status of a job, or status events for the job.

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
        <p>Status Type</p>
      </td>
      <td>
        <p>Select whether you want the module to return the latest status of a job, or all status events for the job.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>ID</p>
      </td>
      <td>
        <p>Enter or map the ID of the job that you want to return status information for.</p>
      </td>
    </tr>
  </tbody>
</table>

### Document data

This action module retrieves the requested data from the document. The data may include information around the relatinship between spreads and pages, information about the page items, information about the text stories, and data merge tags.

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
        <p>Assets</p>
      </td>
      <td>
        <p>For each document that you want to return data for, click <b>Add</b> and </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Target Document</p>
      </td>
      <td>
        <p>Text</p>
      </td>
    </tr>
  </tbody>
</table>
