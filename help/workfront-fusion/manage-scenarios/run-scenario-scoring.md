---
title: Run the Scenario Scoring Expert
description: The Scenario Scoring Expert can help you ensure that your scenario is configured in a way that follows best practices. It checks your scenario and gives recommendations for its structure and organization.
author: Becky
feature: Workfront Fusion
---
# Run the Scenario Scoring Expert

The Scenario Scoring Expert can help you ensure that your scenario is configured in a way that follows best practices. It checks your scenario and gives recommendations for its structure and organization.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] package</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] license</td> 
   <td> <p>New: [!UICONTROL Standard]</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] license**</td> 
   <td>
   <p>Current: No [!DNL Workfront Fusion] license requirement.</p>
   <p>Or</p>
   <p>Legacy: Any </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan: [!DNL Workfront Fusion] is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Access level configurations*</td> 
   <td> 
     <p>You must be a [!DNL Workfront Fusion] administrator for your organization.</p>
     <p>You must be a [!DNL Workfront Fusion] administrator for your team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Run the Scenario Scoring Expert

1. Click the **[!UICONTROL Scenario]** tab in the left panel.
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
   
   For instructions, see [Event subscription filters in the [!DNL Workfront] > [!UICONTROL Watch Events] module](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules).

