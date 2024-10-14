---
title: Adobe Workfront Fusion Glossary
description: The following glossary explains some common terms in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
---
# Adobe Workfront Fusion Glossary

The following glossary explains some common terms in Adobe Workfront Fusion.


<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Action</p> </td> 
   <td>A module that allows you to perform an action, such as reading or writing data from or into a selected app or service.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Aggregator</p> </td> 
   <td> <p>A type of module that merges together multiple bundles (multiple collections of data) into one single bundle. For more information, see <a href="/help/workfront-fusion/references/modules/aggregator-module.md" class="MCXref xref">Aggregator module</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API</td> 
   <td>Application Programming Interfaces (APIs) are a way for applications and services to communicate with one another. Fusion uses APIs to communicate with the application you are connecting to. Each application has a separate API. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API Key</td> 
   <td>A unique code that identifies the user, developer, or program that is calling a software's API, used for authentication. Because Fusion modules work by connecting APIs, API keys are sometimes necessary. API keys are distributed by the app that requires them. For example, if you need an API key to connect Fusion to Adobe Lightroom, you would request it though your Adobe Lightroom account.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">App or service</td> 
   <td> <p>A software application. Fusion can connect to most applications, even if it does not have a dedicated connector for that application.</p> <p>An app can also be a special function that manipulates data, such as an iterator or an aggregator. </p> <p>A service is a source of data that might include a web API, web page, different types of servers (FTP, SMTP, IMAP), and so on. </p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Bundle</p> </td> 
   <td> <p>A bundle is a basic unit of data that is returned or received by modules. For example, a Search module that returns three records would output three bundles of data, one for each record. A bundle consists of items.</p> </td> 
  </tr> 
  <tr>
   <td role="rowheader"> <p>Connection</p> </td> 
   <td> <p>A connections represents a set of credentials to connect to a given service. You can configure connections inside any module, and then can use that connection in any other module. Every module must have a connection selected, so that Fusion can use those credentials to access the information that the module requires. <!--For more information, see <a href="../../workfront-fusion/connections/about-connecting-wf-fusion-to-app-or-service.md" class="MCXref xref">Connections overview</a>.--></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Connector</td> 
   <td>A connector is the set of modules for a given application. Workfront Fusion offers connectors to many common work applications, such as Workfront, Salesforce, and Jira.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Cycle</p> </td> 
   <td> <p>A cycle consists two phases of the scenario run: operation and commit. The scenario may consists of one or more cycles. For more detailed information, see <a href="/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md" class="MCXref xref">Scenario execution, cycles, and phases in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Data Store</p> </td> 
   <td> <p>A data store stores data from scenarios or allows you to transfer data between individual scenarios or scenario runs. <!--For more information, see <a href="../../workfront-fusion/modules/data-stores.md" class="MCXref xref">Data Stores in [!UICONTROL Adobe Workfront Fusion]</a>.--></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Filter</p> </td> 
   <td> <p> A filter can be applied between two modules, and allows you to then only work with bundles that fit certain criteria. There are a number of different filters you can apply. <!-- For more information, see <a href="../../workfront-fusion/scenarios/add-a-filter-to-a-scenario.md" class="MCXref xref">Add a filter to a scenario in [!UICONTROL Adobe Workfront Fusion]</a>.--></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID </p> </td> 
   <td> <p>A name that is used to uniquely identify a bundle. An ID is usually used to differentiate a bundle that is to be updated or deleted from a given service. IDs can be mapped from the output of a previous module.</p> </td> 
  </tr> 
  <!--<tr> 
   <td role="rowheader"> <p>Items</p> </td> 
   <td> <p>A part of a bundle. Bundles can consist of multiple items. There are several different types of items: text, number, boolean (yes/no), date, time, buffer (binary data), collections, select menu, array, and validation.</p> </td> 
  </tr> -->
  <tr> 
   <td role="rowheader"> <p>Iterator</p> </td> 
   <td> <p>A type of module that allows you to take one bundle of data (a collection of data) and divide into separate bundles. These bundles can then be processed individually by later modules. <!--For more information, see <a href="../../workfront-fusion/modules/iterator-module.md" class="MCXref xref">[!UICONTROL Iterator] module in [!DNL Adobe Workfront Fusion]</a>.--></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Module</p> </td> 
   <td> <p>A single step within a scenario that performs a function, such as creating a record, within the associated app or service.</p> <p>Each app or service has various modules that define the way it responds to a request.</p>  <p> <img src="assets/module.png"> </p> <!--<p>For more information, see <a href="../../workfront-fusion/modules/module-types.md" class="MCXref xref">Types of modules</a>.</p>--> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Operation</p> </td> 
   <td> <p>A task performed by a module, such as retrieving a record or uploading a file.</p><!--<p>For more information, see <a href="../../workfront-fusion/get-started/operations-in-workfront-fusion.md" class="MCXref xref">Operations in [!DNL Adobe Workfront Fusion]</a>.</p>-->
  </tr> 
  <tr> 
   <td role="rowheader">Public/Private Keys</td> 
   <td>Public and private keys are used to encrypt and decrypt data. The public key can be distributed, and anyone with the public key can encrypt data, but only the private key can decrypt it. Similarly, a user with a private key can encrypt data that anyone with the public key can decrypt. The private key encryption assures that the data came from the owner of the private key and serves as validation of the data's source.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Router</p> </td> 
   <td>A router allows you to duplicate data or add new routes to a scenario, so to re-route data and handle different groups of data separately. <!--For more information, see <a href="../../workfront-fusion/modules/router-module.md" class="MCXref xref">[!UICONTROL Router] module in [!DNL Adobe Workfront Fusion]</a>.--></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Scenario</p> </td> 
   <td> <p>A user-created series of automated steps, each represented and performed by a module. The purpose of a scenario is to move and manipulate data.</p> <p> <img src="assets/entire-scenario-blank.png" style="width: 350;height: 178;"> </p> <!--<p> For more information, see <a href="../../workfront-fusion/scenarios/create-a-scenario.md" class="MCXref xref">Create a scenario in[!UICONTROL  Adobe Workfront Fusion]</a>.--></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Scenario segment</p> </td> 
   <td> <p> A scenario segments is a section of a scenario consisting of a series of modules that all connect to the same application. Scenario segments often represent a short workflow in the application.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Trigger</p> </td> 
   <td> <p>A trigger is a kind of module that watches for new and updated data, and starts the scenario when certain conditions configured in the module apply. Triggers can be configured to start a scenario on a schedule (polling), or whenever data changes occur (instant trigger or webhook).<!-- For more information, see <a href="../../workfront-fusion/webhooks/instant-triggers-webhooks.md" class="MCXref xref">Instant triggers (webhooks) in [!DNL Adobe Workfront Fusion]</a>.--></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Webhook</p> </td> 
   <td> <p>A special type of trigger that allows you to run a scenario immediately after a new bundle is available. For more information, see <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Instant triggers (webhooks) in [!UICONTROL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
