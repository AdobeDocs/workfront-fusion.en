---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Manage locked scenarios
description: Manage locked scenarios in Adobe Workfront Fusion
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
---
# Manage locked scenarios

In some cases, a scenario might be temporarily locked in Workfront Fusion. Locked scenarios will be automatically unlocked within 2-4 hours. You can unlock scenarios manually, but it is not generally recommended.

Scenarios may be locked for a number of reasons:  

* Workfront Fusion does not support parallel processing of scheduled scenarios. These scenarios are locked at the beginning of the scenario execution and unlocked when it completes. If the execution is interrupted, the scenario may not unlock. This may occur when a user manually force-stops the scenario, or when there is a system issue.

* The Workfront Fusion engineering team may lock a scenario because it is causing performance or other issues.

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

## Unlock a locked scenario

Locked scenarios will unlock 2-4 hours from the time they were locked. You can unlock a scenario manually before it is scheduled to unlock automatically. 

>[!WARNING]
>
>Unlocking a scenario manually can cause errors in a scenario's executions. We recommend manually unlocking scenarios only when a scenario is locked due to running and stopping executions as part of designing the scenario. In other circumstances, we recommend that you wait for the scenario to be unlocked automatically.


To manually unlock a locked scenario:

1. Go the Scenario details page of the locked scenario.
1. Click **[!UICONTROL Options]** in the upper-right corner of the screen.
1. Select **[!UICONTROL Unlock execution]**.
1. Click **[!UICONTROL Unlock]**.
    ![Unlock scenario](assets/unlock-scenario.png)
