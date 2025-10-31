---
title: Add a filter to a scenario
description: In some scenarios, you need to work only with bundles that meet specific criteria. Filters allow you to select those bundles.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
---
# Add a filter to a scenario

In some scenarios, you need to work only with bundles that meet specific criteria. Filters allow you to select those bundles.

For example, you could create a scenario with the [!UICONTROL Watch records] trigger for Workfront to capture only tasks assigned to a specific user.

You can add a filter between two modules and check whether bundles received from the preceding modules fulfill specific filter conditions:

* If they do, the bundles pass on to the next module in the scenario.
* If they don't, processing for the bundles terminates.

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

+++## Prerequisites

You must add both modules to a scenario before you can add a filter between them.

## Add a filter between two modules:

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a filter.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Click the wrench icon ![Wrench icon](assets/wrench-icon.png) between the modules where you want to add a filter and select **Set up a filter**.
1. In the box that displays, enter a **[!UICONTROL Label]** for the filter.
1. Define the filter **[!UICONTROL Condition]**.

   Enter the field that you want to filter by in the first field, the operator, and (if necessary) the value that you want to compare the field to.

   >[!TIP]
   >
   >You can enter values into filter fields from the mapping panel
   >For more information on mapping, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   For example, if you wanted the filter to pass files in Adobe Workfront ending with XML, you would enter **[!UICONTROL File name]** in the first box and .**[!UICONTROL xml]** in the second box. In the drop-down menu between them, you would select **[!UICONTROL Ends with (case insensitive)]**. This filter would apply to incoming bundles from the first module (Workfront). Only bundles containing XML files would pass on to the next module.

   ![Set up a filter](assets/set-up-filter-box.png)

1. Click **[!DNL OK]**.

## Copy a filter

Currently, the scenario editor does include a feature for copying a filter.

>[!NOTE]
>
>If you copy the modules on either side of the filter, the filter is also copied.
>
>For more information on copying modules, see [Copy modules or scenarios in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

To copy a filter without copying modules, you can use the Fusion DevTool

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a filter.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Open the Fusion DevTool by clicking on the DevTool icon ![DevTool icon](assets/debugger-icon.png) near the bottom of the screen.
   
   If you do not see the DevTool icon, see [Debug a scenario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) for instructions on opening the DevTool.
   
1. Click the **[!UICONTROL Tools]** icon ![DevTool tools](assets/devtools-tools-icon.png) in the left side bar.

1. Click **[!UICONTROL Copy Filter]**, then configure the **[!UICONTROL Copy Filter]** tool in the right side panel:

   1. Set the **[!UICONTROL Source Module]** as the module directly after the filter you want to copy.
   1. Set the **[!UICONTROL Target Module]** as the module that you want to place the filter directly after.

1. Click **[!UICONTROL Run]**.
