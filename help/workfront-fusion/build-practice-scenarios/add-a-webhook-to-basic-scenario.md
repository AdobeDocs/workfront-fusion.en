---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Add a webhook to a basic scenario
description: Webhooks, also known as instant triggers, are a specific kind of trigger module that can start a scenario whenever a change is made, instead of on a given schedule.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
---
# Add a webhook to a basic scenario

Webhooks, also known as instant triggers, are a specific kind of trigger module that can start a scenario whenever a change is made, instead of on a given schedule. 

In this example, you will add a webhook to start a scenario as soon as any requests have been submitted to a specific request queue. The scenario then converts those requests to a project.

This example modifies the scenario created in [Create a basic scenario](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

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

## Prerequisites

You must create the scenario described in [Create a basic scenario](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) before following this procedure.

## Add and configure the webhook


### Add the webhook module

1. Open the scenario in the scenario editor.
1. Right click on the first module and select **Delete module**.

   The module is deleted, leaving a blank placeholder.

1. Click the blank module, and select **Adobe Workfront** from the list of apps.
1. Select **Watch Events**.
1. Click **Add** next to the Webhook field.
1. in the Record Type field, select **Issue**, so the module will trigger for changes in issues.
1. In the State field, select **New state**. This is a required field that is used for the filter, which this example does not cover.
1. In the Record Origin field, select **New Record Only**. This allows the scenario to trigger when an issue is added, not when one is updated or deleted.
1. Click **Save** to save the module configuration.

## Update the second module

1. Open the scenario.
1. Click the **Convert object** module to open it.
1. In the Issue ID field, delete the black ID block. The block is black because the module it was mapped from is no longer available.
1. Select the ID block under the first module (Watch Events) to map it to the second module.
1. Click **OK**.



### Test and activate

1. Click **[!UICONTROL Run once]** in the lower-left corner of the scenario editor.

   The scenario must be running to watch for the new request.
1. Go to the Workfront environment that Fusion is connecting to and add an issue. 

   The scenario should run.
1. Examine the output to ensure that the scenario ran as expected.
1. When you are satisfied that the scenario is working as expected, click the **Scheduling** toggle in the lower-left of the screen to **On**.

   This activates the scenario. 
1. In Workfront Fusion, click **[!UICONTROL Save]** near the lower-left corner to save your progress on the scenario.
