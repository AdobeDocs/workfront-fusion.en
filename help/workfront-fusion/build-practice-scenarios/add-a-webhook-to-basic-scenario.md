---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Add a webhook to a basic scenario
description: Webhooks, also known as instant triggers, are a specific kind of trigger module that can start a scenario whenever a change is made, instead of on a given schedule.
author: Becky
feature: Workfront Fusion
---
# Add a webhook to a basic scenario

Webhooks, also known as instant triggers, are a specific kind of trigger module that can start a scenario whenever a change is made, instead of on a given schedule. 

In this example, you will add a webhook to start a scenario as soon as any requests have been submitted to a specific queue. The scenario then converts those requests to a project.

This example modifies the scenario created in [Create a basic scenario](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

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

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

You must create the scenario described in [Create a basic scenario](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) before following this procedure.

## Add and configure the webhook

1. Open the Convert object module.
1. In the Issue ID field, delete the black ID block. The block is black because the module it was mapped from is no longer available.
1. Select the ID block under the first module (Watch Events) to map it to the second module.
1. Click **OK**.

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
