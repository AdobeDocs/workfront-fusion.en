---
content-type: reference
title: Directives for Error Handling
description: This article describes directives that you can use for error handling in your Adobe Workfront Fusion scenarios.
author: Becky
feature: Workfront Fusion
exl-id: d7b0141f-d99d-4ab7-a60f-ed552a76f05d
---
# Directives for error handling

Error handling directives allow you to choose what occurs when a scenario encounters an error.

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

+++## Directives for error handling

The following error handling directives are available in Workfront Fusion.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Rollback</p> <p> <img src="assets/rollback.png"> </p> </td> 
   <td> <ul><li><p>Scenario execution is stopped immediately.</li><li>A Rollback phase is started on all the modules, in an attempt to revert them all to their initial state. </li><li>Subsequent modules are not processed.</p></li><li> <p>In most cases, the scenario is deactivated after the number of consecutive errors specified under Scenario settings. For more information, see <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors" class="MCXref xref">Number of consecutive errors</a>.</p> </li><li><p>The scenario execution status is marked as "Error."</p></li></ul> <p><b>Note</b>: This is the default behavior if no error handler route is attached to the module and the <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions" class="MCXref xref">Allow storing incomplete executions</a>Allow storing incomplete executions setting under [!UICONTROL Scenario settings] is not checked.</p> </td> 
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
   <td><ul><li> <p>The state of the scenario execution is stored in the queue of incomplete executions where the error can be resolved manually. For more information, see <a href="/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md" class="MCXref xref">View and resolve incomplete executions</a>.</p> <p>There are, however, some exceptions. For more information, see <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow" class="MCXref xref">Allow storing incomplete executions</a> in the article Configure scenario settings</a>.</p></li><li> <p>Subsequent modules are not processed.</p></li><li> <p>If there are unprocessed bundles, the scenario execution continues normally.</p> </li><li><p>The scenario execution status is marked as "warning" when the [!UICONTROL Automatically complete execution] option is disabled.</p></li></ul> <p>For more information, see the <a href="#break" class="MCXref xref">[!UICONTROL Break]</a> section in this article</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Retry</p> <p> <img src="assets/retry.png"> </p> </td> 
   <td> <p>In some cases it may be useful to re-execute a failing module when there is a chance that the reason for the failure might pass over time.</p> <p>Workfront Fusion currently does not offer the Retry directive, though several workarounds can be employed to mimic its functionality. For more information, see <a href="/help/workfront-fusion/create-scenarios/config-error-handling/retry.md" class="MCXref xref">Retry error handling</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Error handling directives cannot be used outside of an error handling route.
>* Workfront Fusion currently does not offer a Throw module that would enable you to easily conditionally generate (throw) errors, though a workaround can be employed to mimic its functionality.
>
>  For more information, see [Configure `throw` error workaround](/help/workfront-fusion/create-scenarios/config-error-handling/throw.md).

## Resources

* For information on rollback and the Rollback phase, see [Rollback](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) in the article Scenario execution, cycles, and phases.
* For information on the Commit phase, see [Commit](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#commit) in the article Scenario execution, cycles, and phases.
