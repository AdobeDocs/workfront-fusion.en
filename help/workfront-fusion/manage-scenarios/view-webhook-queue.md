---
title: k's queue
description: Many services provide webhooks to deliver instant notifications whenever a certain change occurs in the service. Instant triggers, also known as webhooks, can use these events to begin scenarios. The events go into the webhook's queue while they are awaiting processing, such as when the scenario is already running. You can view the webhook's queue.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
---
# View a webhook's queue

Many services provide webhooks to deliver instant notifications whenever a certain change occurs in the service. Instant triggers, also known as webhooks, can use these events to begin scenarios. The events go into the webhook's queue while they are awaiting processing, such as when the scenario is already running. You can view the webhook's queue.

Incoming webhook data is always stored in the queue regardless of how you have set the Data is confidential option in the scenario settings panel. After the data is processed in a scenario, it is permanently deleted from the queue.

For more information on webhooks, see [Instant triggers (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

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

## View a webhook's queue

All messages from incoming webhooks are stored in the webhook's queue.

If a scenario currently has a queue, a banner displays in that scenario:

![Queue banner](assets/queue-banner.png)

To view a webhook's queue:

1. Click **[!UICONTROL Webhooks]** in the menu on left.
1. Locate the Webhook for which you want to view the queue.
1. Locate the number of events in the Events received button. 

   ![Webhook queue](assets/webhook-queue.png)
   
1. Click the button to view details about events in the queue.
