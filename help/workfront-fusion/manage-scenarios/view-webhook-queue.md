---
title: View a webhook's queue
description: Many services provide webhooks to deliver instant notifications whenever a certain change occurs in the service. Instant triggers, also known as webhooks, can use these events to begin scenarios. The events go into the webhook's queue while they are awaiting processing, such as when the scenario is already running. You can view the webhook's queue.
author: Becky
feature: Workfront Fusion
---
# View a webhook's queue

<!--audited 11/2024-->

Many services provide webhooks to deliver instant notifications whenever a certain change occurs in the service. Instant triggers, also known as webhooks, can use these events to begin scenarios. The events go into the webhook's queue while they are awaiting processing, such as when the scenario is already running. You can view the webhook's queue.


Incoming webhook data is always stored in the queue regardless of how you have set the Data is confidential option in the scenario settings panel. After the data is processed in a scenario, it is permanently deleted from the queue.

For more information on webhooks, see [Instant triggers (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md)

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan</td> 
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

<!--For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md).-->

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## View a webhook's queue

All messages from incoming webhooks are stored in the webhook's queue.

1. Click **[!UICONTROL Webhooks]** in the menu on left.
1. Locate the Webhook for which you want to view the queue.
1. Locate the number of events in the Events received button. 

   ![Webhook queue](/help/workfront-fusion/references/apps-and-modules/assets/webhook-queue.png)
   
1. Click the button to view details about events in the queue.


   