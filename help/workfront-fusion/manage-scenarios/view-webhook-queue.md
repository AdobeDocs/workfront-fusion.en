---
title: k's queue
description: Many services provide webhooks to deliver instant notifications whenever a certain change occurs in the service. Instant triggers, also known as webhooks, can use these events to begin scenarios. The events go into the webhook's queue while they are awaiting processing, such as when the scenario is already running. You can view the webhook's queue.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
TQID: 'https://experienceleague.adobe.com/FtTjoNtYNM9kuPDMaHa4883m13pLO2MRat5ohnjXuAM'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
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

   The webhook's queue page opens. The page lists the events in the queue in a table with the following columns: **[!UICONTROL ID]**, **[!UICONTROL Created at]**, **[!UICONTROL Size]**, and **[!UICONTROL Details]**.

<!-- BECKY CHECK ME: The request does not describe how to open the queue page. The steps above are from the existing article. Confirm that clicking the Events received button still opens the queue page, and retake the Webhook queue screenshot above if the Webhooks list changed. -->

<!-- BECKY CHECK ME: Add a screenshot of the queue page. The screenshot in the Slack thread is from a staging org, so retake it in a production environment. -->

## Manage events in a webhook's queue

The queue page has the same layout as the **[!UICONTROL Scenarios]** and **[!UICONTROL Webhooks]** lists.

>[!NOTE]
>
>Search and sorting apply only to the events that are currently loaded in the table, not to the entire queue. To include more events, load additional events first.

### Search for events

To filter the events in the table, enter text in the **[!UICONTROL Search]** field above the table.

### Sort events

To sort the events, click the sort icon in the **[!UICONTROL ID]**, **[!UICONTROL Created at]**, or **[!UICONTROL Size]** column header.

<!-- BECKY CHECK ME: Confirm whether clicking the sort icon again reverses the sort order, and whether the sort icon shows the current direction. -->

### Change the page size, navigate pages, and load more events

Use the controls below the table to change the number of events that display on each page, move between pages, and load additional events.

<!-- BECKY CHECK ME: The request mentions changing the page size, navigating pages, and loading additional entries, but the screenshot does not show these controls. Confirm their labels and location, the available page sizes, and how many events load at a time. -->

### View an event's payload

1. In the row for the event, click **[!UICONTROL Details]**.

   The details dialog opens and displays the event's payload.

<!-- BECKY CHECK ME: Confirm what the details dialog shows (for example, only the payload, or also the ID and creation date) and how to close it. The request says the dialog is updated, but does not describe what changed. -->

### Select and delete events

1. Select the checkbox next to each event that you want to select.

   Or

   Select the **[!UICONTROL Select all]** checkbox to select the entire queue, not just the events that are currently loaded. You can then clear the checkbox for any events that you want to exclude from the selection.

1. Delete the selected events.

   Deleting all events empties the queue. It does not delete the webhook.

<!-- BECKY CHECK ME: The request does not say where the delete button appears, what it is labeled, or whether a confirmation dialog appears. Confirm the label and the step. Also confirm that Select all selects every event in the queue (not just the loaded ones), and how the exclusions work. -->
