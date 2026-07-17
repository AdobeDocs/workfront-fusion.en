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

#### Color tagging

This module returns histogram of pixel colors, sorted into 40 color categories.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Content Tagger, see <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Create a connection to Adobe Content Tagger</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Image URL</td> 
   <td>Enter or map a presigned URL that represents the image you want to apply XMP to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Storage type</td> 
   <td>Select the type of storage that the image is stored in.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Output storage</td> 
    <td>Select where you want the output file to be stored. <p>Fusion internal storage does not store the image outside of the scenario, but allows other modules in the scenario to access the image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output type</td> 
   <td>Select the file type for the output file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overwrite</td> 
   <td>Select yes if you want to allow the module to overwrite output if it already exists. This applies only to Adobe cloud storage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Quality</td> 
   <td>Enter or map the quality of the output image. 1 is the lowest quality, and 12 is the highest. This applies only to JPEG files.</td> 
  </tr> 
 </tbody> 
</table>


