---
title: Configure retry error handling workaround
description: Sometimes, it is useful to re-execute a failing module if there is a chance that the reason for the failure might resolve quickly.
author: Becky
feature: Workfront Fusion
exl-id: 08e19a1a-7ca9-4c79-a165-f200048a5cda
---
# Configure `retry` error handling workaround

Sometimes, it is useful to re-execute a failing module if there is a chance that the reason for the failure might resolve quickly.

Adobe Workfront Fusion currently does not offer the `retry` error handling directive, but two workarounds are available to mimic `retry` functionality.

## Access requirements

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan*</td> 
   <td> <p>[!DNL Pro] or higher</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] license*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] license**</td> 
   <td>
   <p>Current license requirement: No [!DNL Workfront Fusion] license requirement.</p>
   <p>Or</p>
   <p>Legacy license requirement: [!UICONTROL [!DNL Workfront Fusion] for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Current product requirement: If you have the [!UICONTROL Select] or [!UICONTROL Prime] [!DNL Adobe Workfront] plan, your organization must purchase [!DNL Adobe Workfront Fusion] as well as [!DNL Adobe Workfront] to use functionality described in this article. [!DNL Workfront Fusion] is included in the [!UICONTROL Ultimate] [!DNL Workfront] plan.</p>
   <p>Or</p>
   <p>Legacy product requirement: Your organization must purchase [!DNL Adobe Workfront Fusion] as well as [!DNL Adobe Workfront] to use functionality described in this article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

To find out what plan, license type, or access you have, contact your [!DNL Workfront] administrator.

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion licenses]](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Workarounds to the [!UICONTROL Retry] error handling directive

Workfront Fusion currently does not offer the `retry` error handling directive. Use one of the following workarounds to mimic retry functionality. 
 
For instructions, see [Directives for error handling](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

* [Use the Break directive](#use-the-break-directive)
* [Use the Repeater module](#use-the-repeater-module)

### Use the Break directive

When the Break directive executes, the state of the scenario execution is stored in the queue of incomplete executions. If this occurs, you can then resolve the incomplete execution manually. 

For instructions see [Resolve errors handled by the Break directive](/help/workfront-fusion/create-scenarios/config-error-handling/resolve-error-from-break-directive.md)

For instructions on resolving incomplete executions, see [View and resolve incomplete executions](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

#### Drawbacks

* The minimum retry interval is one minute.
* If the module is processing multiple bundles and the processing of a bundle fails, the partial execution (only the bundle that caused the error) is moved to the incomplete executions folder and scheduled for retries according to the [!UICONTROL Break] directive settings. However, the current execution continues and the module continues to process the subsequent bundles. 

   To prevent the scenario from executing again until the execution stored in the the Incomplete executions folder has been successfully resolved, enable the "[!UICONTROL Sequential processing]" option in the [!UICONTROL Scenario settings].

For more information on incomplete executions, see [View and resolve incomplete executions in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

### Use the Repeater module

The Repeater module workaround is more complex, but more customizable.

#### Configure the error handler route

1. Click the **[!UICONTROL Scenario]** tab in the left panel.
1. Select the scenario where you want to add the workaround.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Click the **Flow Control** icon ![Flow control](assets/flow-control-icon.png) and select **Repeater**.
1. In the Repeater module, set the **[!UICONTROL Repeats]** field to the maximum number of times that you want the scenario to retry.
1. Attach the potentially failing module after the **[!UICONTROL Repeater]** module.
1. Attach an error handler route to the potentially failing module.

   For instructions, see [Add error handling](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md).
1. Add the **[!UICONTROL Tools] > [!UICONTROL Sleep]** module to the error handler route and set its **[!UICONTROL Delay]** field to the number of seconds between retry attempts.

1. Add the **[!UICONTROL Ignore]** directive after the **[!UICONTROL Tools] > [!UICONTROL Sleep]** module. 
1. Continue to [Configure the default route](#configure-the-default-route).

#### Configure the default route

1. Add the **[!UICONTROL Tools] > [!UICONTROL Set variable]** module in a separate (non-error handler) route after the the potentially failing module, and configure it to store the module's result in a variable named, such as `Result`.

1. Add the **[!UICONTROL Array aggregator]** module after the **[!UICONTROL Tools] > [!UICONTROL Set variable]**, and select the **[!DNL Repeater]** module in its Source Module field.

1. Add the **[!UICONTROL Tools] > [!UICONTROL Get variable]** module after the **[!UICONTROL Array aggregator]** module, and map the value of the `Result` variable to it.

1. Insert the **[!UICONTROL Tools] > [!UICONTROL Get variable]** module between the **[!UICONTROL Repeater]** module and the potentially failing module, and map the value of the `Result` variable to it.

1. Insert a filter between this **[!UICONTROL Tools] > [!UICONTROL Get variable]** module and the potentially failing module to continue only if the `Result` variable does not exist.

>[!BEGINSHADEBOX]

**Example:** 

In this sample scenario, the [!UICONTROL HTTP] > [!UICONTROL Make a request] module represents the potentially failing module:

![](assets/http-make-request.png)

>[!ENDSHADEBOX]

If the result of the potentially failing module is too complex to be stored in a simple variable, you can use a data store to store and retrieve the result. The data store would contain just one record. The record's key can be, for example, `Result`.

For more information on data stores, see [Data Stores](/help/workfront-fusion/create-scenarios/map-data/data-stores.md).

#### Drawbacks

* This workaround is more complex.
* This workaround uses more operations.

## Resources

* For more information on Repeater modules and break directives, see [Flow control](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/flow-control.md).
* For more information on Get Variable modules, see [Tools](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/tools-modules.md).
