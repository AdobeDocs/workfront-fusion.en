---
title: Find and replace variables, sources, and connections in a scenario
description: Use Find and replace to replace a mapped variable, remap references from one source module to another, or copy a connection to other modules in your scenario.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---

# Find and replace variables, sources, and connections in a scenario

>[!NOTE]
>
>This functionality is available in the new scenario editor experience only. For more information, see [New and classic experiences](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) in the article Scenario editor.

Find and replace lets you make the same change across many modules at once. You can:

* Replace a mapped variable across the whole scenario or in one module.
* Remap references from one source module to another.
* Copy a connection to one or all compatible modules from the same app.

Before it makes a change, Find and replace shows a preview of the modules that will be affected.

In the classic experience, you can use the Swap variable, Remap source, and Swap connection tools in the DevTool to do these tasks. For more information, see [Debug a scenario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md).

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
   <td role="rowheader">Product</td> 
   <td>
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Open Find and replace

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to make changes.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Click the **Find and replace** icon ![Find and replace](assets/find-replace-icon.png) in the Controls area.

   You might need to click the three-dot icon in the Controls area to see the Find and replace icon.

Find and replace opens in the panel on the right side of the canvas.

## Replace a variable

Use the **Variable** tab to replace a mapped variable.

1. Open Find and replace, then click the **Variable** tab.
1. In the Variable to find field, paste in the variable that you want to replace.
1. In the Replace with field, paste in the variable that will replace the previous variable.
1. In the Module field, choose the module that the change will apply to, or select **Whole scenario** to apply the change to all affected modules in the scenario.
1. Click **Replace**
1. Review the preview of the modules that will be affected. To go to a module on the canvas, select its row in the preview.
1. Click **Apply**.

## Remap a source

Use the **Source** tab to change which module the mappings in other modules refer to.

1. Open Find and replace, then click the **Source** tab.
1. In the Source module field, Select the source module that the mappings currently refer to.
1. In the Target module fields, select the module that they should refer to instead.
1. In the Module field, choose the module that the change will apply to, or select **Whole scenario** to apply the change to all affected modules in the scenario.
1. Click **Replace**
1. Review the preview of the modules that will be affected. To go to a module on the canvas, select its row in the preview.
1. Click **Apply**.

## Copy a connection to other modules

Use the **Connection** tab to use the same connection in more than one module of the same app.

1. Open Find and replace, then click the **Connection** tab.
1. In the Connection from field, select a module that currently has the connection that you want to use for other modules.
1. In the Apply to field, choose the module that the change will apply to, or whether to apply the change to all compatible modules in the scenario.
1. Click **Apply**.
