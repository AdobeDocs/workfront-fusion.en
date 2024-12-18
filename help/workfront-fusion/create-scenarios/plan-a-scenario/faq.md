---
title: Scenario planning FAQ
description: The information in this article may be useful as you begin creating scenarios in Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 6a1d672d-0bd7-4a3a-b96d-6d8b4c97522d
---
# Scenario planning FAQ

The information in this article may be useful as you begin creating scenarios in Workfront Fusion.

## What is a scenario?

### Answer

A scenario defines a sequence of steps to be executed by Adobe Workfront Fusion. For each scenario, you specify the data source, which data to use, and how the data is to be processed. Fusion lets you create simple or complex of scenarios, able to meet the use cases for your organization..

For more information on scenarios, see [Scenario overview](/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md).

## How many modules can I use in a scenario?

### Answer

You can use as many modules as you want in a scenario. You can separate modules into routes, and can specify which data should flow through each route. You can also use the output of one module as input to another module.

Although there is no limit to the number of modules in a scenario, more than 150 modules can affect scenario performance.

Fore more information on modules, see [Module overview](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md).

## Can [!DNL Workfront Fusion] work with files?

### Answer

Yes. Workfront Fusion can receive, save, transform, convert, and encrypt files. Fusion also provides a wide range of built-in features designed to enable users to work effectively and creatively with the data contained in the files.

For more information on working with files in Fusion, see [Map a file between modules](/help/workfront-fusion/create-scenarios/map-data/map-files.md).

## Some triggers allow scenarios to run instantly. What does "instantly" mean?

### Answer

Scenarios can run at intervals according to the schedule you specify, such as every hour or every 5 minutes. There are special triggers, called instant triggers (webhooks), that can start your scenario immediately after they receive data from a given service. Fusion processes the received data immediately, without waiting for the next scheduled run. 

For more information on the difference between polled and instant triggers, see [Trigger modules](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) in the article Module overview.

## What is an operation?

### Answer

An operation is any task performed by a module. An operation occurs, for example, every time a trigger runs and every time an action performs a task.

Some Fusion plans are based on the number of operations your organization uses.

For more information on operations, see [Operations](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

## What is data transfer?

### Answer

Data transfer refers to the amount of data transferred through your scenario. For example,  a scenario that retrieves a 100KB image from Workfront, then uploads the image to a document storage provider. The amount of data used in this scenario is 200KB.

## What is a connection?

### Answer

A connection is the link between your [!DNL Workfront Fusion] account and the third-party service you want to use. The connection can be  created when editing a scenario. 

For more information, see [Connection overview](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

## What are aggregators?

### Answer

An [!UICONTROL Aggregator] merges data into one single collection. An example of this is files being compressed into a zip archive and sent as an email attachment.

For more information, see [[!UICONTROL Aggregator] module](/help/workfront-fusion/references/modules/aggregator-module.md).

## What happens if I let [!DNL Workfront Fusion] process an email containing more than one attachment?

### Answer

If you use the [!UICONTROL Email] module [!UICONTROL Retrieve attachments], each attachment is sent individually through the rest of the modules in the scenario. Similar modules are also available in other apps that receive multiple files at once.
