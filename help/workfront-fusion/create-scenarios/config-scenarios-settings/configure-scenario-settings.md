---
content-type: reference
title: Configure scenario settings
description: You can configure specific settings for scenarios in the scenario settings panel.
author: Becky
feature: Workfront Fusion
exl-id: 105e3d39-b0ef-4c22-901d-fb4f29e685a9
---
# Configure scenario settings

You can configure specific settings for scenarios in the scenario settings panel. 

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
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] Plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Access level configurations*</td> 
   <td> 
     <p>You must be a [!DNL Workfront Fusion] administrator for your organization.</p>
     <p>You must be a [!DNL Workfront Fusion] administrator for your team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Open the scenario settings

1. Click **Scenarios** in the left panel.
1. Find the scenario you want, then click the name.
1. Click anywhere on the scenario to enter the scenario editor.
1. Click the gear icon near the lower-left corner of the page.

   ![Scenario settings](assets/scenario-settings-350x221.png)

   In the [!UICONTROL Scenario settings] panel that displays, you can configure various advanced settings for the scenario.
1. Enable or disable the Scenario settings as needed. See [Scenario settings options](#scenario-settings-options) below.

## Scenario settings options

### [!UICONTROL Sequential processing]

This option forces all executions to happen in order and is primarily relevant for Webhooks and for Incomplete Executions.

When sequential processing is enabled, parallel executions of the scenario are disabled.

**Instant Webhooks**: If a webhook trigger is configured as `instant` and "Sequential processing" is enabled, then all instant webhook payloads will be queued and processed in the order that they arrive. This can be useful when processing events from external systems in an exact order.

   >[!NOTE]
   >
   >There will be automatic processing delays as each payload is processed before the next is started.

**Incomplete Executions**: If "Incomplete Executions" is also enabled, if an error occurs during the execution of a scenario, the scenario is paused. One of the following then occurs:

* If the Sequential processing option is **enabled**, Workfront Fusion stops processing the pre-existing sequence until all incomplete executions are resolved.
* If the Sequential processing option is **disabled**, the scenario continues to run according to its schedule, accompanied by repeated attempts to rerun the incomplete executions.

   For more information on incomplete executions, see [View and resolve incomplete executions](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

   >[!NOTE]
   >
   >Sequential processing may cause a delay in the execution of a scenario. If there are incomplete executions still in the queue when an instant scenario triggers or a scheduled scenario is set to execute, that scenario will execute after all of the executions before it in the queue are complete.
   >
   >If the use case for your scenarios does not require sequential processing, we recommend disabling the sequential processing option.

   For more information on scheduling, see [Schedule a scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

### Data is confidential

Once a scenario has been executed, you can by default display information about which data was processed by modules in the scenario. If you do not want this information to be stored, enable the [!UICONTROL Data is confidential] option.

>[!IMPORTANT]
>
>If you enable this option, it may be difficult to solve errors that may occur during the execution of a scenario.

### [!UICONTROL Allow storing incomplete executions]

This option determines how [!DNL Adobe Workfront Fusion] proceeds if an error occurs during the execution of a scenario. With this option enabled, the scenario is paused and moved to the incomplete execustion folder. This gives you the possibility to fix the issue and continue executing from where the scenario was stopped. If this option is disabled, the scenario run stops and a rollback phase is started.

For more information on incomplete executions, see [View and resolve incomplete executions](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

### Enable data loss

This option has to do with enabling data loss if [!DNL Workfront Fusion] fails to save a bundle to the queue of incomplete executions (for example, due to a lack of free space). With this option enabled, the data is lost in order to prevent interruptions in the overall scenario execution. This is useful for scenarios where the highest priority is continuous execution and the incoming erroneous data is not that important.

Beyond that, when executing a scenario, a module can sometimes encounter a file that is larger than the maximum allowed size. In this case, [!DNL Workfront Fusion] proceeds in accordance with the setting of the [!UICONTROL Enable data loss] option and a warning message is shown.

For more information on incomplete executions, see [View and resolve incomplete executions](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

For more information about maximum file size, see [Fusion performance guardrails](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#files).

For more information on warnings, see [Error types](/help/workfront-fusion/references/errors/error-processing.md).

### [!UICONTROL Auto commit]

The [!UICONTROL Auto commit] settings applies to transactions and defines the way to process a scenario. If the Auto commit option is on, the commit phase on each module starts immediately after completing the operation phase. With the Auto commit option disabled, no commit occurs until operations are executed for all modules (this is the default mode).

### Maximum number of cycles

>[!NOTE]
>
>You must enable the **Show advanced settings** checkbox to see this option.


Setting more cycles can be useful when you want to prevent connection interruption to a third-party service and assure that all records are processed within the one scenario run.

* If the scenario starts with a polling trigger, the setting defines the maximum number of cycles allowed during the scenario execution.

   For more information on polling triggers, see [Polling triggers](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#polling-triggers) in the article Module overview.

* If the scenario starts with an instant trigger, the setting is ignored and all the pending events are processed during a single scenario execution, one event per one cycle.

   For more information on instant triggers, see [Instant triggers](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers) in the article Module overview.

* If the scenario does not start with a trigger (instant/polling), the specified maximum number of cycles is always performed.

>[!BEGINSHADEBOX]

**Examples:**  [!DNL Workfront] > [!UICONTROL Watch record] watches for new issues that come in, and [!DNL Workfront] >[!UICONTROL Convert object] converts the new request into a project and assigns it the appropriate template.

![Scenario settings](assets/scenario-settings-ex-1-350x157.png)

A [!UICONTROL more cycles] setting is applied only when you schedule your scenario execution. When you use the [!UICONTROL Run once] button, cycle settings are taken into account.

#### Max number of cycles is set to 1 (default)

![Maximum number of cycles](assets/max-number-cycles-1-350x201.png)

The Max number of cycles in the Workfront > Watch records module is set to `10`.
If 100 requests are submitted to [!DNL Workfront], and the Max number of cycles field is set to 10, then 90 files are left unprocessed after one scenario run. The next 10 files are processed in the next scheduled scenario execution.

#### Max number of cycles is set to 10

The Max number of cycles in the Workfront > Watch records module is set to `10`.

If 100 files are added to the Dropbox folder and the Max number of cycles option is set to 10, then 10 files are processed during the first cycle, the next 10 files in the second cycle, the next 10 files in the third cycle and so on, until all files are processed.

All files are processed within 1 scenario run.

You can see the already-run cycles in the Scenario details:

![Scenario detail](assets/scenario-detail-350x207.png)

For more information about this page, see [Scenario details](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-details.md).

>[!ENDSHADEBOX]

### Number of consecutive errors

Defines the maximum number of consecutive execution attempts before the execution of a scenario is deactivated (excluding `DataError`, `DuplicateDataError` and `ConnectionError`).

For more information on errors, see [Error types](/help/workfront-fusion/references/errors/error-processing.md).

>[!NOTE]
>
>If a scenario starts with an instant trigger, the setting is ignored and the scenario is deactivated immediately once the first error has occurred.

### Worker pool

>[!NOTE]
>
>This setting is visible only if the following two conditions are met:
>
>* You are an organization admin or owner
>* More than one worker pool is associated with your organization.

This setting assigns the scenario to a specific worker pool associated with your organization, allowing you to dedicate resources to high priority scenarios.
