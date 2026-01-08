---
title: API overview
description: Application Programming Interfaces (APIs) are a way for applications and services to communicate with one another. Fusion uses APIs to communicate with the application you are connecting to. Each application has a separate API.
author: Becky
feature: Workfront Fusion
---
# Overview of APIs in Fusion

<!--Add me to TOCs-->

Application Programming Interfaces (APIs) are a way for applications and services to communicate with one another. Fusion uses APIs to communicate with the applications that you are connecting to. 

APIs are created and controlled by the owners of the application. For example, the Workfront API is owned by the Workfront team at Adobe, and the Microsoft Graph API is owned by Microsoft. The owner of the API defines which actions are available through the API.

## Considerations

The fact that APIs are defined by their owners and not by Fusion leads to some important considerations:

* **You can use Fusion to connect to any app or service that has a public API**, whether or not Fusion offers a dedicated connector to that app or service. You can use Fusion's universal connectors to bring these apps or services into your scenarios.

   For a list of universal connectors, see [Universal connectors](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

* **Changes made to an application's API by its owner can affect Fusion functionality.** If the changes are severe enough, Fusion may need to update modules or connection types, or in extreme cases may create a new connector for the application.

   For more information on these extreme situations, known as "breaking changes," see [Breaking changes](#breaking-changes) in this article.
   

## Breaking changes

A common cause for breaking changes is deprecation, when an API owner removes part or all of an API from availability. When this occurs, the Fusion team makes every effort to quickly realign Fusion functionality with the new version of the application's API. This usually takes the form of new modules, connection types, or connectors.

Because your Fusion scenarios are configured with your specific data, you may need to update your scenarios.

* If the changes were related to authentication or authorization, you may need to update the connections for that application.
* If the changes were related to a specific action (endpoint) in the API, you may need to update any module related to that action to a new version of the module.
* If the entire API version used by Fusion is deprecated, you may need to update all modules of that connector to a new version of the connector.

In many cases, you can upgrade to the new version of a module without needing to reconfigure that module. 

For information and instructions on upgrading a module, see [Upgrade a module to a new version](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md).
