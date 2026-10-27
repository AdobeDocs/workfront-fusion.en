---
title: View the Insights dashboard for an organization
description: Fusion administrators can view a dashboard that shows execution metrics for an organization.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: 'https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
---
# View the Insights dashboard for an organization

The Fusion Insights Dashboard allows you to quickly see which scenarios are running the most, where delays are occurring, and how effectively your worker pools are operating. This provides real-time visibility into execution volumes, queue depth, pool utilization, and scenario-level performance.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Adobe Workfront Workflow Ultimate and Adobe Workfront Automation and Integration Ultimate</p><p>Workfront Ultimate</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront licenses</td> 
   <td> <p>Standard</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Access level configurations</td> 
   <td> 
     <p>You must be a Workfront Fusion administrator for your organization.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Insights dashboard components

>[!NOTE]
>
>Metrics are shown by worker pool. To view a different worker pool, click the Pool field near the upper-left corner of the dashboard, then select the pool you want to view metrics for.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

In the Fusion Insights dashboard, you can see the following metrics.

* **Failed Executions Logs**
   This table lists every failed or warning scenario execution across your organization, so you can find and troubleshoot problem runs without leaving the dashboard.

* **Executions waiting to be processed**
   This chart shows the number of executions waiting to be processed (also known as the execution backlog) at a given point in time. 

   A high number of executions waiting to be processed may affect performance in your Fusion instance. You will receive a notification if your execution backlog reaches 5000 executions. We recommend identifying responsible scenarios and modifying or disabling them. If the high execution backlog persists, the Fusion team will protect the performance of your Fusion instance by disabling the responsible scenarios.
* **Pool Utilization**
   This chart shows worker pool utilization over time. If this chart routinely shows worker pool utilization, you may want to assign some scenarios to another pool.

   If a pool is nearing 100% utilization, other resources that use the same pool may be delayed or disrupted. If this occurs, we recommend reassigning a high-usage scenario to another worker pool, or modifying existing scenarios to be less resource intensive.
* **Executions per scenario**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify which scenarios may be causing an execution backlog or high worker pool utilization. 
* **Duration of executions**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify scenarios that are taking longer than usual, including those affected by issues with a connected app or service.

## View the Fusion Insights Dashboard

1. In Fusion, click **Insights** in the left navigation.
  
   The Dashboard opens.

1. To view data for a specific point in time, hover over a dashboard and adjust your cursor to be over the point in time you want to view.

   A line appears over that point in time on all the graphs, and a window showing data for that time appears on each graph.
1. To view data for a specific scenario in the Executions per scenario chart or the Duration of executions chart, click on a bar of the color for the scenario you want to view data for. To return to the view showing all scenarios, click on the graph again.
1. To go to a specific scenario shown in the Executions per scenario chart or the Duration of executions chart, right click on a bar of the color for the scenario, and select **Open scenario in new tab**.
1. To expand a chart, click the **Expand** icon ![Expand icon](assets/expand-icon.png) at the upper-right corner of that chart.
1. To change the time range of the dashboard, the Time Range field in the upper-right corner of the dashboard, then select a new time frame. The longest available time frame is 24 hours, and the shortest is 15 minutes.
1. To refresh the charts, click the Refresh icon near the upper-right corner of the dashboard.
1. To view a different worker pool, click the Pool field near the upper-left corner of the dashboard, then select the pool you want to view.

## Customize the Insights dashboard

You can choose which widgets appear on the Insights dashboard, and in what order.

<!-- BECKY CHECK ME: The widget list in "Insights dashboard components" above does not describe the Organization Operations, Top Scenarios by Operations, or Performance widgets that this section refers to. Add descriptions of these widgets. -->

### Add or remove widgets

1. Click **[!UICONTROL Customize]** in the Insights header.

   A side panel opens. It lists every widget as a card that shows a preview, the widget name, and a description.

1. To show or hide a widget, click its card, or click the **[!UICONTROL Add widget]** or **[!UICONTROL Remove widget]** button on the card.

   Widgets that are shown have a checkmark.

Your choices are saved per browser. Widgets that are added in later releases appear in the panel automatically.

If you remove all of the widgets, the page displays a "No widgets on this page" message.

### Change the order of widgets

1. Click **[!UICONTROL Customize]** in the Insights header.
1. Drag a widget card to a new position in the panel.

   A dashed placeholder and a drop bar show where the card will land.

The new order is saved with your layout.

>[!NOTE]
>
>You can reorder widgets only by dragging them with the mouse. Reordering with the keyboard is not supported.

## Refresh the Insights dashboard

To reload the data of every widget, click **[!UICONTROL Refresh]** next to **[!UICONTROL Customize]**.

* Each widget keeps its filters.
* The **[!UICONTROL Refresh]** button shows a pending state until all widgets finish loading.
* Charts keep the previous chart under a loading spinner, and the Executions Log dims its table under a spinner while the data reloads.
* If a refresh fails, widgets keep their last good data.

## Take the Insights tour

The first time you open the Insights dashboard, a welcome dialog gives you the option to start a tour or skip it.

The tour highlights each widget, in your saved order, as well as the **[!UICONTROL Customize]** button and panel, the **[!UICONTROL Refresh]** button, and the **[!UICONTROL Replay tour]** button in the title bar.

To restart the tour at any time, click **[!UICONTROL Replay tour]** in the title bar.

The tour does not start when you open the Insights dashboard from a link in a scenario. For more information, see [Open the Insights dashboard from a scenario](#open-the-insights-dashboard-from-a-scenario) in this article.

<!-- BECKY CHECK ME: Confirm that "Replay tour" is the button label and that the tour remembers that you've seen it for each user, not per browser. -->

## Search for scenarios and teams by ID

In the **[!UICONTROL Organization Operations]** and **[!UICONTROL Top Scenarios by Operations]** widgets, the **[!UICONTROL Scenario]** and **[!UICONTROL Team]** fields match on ID as well as name. Each option shows its ID under the name, for example "ID 123".

* The lists load the first 500 scenarios and the first 200 teams. If you enter an ID that is not in the loaded list, Fusion looks it up automatically after a short delay.
* If you clear a scenario, the team that was filled in automatically for that scenario is also cleared.

>[!NOTE]
>
>The scenario filter in the Executions Log does not match on ID.

## Open the Insights dashboard from a scenario

You can open the Insights dashboard with the **[!UICONTROL Organization Operations]** widget filtered to a specific scenario and team.

<!-- BECKY CHECK ME: The request says the entry point is the scenario's Reports tab in the shell. Confirm the tab name, the control that the user clicks, and the exact steps. -->

When the link includes a valid scenario and team:

* The **[!UICONTROL Organization Operations]** widget opens filtered to that scenario and team, and the page scrolls to the widget.
* If you have removed the widget from the page, a warning with an **[!UICONTROL Add widget]** button appears instead.
* If the scenario was deleted or is unknown, the filter is ignored.

A link without a valid scenario and team opens the dashboard as usual.

## Use dark mode

The Insights dashboard and its widgets automatically follow your dark mode setting. When you change the setting, the page updates immediately, without reloading, and keeps your current state. Light mode is unchanged.

<!-- BECKY CHECK ME: The request says dark mode "requires the matching fusion-frontend change; without it the page stays light". Confirm that both parts have shipped, and confirm where users change the dark mode setting (the source calls it the Unified Shell's dark mode setting) and how to refer to it in customer docs. -->

## Performance widget access

The **[!UICONTROL Performance]** widget is shown only to users who have one of the following permissions:

* Organization Edit in the active organization
* Organization View on the admin page

The widget is hidden from the page and from the **[!UICONTROL Customize]** panel for other users. If a user is granted access later, the widget returns in its saved position. Opening the Insights URL directly does not bypass this check.

<!-- BECKY CHECK ME: Confirm the permission names ("Organization Edit", "Organization View") and where an administrator grants them. -->

## Filter and triage executions in the Execution Log

Use the Execution Log to find scenario executions that failed or returned a warning across your organization, and reactivate any scenarios that were automatically deactivated after repeated failures.

1. In the Execution Log, filter executions by any of the following:

   * [!UICONTROL Team]
   * [!UICONTROL Scenario]
   * [!UICONTROL Run type]
   * [!UICONTROL Date range]
   * [!UICONTROL Deactivation state]
   * [!UICONTROL Error message]

   For most filters, you can choose to match only the values you select, or everything except them.

1. Click an execution to view more detail about its error.
1. To reactivate one or more scenarios that were automatically deactivated after repeated failures, select the executions, then click **Activate**.

   >[!NOTE]
   >
   >Before reactivating a scenario, investigate the cause of the failures, such as expired credentials or a connector issue, so the scenario doesn't immediately fail again.
