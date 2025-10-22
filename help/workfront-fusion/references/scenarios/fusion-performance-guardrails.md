---
title: Fusion Performance Guardrails
description: Work automation requires rapid processing, so Adobe Workfront Fusion is designed for high performance. Because long-running scenarios can slow down the pace of your work, we've designed Workfront Fusion with performance-preserving guardrails that limit execution time, data size, and other scenario parameters. Workfront Fusion designers should be aware of these guardrails and incorporate them into their design practices.
author: Becky
feature: Workfront Fusion
exl-id: d142a521-edbc-4d7b-b5cd-872a9d3d2e1c
---
# Fusion performance guardrails

Work automation requires rapid processing, so Adobe Workfront Fusion is designed for high performance. Because long-running scenarios can slow down the pace of your work, we've designed Workfront Fusion with performance-preserving guardrails that limit execution time, data size, and other scenario parameters. Workfront Fusion designers should be aware of these guardrails and incorporate them into their design practices.

## Browsers

* Workfront Fusion supports only Chrome based browsers.

## Scenarios

* The default scenario execution timeout is **40 minutes**. When the execution reaches this timeout, Workfront Fusion interrupts scenario execution after the next cycle or operation, depending on the scenario. This forces the scenario to stop shortly after the 40 minute limit is reached

   Chaining scenarios does not count toward scenario execution timeout. A parent scenario does not accrue time while waiting for a child scenario to execute.
* The maximum size of a scenario blueprint is **5 MB**, but we recommend keeping scenario size under **3 MB**.

  App modules that create or update data with large numbers of fields can cause very large blueprints.

  * When using the Workfront app, be sure to only select fields needed for your create or update use cases. 
  * When using other apps, use custom API modules to interact with any record type that has a large number of fields.

* While there is no cap for the number of modules in a scenario, scenarios with more than 150 modules negatively impact the performance of your Workfront Fusion system. For this reason, we do not recommend creating scenarios with over 150 modules.

## Operations

* The default operation timeout is typically **40 seconds**.

<!--
* The operation timeout for calls to Adobe Workfront is **120 seconds**.
-->

## Files

* Fusion's total processing capacity for files is **1 GB**. The limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.
* Organizations on the Workfront Ultimate plan have access to increased file processing beyond 1 GB. However, there are other factors that affect data transfer. The service that Fusion is connecting to may limit file size, which would affect any files processed by that service In addition, large files can affect scenario execution time. Fusion will process files until the execution limit of 40 minutes is reached, at which point the execution will fail. 
* If a file is downloaded using a module that supports large files and then passed to a module that does not support large files, that module does not successfully process the file. Large files must be handled exclusively with supported modules throughout the workflow.
* Modules that do not support large files can process files up to **200 MB** in size.

For more information, see [Working with large files](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

## Server Memory Usage

* Server memory usage for a single execution is limited to **1 GB**.

  Many factors, such as large files or complex modules, can affect server memory usage in ways that are difficult to predict or control. Because of this, your scenario execution may exceed the 1 GB memory limit, even if the scenario follows all other performance guardrails. Exceeding the memory limit causes the execution to fail.

## Webhooks

* The default maximum size of a payload is **5 MB**.
* Webhooks are limited to **100 requests per second**. When this limit is reached, Workfront Fusion sends a 429 ([!UICONTROL Too Many Requests]) status.
* Workfront Fusion stores webhook payloads for 30 days. Accessing a webhook payload more than 30 days after it was received results in the error "[!UICONTROL Failed to read file from storage.]"
* Webhooks are deactivated automatically if either of the following applies:

  * The webhook has not been connected to any scenario for more than 5 days
  * The webhook is used only in inactive scenarios, which have been inactive for more than 30 days.

* Deactivated webhooks are deleted and unregistered automatically if they are not connected to any scenarios and have been in deactivated status for over 30 days.
* Timeout for a webhook response is 5 minutes.

## Execution history

* Execution history logs are limited to a size of **100 MB**. If the execution history exceeds this size, only the first 100 MB will be shown.
* If a scenario has multiple concurrent executions, only 5 executions display in the Executions area of the scenario details page. This is true even when more than 5 executions are running.

## Incomplete executions

* Incomplete executions are limited to a total size of **10 MB** per scenario. If the 10 MB limit is reached, no more incomplete executions will be stored for that scenario.
* Incomplete executions are limited to a total size of **500 MB** per team. If the 500 MB limit is reached, no more incomplete executions will be stored for that team.
* Workfront Fusion allows up to 5 failures per minute.

## Retries

* When using the Break module and specifying the Retry directive, if a scenario fails consecutively 10 times within a 2-minute timeframe, the scenario will be automatically deactivated.

## Recursion

Recursion occurs when a scenario triggers a new execution of itself, which triggers a new execution, and so on in an infinite loop. 

For example, a scenario is triggered when a task is created, and that scenario creates two tasks. The newly created tasks both trigger the scenario again, which create four new tasks. Every time a task is created, the scenario is triggered, and every time the scenario runs, the number of tasks doubles. The number of tasks grows exponentially.

Recursion can cause performance issues for both the organization that owns the recursive scenario, and to other organizations.

Consider the following regarding recursion:

* **When a scenario is causing recursion, it is deactivated by the Fusion engineering team to prevent further performance issues.**
* Because recursion is a result of scenario design, you must design your scenarios in a way that ensures that the scenario does not include actions that trigger the scenario.

## TLS

* Fusion currently supports TLS version 1.2 by default.
* Fusion can use TLS 1.3 for outbound HTTPS requests if TLS 1.3 is enabled for the destination service. 
* Fusion supports both TLS 1.2 and TLS 1.3 for incoming HTTPS requests to Webhooks.
* Organizations can request that TLS version 1.3 be enabled for their Fusion instance.

>[!NOTE]
>
> If you are connecting to Workfront, be aware that this TLS functionality is enabled in Workfront for calls to domains that have the format `https://<domain>.my.workfront.com`. 
