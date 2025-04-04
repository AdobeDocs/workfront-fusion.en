---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: errors
title: Configure throw error workaround
description: In some cases you may want to forcibly stop the scenario execution followed by Rollback or Commit phase or to stop the processing of a route and optionally store it in the queue of View and resolve incomplete executions in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 4bf2a6c7-16b2-4545-9adf-be3947a7017d
---
# Configure `throw` error workaround

In some cases, you may want to forcibly stop the scenario execution followed by  Rollback or Commit phase, or to stop the processing of a route and optionally store it in the queue of incomplete executions.

Currently, the error handling directives cannot be used out of the scope of an error handler route, and Adobe Workfront Fusion does not offer a module that would enable you to easily conditionally generate (throw) errors.

You can use the following workaround to mimic `throw` error functionality.

For information on incomplete executions, see [View and resolve incomplete executions in Adobe Workfront Fusion](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

For information on error handling directives, see [Directives for error handling in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current: Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>Current: No Workfront Fusion license requirement</p>
   <p>Or</p>
   <p>Legacy: Any </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>Select or Prime Workfront Plan: Your organization must purchase Adobe Workfront Fusion.</li><li>Ultimate Workfront Plan: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Workaround for `throw`

To conditionally throw an error, you can configure a module to make it purposely fail during its operation. One possibility is to employ the [!UICONTROL JSON] > [!UICONTROL Parse JSON] module, configured to optionally throw an error (`BundleValidationError` in this case):

![JSON error](assets/json-parse-json.png)

You can then attach one of the error handling directives to the error handling route:

* **Rollback**: Force the scenario execution to stop and perform the rollback phase.
* **Commit**: Force the scenario execution to stop and perform the commit phase.
* **Ignore**: Stop the processing of a route.
* **Break**: Stop the processing of a route and store it in the queue of incomplete executions folder.

The following example shows the use of the [!DNL Rollback] directive:

![Rollback directive](assets/rollback-directive.png)
