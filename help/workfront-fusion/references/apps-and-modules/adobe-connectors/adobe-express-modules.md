---
title: Adobe Express modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Adobe Express.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
---
# Adobe Express modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use Adobe Express, as well as connect it to multiple third-party applications and services. 

If you need instructions on creating a scenario, see the articles under [Create a scenario: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Before you can use the Adobe Express connector, you must ensure that the following prerequisites are met:

* You must have an active Adobe Express account.

## Create a connection to Adobe Express

To create a connection for your Adobe Express modules:

1. In any module, click **[!UICONTROL Add]** next to the Connection box.
    
1. Fill in the following fields:
    
    <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
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
        <td>Select whether you are connecting to a production or non-production environment.</td>
        </tr>
        <tr>
        <td role="rowheader">Type</td>
        <td>Select whether you are connecting to a service account or a personal account.</td>
        </tr>
        <tr>
        <td role="rowheader">Client ID</td>
        <td>Enter your Adobe Client ID. This can be found in the Credentials details section of the Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Client Secret</td>
        <td>Enter your Adobe Client Secret. This can be found in the Credentials details section of the Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>
    
1. Click **[!UICONTROL Continue]** to save the connection and return to the module.


## Adobe Express modules and their fields

When you configure Adobe Express modules, Workfront Fusion displays the fields listed below. Along with these, additional Adobe Express fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Actions

#### Export a rendition

This module exports a document into JPG or PNG format. It can provide pre-signed URLs for the page renditions, which are valid for four hours.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Express, see <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Create a connection to Adobe Express</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Document</td> 
   <td>Select the document that you want to export a rendition for.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Page numbers</td> 
   <td>Enter or map the page numbers that you want to include in the rendition. A comma-separated string of page numbers for which the rendition request is made. For example, "1,2,3". Page ranges can also be specified. For example, "1-3" includes pages 1, 2, and 3. Another example is "1,3-5", which includes pages 1, 3, 4, and 5. "1-" can be used to specify all pages, while "5-" indicates page 5 to the last page. If not provided, the first page is considered by default. Page numbers start from 1.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Rendition type</td> 
   <td>Select the type of rendition that you want to export: image, video, or PDF</td> 
  </tr>
  <tr> 
   <td role="rowheader">Format</td> 
   <td>Select the file format for your rendition.</td> 
  </tr>
  <tr> 
   <td role="rowheader">PDF type</td> 
   <td>If you are exporting a PDF, select whether to export a standard or print PDF.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Size</td> 
   <td>If you are exporting an image or video, enter or map the size, in pixels, of the longest side. The aspect ratio is maintained. For image the minimum size supported is 1px and maximum size supported is 8192px. If not provided, the default size of page is considered.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Download individual PDF files</td> 
   <td>If you are exporting a PDF, select whether pages are downloaded as separate PDF files. When true, each page is downloaded as its own PDF file. When false, all pages are combined into a single PDF file.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Configuration</td> 
   <td>If you are exporting a PDF, select whether you want the PDF in standard or print configuration.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Accessibility tage</td> 
   <td>If you are exporting a PDF, select whether to include accessibility tags in the PDF.</td> 
  </tr>
 </tbody> 
</table> 

#### Generate variations

This module creates a document variation based on provided input parameters. After processing, it temporarily stores the generated document and makes it available to the user within a designated folder. The document remains accessible for 30 days, after which the system automatically removes it.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Express, see <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Create a connection to Adobe Express</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Document</td> 
   <td>Select the document that you want to generate variations for.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Page numbers</td> 
   <td>Enter or map the page numbers that you want to include in the rendition. A comma-separated string of page numbers for which the variation request is made. For example, "1,2,3". Page ranges can also be specified. For example, "1-3" includes pages 1, 2, and 3. Another example is "1,3-5", which includes pages 1, 3, 4, and 5. "1-" can be used to specify all pages, while "5-" indicates page 5 to the last page. If not provided, the first page is considered by default. Page numbers start from 1.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Preferred document name.</td> 
   <td>Enter or map a name for the new document. If you do not provide a name or the name is already in use, the system will generate a unique name.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Project ID</td> 
   <td>Enter the ID of the project where the variations will be stored.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Other fields</td> 
   <td>Enter values for other fields. Available fields are based on the selected document.</td> 
  </tr>
 </tbody> 
</table> 


### Searches

#### Retrieve tagged documents

This module retrieves a list of tagged documents, along with relevant metadata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Express, see <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Create a connection to Adobe Express</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Start index</td> 
   <td>Enter or map the pagination start index. Use this when you have retrieved another list of results, and you want to continue that list. Default index is 0.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of results that you want the module to return for each execution cycle.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sort by</td> 
   <td>Select the attribute by which you want to sort results.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Direction</td> 
   <td>Select whether you want to sort results ascending or descending.</td> 
  </tr>
 </tbody> 
</table> 

#### Retrieve document details

This module retrieves details of the pages and tagged elements within a specified document. It returns a paginated list of the document's pages and metadata about each page. If the document has tagged elements, the API includes their respective details, such as size and position. If the document does not have tagged elements, it returns an empty array. The response includes pagination information to help users navigate the document's pages. A maximum of 10 pages can be returned in 1 cycle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Express, see <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Create a connection to Adobe Express</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Document</td> 
   <td>Select the document that you want to return pages and details for.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Starting page</td> 
   <td>Enter or map the the page number of the first page from which details will be retrieved.</td> 

#### Retrieve a job's status

This module retrieves a job's status by its job ID. Depending on the job type, the response may include job-specific details.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Express, see <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Create a connection to Adobe Express</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Job ID</td> 
   <td>Enter or map the ID of the job that you want to retrieve details for.</td> 
  </tr>

