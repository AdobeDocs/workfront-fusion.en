---
title: Edit Webhooks
description: You can edit existing webhooks for the Workfront and Workfront Planning connectors.
author: Becky
feature: Workfront Fusion
exl-id: 7bedf002-061b-40fc-a0f8-c12d2930bcf9
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



### Edit a webhook from the Webhooks list

