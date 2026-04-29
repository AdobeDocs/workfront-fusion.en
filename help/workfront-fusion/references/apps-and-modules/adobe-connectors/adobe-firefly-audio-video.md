---
title: Adobe Firefly modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Adobe Firefly Audio and Video, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
---
# Adobe Firefly Audio and Video modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use Adobe Firefly Audio and Video, as well as connect it to multiple third-party applications and services. 

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

Before you can use the Adobe Firefly Audio and Video connector, you must ensure that the following prerequisites are met:

* You must have an active Adobe Firefly Audio and Video account.

## Create a connection to Adobe Firefly Audio and Video

To create a connection for your Adobe Firefly Audio and Video modules:

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


## Adobe Firefly Audio and Video modules and their fields

When you configure Adobe Firefly Audio and Video modules, Workfront Fusion displays the fields listed below. Along with these, additional Adobe Firefly Audio and Video fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

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

This action module generates an avatar video from a transcript or audio file you provide.

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
   <td>Enter or map the presigned URL that the module will use for input.   </td> 
  </tr>
  <tr> 
  <tr> 
   <td role="rowheader">Locale code</td> 
   <td>Select the locale code that represents the language you want to use in the result.</td> 
  </tr>
   <td role="rowheader">Media type (Source)</td> 
   <td>Select the media type of the input file</td> 
  </tr>
  <tr> 
   <td role="rowheader">Avatar</td> 
   <td>Select the avatar that you want to use for the generated video.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Media type</td> 
   <td>Select the output media type for the generated video.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Width</td> 
   <td>Enter or map the width for the generated video.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Height</td> 
   <td>Enter or map the height for the generated video.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Background</td> 
   <td>Select the type of background that you want to use for the generated video:
   <ul>
   <li><b>Video</b>: Enter or map the URL of the background video.</li> 
   <li><b>Image</b>: Enter or map the URL of the background image.</li>
   <li><b>Color</b>: Enter or map the hex value of the color you want to use for the video background.</li> 
   </ul>
   </td>
  </tr>
 </tbody> 
</table> 

#### Generate Speech From Text

This action module generates speech from a transcript. You can provide either a plain text transcript or a presigned URL. The response includes a job ID and a status URL for tracking the job.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly, see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to Adobe Firefly</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Script</td> 
   <td>Select the type of script that you want to provide.
   <ul>
   <li><b>Text</b>: Enter or map the source text into the Text field.</li>
   <li><b>Text file</b>: Enter or map the URL of the text file in the URL field.</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Locale code</td> 
   <td>Select the locale code that represents the language you want to use in the result.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Media type</td> 
   <td>This should be <code>text/plain</code>.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Voice</td> 
   <td>Select the voice that you want to use. Available voices are from the Adobe Firefly catalog of voices.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Output</td> 
   <td>This should be <code>audio/wav</code>.</td> 
  </tr>
 </tbody> 
</table> 

#### Reframe video V2

This module reframes the media you provide. Media is provided via a presigned URL.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly, see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to Adobe Firefly</a> in this article.</td> 
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
   <td role="rowheader">Scene edit detection</td> 
   <td>Select whether to apply scene edit detection before reframing. </td> 
  </tr>
  <tr> 
   <td role="rowheader">Focal point</td> 
   <td>For each focal point you want to add, click <b>Add item</b> and enter or the keyword identifier for the focal point.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Overlays</td> 
   <td>For each overlay you want to add, click <b>Add item</b> and enter the overlay information.
   <ul>
   <li><b>Source</b>: Enter or map the URL that points to the source media.</li> 
   <li><b>Start time</b>: Enter or map the start time.</li>
   <li><b>Duration</b>: Enter or map the duration of the overlay.</li> 
   <li><b>Width</b>: Enter or map the width of the scaled overlay.</li> 
   <li><b>Height</b>: Enter or map the height of the scaled overlay.</li> 
   <li><b>Anchor point</b>: Select the anchor point for the overlay.</li> 
   <li><b>Offset X</b>: Enter or map the horizontal offset for the overlay.</li> 
   <li><b>Offset Y</b>: Enter or map the vertical offset for the overlay.</li> 
   <li><b>Repeat</b>: Enter <code>loop</code> to cause a GIF to loop.</li> 
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Media format</td> 
   <td>Select the format for the reframed video.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sidecar format</td> 
   <td>Select the format for additional metadata.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Renditions</td> 
   <td>To add additional renditions, click <b>Add item</b> and enter the rendition information.<!--add additional info--></td> 
  </tr>
 </tbody> 
</table> 

#### Render Template

This module renders one or more video variations by applying overrides and export presets.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly, see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to Adobe Firefly</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Input template file URL</td> 
   <td>Enter or map the presigned URL that represents the template that you want to render.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Fonts</td> 
   <td>For each font that you want to add, click <b>Add item</b> and enter the postscript name of the font and the font file URL.</td> 
  </tr>
  <tr> 
   <td role="rowheader">When a font is missing</td> 
   <td>Select whether you want to fail the render or use the default font if a font is missing.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Media assets</td> 
   <td>For each media asset that you want to add, click <b>Add item</b> and enter or map the presigned URL that represents the asset.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Export presets</td> 
   <td>For each export preset that you want to add, click <b>Add item</b> and select the video preset, and enter or map the presigned URL that represents the preset.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Variations</td> 
   <td>For each variation that you want to add, click <b>Add item</b> and enter details for the variation. You must enter details for at least one variation.<!--add data here--></td> 
  </tr>
  <tr> 
   <td role="rowheader">Output definitions</td> 
   <td>Define outputs by clicking <b>Add item</b> and selecting which of the added variations and presets you want to use, and adding a filename. Variations and presets are indexed to 0 (the first item in the list of variations is 0, the next is 1, and so on).</td> 
  </tr>
 </tbody> 
</table> 

#### Transcribe media

This module transcribes audio or video.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td>For instructions on creating a connection to Adobe Firefly, see <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Create a connection to Adobe Firefly</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Transcription type</td> 
   <td>Select whether you want to transcribe audio or video.   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Presigned URL</td> 
   <td>Enter or map the presigned URL that the module will use for input.   </td> 
  </tr>
  <tr> 
  </tr>
   <td role="rowheader">Media type </td> 
   <td>Select the media type of the input file</td> 
  </tr>
  <tr> 
   <td role="rowheader">Target locale codes</td> 
   <td>For each locale code that you want to add, click <b>Add item</b> and select the locale code that represents the language you want to use in the result.</td> 
  <tr> 
   <td role="rowheader">Caption format</td> 
   <td>Enter <code>SRT</code> to include captions, or leave blank if you do not want captions.</td> 
  </tr>
 </tbody> 
</table> 



