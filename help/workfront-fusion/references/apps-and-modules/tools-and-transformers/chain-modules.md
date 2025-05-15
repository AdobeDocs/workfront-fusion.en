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

This module is the trigger module in the child scenario, and is triggered by the Add ChainCaller module in the parent scenario. It receives data from the parent scenario, which can be processed in the child scenario.

To configure the Add Receiver module:

1. (Optional) To use an existing data structure, in the Data structure field, select the data structure that will be used for the scenario's input data. 
1. (Optional) To create a new data structure to use as the scenario's input data, click **Add** next to the Data structure field and create the data structure.

   For instructions on creating a data structure, see [Data structures](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Click **OK** to save the module.

### Actions

#### Add ChainCaller

This module is located in the parent scenario. The fields reflect the data structure set in the Add Receiver module in the child scenario.

>[!NOTE]
>
>* You can select an existing child scenario, or create a new one through this module.
>* You can create the data structure when creating child scenario.

To configure the Add ChainCaller module

1. Add the Add ChainCaller module to your scenario.
1. (Optional) To use an existing scenario, in the Chain field, select the child scenario that you want to call.
1. (Optional) To use a new scenario, click Add next to the Chain field. For instructions on configuring the child scenario, see []().

   The fields configured in the trigger module of the child scenario appear in the Add ChainCaller module.

1. Enter or map the information to be passed to the child scenario into the Add ChainCaller module.
1. Click **OK** to save the module.

#### Add Respond

This is in the child scenario, and sends data in the selected structure to the parent scenario. You can map this data in later modules in the parent scenario.

To configure the Add Responder module:

1. (Optional) To use an existing data structure, in the Data structure field, select the data structure that will be used for the scenario's input data. 
1. (Optional) To create a new data structure to use as the scenario's input data, click **Add** next to the Data structure field and create the data structure.

   For instructions on creating a data structure, see [Data structures](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Click **OK** to save the module.

