---
title: Chain Multiple Scenarios Together
description: You can chain scenarios together, allowing one scenario to trigger another, and returning the data output by the second scenario to the first.
author: Becky
feature: Workfront Fusion
---

# Chain multiple scenarios together

You can chain scenarios together, allowing one scenario to trigger another, and returning the data output by the second scenario to the first. This allows more modular scenario creation, where you do not have to duplicate scenario sections in multiple scenarios.

You can call multiple child scenarios from a parent scenario, and you can call a child scenario from multiple parent scenarios. You can also nest child scenarios, calling one from another.

When a parent scenario is waiting for a child scenario to return data, that time does not count against the parent scenario's timeout. <!--For example, if a parent scenario calls 5 child scenarios, each of which takes 10 minutes to run, for a total of 50 minutes. The modules in the parent scenario itself take 15 minutes to run. The parent scenario does not time out, even though a total of 65 minutes has passed, which is over the timeout limit of 40 minutes.-->

<!--Example???-->

<!--This article will be about the concept and use cases-->

For instructions on configuring Chain modules, see [Chain modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

## Parent and child scenarios

* The **parent** scenario calls another scenario, using the **Chain** > **Add ChainCaller** module. It receives the output of the child scenario, which it can process in later scenario modules. 
* The **child** scenario is called by the parent scenario. Its trigger module receives data from the parent scenario, and returns output to the parent scenario.

The parent scenario requires a response from the child scenario. Child scenarios that do not return data are currently not supported.

## Data structures in chained scenarios

Workfront Fusion uses data structures to transfer information from the parent scenario to the child scenario. The data structure is configured in the child scenario. When the child scenario is selected from the parent scenario, the fields for the data structure used as the child scenario's input appear in the parent scenario. You can map values to these fields, which are passed to the child scenario when it is triggered.

For information on the modules to configure in the parent and child scenarios, see [Chain modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

For information on data structures, see [Data structures](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

## Data flow

1. Data flows through the parent scenario.
1. Data reaches the ChainCaller module. Data is mapped to the fields in the ChainCaller module, which match the fields in the data structure used in the child scenario's trigger module.
1. Data from the ChainCaller is passed to the child scenario.
1. The child scenario processes data and performs actions.
1. The child scenario ends with the Add Respond module.
1. The output of the Add Respond module is passed to the parent scenario.
1. The output of the ChainCaller is the output of the child scenario. This output can be processed later in the parent scenario.

## Use cases

## Planning your parent and child scenarios

## Errors and incomplete executions

### Error handling

If the child scenario errors out, that may affect getting data back to your parent 

