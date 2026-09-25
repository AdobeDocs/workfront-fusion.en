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

## Worker pool overview

A worker pool is a way to process scenario executions in parallel. Each worker pool is associated with: 

* A number of workers.
* An execution queue.

When a scenario is executed, it passes into the worker pool's execution queue. Workers in the pool continuously pull tasks from the execution pool and process them in parallel.

If the execution queue depth increases, and all existing workers are being used, Workfront Fusion automatically scales the pool by adding more workers. This scaling is dynamic and event-driven, meaning capacity exacts or contracts based on real-time load without action from your or your organization.

The Workfront Fusion team continuously monitors utilization and scaling behavior of pools, and can review thresholds or patterns to ensure consistent performance as usage grows.
