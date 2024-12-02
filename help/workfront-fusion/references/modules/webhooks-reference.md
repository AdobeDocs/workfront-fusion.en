---
title: Instant triggers (webhooks)
description: Many services provide webhooks to deliver instant notifications whenever a certain change occurs in the service. To process these notifications, we recommend that you use instant triggers. This article describes the use and functionality of instant triggers in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
---
# Instant triggers (webhooks)

<!--Add more info from the webhooks article in apps and their modules-->

Many services provide webhooks to deliver instant notifications whenever a certain change (event) occurs in the service. To process these events, we recommend that you use instant triggers. Instant triggers display the `Instant` tag in the list of modules for a given connector.

![](/help/workfront-fusion/references/apps-and-modules/assets/instant.png)

If a connector does not include a webhook, you can do one of the following:

* Create a custom webhook using the Webhook module.
   <!--For more information, see [Webhooks]()-->
* Use polling triggers to periodically poll the service.
   <!--For more information see [Schedule a scenario]()-->

For a video introduction to webhooks in Workfront Fusion, see:

* [Intro to Webhooks](https://video.tv.adobe.com/v/3427025/){target=_blank}
* [Intermediate Webhooks](https://video.tv.adobe.com/v/3427030/){target=_blank}

## Schedule instant triggers

When you configure an instant trigger, you are prompted to select when it runs.

![](/help/workfront-fusion/references/apps-and-modules/assets/schedule-setting.png)

Select `Immediately` to run the scenario immediately when [!DNL Workfront Fusion] receives new events from the service. These events go into a queue, and are then processed in the scenario one at a time.

When the scenario executes, the total amount of pending events waiting in the queue is counted, and the scenario performs as many cycles as there are pending events, processing one event per cycle.

>[!NOTE]
>
>* A cycle is not the same as a scenario run. There can be multiple cycles within one scenario run. 
>* When you execute a scenario with an instant trigger scheduled to be run `Immediately`, the following exceptions apply:
>
>     * The interval between two executions is not subject to the minimum interval according to the pricing plan.
>
>       For example, once the scenario finishes its execution, the webhook's queue is checked again. If there are any pending webhooks, the scenario executes immediately again, processing all the pending webhooks once again.
>   
>     * The Maximum number of cycles scenario setting is ignored and set to 100, which means that no more than 100 pending webhooks will be processed during a single scenario execution (at the rate of 1 event per cycle).
>


If you use any other schedule setting than [!UICONTROL Immediately], the scenario executes at the intervals you specify. Because several webhooks can be gathered in the queue during the interval, we recommend setting the [!UICONTROL Maximum number of cycles] option to a higher value than the default 1 to process more webhooks in one scenario run:

1. Click the [!UICONTROL Scenario settings] icon ![](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png) at the bottom of your scenario.
1. In the **[!UICONTROL Scenario settings]** panel that appears, enter a number in the **[!UICONTROL Max number of cycles]** field to indicate the number of events from the queue that you want to run each time you execute the scenario. 

Events remaining in the queue will be processed next time the scenario is run, up to the number set in the Max number of cycles field.

## Webhook guardrails

To ensure good performance, Workfront Fusion has the following guardrails in place for webhooks:

### Rate limits

The current rate limit is 5 webhooks per second. If the limit is exceeded, a `429` status code is returned.

### Expiration of inactive webhooks

A webhook that has not been assigned to any scenario for more than 120 hours is removed.

### Webhook payloads

[!DNL Workfront Fusion] stores webhook payloads for 30 days. Accessing a webhook payload more than 30 days after it was created results in the error [!UICONTROL `Failed to read file from storage.`]

### Error handling

When there is an error in your scenario with an instant trigger, the scenario:

* Stops immediately when the scenario is set to run [!UICONTROL Immediately].
* Stops after 3 unsuccessful attempts (3 errors) when the scenario is set to run as scheduled.

If an error occurs during the scenario execution, the event is placed back into the queue during the instant trigger's rollback phase. In such a situation, you can fix the scenario and run it again. 

For more information, see [Rollback](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) in the article Scenario execution, cycles, and phases.

If there is a Webhook response module in your scenario, the error is sent to the Webhook response. The Webhook response module is always executed last (when the [!UICONTROL Auto commit] option in the Scenario settings is not enabled). 

<!--For more information, see [Responding to webhooks](../../workfront-fusion/apps-and-their-modules/webhooks-updated.md#respondi) in the article [Webhooks](../../workfront-fusion/apps-and-their-modules/webhooks-updated.md).-->

### Webhook deactivation

Webhooks are deactivated automatically if either of the following applies:

* The webhook has not been connected to any scenario for more than 5 days.
* The webhook is used only in inactive scenarios, which have been inactive for more than 30 days.

Deactivated webhooks are deleted and unregistered automatically if they are not connected to any scenarios, and have been in deactivated status for over 30 days.

## Custom webhooks

You can create your own webhooks. <!--For more information, see [Webhooks](../../workfront-fusion/apps-and-their-modules/webhooks-updated.md).-->

## Resources

For more information on cycles, see [Scenario execution, cycles, and phases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).




