---
title: Workflow for creating a scenario
description: Follow this general workflow to create a scenario
author: Becky
feature: Workfront Fusion
exl-id: 49f8edd7-e29a-4ead-9134-a9f0d1cc244d
---
# Workflow for creating a scenario

Scenarios are built to meet the needs of your organization, with applications and modules that address your use cases. However, creating a scenario follows the same basic workflow regardless of use case. This article describes the basic process of creating a scenario.


1. [Create and name the scenario](#1-create-and-name-the-scenario)
2. [Add and configure the first module](#3-configure-the-first-module)
3. [Create connections](#3-create-connections)
4. [Add and configure additional modules](#4-add-and-configure-additional-modules)
5. [Map data between modules](#5-map-data-between-modules)
6. [Configure routing](#6-configure-routing)
7. [Configure error handling](#7-configure-error-handling)
8. [Configure scenario settings](#8-configure-scenario-settings)
9. Test and revise
10. Activate

Keyboard shortcuts



## 1. Create and name the scenario

1. Sign into your [!DNL Workfront Fusion] account.
1. Click **[!UICONTROL Scenarios]** ![](assets/scenarios-icon.png) in the left panel.

   >[!NOTE]
   >
   >If you do not see the left navigation panel or its icons, click the Menu ![Menu](assets/main-menu-icon-left-nav.png) icon.

1. (Optional)In the [!UICONTROL **Folders**] panel, click the **[!UICONTROL Add folder]** icon ![](assets/add-folder-icon.png), then type a name like "Practice scenarios" for your first folder.

1. (Optional) Open the folder, then click **[!UICONTROL Create a new scenario]** in the upper-right corner of the page.

1. Select the **[!UICONTROL New scenario]** placeholder name in the upper-left corner, then type a name such as "Practice scenario 1."

   ![](assets/name-the-scenario.png)

1. Continue with [Connect the first module](#2-connect-the-first-module) below.

## 2. Add and configure the first module

The first module for your scenario is a trigger module, which will start the scenario when certain conditions are met.

For instructions on adding the first module to a scenario, see [Add the first module to a scenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-basic.md#add-the-first-module-to-a-scenario) in the article Add a module to a scenario.

For instructions on configuring a module, see [Configure a module](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)

## 3. Create connections 

When configuring a module, you must enter or create a connection. The module uses this connection and the permissions it contains to access date in the application.

For basic instructions on how to create a connection, see [Create a connection - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

For specific use cases involving Google, Microsoft, or applications without dedicated connectors, see the other articles under [Connect to applications: article index](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-apps-toc.md).

## 4. Add and configure additional modules

Continue adding and configuring additional modules.

For instructions on the ways to add modules, see the articles listed under [Add modules: article index](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

## 5. Map data between modules

You can use output from previous modules as input into subsequent modules. For example, you can create a Workfront project in one module, and upload a document to that module in a subsequent module.

For instructions, see the articles under [Map data: article index](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md).

## 6. Configure routing

Routing allows the scenario to perform different actions based on data values. 

For instructions, see [Add a Router module and configure routes](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## 7. Configure error handling

Error handling allows the scenario to recover from errors. You can select how you want the scenario to react in different error situations.

For instructions, see [Add error handling](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md).

## 8. Configure scenario settings

You can configure settings for your scenario as a whole, such as scheduling a scenario, making notes, or determining how data is stored. 

For instructions, see the articles under [Configure scenario settings: article index](/help/workfront-fusion/create-scenarios/config-scenarios-settings/config-scenario-settings-toc.md).

## 9. Test and revise

Testing your scenario enables you to determine if your scenario is working as intended. You can then revise the scenario based on your results, and then retest.

1. Click **[!UICONTROL Run once]** in the lower-left corner of the scenario editor.
1. After the scenario finishes running, click the execution inspector bubble above the each module to see the input of information and the output of that module.

   * For general information on reading scenario execution information, see [Scenario execution flow](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * For information about processed bundles, see [Scenario execution, cycles, and phases in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. In [!DNL Workfront Fusion], click **[!UICONTROL Save]** ![](assets/save-icon.png) near the lower-left corner to save your progress on the scenario.

   >[!IMPORTANT]
   >
   >Save often as you hone and test a scenario.

## 10. Activate the scenario

This example scenario does not have a trigger module. If this were a scenario you would be using for real data it would start with a trigger module, and the last thing you would do is activate it. After you activate a scenario, by default, it runs every 15 minutes. You can change this by defining when and how often you want it to run.

For more information about activating scenarios, see [Activate or deactivate a scenario](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).

For information about schedules, see [Schedule a scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
