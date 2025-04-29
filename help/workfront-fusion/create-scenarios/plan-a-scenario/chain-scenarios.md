---
title: Chain Multiple Scenarios Together
description: You can chain scenarios together, allowing one scenario to trigger another, and returning the data output by the second scenario to the first.
author: Becky
feature: Workfront Fusion
---

# Chain multiple scenarios together

You can chain scenarios together, allowing one scenario to trigger another, and returning the data output by the second scenario to the first. <!--This allows you to ???-->

<!--This article will be about the concept and use cases-->

For instructions on configuring Chain modules, see [Chain modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

## Parent and child scenarios

* The **parent** scenario calls another scenario, using the **Chain** > **Add ChainCaller** module. It receives the output of the child scenario, which it can process in later scenario modules. 
* The **child** scenario is called by the parent scenario. Its trigger module receives data from the parent scenario, and returns output to the parent scenario.

The parent scenario requires a response from the child scenario. Child scenarios that do not return data are currently not supported.

## Data structures in chained scenarios

Workfront Fusion uses data structures to transfer information from the parent scenario to the child scenario. The data structure is configured in the child scenario. When the child scenario is selected from the parent scenario, the fields for that data structure appear in the parent scenario. You can map values to these fields, which are passed to the child scenario when it is triggered.

For information on the modules to configure in the parent and child scenarios, see [Chain modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

For information on data structures, see [Data structures](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).


## Use cases

## Planning your parent and child scenarios



