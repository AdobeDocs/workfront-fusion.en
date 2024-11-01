---
content-type: reference
title: Directives for Error Handling
description: This article describes directives that you can use for error handling in your [!DNL Adobe Workfront Fusion] scenarios.
author: Becky
feature: Workfront Fusion
---
# Directives for error handling

Error handling directives allow you to choose what occurs when a scenario encounters an error.

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
   <td> New: Standard<p>Or</p><p>Current: Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] license</td> 
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
 </tbody> 
</table>


To find out what plan, license type, or access you have, contact your [!DNL Workfront] administrator.

For information on [!DNL Adobe Workfront Fusion] for information about Adobe Workfront Fusion licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Directives for error handling

The following error handling directives are available in Workfront Fusion.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Rollback</p> <p> <img src="assets/rollback.png"> </p> </td> 
   <td> <ul><li><p>Scenario execution is stopped immediately.</li><li>A Rollback phase is started on all the modules, in an attempt to revert them all to their initial state. </li><li>Subsequent modules are not processed.</p></li><li> <p>In most cases, the scenario is deactivated after the number of consecutive errors specified under Scenario settings. <!--For more information, see <a href="../../workfront-fusion/scenarios/scenario-settings-panel.md#number" class="MCXref xref">Number of consecutive errors</a>.</p>--> </li><li><p>The scenario execution status is marked as "Error."</p></li></ul> <p><b>Note</b>: This is the default behavior if no error handler route is attached to the module and the <!--<a href="../../workfront-fusion/scenarios/scenario-settings-panel.md#allow" class="MCXref xref">[!UICONTROL Allow storing incomplete executions]</a>-->[!UICONTROL Allow storing incomplete executions] setting under [!UICONTROL Scenario settings] is not checked.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Commit</p> <p> <img src="assets/commit.png"> </p> </td> 
   <td> <ul><li><p>Scenario execution is stopped immediately.</li><li>A Commit phase is started on all modules. </li><li>Subsequent modules are not processed.</p></li><li> <p>All unprocessed bundles are ignored.</p> </li><li><p>The scenario execution status is marked as "success." </p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Resume</p> <p> <img src="assets/resume.png"> </p> </td> 
   <td> <ul><li><p>A substitute output is specified and supplied to the module that encounters an error.</p> </li><li><p>Subsequent modules are processed.</p></li><li> <p>The scenario execution status is marked as "success."</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Ignore</p> <p> <img src="assets/ignore.png"> </p> </td> 
   <td><ul><li> <p>The error is ignored.</li><li> Subsequent modules are not processed.</p> </li><li><p>If there are unprocessed bundles, the scenario execution continues normally.</p> </li><li><p>The scenario execution status is marked as "success."</p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Break</p> <p> <img src="assets/break.png"> </p> </td> 
   <td><ul><li> <p>The state of the scenario execution is stored in the queue of incomplete executions where the error can be resolved manually. <!--For more information, see <a href="../../workfront-fusion/scenarios/view-and-resolve-incomplete-executions.md" class="MCXref xref">View and resolve incomplete executions</a>. --></p> <p>There are, however, some exceptions. <!--For more information, see <a href="../../workfront-fusion/scenarios/scenario-settings-panel.md#allow" class="MCXref xref">Allow storing incomplete executions</a> in the article <a href="../../workfront-fusion/scenarios/scenario-settings-panel.md" class="MCXref xref">The scenario settings panel</a>.--></p></li><li> <p>Subsequent modules are not processed.</p></li><li> <p>If there are unprocessed bundles, the scenario execution continues normally.</p> </li><li><p>The scenario execution status is marked as "warning" when the [!UICONTROL Automatically complete execution] option is disabled.</p></li></ul> <p>For more information, see the <a href="#break" class="MCXref xref">[!UICONTROL Break]</a> section in this article</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Retry</p> <p> <img src="assets/retry.png"> </p> </td> 
   <td> <p>In some cases it may be useful to re-execute a failing module when there is a chance that the reason for the failure might pass over time.</p> <p>Workfront Fusion currently does not offer the Retry directive, though several workarounds can be employed to mimic its functionality. <!--For more information, see <a href="../../workfront-fusion/errors/retry.md" class="MCXref xref">Retry error handling</a>.--></p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Error handling directives cannot be used outside of an error handling route.
>
>   <!--For more information, see [Error handler route](../../workfront-fusion/errors/error-handling.md#error) in the article Error handling.-->
>* [!DNL Workfront Fusion] currently does not offer a Throw module that would enable you to easily conditionally generate (throw) errors, though a workaround can be employed to mimic its functionality.
>
>  <!-- For more information, see [Workaround for Throw](../../workfront-fusion/errors/throw.md#workaround-for-throw) in the article Throw error handling.-->

<!-- move this section to how-to

## Break {#break}

When an error is handled by the [!DNL Break] directive, a record is created in the Incomplete executions folder. This record stores the state of the scenario execution, along with data from the prior modules. The record references the module where the error originated and contains information regarding the data that was received by the module as input. For each bundle of data that causes the error, a separate record is created.

For more information, see [View and resolve incomplete executions](../../workfront-fusion/scenarios/view-and-resolve-incomplete-executions.md).

### Resolve errors resulting from the Break directive

You can resolve the error manually by updating the scenario (if needed) and running it once.

You can also configure the scenario to automatically process an incomplete execution by re-executing the scenario. To configure the module to process incomplete executions:

1. Inside the Break module, enable the [!UICONTROL **Automatically complete execution**] option.
1. In the **Number of attempts** field, enter or map the maximum number of attemps that you want the module to retry the execution

   This number must be between 1 and 100.
1. In the **Interval between attempts** field, enter or map the number of minutes between each retry attempt.

With this option enabled, when an error takes place, the incomplete execution is retrieved (after the time specified in the [!UICONTROL Interval between attempts] field) and executed with the original input data. This will repeat until the execution of the module completes without an error or until the Number of attempts specified is reached.

   >[!NOTE]
   >
   >If the initial retry attempt fails, the interval between retries increases exponentially every other attempt.


When "Automatically complete execution" is turned on, the scenario run is marked as "Success" because the Break error handler's auto-retry is handling the issue automatically. In this case, users do not receive an email about the failed run.

When "Automatically complete execution" is turned off, the run is marked as "Warning". 

There are some exceptions to executions being stored under Incomplete Executions, and with some error types, the auto-retry of a scenario execution is not possible. 

For more information, see [Allow storing incomplete executions](../../workfront-fusion/scenarios/scenario-settings-panel.md#allow) in the article [The scenario settings panel](../../workfront-fusion/scenarios/scenario-settings-panel.md).

For additional information, see [Advanced error handling](../../workfront-fusion/errors/advanced-error-handling.md).

-->

## Resources

* For information on rollback and the Rollback phase, see [Rollback](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) in the article Scenario execution, cycles, and phases.
* For information on the Commit phase, see [Commit](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#commit) in the article Scenario execution, cycles, and phases.




