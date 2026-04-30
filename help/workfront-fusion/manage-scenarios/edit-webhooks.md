---
title: Edit Webhooks
description: You can edit existing webhooks for the Workfront and Workfront Planning connectors.
author: Becky
feature: Workfront Fusion
---
# Edit webhooks

You can edit existing webhooks. Scenarios that use these webhooks will use the new configuration moving forward, which eliminates the need to create a new webhook and manually assign it to all affected scenarios.

Webhooks can be edited for only the following connectors:

* Workfront
* Workfront Planning

>[!IMPORTANT]
>
>Consider the following when updating a webhook:
>
>* The edited webhook is treated by Workfront event subscriptions as a new subscription. Event subscription history is not preserved for the previous webhook configuration, because that is considered a separate event subscription.
>* The switch from old to new event subscription may not be perfectly synchronized. It is therefore possible to receive an event twice (if the new subscription begins running before the old one stops) or to miss an event (if the old subscription stops before the new one begins running). 

## Edit a webhook

You can edit webhooks from a scenario, or from the Webhooks list.

### Edit a webhook in a scenario

>[!NOTE]
>
>This functionality is available only for scenarios that have a Workfront or Workfront Planning instant trigger module.

1. Go to the scenario that includes the webhook you want to edit. 
1. In the scenario's trigger module, click the dropdown next to the Webhook field, and select **Edit item**.
   
   The webhook's configuration window opens, populated with the existing configuration.

1. Make any desired edits to the webhook.
1. Click **Save** to save the webhook and return to the module.

### Edit a webhook from the Webhooks list

1. In the left navigation, select **Webhooks** ![Webhooks icon](assets/webhooks-icon.png).
1. Click the checkbox next to the webhook you want to edit.
1. In the blue banner at the bottom of the screen, click **Edit**.
1. Make any desired edits to the webhook.
1. Click **Save** to save the webhook and return to the Webhooks list.

