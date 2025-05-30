---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Add a filter to a basic scenario
description: Filters allow you to ensure that your scenario progresses only if certain conditions are met.
author: Becky
feature: Workfront Fusion
exl-id: 78ab27fe-e2dd-4b52-b986-77b4b7ea3b5e
---
# Add a filter to a basic scenario 

Filters allow you to ensure that your scenario progresses only if certain conditions are met. 

In this example, you will add a filter to your scenario that allows a new project to be created from a request only if the request was submitted to a specific request queue.

This example modifies the scenario created in [Create a basic scenario](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

>[!NOTE]
>
>Workfront trigger modules include filters that allow a scenario to start only if certain conditions are met. However, because between-module filters are used for every non-trigger and non-Workfront use case, it is important to learn how to use filters between modules. This example uses a between-module filter for functionality that could be met with an in-module filter.

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
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

You must create the scenario described in [Create a basic scenario](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) before following this procedure.

## Add a filter 

### Prepare to add the filter

1. Open the scenario.
1. Click the first module to open it.
1. In the **Outputs** area, select `Project`. 
   You should now have `ID`, `Name`, and `Project` selected.
1. Click OK to save the module settings.
1. Open Workfront. 
1. In Workfront, locate the project that represents the request queue that the Fusion scenario will be working with. 

   This project must be in the same Workfront account that the Fusion connection is set up for.
   
1. Make note of the project ID in the URL.

   Example: https://\<MyDomain\>.my.workfront.com/project/\<ProjectID\>/tasks

### Add and configure the filter

1. Return to the scenario in the scenario editor.
1. Click the wrench icon ![Wrench icon](assets/wrench-icon.png) between the first and second module, and select **Set up a filter**.
1. In the Label field, enter a label for this filter, such as "Filter for request queue."
1. In the **Condition** area, in the top field, map the `projectID` from the first module.

   ![Map project ID](assets/map-proj-id.png)
1. Leave the **Condition** operator as Equal to.
1. In the bottom field of the **Condition** area, paste in the project ID that you made note of from the project URL in [Prepare to add the filter](#prepare-to-add-the-filter).
1. Click **OK** to save the filter settings.

### Test and activate

1. Go to the Workfront environment that Fusion is connecting to and add an issue to the project that you specified in the filter. Add another issue to a different project. 
1. Click **[!UICONTROL Run once]** in the lower-left corner of the scenario editor.
1. Examine the output to ensure that the scenario ran as expected.

   Both issues should appear in the output of the first module, but only the issue in the specified project should appear as input into the second module.
1. When you are satisfied that the scenario is working as expected, click the **Scheduling** toggle in the lower-left of the screen to **On**.

   This activates the scenario. 
1. In [!DNL Workfront Fusion], click **[!UICONTROL Save]** near the lower-left corner to save your progress on the scenario.

   >[!IMPORTANT]
   >
   >Save often as you hone and test a scenario.

## Resources

* For more information on filters, see [Add a filter to a scenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).
