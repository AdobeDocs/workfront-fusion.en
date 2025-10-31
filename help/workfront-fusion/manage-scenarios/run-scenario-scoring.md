---
title: Run the Scenario Scoring Expert
description: The Scenario Scoring Expert can help you ensure that your scenario is configured in a way that follows best practices. It checks your scenario and gives recommendations for its structure and organization.
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
---
# Run the Scenario Scoring Expert

>[!IMPORTANT]
>
>The Scenario Scoring Expert has been temporarily disabled.

The Scenario Scoring Expert can help you ensure that your scenario is configured in a way that follows best practices. It checks your scenario and gives recommendations for its structure and organization.

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

+++

## Run the Scenario Scoring Expert

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to run the Scenario Scoring Expert.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Click the Scenario Scoring Expert icon ![Scenario scoring expert](assets/scoring-expert-icon.png) near the bottom of the screen.

   The Scenario Scoring Expert panel opens.
1. Click **Evaluate**.

The Scenario Scoring Expert returns a score out of 10, and shows which checks have passed or failed. If a check has failed, the Scenario Scoring Expert gives recommendations for how to ensure that the scenario meets these checks.

![Scenario score](assets/scenario-score.png)

## Scenario scoring checks

The Scenario Scoring Expert uses the following checks:

* The scenario must be named.
* All modules must be labeled.
* The scenario must run on a set schedule.

   For instructions, see [Schedule a scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
* The scenario blueprint size must be under 5 MB.

   For more information, see [Fusion performance guardrails](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#scenarios).
* If a Workfront instant trigger module is used, it must be filtered.
   
   For instructions, see [Event subscription filters in the Workfront > [!UICONTROL Watch Events] module](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules).
