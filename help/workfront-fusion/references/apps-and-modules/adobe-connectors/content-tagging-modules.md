---
title: Adobe Content Tagger modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Adobe Content Tagger, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
---
# Adobe Content Tagger modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use Adobe Content Tagger, as well as connect it to multiple third-party applications and services. 

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

## Create a connection to Adobe Content Tagger

To create a connection for your Adobe Content Tagger modules:

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


## Adobe Content Tagger modules and their fields

When you configure Adobe Content Tagger modules, Workfront Fusion displays the fields listed below. Along with these, additional Adobe Content Tagger fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Actions

* [Tag colors](#tag-colors)
* [Tag keywords](#tag-keywords)
* [Tag text in an image](#tag-text-in-an-image)

#### Tag colors

This module returns the percentage of an image covered by different pixel colors, sorted into 40 color categories.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Content Tagger, see <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Create a connection to Adobe Content Tagger</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image file name</td> 
   <td>Enter or map the file name of the image that you want to tag colors for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image data</td> 
   <td>Enter or map the file data of the image you want to tag colors for.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Image format</td> 
    <td>Select the image type for the image you want to tag colors for.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Number of colors</td> 
    <td>Enter or map the number of colors to return. To return all results, enter 0.</p></td> 
  </tr> 
 <tr> 
   <td role="rowheader">Minimum coverage</td> 
   <td>Enter or map the minimum coverage that you want to tag colors for. Only colors covering at least this amount of the image will be returned. A value of 1 is 100% of the image, and a value of .5 represents 50% of the image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Resize image before extraction.</td> 
   <td>Select Yes to resize the image to 320x320 before extracting the colors. Select No to extract colors from the full-size image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enable foreground/background mask</td> 
   <td>Select Yes if you want to report colors separately for the overall image, foreground, and background.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Retrieve tones</td> 
   <td>Select Yes if you want to retrieve data about warm, neutral, and cool tones in addition to colors.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned colors</td> 
   <td>Enter or map the maximum number of colors that the module with return for one execution cycle.</td> 
  </tr> 
 </tbody> 
</table>



#### Tag keywords

This module extracts keywords or key phrases that best describe the subject of the document.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Content Tagger, see <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Create a connection to Adobe Content Tagger</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Document file name</td> 
   <td>Enter or map the file name of the document that you want to extract keywords from.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image data</td> 
   <td>Enter or map the file data of the document that you want to extract keywords from.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Image format</td> 
    <td>Select the format of the document that you want to extract keywords from.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Application ID</td> 
   <td>Enter or map the application ID for the document.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Number of key phrases</td> 
   <td>Enter or map the number of key phrases that you want the module to return. To return all results, enter 0.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Minimal relevance</td> 
   <td>Enter or map the score threshold below which results will not be returned.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Minimum key phrase length (words)</td> 
   <td>Enter or map the minimum number of words required in key phrases.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum key phrase length (words)</td> 
   <td>Enter or map the maximum number of words required in key phrases.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Semantic unit depth</td> 
   <td>Select how deep you want the hierarchical responses to go.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Entity types</td> 
   <td>For each entity type that you want to restrict key phrases to, click <b>Add item</b> and enter the information for the entity type.</td> 
  </tr> 
 </tbody> 
</table>

#### Tag text in an image

This module indicates if text is present in an image, and returns the text if present.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Content Tagger, see <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Create a connection to Adobe Content Tagger</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image file name</td> 
   <td>Enter or map the file name of the document that you want to extract text from.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image data</td> 
   <td>Enter or map the file data of the document that you want to extract text from.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Image format</td> 
    <td>Select the format of the document that you want to extract text from.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter with dictionary</td> 
   <td>Select whether to return only words that are in the English dictionary.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Minimum probability</td> 
   <td>Enter or map the minimum probability, where the module will return only words recognized with at least this much probability. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Minimum relevance</td> 
   <td>Enter the minimum percent of the image that returned text should cover. The relevance is computed as the fraction of the area of the extracted text's bounding box in comparison to the full image. 0.01 would translate to a text occupying at least 1% of the image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of results that the module will return for one execution cycle.</td> 
  </tr> 
 </tbody> 
</table>
