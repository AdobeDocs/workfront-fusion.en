---
title: View the performance dashboard for an organization
description: Fusion administrators can view a dashboard that shows execution metrics for an organization.
author: Becky
feature: Workfront Fusion
hide: yes
hidefromtoc: yes
---
# View the performance dashboard for an organization

The Fusion Performance Dashboard allows you to quickly see which scenarios are running the most, where delays are occurring, and how effectively your worker pools are operating. This provides real-time visibility into execution volumes, queue depth, pool utilization, and scenario-level performance.

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

## Performance dashboard components

In the Fusion performance dashboard, you can see the following metrics.

* Executions waiting to be processed
   This chart shows the number of executions waiting to be processed at a given point in time. 
* Pool Utilization
   This chart shows worker pool utilization over time. If this chart routinely shows worker pool utilization, you may want to assign some scenarios to another pool.
* Executions per scenario
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.
* Duration of executions
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

## View the Fusion Performance Dashboard

1. In Fusion, click Performance in the left navigation.
  
   The Dashboard opens.

1. To view data for a specific point in time, hover over a dashboard and adjust your cursor to be over the point in time you want to view.

   A line appears over that point in time on all the graphs, and a window showing data for that time appears on each graph.
1. To view data for a specific scenario in the Executions per scenario chart or the Duration of executions chart, click on a bar of the color for the scenario you want to view data for. To return to the view showing all scenarios, click on the graph again.
1. To go to a specific scenario shown in the Executions per scenario chart or the Duration of executions chart, right click on a bar of the color for the scenario, and select **Open scenario in new tab**.
1. To expand a chart, click the **Expand** icon ![Expand icon](assets/expand-icon.png) at the upper-right corner of that chart.
1. To change the time range of the dashboard, the Time Range field in the upper-right corner of the dashboard, then select a new time frame. The longest available time frame is 24 hours, and the shortest is 15 minutes.
1. To refresh the charts, click the Refresh icon near the upper-right corner of the dashboard.
1. To view a different worker pool, click the Pool field near the upper-left corner of the dashboard, then select the pool you want to view.



