---
title: Explain a scenario error with AI
description: When a scenario run fails, you can click Explain next to the error to get a short, plain-language description of what went wrong and how to fix it.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
---
# Explain a scenario error with AI

When a scenario run fails, you can click **[!UICONTROL Explain]** next to the error. AI gives you a short, plain-language description of what went wrong and how to fix it. The explanation appears next to the original error, so you can read both together.

You can explain errors in the following areas of Workfront Fusion:

* The module error details in the scenario designer
* The run details in a scenario's execution history
* The [!UICONTROL Failed executions] table on the Insights page

<!-- BECKY CHECK ME: The Slack request calls it the "Failed executions table" on the Insights page. The existing Insights dashboard article calls it the "Failed Executions Logs" table and the "Execution Log". Confirm the label in the UI. -->

>[!NOTE]
>
>The **[!UICONTROL Explain]** button is available only in the new scenario designer. It is not available in the legacy scenario designer.

## Access requirements

<!-- BECKY CHECK ME: This table is copied from other Fusion articles. The source says only that the organization needs an AI license. Confirm whether the access requirements are the same. -->

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

## Prerequisites

Your organization must have an AI license.

<!-- BECKY CHECK ME: Confirm the name of the license and whether there is an existing article to link to. -->

## How the Explain button works

* The **[!UICONTROL Explain]** button is a pill with an AI gradient. When you hover over it, the tooltip "Explain with AI" appears.
* The explanation appears under the error. To hide the explanation, click **[!UICONTROL Explain]** again.
* Explanations are short, about 100 words at most.
* While AI generates the explanation, a loading state appears. If the explanation fails to generate, click **[!UICONTROL Try again]**.
* If your organization reaches its AI usage limit, a usage-limit message appears instead of an explanation.

## Explain an error in the scenario designer

1. Open the scenario in the scenario designer, and run the scenario.
1. When a module fails, open the module's error details.
1. Click **[!UICONTROL Explain]**.

   The button is under the error, below "More information about error handling."

The explanation appears under the error.

## Explain an error in a scenario's execution history

1. Click the **[!UICONTROL Scenarios]** tab in the left panel, then click the scenario.
1. Click **[!UICONTROL History]** near the name of the scenario.
1. Click the failed run that you want to view.

   Each error in the run details has an **[!UICONTROL Explain]** button under it.

1. Click **[!UICONTROL Explain]** under the error that you want explained.

   If several modules failed in the run, you can explain each error on its own.

For more information about viewing a run, see [View a scenario's execution history](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md) and [View a specific scenario execution](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md).

## Explain an error on the Insights page

1. In Fusion, click **[!UICONTROL Insights]** in the left navigation.
1. In the [!UICONTROL Failed executions] table, hover over the failed row that you want to view.

   An **[!UICONTROL Explain]** button appears.

1. Click **[!UICONTROL Explain]**.

   A popup opens that shows the error and the AI explanation.

For more information about the Insights page, see [View the Insights dashboard for an organization](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/view-insights-dashboard.md).
