---
title: Chain Multiple Scenarios Together
description: You can chain scenarios together, allowing one scenario to trigger another, and returning the data output by the second scenario to the first.
author: Becky
feature: Workfront Fusion
hide: yes
hidefromtoc: yes
exl-id: def8d4c1-fc20-4b93-b1fd-be2f60300464
---
# Chain multiple scenarios together

You can chain scenarios together, allowing one scenario to trigger another, and returning the data output by the second scenario to the first. This allows more modular scenario creation, where you do not have to duplicate scenario sections in multiple scenarios.

You can call multiple child scenarios from a parent scenario, and you can call a child scenario from multiple parent scenarios. You can also nest child scenarios, calling one from another.

When a parent scenario is waiting for a child scenario to return data, that time does not count against the parent scenario's timeout. For example, a parent scenario calls 5 child scenarios, each of which takes 10 minutes to run, for a total of 50 minutes. The modules in the parent scenario itself take 15 minutes to run. The parent scenario does not time out, even though a total of 65 minutes has passed, which is over the timeout limit of 40 minutes.

For more information on Fusion's performance guardrails, including timeouts, see [Fusion performance guardrails](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md).

For instructions on configuring Chain modules, see [Chain modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

## Parent and child scenarios

* The **parent** scenario calls another scenario, using the **Chain** > **Call a child scenario** module. It receives the output of the child scenario, which it can process in later scenario modules. 
* The **child** scenario is called by the parent scenario. Its trigger module receives data from the parent scenario, and returns output to the parent scenario.

The parent scenario requires a response from the child scenario. Child scenarios that do not return data are currently not supported.

## Data structures in chained scenarios

Workfront Fusion uses data structures to transfer information from the parent scenario to the child scenario. The data structure is configured in the child scenario. When the child scenario is selected from the parent scenario, the fields for the data structure used as the child scenario's input appear in the parent scenario. You can map values to these fields, which are passed to the child scenario when it is triggered.

For information on the modules to configure in the parent and child scenarios, see [Chain modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

For information on data structures, see [Data structures](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

## Data flow

1. Data flows through the parent scenario.
1. Data reaches the Call a child scenario module. Data is mapped to the fields in the Call a child scenario module, which match the fields in the data structure used in the child scenario's trigger module.
1. Data from the Call a child scenario is passed to the child scenario.
1. The child scenario processes data and performs actions.
1. The child scenario ends with the Return response to parent module.
1. The output of the Return response to parent module is passed to the parent scenario.
1. The output of the Call a child scenario is the output of the child scenario. This output can be processed later in the parent scenario.

## Use cases

Consider the following example use cases for chaining scenarios:

* **Reusable logic**:  You can chain scenario for repeated actions used across multiple scenarios. For example, if you have multiple scenarios that archive content, you can create a single child scenario called "Archive content" that you can then use as a child scenario for any workflows that archive content.

* **Error handling**: It's common for organizations to have the same error handling actions across multiple scenarios, such as an error handling route that sends an error log to a data store and creates a slack notification. You can create a child scenario with these actions and chain that scenario in error handling routes in multiple scenarios.

* **Extending time**: You can use chaining for large batch operations with long running actions, such as when you to export and import files. This operation takes some time if there are many files. Because child scenarios do not count against the parent scenario's timeout, you can exceed execution time by using multiple child scenarios to export or import the files.

* **Replacing iterators** Replacing iterators with child scenarios can reduce memory usage, such as in complex operations in an iteration that cause Out of Memory error. You can create a separate scenario for the complex operation and replace the iterator with Call a child scenario module

* **Search for and create a record**:  For example, you could create a scenario that searches for a user. If they exist, the scehario adds them as approver with access they need to review and approve. If they don't exist, the scenario creates a request for the admin to onboard a new user.

## Viewing execution history for chained scenarios

You can view execution history for chained scenarios by viewing the history of each scenario included in the chain. For example, the parent scenario's execution history would include information about modules and data processed directly in the parent scenario. To view execution history for modules and data processed in a child scenario, open the child scenario and view the execution history there.

We recommend using the **Go to the child scenario** button in the Call a child scenario module to quickly go to the child scenario, where you can view its execution history. The child scenario opens in another browser window, allowing you to see parent and child scenarios at the same time.

![Go to the child scenario button](assets/go-to-the-child-button.png)

## Errors and incomplete executions

### Error handling

If the child scenario errors out, that may affect getting data back to your parent. 

We recommend configuring error handling in the child scenario to ensure that if something goes wrong in the child scenario, the parent scenario is not stuck waiting for the response from the child scenario.

## Best Practices

Consider the following best practices when chaining a scenario.

### Avoid recursion when chaining scenarios

Recursion occurs when a scenario triggers a new execution of itself, which triggers a new execution, and so on in an infinite loop.

Recursion can cause performance issues for both the organization that owns the recursive scenario, and to other organizations.

When chaining scenarios, follow these practices to avoid recursion:

* Ensure that **child scenarios cannot trigger the parent scenario**. For example, if a parent scenario is triggered when a request is created, ensure that the child scenarios do not create requests.
* Ensure that **child scenarios do not call each other**. For example, If child scenario A calls child scenario B, ensure that child scenario B does not call child scenario A.
* Ensure that **a scenario cannot call itself**. For example, a scenario is triggered when a task is created, and that scenario creates two tasks. The newly created tasks both trigger the scenario again, which create four new tasks. Every time a task is created, the scenario is triggered, and every time the scenario runs, the number of tasks doubles. The number of tasks grows exponentially.

>[!IMPORTANT]
>
>* **When a scenario is causing recursion, it is deactivated by the Fusion engineering team to prevent further performance issues.**
>* Because recursion is a result of scenario design, you must design your scenarios in a way that ensures that the scenario does not include actions that trigger the scenario.

### Use error handling to ensure a response

Because the parent scenario is waiting for a response from the child scenario before it can continue, you must ensure that the child scenario is built so that it will provide a response even if it encounters an error.
