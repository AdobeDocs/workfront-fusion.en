---
title: Use Live Trail to review a scenario run
description: Live Trail shows a scenario run as it happens, combining module requests and run activity in one list. You can open the request and response details for any operation.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
<!-- BECKY CHECK ME (article-level): New article, drafted from the 10/23/26 release notes (Fusion Scenario Designer: New UI/UX; release 2026-10-28) with no access to the live UI. Every UI label, menu path, and step below needs to be verified against the product, and screenshots are needed throughout. Also decide whether this should stay a separate article or be folded into debug-a-scenario.md. The exl-id and TQID front matter fields are intentionally absent; add them if your pipeline requires them. -->

# Use Live Trail to review a scenario run

Live Trail shows a scenario run as it happens. It combines module requests and run activity in one chronological list, so you can follow a run in the scenario editor and see what went wrong without leaving the canvas.

>[!NOTE]
>
>This functionality is available in the new scenario editor experience only. For more information, see [New and classic experiences](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) in the article Scenario editor.
<!-- BECKY CHECK ME: confirm this feature is not available in the classic experience, and whether this standard note wording should be used instead of the transitioning note. -->

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
1. Open Live Trail.

   <!-- BECKY CHECK ME: how do you open Live Trail? Does it open automatically when a run starts, or from a button, menu item, or Controls icon? Add the exact label, an icon image, and a screenshot of the panel. -->

Live Trail opens in the panel on the right side of the canvas. If you close the panel during a run, a small control lets you open it again without losing the events that were captured.

## Review events in Live Trail

Live Trail lists module requests and run activity in the order that they happen. You can:

* Search the list.
* Filter the list by status.
* Follow the newest event as the run continues.
* Clear the current trail.

<!-- BECKY CHECK ME: confirm the names of these controls (for example "Follow latest" vs. "Follow newest"), and whether to present them as a table with an icon column. Also confirm which statuses you can filter by. -->

## View request and response details

1. In Live Trail, select a request.

   The module that made the request is revealed on the canvas, and the request and response details open in the panel.

1. Review the details. The detail view includes:

   * Navigation between the operations of the module
   * Request headers and body
   * Response headers and body

1. (Optional) Copy the details to use them elsewhere:

   * Copy a raw report of the request and response.
   * Copy a cURL command for the request.

   <!-- BECKY CHECK ME: confirm the labels of the copy actions and where they appear (buttons at the top of the detail view?). -->

1. To return to the list, click **Back**.

<!-- BECKY CHECK ME: confirm that Back is the label. The release notes say opening a nested view replaces the current panel and gives you a Back action. -->

## Make sure request and response details are available

Request and response details are not kept for every scheduled or triggered run, because they take a lot of storage.

* Run once always keeps request and response details.
* For a scenario's regular runs, turn on Temporary debug logs in the scenario settings before the runs that you want to inspect. For more information, see [Temporary debug logs](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs) in the article Configure scenario settings.

If you open a run from the execution history and the request and response panel has no data, the panel directs you to the Temporary debug logs setting.

## Related information

* The same request and response panel is available when you review an execution. For more information, see [View a specific scenario execution](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md).
* For other debugging tools, including the DevTool, see [Debug a scenario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md).

<!-- BECKY CHECK ME: the DevTool has a "Live Stream" section. Confirm whether Live Trail replaces it for most uses, and add a sentence comparing them if so. -->
