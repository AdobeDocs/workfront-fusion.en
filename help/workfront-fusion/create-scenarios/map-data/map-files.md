---
title: Map a file between modules
description: Some modules have the capability to process files. These modules can either return an output file to be sent for further processing or require a file to be passed to them for processing. Before these modules can work together to process files, they have to be mapped to each other.
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
---
# Map a file between modules

Some modules can process files. These modules can either return an output file to be sent for further processing, or require a file to be passed to them for processing. Files can me mapped, so that a file output by one module can be processed by another.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] package</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] license</td> 
   <td> <p>New: [!UICONTROL Standard]</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] license**</td> 
   <td>
   <p>Current: No [!DNL Workfront Fusion] license requirement.</p>
   <p>Or</p>
   <p>Legacy: Any </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan: [!DNL Workfront Fusion] is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Access level configurations*</td> 
   <td> 
     <p>You must be a [!DNL Workfront Fusion] administrator for your organization.</p>
     <p>You must be a [!DNL Workfront Fusion] administrator for your team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Map files from source modules to target modules

Modules can process  files require two pieces of information:

* File name
* File content (data)

If any previous modules output a file, you can select the source module, and the name and data of the file output by that module are mapped to the target module.

You can also enter this name and data manually, or map it from previous modules. This may be convenient when, for exameple, renaming a file.

>[!NOTE]
>
>If you need to process a file from a URL, we recommend using the `HTTP > Get a File` module to download the file from the URL, and then mapping the file from the `HTTP > Get a File` module to the desired module's field in your scenario.
>
>![Map file](assets/map-source-file.png)

To map a file:

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to map a file.
1. Click anywhere on the scenario to enter the Scenario editor.
1. In the target module, which is the target you are mapping to, locate the **Source file** area.
1. To map a file output by a previous module, select the module that output the file.

   ![Workfront download document](assets/wf-download-document.png)

1. To map the name and data manually, select Map, then enter or map the file's name and data.

   ![Use the map option](assets/use-the-map-option.png)

1. Continue configuring the module, or click **OK**.
