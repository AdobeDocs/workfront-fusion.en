---
title: Configure a webhook for a web service without a connector
description: If a web service does not currently have a dedicated connector in Workfront Fusion, but it supports sending webhooks, you can add the service to a scenario using the Custom webhook module as an instant trigger.
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
---
# Configure a webhook for a web service without a connector

If a web service does not currently have a dedicated connector in Workfront Fusion, but it supports sending webhooks, you can add the service to a scenario using the Custom webhook module as an instant trigger. This process is called receiving a webhook, and it requires some configuration on the side of the application you are connecting to.

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

## Receive a webhook

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a webhook.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Add the **Webhooks > Custom webhook** module to begin your scenario.
1. Click **Add** next to the Webhook field.
1. Enter a **Webhook name** in the box that displays
1. (Optional) configure the webhook. 

   For instructions, see [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).
   
1. Click **Save**.

1. Click **Copy address to clipboard**, then click **OK**.

1. Log in to the web service and do the following there:

   1. In the Settings area for the web service, create a webhook.

      Specific instructions depend on the application. We recommend searching the application's documentation for "Create a webhook."
   1. Paste the address you copied to your clipboard in step 3.
   1. Select the event that will trigger the webhook.

1. Run the scenario.

   When the event or events occur, the Custom webhook module triggers and the scenario runs.
