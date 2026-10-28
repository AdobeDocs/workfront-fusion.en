---
title: Use Live Trail to review a scenario run
description: Live Trail shows a scenario run as it happens, combining module requests and run activity in one list. You can open the request and response details for any operation.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---

# Use Live Trail to review a scenario run

Live Trail shows a scenario run as it happens. It combines module requests and run activity in one chronological list, so you can follow a run in the scenario editor and see what went wrong without leaving the canvas.

>[!NOTE]
>
>This functionality is available in the new scenario editor experience only. For more information, see [New and classic experiences](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) in the article Scenario editor.

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

## Open Live Trail

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario that you want to review.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Start a run of the scenario, for example by clicking **Run once**.



Live Trail opens in the panel on the right side of the canvas. If you close the panel during a run, a small tab on the right of the screen lets you open it again without losing the events that were captured.

## Review events in Live Trail

Live Trail lists module requests and run activity in the order that they happen. You can:

* Search the list.
* Filter the list by status.
* Follow the newest event as the run continues.
* Clear the current trail.

## View request and response details

1. In Live Trail, click the request that you want to view details for.

   The module that made the request is revealed on the canvas, and the request and response details open in the panel.

1. Review the details. The detail view includes:

   * Navigation between the operations of the module
   * Request headers and body
   * Response headers and body

1. (Optional) Copy the details to use them elsewhere by clicking **Copy raw** or **Copy cURL**:

   * Copy a raw report of the request and response.
   * Copy a cURL command for the request.

1. To return to the list, click the back arrow at the upper-left of the panel.

## Make sure request and response details are available

Request and response details are not kept for every scheduled or triggered run, because they take a lot of storage.

* Run once always keeps request and response details.
* For a scenario's regular runs, turn on Temporary debug logs in the scenario settings before the runs that you want to inspect. For more information, see [Temporary debug logs](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs) in the article Configure scenario settings.

If you open a run from the execution history and the request and response panel has no data, the panel directs you to the Temporary debug logs setting.
