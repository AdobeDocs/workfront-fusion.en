---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Create a basic scenario
description: Learn how to create a simple automation scenario with Adobe Workfront Fusion. Automation scenarios automate Workfront processes, including data manipulation and transformation. This example takes you through the process of creating a scenario that searches for a Workfront task in Workfront and the converts it to a project.
author: Becky
feature: Workfront Fusion
exl-id: 5284dee1-e890-4357-a28d-29e09ac02822
---
# Create a basic scenario

The role of Adobe Workfront Fusion is to automate your processes so that you can concentrate on new tasks rather than repeating the same tasks again and again. It works by linking actions within and between apps and services to create a scenario that transfers and transforms your data automatically. The scenario you create watches for data in an app or service and processes that data to provide the result you want.

This example takes you through the process of creating a scenario that searches for a request in Workfront and the converts it to a project.

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
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++



## Create a practice scenario

### Begin creating the scenario

1. In the **Scenarios** area, click **Create a new scenario**.

   To locate the Scenarios area, see [Navigate Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/navigate-workfront-fusion.md).

   The scenario editor displays, containing an empty module in the center.

1. Select the **[!UICONTROL New scenario]** placeholder name in the upper-left corner, then enter a name.
1. Continue with [Add and configure the first module](#add-and-configure-the-first-module).

### Add and configure the first module

1. Click the empty module to choose the app from which you will select a module.

   A list of apps appears to the right of the module.

1. Select **Adobe Workfront**. If it is not visible, click the search bar at the bottom of the list, type "Workfront," and select it when it appears in the list.

   The list changes to display all Workfront modules that you can use.

1. Click the **[!UICONTROL Search]** module.

   The module configuration window opens.

1. In the [!UICONTROL Connection] box, select your Workfront connection. 

   If you do not have a Workfront connection, see [Create a connection](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)
1. In the [!UICONTROL Record Type] box, select **[!UICONTROL Issue]**. This sets the module to search only issues, which include requests.

   You can find **[!UICONTROL Issue]** in the list if you start typing the word "[!UICONTROL Issue]."

1. In the **[!UICONTROL Result Set]** box, select **[!UICONTROL First Matching Record]**. 

   This sets the module to return only the first record it finds that meets the criteria. 
1. In the **[!UICONTROL Search criteria]** area, configure the criteria to return the specific task.

   1. In the first box under [!UICONTROL Search Criteria], select the field that you want to include in your search. For this example, select **[!UICONTROL Name]**.

      You can find **[!UICONTROL Name]** in the list if you start typing the word "[!UICONTROL name]."
   1. For the operator, click the dropdown arrow next to **Exist** and change it to [!UICONTROL **Contains (case insensitive)**]. 
      
      This allows the module to find projects with your chosen words in its name, even if you do not enter the entire name, or enter the name with the incorrect case (such as all caps).
   1. In the last field under [!UICONTROL Search Criteria], enter a word or phrase that you know is in the name of the task you are searching for.

1. In the **[!UICONTROL Outputs]** list, select the fields that you want the module to output. For this example, select the **[!UICONTROL ID]** and **[!UICONTROL Name]** fields.

   >[!TIP]
   >
   >You can use **Cmd+F** ([!DNL Mac] OS) or **Ctrl-F** ([!DNL Windows] OS) to find a field quickly.

1. Click **[!UICONTROL OK]** to save the module configuration.

1. Right-click the module, click **[!UICONTROL Rename]**, then type a name the describes what you want the module to do (such as "Search for requests)," then click **[!UICONTROL OK]**.

   The name appears just below the module. Below that, Workfront Fusion includes a brief description of the type of action performed by the module.

   ![Renamed module](assets/module-renamed-wf.png)

1. Continue with [Add and configure the second module](#add-and-configure-the-second-module).

## Add and configure the second module

1. Hover over the partial circle to the right of the of the module, then click **[!UICONTROL Add another module]**. 
1. Select Adobe Workfront from the list of applications, then choose the module **[!UICONTROL Convert object]**.
1. In the [!UICONTROL Connection] field, select  the same Workfront connection that you used in the previous module . 
1. In the **[!UICONTROL Record type]** field, select **[!UICONTROL issue]**, because the module will convert an issue.
1. In the **[!UICONTROL Convert to]** field, select **Project**. 
1. Next to the Task ID field, click the map toggle to enable it. 

   The toggle turns blue when it is enabled. This allows you to map the task ID from the previous module.

   ![Map toggle](assets/map-toggle.png)
1. Click the **[!UICONTROL Task ID]** field.  

   A panel opens that allows you to select what to use as the ID of the task you want to convert to a project. Because you enabled mapping, the panel includes output from any previous modules. You selected ID as an output of the previous module, so it is now available in the panel.

   This panel is called the mapping panel. For more information on the mapping panel, see [Mapping overview](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).
1. Select **ID** in the mapping panel.

   An ID block appears in the ID field. It shows the number of the module it is mapped from, and the field that is mapped.

   ![Map ID](assets/map-id.png)

1. Click the **Template ID** field, begin typing the name of the Workfront template you want to use for this project, then select it when it appears in the list.
1. Click **[!UICONTROL OK]** to save the module configuration.

1. Right-click the module, click **[!UICONTROL Rename]**, then type a name the describes what you want the module to do (such as "Convert to project)," then click **[!UICONTROL OK]**.

1. Continue to [Test the scenario](#test-the-scenario).

## Test the scenario

Before you activate your scenario, it's important to test it by running it at least once and viewing the results. This helps you understand how data flows through the scenario and find any errors.

For this scenario, a successful test would result in locating the request and converting it to a project.

1. Click **[!UICONTROL Run once]** in the lower-left corner of the scenario editor.
1. After the scenario finishes running, click the bubble above the first module to can view information about the bundle of data that the module processed, including data pulled from the request that the module returned.

1. Click the execution inspector bubble above the second module to see the input (the request) and the output (the converted project).

   For more information about the data in the inspection bubbles, see:

   * For general information, see [Scenario execution flow](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * For information about processed bundles, see [Scenario execution, cycles, and phases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. In Workfront Fusion, click **[!UICONTROL Save]** near the lower-left corner to save your progress on the scenario.

   >[!IMPORTANT]
   >
   >Save often as you hone and test a scenario.

>[!TIP]
>
>We recommend the optional but useful practice of adding notes about each module.
>
>1. Right-click a module, then select **[!UICONTROL Add a note]**.
>1. In the note that displays, type an overview for the module.
>
>    You can add multiple notes for a module.
>
>1. Close the **[!UICONTROL Notes]** area.
>
>     After you add a note to a scenario, a dot displays on the **[!UICONTROL Notes]** icon ![Notes icon with dot](assets/notes-icon-w-dot.png) at the bottom of the scenario editor.
>
>1. Click the **[!UICONTROL Notes]** icon ![Notes icon with dot](assets/notes-icon-w-dot.png) to view your notes. When notes are open, a circle appears around the Notes icon.
>

## Activate the scenario

The last step in creating a scenario is activating it.

Because this scenario is searching for a specific issue, there is no need to activate it. Activating a scenario causes it to run on a schedule or when a specific action occurs in an application. After you activate a scenario, by default, it runs every 15 minutes. You can change this by defining when and how often you want it to run.

For more information about activating scenarios, see [Activate or deactivate a scenario](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).

For information about schedules, see [Schedule a scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Next steps

* [Add a trigger module](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) to allow the scenario to periodically look for new requests and convert them to projects.
* [Add a webhook](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) to allow the scenario to execute every time a request is entered.
* [Add a filter](/help/workfront-fusion/build-practice-scenarios/add-filter-basic-scenario.md) to ensure that only certain requests are converted to projects.
* [Add a function](/help/workfront-fusion/build-practice-scenarios/use-function-to-build-practice-scenario.md) that customizes the name of the new project.
