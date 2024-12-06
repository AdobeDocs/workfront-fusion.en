---
content-type: overview
title: Scenario Execution Flow
description: This article explains how a scenario executes and how data flows through it. It also explains where you can find information about your processed data and how to read it.
author: Becky
feature: Workfront Fusion
---
# Scenario execution flow

<!--audited: 09/2024-->

This article explains how a scenario executes and how data flows through it, and how to view the data processed by each module.

## Scenario execution flow

After a scenario is set up correctly and activated, it executes according to its defined schedule.

As the scenario begins, the first module responds to an event it has been set to watch for. When it returns data, that data is packaged into bundles. The scenario returns one bundle for each event. For example, if a module is set to watch for issues, it will return a bundle of data for each issue it finds. 

If the trigger module returns any bundles of data, those bundles pass on to the next module and the scenario continues, passing the bundles through each successive module, one at a time.

If the bundles process correctly through all of the modules, the scenario is marked as a success in the scenario details page.

### Example: [!UICONTROL [!DNL Workfront Fusion] for Work Automation]

>[!BEGINSHADEBOX]

**Example:** In this scenario that watches for incoming requests in [!DNL Workfront] and then converts them to [!DNL Workfront] projects, data would flow as follows:

The scenario's first step, performed by the first module, is to watch for requests. Each request that it finds is considered one bundle. If the module runs without finding any bundles, the scenario ends after the first module.

If the first module returns a bundle, the bundle passes through the rest of the scenario. In this example, the bundle would go to the second module, which converts the request to a project.

![](assets/example-execution-flow-wf-only.png)

>[!ENDSHADEBOX]

### Example: [!UICONTROL [!DNL Workfront Fusion] for Work Automation and Integration]

>[!BEGINSHADEBOX]

**Example:** In This scenario that downloads documents from [!DNL Adobe Workfront] and sends them to a folder in [!DNL Dropbox], data would flow as follows:

The scenario's first step, performed by the first module, is to watch for documents in Workfront.. Each document that it finds is considered one bundle. If the module runs without finding any bundles, the scenario ends after the first module.

If a bundle is returned, the bundle passes through the rest of the scenario. In this example, the rest of the scenario consists of the secondmodule, which uploads the bundle to the [!DNL Dropbox] folder.

![](assets/example-execution-flow-wf-dropbox.png)

If the first module returns multiple bundles, the first bundle is uploaded to [!DNL Dropbox] before the second bundle is uploaded. Then the second bundle uploads, then the third, and so on.

>[!ENDSHADEBOX]

## Information about processed bundles

For each module, the bundle goes through a 4-step process before going on to the next module or reaching its final destination. 

* Initialization
* Operation
* Commit/Rollback
* Finalization

>[!NOTE]
>
>The larger scenario goes through this process as well. For information about this process on the scenario level, see [Scenario execution, cycles, and phases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

After a scenario run is complete, each module displays an icon showing the number of operations performed. You can click this icon to display the detailed information about the processed bundles for each step in the process. You can see which module settings were used, and which bundles were returned by each module.

![](assets/Info-processed-bundles.png)

In this example, the module received input information such as:

* The ID of the issue it found
* The object that the issue will be converted to (Project)
* The ID of the template it will use to create the project
* The record type of the object it found (OPTASK, which is an issue)

After processing, the module returned this output information:

* ID of the newly created project.

If the module found more than one issue, the information is captured for each bundle separately. There would be an Operation 2 area with input and output sections describing the second bundle, and so on.

## Errors while executing a scenario

An error might occur during the scenario run. For example, if you have deleted the template that the module will use to create the new project, the scenario terminates with an error message. For more information about how to handle errors, see [Error types](/help/workfront-fusion/references/errors/error-processing.md).

## Resources

* For more information on setting up a scenario, see [The scenario editor](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md)
* For more information on the scenario details page, see [Scenario details](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario.details.md).
* For more information on activating a scenario, see [Activate or deactivate a scenario](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).
* For more information on scheduling a scenario, see [Schedule a scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
* For more information on modules, see [Module overview](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md).




