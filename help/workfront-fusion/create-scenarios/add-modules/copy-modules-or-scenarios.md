---
title: Copy modules or scenarios
description: You can copy modules, groups of modules, or entire scenarios in Adobe Workfront Fusion. This ability allows you to reuse scenarios or parts of scenarios without having to build them again.
author: Becky
feature: Workfront Fusion
exl-id: 5cece7d4-b2c7-4276-8a6f-f65bad799c7a
---
# Copy modules or scenarios

You can copy modules, groups of modules, or entire scenarios in Adobe Workfront Fusion. This ability allows you to reuse scenarios or parts of scenarios without having to build them again.

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
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisites

The modules must exist in a scenario before you can copy them.

## Copy a module or a group of modules

When you copy a module, the copy retains all of the field values and settings of the original module.

You can paste the module or modules into another area of the same scenario, or into a different scenario.

Consider the following when pasting modules into a different scenario:

* Any field values that pull information from another module that you did not copy can no longer access that information. You must set these fields to pull information from the new scenario.
* If you paste the modules into a scenario owned by another team or organization, all connections must be updated to connections owned by the team or organization that owns the new scenario.

### Copy modules

Copying a group of modules is similar to copying a single module.

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to copy a module.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Right-click on the module that you want to copy.

   >[!NOTE]
   >
   >You can select more than one module by holding [!UICONTROL shift] and clicking on the modules that you want to copy. Copying a group of modules also copies any connecting lines, filters, or routing logic between them.

1. Select **[!UICONTROL Copy module]**.
1. Move the cursor to the area of the scenario where you want the copy of the scenario.
1. Right click, and select **[!UICONTROL Paste]**.
1. Connect the pasted modules to the scenario by dragging them to the appropriate location in the scenario.

   You can also use keyboard shortcuts to copy and paste.

## Copy a scenario by cloning

Cloning a scenario creates a copy of the scenario, which you can then edit.

1. Open the scenario detail page:

   1. Click the **[!UICONTROL Scenario]** tab in the left panel, then click a scenario you would like details on.

      Or

      If you are working on the scenario in the the scenario editor, click the left arrow ![Exit editing arrow](assets/exit-editing-arrow.png) near the upper-left corner of the window.

1. Right click **[!UICONTROL Options]** at the upper-right of the page.
1. Select **[!UICONTROL Clone]**.
1. (Optional) Enter a name for the new scenario.
1. (Optional) Enable **[!UICONTROL Keep the states of any new modules the same as those being duplicated]** to ensure that the copied scenario also includes information about the most recent records processed by the original scenario.
1. Click **[!UICONTROL Save]** to create the scenario.

## Copy a scenario by using blueprints

Scenario blueprints represent the arrangement, mapping, and field values of a given scenario at a given point in time. You can export a scenario blueprint into a JSON file on your computer, then import it when creating a new scenario. Scenarios imported from a scenario blueprint can be edited.

A scenario blueprint represents the entire scenario. If you want to copy only certain modules from a scenario, see [Copy a module or a group of modules](#copy-a-module-or-a-group-of-modules) in this article.

### Export a scenario blueprint

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to export a blueprint.
1. Click anywhere on the scenario to enter the Scenario editor.
1. In the scenario, click the **[!UICONTROL More]** menu in the scenario settings area.
1. Click **[!UICONTROL Export Blueprint]**.

   A JSON file is created and downloads to your computer. You can locate this file in your [!DNL Downloads] folder.

>[!NOTE]
>
>To export the blueprint for a previous version of a scenario, see [View and manage scenario versions](/help/workfront-fusion/manage-scenarios/restore-a-scenario-version.md).

### Import a blueprint

>[!IMPORTANT]
>
>If you import a blueprint to an existing scenario, the scenario blueprint replaces the existing scenario. You cannot append a blueprint onto an existing scenario.

1. Begin creating a new scenario.
1. In the scenario, click the **[!UICONTROL More]** menu in the scenario settings area.
1. Click **[!UICONTROL Import Blueprint]**.
1. In the dialog that appears, click **[!UICONTROL Browse]**
1. Navigate to the blueprint you want to import, and click **[!UICONTROL Open]**.
1. Click **[!UICONTROL Save]**.

   A JSON file is created and downloads to your computer. You can locate this file in your [!UICONTROL Downloads] folder.

## Copy and reuse scenarios by using templates

You can create templates as a starting point for your Workfront Fusion scenarios. When you create a scenario from a template, you can modify the scenario without modifying the template. Field values are not saved in templates.

For more information on creating a scenario using a template, see [Create scenarios with templates](/help/workfront-fusion/create-scenarios/add-modules/create-scenarios-with-fusion-templates.md).

## Troubleshooting

If you are copying and pasting modules as described in [Copy a module or a group of modules](#copy-a-module-or-a-group-of-modules) and nothing appears when you paste, check your browser's site settings to ensure that pasting from the clipboard is allowed.
