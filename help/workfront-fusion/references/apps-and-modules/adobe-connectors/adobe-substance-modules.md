---
title: Adobe Substance modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use [!DNL Adobe Substance], as well as connect it to multiple third-party applications and services. [!DNL Adobe Substance] modules allow you to create, read, update, or delete records, list all records of a given type, search records based on criteria you specify, or perform a custom API call to the [!DNL Adobe Substance] API.
author: Becky
feature: Workfront Fusion
exl-id: f3c1ed7b-b69b-478a-8240-1a2ab89e11e5
---
# [!DNL Adobe Substance] Modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use [!DNL Adobe Substance], as well as connect it to multiple third-party applications and services. 

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

Before you can use the [!DNL Adobe Substance] connector, you must ensure that the following prerequisites are met:

* You must have an active [!DNL Adobe Substance] account.



## [!DNL Adobe Substance] modules and their fields

When you configure [!DNL Adobe Substance] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Adobe Substance] fields might display, depending on factors such as your access level in the app or service. An asterisk next to the field name in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Composites](#composites)
* [Scenes](#scenes)
* [Spaces](#spaces)

### Composites

#### Generate 3D object composite

This action module generates content for a 3D composite that includes the selected hero asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions on connecting your [!DNL Adobe Substance] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Other fields</td> 
   <td>Configure other fields as desired. For details of fields, see the <a href="https://s3d.adobe.io/docs#/operations/v1/composites/compose">Adobe Substance API documentation</a>.</td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">Camera name</td> 
   <td>Enter or map the name of an existing camera that has been previously defined in the source 3D file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Content class</td> 
   <td>Select whether you want the composite to have the style of art or of a photo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enable ground plane</td> 
   <td>Enable this to enable the auto-generated ground plane under the hero asset. This is useful if the 3D scene contains only a hero asset, without additional elements.</td> 
  </tr> -->
 </tbody> 
</table>

### Scenes

* [Convert 3D files](#convert-3d-files)
* [Create 3D scene](#create-3d-scene)
* [Describe 3D scene](#describe-3d-scene)
* [Render 3D object](#render-3d-object)
* [Render 3D object (basic version)](#render-3d-object-basic-version)

#### Convert 3D files

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions on connecting your [!DNL Adobe Substance] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Format</td> 
   <td>Select the format that you are converting the file to.</td> 
  </tr> 
<tr> 
   <td role="rowheader">Model entrypoint</td> 
   <td>Conversion usually takes the first file that's considered a valid 3D model. Define this entry point to disambiguate when there are multiple options.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sources</td> 
   <td>For each file that you want to convert, click <b> Add item</b> and enter the file information.</td> 
  </tr> 
 </tbody> 
</table>

#### Create 3D scene

This action module creates a scene using assets you specify.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions on connecting your [!DNL Adobe Substance] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Encoding</td> 
   <td>Select the file type for the scene.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">File base name</td> 
   <td>Enter or map a name for the output file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Other fields</td> 
   <td>Configure other fields as desired. For details of fields, see the <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/assemble">Adobe Substance API documentation</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Sources</td> 
   <td>For each file that you want to use, click <b> Add item</b> and enter the file information.</td> 
  </tr> 
 </tbody> 
</table>

#### Describe 3D scene

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions on connecting your [!DNL Adobe Substance] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Scene file</td> 
   <td>Enter or map the path to the scene file that you want to describe.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Sources</td> 
   <td>For each file that you want to describe, click <b> Add item</b> and enter the file information.</td> 
  </tr> 
 </tbody> 
</table>

#### Render 3D object

#### Render 3D object (basic version)

### Spaces

#### Create space


