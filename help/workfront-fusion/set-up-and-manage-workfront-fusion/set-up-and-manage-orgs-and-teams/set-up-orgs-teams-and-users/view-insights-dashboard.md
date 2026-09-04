---
title: View the Insights dashboard for an organization
description: Fusion administrators can view a dashboard that shows execution metrics for an organization.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
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
* **Execution Log**
   This table lists every failed or warning scenario execution across your organization, so you can find and troubleshoot problem runs without leaving the dashboard.

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

   <!-- BECKY CHECK ME: confirm this button's exact label against the live UI. The Slack feature request calls it "Activate," but a related community post describes the same action as "Reactivate." -->

   Before reactivating a scenario, investigate the cause of the failures, such as expired credentials or a connector issue, so the scenario doesn't immediately fail again.
