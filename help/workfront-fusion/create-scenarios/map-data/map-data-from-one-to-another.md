---
title: Map information from one module to another
description: Mapping is the process of assigning a module's outputs, structured into items, to another module's input fields.
author: Becky
feature: Workfront Fusion
exl-id: 1e3f7729-f48e-451e-a90b-d680c9e3bcbc
---
# Map information from one module to another

Mapping is the process of assigning a module's outputs to another module's input fields.

The mapping panel displays when you click a field where you can insert a value outputted from a preceding module in a scenario. 

You can also create a formula using any combination of functions and mapped items from the mapping panel with static text that you type. These elements can be nested inside each other.

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

## Map an item

After you have created a sequence of modules by linking two or more of them, each module can process values of items outputted by the modules that precede it.

To assign output items to a module's input fields:

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to map data.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Click on the module that should process the output of the preceding module or modules.
1. In the Module settings panel that displays, click a field where you want to use the value of an item outputted from a preceding module.

   The mapping panel opens.

1. (Optional) To search for a particular field in the mapping panel, click the mapping panel search bar and type in the term you want to search for. Click the field when it appears in the list.

   Search results contain the search term and are not case sensitive.
1. To select a value that is an element of a collection, click the arrow next to that collection, then select the element when it appears.
    
    ![Collection element](assets/collection-dropdown.png)

1. Click an item from the mapping panel to insert it into the field.

For more information, see [Configure a module](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).


## Troubleshooting

### Problem: Missing items in the mapping panel

The mapping panel displays output items from previous modules. Occasionally, some items might be missing from this panel. You can run the module that is missing output in the scenario editor, and the mapping panel can then include those items in later modules. The exact procedure differs depending on the module's type

* [Instant trigger](#instant-trigger)
* [Polling trigger](#polling-trigger)
* [Other modules](#other-modules)

#### Instant trigger

1. Right-click the module, then click **[!UICONTROL Run this module only]** in the menu that displays.

   Because this is an instant trigger, it begins watching for events.

1. Create the event that the module is watching. 

   For example, if the module is a Workfront > Watch Events module that is watching for task assignments, log into Workfront (as a user that is not the one that the Fusion connection is using) and assign a task.

1. When the module finishes running, click the bubble above the module to explore its full output.

   The mapping panel for later modules now contains all of the items in the module's output.

#### Polling trigger

1. Right-click the module, then click **[!UICONTROL Run this module only]** in the menu that displays.
1. If there is no output, click **[!UICONTROL Choose where to start]** and adjust the settings.
1. (Conditional) If there is no event to be processed, create the event that the module watches for and repeat step 2.

   For example, if the module is a Workfront > Watch records module that is watching for task assignments, log into Workfront (as a user that is not the one that the Fusion connection is using) and assign a task, then run the module again.

1. When the module finishes running, click the bubble above the module to explore its full output.

   The mapping panel for later modules now contains all of the items in the module's output.

#### Other modules

You may choose to execute:

* The whole scenario (or just the part containing the module)
* The single module

To execute the single module:

1. Right-click the module, then click **[!UICONTROL Run this module only]** in the menu that displays..
1. Provide sample values for the input items, then click **[!UICONTROL OK]** .
1. When the module finishes running, click the bubble above the module to explore its full output.

   The mapping panel for later modules now contains all of the items in the module's output.
