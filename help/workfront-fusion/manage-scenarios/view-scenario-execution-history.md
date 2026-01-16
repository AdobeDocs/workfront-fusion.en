---
title: View a scenario's execution history
description: You can display information about a scenario's events or executions, or you can search all executions of the scenario for specific data. 
author: Becky
feature: Workfront Fusion
exl-id: 974b32b4-d86a-48cd-a8d4-1ae2cf309b9b
---
# View a scenario's execution history

You can display information about a scenario's events or executions, or you can search all executions of the scenario for specific data. 

A scenario execution represents a single run of the scenario.

A scenario event is a modification to the scenario, such as editing, activating, or deactivating it. 

>[!NOTE]
>
>A scenario's history displays all of a scenario's executions for the last 30 days.

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

+++

## View scenario history


### View scenario history on the History tab

The [!UICONTROL History] tab shows more detail than is available on the [!UICONTROL Scenario detail] page. You can also filter and sort the executions on the [!UICONTROL History] tab.

>[!NOTE]
>
>If you view a scenario history while it is still running, Fusion displays a note that informs you that data is still being processes, and only partial scenario history displays until the processing is complete.

1. Click the **[!UICONTROL Scenario]** tab in the left panel, then click the scenario.

   Or

   If you are working on the scenario in the Scenario editor, click the left arrow ![Exit editing arrow](assets/exit-editing-arrow.png) near the upper-left corner of the window.

1. Click **History** near the name of the scenario.
    ![history tab](assets/history-tab.png)

   The following details are listed for every execution of the scenario:

   * Date when the run was **[!UICONTROL Started]**
   * Execution ID
   * **[!UICONTROL Status]** (success or failed)
   * Run **[!UICONTROL Duration]**
   * Number of **[!UICONTROL Operations]**
   * Size of **[!UICONTROL Data Transfer]**
  
   >[!NOTE]
   >
   >The scenario history displays a **Processing** badge next to scenarios that have recently executed, while the execution details are written to storage. Processing occurs immediately after the scenario executes. and should last no more than a few minutes. Details of the scenario execution may not be visible while the execution is processing.
   
1. To view details for a specific scenario execution, click **Details** in the far right. The [!UICONTROL details] link is visible only if the execution has details available.

   For more information on viewing scenario execution details, see [View a specific scenario execution](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md).
1. To view events, toggle **Show events** on.


### View scenario history on the Scenario Detail page


1. Click the **[!UICONTROL Scenario]** tab in the left panel, then click the scenario.

   Or

   If you are working on the scenario in the Scenario editor, click the left arrow ![Exit editing arrow](assets/exit-editing-arrow.png) near the upper-left corner of the window.

1. Click the **[!UICONTROL History]** tab in the right panel.
1. (Optional) For detailed information about a selected scenario run, click on the execution in the right panel.

   For more information on processing bundles, see [Scenario execution flow](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)

   >[!NOTE]
   >
   >* The scenario history displays a **Processing history** badge next to scenarios that have recently executed, while the execution details are written to storage. Processing occurs immediately after the scenario executes. and should last no more than a few minutes. Details of the scenario execution may not be visible while the execution is processing.

1. To view events, click the **Events** tab. 

## Filter the scenario execution history

You can filter the execution history to view only executions with the specified values.

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-history-on-the-history-tab) in this article.
1. Click the [!UICONTROL filter] icon ![Scenario filter icon](assets/fusion-scenario-filter-icon.png) in the header of the column you want to filter by.
1. In the [!UICONTROL filter] dialog, enter the values that you want to filter by.
1. Click **[!UICONTROL Save]**.

The filter icon is orange in columns with an active filter.

<!-- don't see how to do this
## Sort the scenario execution history

You can sort the scenario execution history.

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-execution-history-on-the-history-tab) in this article.
1. Click the [!UICONTROL Sort] icon in the header of the column you want to filter by.
1. Optional: To reverse the order of the sort, click the [!UICONTROL Sort] icon again.
-->

## Search all executions of a scenario

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-history-on-the-history-tab) in this article.
1. Click **[!UICONTROL Fulltext search]** at the top of the list of executions.

   Or

   Type **Ctrl+Shift+F** (Windows) or **Cmd+Shift+F** (Mac)
The [!UICONTROL Search in history] window opens.

1. (Optional) To search for executions that contain specific text, enter the text in the search bar of the **[!UICONTROL Search in history]** window.

   To search for exact text, surround the text with double quotation marks ("example").

   >[!INFO]
   >
   >**Example:** If you want to find the execution that created a specific project, enter the project ID into the [!UICONTROL Fulltext search] bar.
   >
   >"625ef2ef0006036bd1794b6e52d737c5"

1. (Optional) To limit your search by date range, select the beginning and ending dates of your desired search in the [!UICONTROL By date range] area.

   >[!NOTE]
   >
   >* Executions are available only for the previous 30 days.
   >
   >* Workfront Fusion stores webhook payloads for 30 days. Accessing a webhook payload more than 30 days after it was created results in the error "[!UICONTROL Failed to read file from storage.]"


1. (Optional) To limit your search by status, select the desired status in the **[!UICONTROL By status]** dropdown.


   Available statuses are:

   * [!UICONTROL All]

   * [!UICONTROL Error]

   * [!UICONTROL Warning]

   * [!UICONTROL Success]

1. (Optional) Change the order that results display in the **[!UICONTROL Sort by dates]** dropdown.

1. (Optional) To copy a scenario execution ID, click the **[!UICONTROL Copy execution ID]** icon <img src="assets/copy-fusion-execution-id-icon.png"> in the row of the desired execution.

1. (Optional) Click on a result of the [!UICONTROL Fulltext search] to examine the scenario module output bundle that contains the information.
