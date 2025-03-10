---
title: Scenario overview
description: Adobe Workfront Fusion requires an Adobe Workfront Fusion license in addition to an Adobe Workfront license.
author: Becky
feature: Workfront Fusion
exl-id: de81ad4c-27e5-4b6c-acf0-f01a8c85922e
---
# Scenario overview

The role of Adobe Workfront Fusion is to automate your processes so that your users don't need to spend as much time on routine tasks. It works by linking actions within and between apps and services to create a scenario that transfers and transforms your data automatically. The scenario you create watches for data in an app or service and processes that data to provide the result you want.

A scenario is comprised of a series of modules that indicate how data should be transformed within an app or transferred between apps and web services. 

## Scenario elements overview

A scenario is built of different elements. Understanding the terminology of those elements makes it easier to use the documentation.

* [Scenario](#scenario)
* [Trigger](#trigger)
* [Module](#module)
* [Route](#route)
* [Scenario segment](#scenario-segment)
* [Connector](#connector)

### Scenario

A **scenario** is a user-created series of automated steps, created to move and manipulate data. The term "scenario" refers to the entire group of connected steps.

![Scenario](assets/entire-scenario-scenario.png)

### Trigger

A scenario begins with a **trigger**. The trigger watches for new and updated data, and starts the scenario when certain conditions configured in the module apply. Triggers can be configured to start a scenario on a schedule (polling), or whenever data changes occur (instant). 

![Trigger](assets/scenario-trigger.png)

### Module

The trigger is followed by a number of **modules**. A module represents single step in a scenario that performs a specific action. Modules are configured and chained together to create scenarios.

![Module](assets/scenario-module.png)

### Route

A scenario may be divided into **routes**. A route is a section of the scenario that may or may not be used for a given bundle of data. Routes are set up using a router module and filters.

![Route](assets/scenario-route.png)

### Scenario segment

A scenario segment is a section of a scenario that consists of a series of contiguous modules that all connect to the same application. Scenario segments often represent a short workflow in the application.

![Scenario segment](assets/scenario-segment.png)

### Connector

A connector is the set of modules for a given application. Workfront Fusion offers connectors to many common work applications, such as Workfront, Salesforce, and Jira, as well as generic connectors that can be used for any web service.

![Connectors](assets/scenario-connectors.png)

## Examples

Expand the following sections to view example scenarios and their explanations.

+++**Automating processes within Adobe Workfront**

Workfront Fusion enables you to automate simple or complex workflows within Workfront, saving time and ensuring that the process is executed consistently.

In this example, the scenario triggers when a specified field changes in a Task or Issue in [!DNL Workfront]. When triggered, the scenario gets information in the related project and creates a tailored update for a person assigned to a specific role on the project.

![Template example](assets/fusion-template-example.png)

+++

+++**Connecting Workfront to another app or web service**

>[!NOTE]
>
>If your organization uses the legacy licensing model, your organization must have a Workfront Fusion for Work Automation and Integration license to connect to other applications.

Workfront Fusion can connect to other applications and web services. You can access, import, manipulate, or export data from other applications, integrating them with Workfront or with each other.

Many applications have dedicated [!DNL Workfront Fusion] connectors. If there is no dedicated connector for the application you want to access, you can use Workfront Fusion's HTTP or SOAP modules to connect to the application through its API.

In this example, the scenario triggers when a user is added to an [!DNL Excel] spreadsheet. The scenario checks whether the user is in [!DNL Workfront]. If not, the scenario creates the user in [!DNL Workfront] and adds their Workfront user ID back to the spreadsheet.

![Integration example](assets/fusion-integration-example.png)

For a list of dedicated connectors, see [Fusion applications and their modules references: article index](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).


>[!IMPORTANT]
>
>[!DNL Adobe Workfront Fusion] can connect to almost any web service. If the app you want to work with does not have a dedicated [!DNL Workfront Fusion] connector, you use universal connectors to connect to the app or service.
>
>For a list of universal connectors, see [Universal connectors](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)

+++

## References

* For a glossary of terms used in Workfront Fusion, see [Adobe Workfront Fusion glossary](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md).
* To begin building a practice scenario, see [Create a basic scenario](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).
* For information on creating and managing scenarios, see the articles listed under:
   * [Create scenarios](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)
   * [Manage scenarios](/help/workfront-fusion/manage-scenarios/manage-scenarios-toc.md)
