---
title: Worker Pools
description: A worker pool is a quantity of Workfront Fusion processing resources dedicated to one or more specific organizations. All Fusion operations and processing happen within the context of an organization's assigned worker pool.
author: Becky
feature: Workfront Fusion
exl-id: 8bf508a8-d1f9-455f-af89-62f688289137
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
---
# Worker pools

A worker pool is a quantity of Workfront Fusion processing resources dedicated to a specific organization. All Fusion operations and processing happen within the context of an organization's assigned worker pool.

Worker pools allow your scenarios to run more efficiently, and eliminate the chances of competing with other organizations for Fusion processing capacity. 

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

## Worker pool overview

A worker pool is a way to process scenario executions in parallel. Each worker pool is associated with: 

* A number of workers.
* An execution queue.

When a scenario is executed, it passes into the worker pool's execution queue. Workers in the pool continuously pull tasks from the execution pool and process them in parallel.

If the execution queue depth increases, and all existing workers are being used, Workfront Fusion automatically scales the pool by adding more workers. This scaling is dynamic and event-driven, meaning capacity exacts or contracts based on real-time load without action from your or your organization.

The Workfront Fusion team continuously monitors utilization and scaling behavior of pools, and can review thresholds or patterns to ensure consistent performance as usage grows.

## Rename a worker pool

Organization owners and admins can rename the worker pools assigned to their organization. Each pool shows a system-generated name by default. You can give a pool a custom name, such as `Marketing EU` or `High-volume integrations`, and change it whenever you need to.

Renaming a pool changes only how it is labeled. Scenarios, executions, and pool capacity are not affected. The new name appears wherever the pool is shown, such as when you assign scenarios to a pool.

>[!NOTE]
>
>The **[!UICONTROL Worker pools]** tab appears only when more than one worker pool is assigned to your organization. If your organization has a single worker pool, or uses the shared pool, you do not see the tab.

To rename a worker pool:

1. In the left navigation, click **Org overview**
1. Click the **[!UICONTROL Worker pools]** tab, near the top of the page.

   The tab lists each pool and shows how many scenarios are assigned to it.

1. Click **[!UICONTROL Rename]** next to the pool that you want to rename.
1. In the panel that opens, enter the new name.
1. Click **Save**.
