---
title: Chain Modules
description: Using these modules, you can chain scenarios together, making one call another.
author: Becky
feature: Workfront Fusion
---
# Chain modules

Using the Chain modules, you can connect one scenario to another.

<!--This article will be about the specific module configuration-->

For instructions on planning chained scenarios, see [Chain multiple scenarios together](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).


## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current:  Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>No Workfront Fusion license requirement</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>Select or Prime Workfront package: Your organization must purchase Adobe Workfront Fusion.</li><li>Ultimate Workfront package: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Chain modules and their fields

### Triggers

#### Add Receiver

This is a trigger in the child scenario. It's called by the Add ChainCaller module in the parent scenario. You can push data to the child scenario and map that data in the child scenario.

### Actions

#### Add ChainCaller

This is in the parent scenario. The fields reflect the data structure set in the Add Reciever module in the child scenario.

Can create child scenario here by clicking Add and setting the input data structure (Receiver) and output data structure (Respond). Can create data structure when creating child scenario.

#### Add Respond

This is in the child scenario, and sends data in the selected structure to the parent scenario. You can map this data in later modules in the parent scenario.
