---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Workfront Fusion release activity: Week of May 3, 2021'
description: This page describes all enhancements made in Adobe Workfront Fusion the week of May 3, 2021.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: yes
exl-id: 8858fc79-5eda-4938-9bb5-c05be38f02bc
---
# Workfront Fusion release activity:&nbsp;Week of May 3, 2021

This page describes all enhancements made in Adobe Workfront Fusion the week of May 3, 2021.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) page and check for any updates labeled Workfront Fusion Maintenance Update.

## Salesforce connector can now search using SOQL

The Salesforce > Search for records module now has the option to search using SOQL (Salesforce Object Query Language). You can also search using the previously available options (SOSL and simple searches).

## New connection type in Azure DevOps connector requires fewer scopes

To enhance security, we've added a new connector type to the Workfront Fusion Azure DevOps Connector. Now, when you create a connection in an Azure DevOps module, you can select from two types of connections:

* Azure DevOps

  This new connection type limits scopes to those specifically needed by Workfront Fusion.

* Azure DevOps (Request all scopes)

  This is the legacy connection type, which requests all scopes available in a connection to Azure DevOps.

We recommend that you use the Azure DevOps connection type in all your new scenarios that use Azure DevOps. We also recommend that you change any Azure DevOps modules in your existing scenarios to use the new connection type. The legacy Azure DevOps (Request all scopes) connection type will be deprecated in the near future.
