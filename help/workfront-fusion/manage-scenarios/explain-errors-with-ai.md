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

When a scenario run fails, AI can give you a short, plain-language description of what went wrong and how to fix it. The explanation appears next to the original error, so you can read both together.

You can explain errors in the following areas of Workfront Fusion:

* The module error details in the scenario designer
* The run details in a scenario's execution history
* The [!UICONTROL Failed Executions Logs] table on the Insights page

>[!NOTE]
>
>The **[!UICONTROL Explain]** button is available only in the new scenario designer. It is not available in the legacy scenario designer.

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

## Explain an error in the module output details

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to explain an error.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Run the scenario, either as scheduled, or by clicking **Run once**.
1. When a module fails, open the module's error details.
1. Click **[!UICONTROL Explain]**.

   The button is under the error.

   ![Explain error in module output](assets/explain-in-module-output.png)

The explanation appears under the error.

>[!NOTE]
>
> * While AI generates the explanation, a loading state appears.
> * If the explanation fails to generate, click **[!UICONTROL Try again]**.
> * If your organization reaches its AI usage limit, a usage-limit message appears instead of an explanation.

## Explain an error in a scenario's execution history

1. Click the **[!UICONTROL Scenarios]** tab in the left panel, then click the scenario.
1. Click **[!UICONTROL History]** near the name of the scenario.
1. Click the failed run that you want to view.

   Each error in the run details has an **[!UICONTROL Explain]** button under it.

1. Click **[!UICONTROL Explain]** under the error that you want explained.

   If several modules failed in the run, you can explain each error on its own.

   ![Explain in execution history](assets/explain-in-execution-details.png)

For more information about viewing a run, see [View a scenario's execution history](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md) and [View a specific scenario execution](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md).

>[!NOTE]
>
> * While AI generates the explanation, a loading state appears.
> * If the explanation fails to generate, click **[!UICONTROL Try again]**.
> * If your organization reaches its AI usage limit, a usage-limit message appears instead of an explanation.

## Explain an error on the Insights page

1. In Fusion, click **[!UICONTROL Insights]** in the left navigation.
1. In the [!UICONTROL Failed executions] table, hover over the failed row that you want to view.

   An **[!UICONTROL Explain]** button appears.

1. Click **[!UICONTROL Explain]**.

   ![Explain in insights page](assets/explain-failed-execution-log.png)

   A popup opens that shows the error and the AI explanation.

For more information about the Insights page, see [View the Insights dashboard for an organization](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/view-insights-dashboard.md).

>[!NOTE]
>
> * While AI generates the explanation, a loading state appears.
> * If the explanation fails to generate, click **[!UICONTROL Try again]**.
> * If your organization reaches its AI usage limit, a usage-limit message appears instead of an explanation.
