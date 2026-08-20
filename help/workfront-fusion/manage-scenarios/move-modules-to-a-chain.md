---
title: Move modules to a chain
description: You can select a group of modules in a scenario and move them into a new chained scenario, without manually recreating mappings or data structures.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# Move modules to a chain

>[!IMPORTANT]
>
>This feature is in Beta and is not recommended for mission-critical production workflows. As a Beta feature, behavior may change and edge cases may not be fully handled. 
>
>If you choose to use chained scenarios, carefully review the design guidance and constraints in [Chain multiple scenarios together](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md), particularly the Best Practices section.

You can select a group of modules in a scenario and move them into a new chained scenario, without manually recreating mappings or data structures. This provides an easy way to modularize large scenarios.

For information on planning chained scenarios, see [Chain multiple scenarios together](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

For instructions on configuring Chain modules manually, see [Chain modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any Adobe Workfront Workflow package and any Adobe Workfront Automation and Integration package</p><p>Workfront Ultimate</p><p>Workfront Prime and Select packages, with an additional purchase of Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront licenses</td> 
   <td> <p>Standard</p><p>Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisites

The modules that you want to move into a chain must already exist in a scenario, and you must select more than one module.

## Limitations

You cannot move a selection of modules into a chain in the following situations:

* The selected modules are not part of a single, unbroken flow. For example, you cannot select modules from two different, unconnected routes at the same time.
* The selection includes a webhook module.
* The selection includes another Chain module.
* A selected module has a subflow, such as an error handler route, and you have not also selected that subflow.
* The selection includes a Router module, and you have not selected all of that router's routes.

## Move modules into a chain

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario that contains the modules you want to move.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Select the modules that you want to move into a chain.

   Select more than one module by holding [!UICONTROL shift] and clicking on the modules that you want to move.
1. Right-click one of the selected modules.
1. Select **[!UICONTROL Move to Chain]**.

When you move a group of modules into a chain, Workfront Fusion:

* Moves the selected modules into a newly created scenario.
* Replaces the selected modules in the original scenario with a Chain module.
* Automatically creates the input and output data structures required for the new child scenario.
* Preserves the existing scenario behavior, so the scenario continues to run the same way it did before the modules were moved.
* Automatically updates mappings:
  * Modules moved into the child scenario receive data through the Chain module's inputs.
  * Outputs from the child scenario are automatically exposed back to the parent scenario.
  * Existing mappings in the blueprint are adjusted to match the new structure.

For information on the modules created by this action, see [Chain modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).
