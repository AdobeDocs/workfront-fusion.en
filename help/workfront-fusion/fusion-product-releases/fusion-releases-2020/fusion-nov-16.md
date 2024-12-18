---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Workfront Fusion release activity: Week of November 16, 2020'
description: This page describes all enhancements made in Adobe Workfront Fusion the week of November 16, 2020.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: yes
exl-id: 69e4a458-fd32-4dcd-be43-19a9467cf678
---
# Workfront Fusion release activity:&nbsp;Week of November 16, 2020

This page describes all enhancements made in Adobe Workfront Fusion the week of November 16, 2020.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) page and check for any updates labeled Workfront Fusion Maintenance Update.

## Updates to Jira Cloud connector

To expand the ways you can use the Jira Cloud connector, we've added three new modules:

* Add issue to sprint
* List Records
* Search for Records

We've also updated existing modules to support the "Sprint" object type. Previously, the "Sprint" object could only be accessed through the Custom API Call module.

## Execution ID is now available for mapping in scenarios

The Execution ID for a scenario is now available in the mapping panel. This ID represents a specific execution of the scenario, and can be used as metadata. For example, the execution ID can be saved with a record that Fusion creates, so that you can later determine which Fusion execution created the record. You can find the Execution ID in the mapping panel under General Functions.

## Keyboard shortcuts for Workfront Fusion 2.0 scenarios

To make scenario building more convenient, we've added some keyboard shortcuts:

* Ctrl/Cmd+Shift+Enter: Run a scenario once
* Ctrl/Cmd + Shift + S: Save a scenario

## Updates to Office 365 Excel connector

To expand the ways you can use the Office 365 Excel connector, we've added some new modules. Now you can:

* Trigger a module from changes to workbooks
* Search or download workbooks
* List worksheets, worksheet rows, tables, or table rows
* Update a table or worksheet row
* Delete a table or worksheet row
* Retrieve metadata for a table
* Make a custom API call

Previously available modules are still present in the app.


## Use OAuth 2.0 in your Workfront app connections

We've updated the Workfront connector to use OAuth 2.0. This update means that it's easier to make changes in your Workfront app connections. For example, if something about your connection changes (such as a password), you no longer need to update each individual connection in your scenarios. In addition, OAuth2 provides other benefits such as improved security and the ability to use Single Sign-on (SSO).

Existing connections do not require any changes at this time. You can, however, reauthorize existing connections if you want to take advantage of the benefits of OAuth 2.0.
