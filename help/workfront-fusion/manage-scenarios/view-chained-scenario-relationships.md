---
title: View chained scenario relationships
description: You can a map of the relationships between parent and child scenarios.
author: Becky
feature: Workfront Fusion
exl-id: 0782c6b1-42a5-48de-bfa0-3ced6ed2bf7f
---
# View and manage chained scenario relationships

You can a map of the relationships between parent and child scenarios. You can also use the map to jump to different scenarios in the chain.

For more information on chained scenarios, see [Chain multiple scenarios together](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

For information on configuring chained scenarios, see [Chain modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md)

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

## View a map of chained relationships

You can view a map of the current scenario and its parent or child scenarios. The map displays a diagram of data flow throughout the chained scenarios.

![Chained scenario relationships](assets/chained-scenario-relationships-2.png)

<!--get a better picture-->

To view the relationship map for a chained scenario:

1. Click the **[!UICONTROL Scenario]** tab in the left panel, then click the scenario.

   Or

   If you are working on the scenario in the Scenario editor, click the left arrow ![Exit editing arrow](assets/exit-editing-arrow.png) near the upper-left corner of the window.

1. Click the **Relationships** tab.

   ![Relationships tab](assets/relations-tab.png)

1. For general details about each chained scenario, check the tags.

   Each scenario has one or more of the following tags:

   * Root: The scenario is the beginning of the chain, and has no parent scenario.
   * Parent: The scenario is a parent scenario.
   * Child: The scenario is a child scenario. A scenario can be both a parent and a child.
   * Current: This is the scenario that the user is currently viewing. In other words, this is the scenario from which the user opened the relationships map.

   ![Scenario tags in relationship map](assets/chained-scenario-maps-tag.png)
1. (Optional) To view a small diagram of a scenario, hover over the scenario.
1. (Optional) to go directly to another scenario from the map, click on the scenario. 

   The clicked scenario opens in another window.
1. (Optional) To switch between horizontal and vertical views of the map, click **Horizontal** or **Vertical** near the upper-right of the Scenario Details page.
1. (Optional) To see a simplified view of the map, check the lower-right corner of the page. 

   This may be convenient if your chain map is large or complex.

   * If you are viewing only a portion of the map, that portion is darker on the simplified map. 
   * The current scenario is marked in blue on the simplified map.
1. To view execution history for the chain, click the History tab near the top of the view. 

   You can click on a history to view the specific data passed between chained scenarios.
