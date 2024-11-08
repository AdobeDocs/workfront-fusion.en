---
title: Add error handling
description: When errors occur during the execution of a scenario, it's usually because a service is unavailable due to a failure, a service responds with unexpected data, or the validation of input data fails.
author: Becky
feature: Workfront Fusion
---
# Add error handling

Errors can occur during the execution of a scenario. 

For example, an error can occur because:

* A service is unavailable due to a failure
* A service responds with unexpected data
* Validation of input data fails
* Other reasons

If a module encounters an error during the scenario execution, and there is no error handling route attached to the module, the default error handling logic executes. 

By adding an error handler route to a module, you can replace the default error handling logic with your own. Adobe Workfront Fusion offers five different directives that can be inserted at the end of your error handler routes. 

For more information on default error handling, see [Error processing](/help/workfront-fusion/references/errors/error-processing.md).

For more information on error handling directives, see [Directives for error handling](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront plan</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current: Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>Current: No Workfront Fusion license requirement.</p>
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

<!--For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md).-->

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Add an error handler

To add an error handler to a module:

1. Click the **[!UICONTROL Scenario]** tab in the left panel.
1. Select the scenario where you want to add an error handling route.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Right click the module after which you want to add an error handler, and select **[!UICONTROL Add error handler]**:

    ![](assets/error-handler-route.png)

    The error handling module shows a list of Directives as well as the apps being used in your scenario. 
    
1. If the module that you added an error handler to is the last module in your route, select one of the directives. 

    Or 

    Add one or more modules to the error handler route. 

    If you add more modules to the route, the Ignore directive is applied by default. If there is an error, the subsequent modules on that route are processed.

<!--this is not what the picture shows

>[!BEGINSHADEBOX]

In this example, if an error occurs while executing the [!UICONTROL Create a folder] module, the [!UICONTROL Ignore] directive will be applied automatically and the scenario will move to the next module on the error handler route.

However, if there is no error, the scenario will move to the [!UICONTROL List all files in a folder module] on the regular route.

![](assets/if-there-is-no-error-350x234.png)

>[!ENDSHADEBOX]

-->

Note that an error handler route is composed of transparent circles, while a regular route is composed of solid circles.

## Error handling directives

The directives are briefly explained below. For more information, see [Directives for error handling in Adobe Workfront Fusion](../../workfront-fusion/errors/directives-for-error-handling.md).

There are a total of five directives which can be grouped into the following categories based on whether a scenario execution should continue or not.

The following directives ensure that a scenario execution continues:

* **[!UICONTROL Resume]**: Allows you to specify a substitute output for the module with the error. The scenario execution status is marked as success
* **[!UICONTROL Ignore]**: ignores the error. The scenario execution status is marked as success
* **[!UICONTROL Break]**: Stores the input to the queue of incomplete executions. The scenario execution status is marked as warning. For more information, see [View and resolve incomplete executions in Adobe Workfront Fusion](../../workfront-fusion/scenarios/view-and-resolve-incomplete-executions.md).

If a scenario execution should stop when an error occurs, use one of the following directives:

* **[!UICONTROL Rollback]**: Stops the scenario execution immediately and marks its status as error
* **[!UICONTROL Commit]**: Stops the scenario execution immediately and marks its status as success

For more information on error handling, see:

* [Directives for error handling in Adobe Workfront Fusion](../../workfront-fusion/errors/directives-for-error-handling.md)
* [Advanced error handling in Adobe Workfront Fusion](../../workfront-fusion/errors/advanced-error-handling.md) 




