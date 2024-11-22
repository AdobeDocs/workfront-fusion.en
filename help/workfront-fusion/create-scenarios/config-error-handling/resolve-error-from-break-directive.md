---
title: Resolve errors handled by the Break directive
description: Sometimes, it is useful to re-execute a failing module if there is a chance that the reason for the failure might resolve quickly.
author: Becky
feature: Workfront Fusion
---
# Resolve errors handled by the Break directive

When an error is handled by the Break directive, a record is created in the Incomplete executions folder. This record stores the state of the scenario execution, along with data from the prior modules. The record references the module where the error originated and contains information regarding the data that was received by the module as input. For each bundle of data that causes the error, a separate record is created.

For more information, see [View and resolve incomplete executions](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

## Resolve errors resulting from the Break directive

You can resolve the error manually by updating the scenario (if needed) and running it once.

You can also configure the scenario to automatically process an incomplete execution by re-executing the scenario. To configure the module to process incomplete executions:

1. Click the **[!UICONTROL Scenario]** tab in the left panel.
1. Select the scenario where you want to add the workaround.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Click the **Flow Control** icon ![Flow control](assets/flow-control-icon.png) and select **Break**.
1. Inside the Break module, enable the [!UICONTROL **Automatically complete execution**] option.
1. In the **Number of attempts** field, enter or map the maximum number of attemps that you want the module to retry the execution

   This number must be between 1 and 100.
1. In the **Interval between attempts** field, enter or map the number of minutes between each retry attempt.

With this option enabled, when an error takes place, the incomplete execution is retrieved (after the time specified in the [!UICONTROL Interval between attempts] field) and executed with the original input data. This will repeat until the execution of the module completes without an error or until the Number of attempts specified is reached.

   >[!NOTE]
   >
   >If the initial retry attempt fails, the interval between retries increases exponentially every other attempt.


When the Automatically complete execution option is enabled, the scenario run is marked as "Success" because the Break error handler's auto-retry is handling the issue automatically. In this case, users do not receive an email about the failed run.

When the Automatically complete execution option is turned off, the run is marked as "Warning". 

There are some exceptions to executions being stored under Incomplete Executions, and with some error types, the auto-retry of a scenario execution is not possible. 

<!--## Resources

For more information, see [Allow storing incomplete executions](../../workfront-fusion/scenarios/scenario-settings-panel.md#allow) in the article [The scenario settings panel](../../workfront-fusion/scenarios/scenario-settings-panel.md).-->


