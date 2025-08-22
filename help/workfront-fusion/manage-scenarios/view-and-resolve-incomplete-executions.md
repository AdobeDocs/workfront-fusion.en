---
title: View and resolve incomplete executions
description: The [!UICONTROL Incomplete executions] folder stores scenario executions that were not successfully finalized due to an error. Each stored incomplete execution can be resolved either manually or automatically.
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
---
# View and resolve incomplete executions

The [!UICONTROL Incomplete executions] folder stores scenario executions that were not successfully finalized due to an error. Each stored incomplete execution can be resolved either manually or automatically.

>[!NOTE]
>
>By default the storing of incomplete executions is disabled. To enable it, enable the [!UICONTROL Allow storing incomplete executions] option in the scenario advanced settings.
>
>For more information about scenario settings, see [Configure scenario settings](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p> </td> 
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
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] Workfront plan: Your organization must purchase Adobe Workfront Fusion.</li><li>[!UICONTROL Ultimate] Workfront plan: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Access level configurations*</td> 
   <td> 
     <p>You must be a Workfront Fusion administrator for your organization.</p>
     <p>You must be a Workfront Fusion administrator for your team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## View incomplete executions

If a module encounters an error during its operation, a new incomplete execution is added to the Incomplete executions folder. Each incomplete execution contains the scenario's blueprint and all the bundles that can be mapped into the failed module. The list of incomplete executions can be opened by clicking on the [!UICONTROL Incomplete Executions] tab on the scenario detail page.

<!--

![Incomplete executions tab](assets/incomplete-executions-tab-350x102.png)

-->

For more information, see [Errors resulting into incomplete executions](#errors-resulting-into-incomplete-executions) in this article.

>[!NOTE]
>
>The current size limit of the unresolved incomplete executions folder per scenario is 10 MB. If your scenario exceeds this limit, you may see the following error:
>
>`DLQ limit per scenario has been exceeded`
>
>Teams are limited to a total of 500 MB for all unresolved incomplete executions.
>
>For more information, see [Enable data loss](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) in the article Configure scenario settings.


## Resolve incomplete executions from the Incomplete Executions tab

When a new incomplete execution is stored, you can resolve it as follows:

1. Open the affected scenario. 
1. Click the **[!UICONTROL Incomplete Executions]** tab.
1. Locate the incomplete execution you would like to resolve, and click **[!UICONTROL Details]**.
1. Open the module's log where all the module's operations are shown.
1. Locate the failed operation and click **[!UICONTROL Resolve]**:

   ![Resolve button](assets/resolve-btn-350x188.png)



## Resolve incomplete executions from the History tab

If you want to see the log of all module's operations before you attempt to resolve the incomplete execution, you can resolve the incomplete execution from the [!UICONTROL History] folder:

1. Open The affected scenario. 
1. Click the **[!UICONTROL History]** tab.
1. Locate the scenario's failed execution, and click **[!UICONTROL Details]**.
1. Open the module's log where all the module's operations are shown.
1. Locate the failed operation and click **[!UICONTROL Resolve]**:

   ![Resolve button](assets/resolve-btn-350x188.png)

## Options related to incomplete executions

The following options in the [!UICONTROL Scenario settings] panel determine if and how the incomplete executions are stored:

* Allow storing incomplete executions
* Sequential processing
* Enable data loss

For more information about these options, see [Configure scenario settings](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Errors resulting into incomplete executions 

There are several categories of errors which result into storing of incomplete executions. These may include:

* Validation errors arising from incomplete or erroneous data, mostly because of a missing item that is expected in order to successfully process all data going through a module.
* Errors occurring from the final destination's unavailability because of temporary or long term connection failure (for example, during connection to email or remote FTP server).

If an error occurs on the first module in the scenario, the execution stops immediately and no incomplete execution is stored.

If an error occurs on any other module and there is no error handler route attached, one of the following occurs:

* An incomplete execution record with auto-retry is stored for the following error types:

   * `ConnectionError`
   * `RateLimitError`
   * `OutOfSpaceError`
   * `ModuleTimeoutError`

* An incomplete execution record without auto-retry is stored for the following error types:

   * `DataError`
   * `InvalidConfigurationError`
   * `InvalidAccessTokenError`
   * `UnexpectedError`
   * `MaxFileSizeExceededError`
   * `MaxResultsExceededError`
   
* If the error type is anything other than the above, the execution fails.
