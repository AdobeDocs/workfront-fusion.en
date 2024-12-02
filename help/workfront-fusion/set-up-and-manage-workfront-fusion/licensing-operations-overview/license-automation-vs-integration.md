---
title: Adobe Workfront Fusion licenses
description: Adobe Workfront Fusion offers two different licenses that determine the functionality you are able to access. Your organization chose one of these licenses when it purchased Workfront Fusion.
author: Becky
feature: Workfront Fusion
---
# Adobe Workfront Fusion licenses

Workfront Fusion has two licensing models, a new operations-based model, and a legacy connector-based model. 

## Operations-based licensing model (New)

The new Workfront Fusion licensing model is based on the number of operations your organization uses. In this model, all organizations have access to the same functionality.

If your organization has a Workfront Ultimate plan, your Fusion instance is included in your plan and allows an unlimited number of Fusion operations per month. If your organization has a Workfront Prime or Select plan, Fusion can be purchased, and pricing is based on the number of operations performed in a month. 

For information on what counts as an operation under the new licensing model, see [Operations](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

## Connector-based licensing model (Legacy)

In the Adobe Workfront Fusion legacy licensing model, Fusion offers two different licenses that determine the functionality you are able to access. Your organization chose one of these licenses when it purchased Workfront Fusion.

* [Workfront Fusion for Work Automation](#workfront-fusion-for-work-automation)
* [Workfront Fusion for Work Automation and Integration](#workfront-fusion-for-work-automation-and-integration)

To find out what type of Workfront Fusion license your organization has, contact your Workfront Fusion administrator.

### Workfront Fusion for Work Automation 

* [Benefits of Workfront Fusion for Work Automation](#benefits-of-workfront-fusion-for-work-automation)
* [Connectors and modules available for Workfront Fusion for Work Automation](#connectors-and-modules-available-for-workfront-fusion-for-work-automation)
* [Example of Workfront Fusion for Work Automation](#example-of-workfront-fusion-for-work-automation)

#### Benefits of Workfront Fusion for Work Automation 

A Workfront Fusion for Work Automation license allows you to automate your [!DNL Workfront] workflows. By using Workfront Fusion for Work Automation, you can create scenarios to automate your organization's unique work processes. 

Benefits to automating your [!DNL Workfront] processes include the following:

* Automation is quicker and less prone to error.
* Workflows that don't require any decisions, or that have decisions are based on simple logic such as if/then, are good candidates for automation.
* Automation can address specific needs in workflows used by your organization that aren't directly addressed in the Workfront product.

#### Connectors and modules available for Workfront Fusion for Work Automation 

With the Workfront Fusion for Work Automation license, you have access to the following:

* Adobe Workfront
* Workfront Proof
* Webhooks
* Tools and transformer modules such as:

    * Archive
    * CSV
    * Data Stores
    * Image
    * JSON
    * Math
    * MIME
    * XML

#### Example of Workfront Fusion for Work Automation 

The following example shows a workflow that:

1. Watches for a field change
1. Gets information about the object the field is attached to, including who the object is assigned to
1. Sends a notification about the field change to the user the object is assigned to

![Automation example](/help/workfront-fusion/references/apps-and-modules/assets/fusion-template-example.png)

### Workfront Fusion for Work Automation and Integration 

* [Benefits of Workfront Fusion for Work Automation and Integration](#benefits-of-workfront-fusion-for-work-automation-and-integration)
* [Connectors and modules available for Workfront Fusion for Work Automation and Integration](#connectors-and-modules-available-for-workfront-fusion-for-work-automation-and-integration)
* [Example of Workfront Fusion for Work Automation and Integration](#example-of-workfront-fusion-for-work-automation-and-integration)

#### Benefits of Workfront Fusion for Work Automation and Integration {#benefits-of-workfront-fusion-for-work-automation-and-integration}

A Workfront Fusion for Work Automation and Integration license allows you access to all of the functionality of the Workfront Fusion for Work Automation license. In addition, this license lets you use other apps and services in your scenarios. For example, you can use Workfront Fusion to automate a process that imports Jira tickets, then turns them into tasks in Workfront. You can also use the HTTP or SFTP connectors to connect to almost any web service, even if Workfront Fusion does not have a dedicated connector for it.

Benefits of a Workfront Fusion for Work Automation and Integration license include the following: 

* Workfront Fusion for Work Automation and Integration includes all of the benefits associated with Workfront Fusion for Work Automation
* Integration reduces the need to jump into and out of various apps when completing a workflow.
* Automating data transfer between applications is quicker and less prone to error than manually transferring data

#### Connectors and modules available for Workfront Fusion for Work Automation and Integration 

<!--For a list of available dedicated connectors, see [Apps and their modules](../../workfront-fusion/apps-and-their-modules/apps-and-their-modules.md).-->

>[!IMPORTANT]
>
>Workfront Fusion can connect to almost any web service. If the app you want to work with does not have a dedicated connector, you can use the [!UICONTROL HTTP], [!UICONTROL SFTP], or [!UICONTROL JSON] connectors to connect directly to the web service.

#### Example of Workfront Fusion for Work Automation and Integration

The following example shows a workflow that:

1. Watches a spreadsheet for new users
1. Checks to see if the user exists in [!DNL Workfront]
1. Creates the user in [!DNL Workfront] if the user did not exist
1. Uploads the [!DNL Workfront] user ID back to the spreadsheet.

![Example automation scenario](/help/workfront-fusion/references/apps-and-modules/assets/fusion-integration-example.png)
