---
title: Adobe Firefly modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use [!DNL Adobe Firefly], as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
---
# [!DNL Adobe Firefly] modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use [!DNL Adobe Firefly], as well as connect it to multiple third-party applications and services. 

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

Before you can use the [!DNL Adobe Firefly] connector, you must ensure that the following prerequisites are met:

* You must have an active [!DNL Adobe Firefly] account.

## Create a connection to [!DNL Adobe Firefly]

To create a connection for your [!DNL Adobe Firefly] modules:

1. In any module, click **[!UICONTROL Add]** next to the Connection box.
    
1. Fill in the following fields:
    
    <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Enter a name for this connection.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Select whether you are connecting to a production or non-production environment.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Select whether you are connecting to a service account or a personal account.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Enter your [!UICONTROL Adobe] [!UICONTROL Client ID]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Enter your [!DNL Adobe] [!UICONTROL Client Secret]. This can be found in the [!UICONTROL Credentials] details section of the [!DNL Adobe Developer Console].</td>
        </tr>
      </tbody>
    </table>
    
1. Click **[!UICONTROL Continue]** to save the connection and return to the module.


## [!DNL Adobe Firefly] modules and their fields

When you configure [!DNL Adobe Firefly] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Adobe Firefly] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Actions

#### Describe Template

This action module analyzes a MOGRT (video template) file and return a manifest of editable controls, fonts, images, audio, video, and other supported values.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly, see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to Adobe Firefly</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Enter or map the presigned URL that points to the input template file.</td> 
  </tr>
 </tbody> 
</table> 

#### Dub Audio or Video

This action module generates dubbed audio or video. It can also include lip sync in the generated video.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly, see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to Adobe Firefly</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dub type</td> 
   <td>Select whether you want to generate an audio or video dub.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Presigned URL</td> 
   <td>Enter or map the presigned URL that the module will use for input.<p>The following domains for media storage are accepted by Firefly Audio and Video</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Media type</td> 
   <td>Select the media type of the input file</td> 
  </tr>
  <tr> 
   <td role="rowheader">Lip sync</td> 
   <td>Select whether to generate a high-quality composited lip sync for the video output.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Target locale codes</td> 
   <td>For each locale code you want to add, click <b>Add item</b> and select the locale code.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Transcripts</td> 
   <td>For each transcript you want to add, click <b>Add item</b> and enter or map the presigned URLs for the transcript.</td> 
  </tr>
 </tbody> 
</table> 

#### Generate Avatar Video From Text or Audio



#### Generate Speech From Text



#### Reframe video V2



#### Render Template



#### Transcribe media



