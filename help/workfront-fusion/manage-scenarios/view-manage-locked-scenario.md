---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Manage locked scenarios
description: Manage locked scenarios in [!DNL Adobe Workfront Fusion]
author: Becky
feature: Workfront Fusion
exl-id: 5fccf336-d904-43fe-ad4a-c3ce76dbcad0
---
# Manage locked scenarios

In some cases, a scenario might be temporarily locked in [!DNL Workfront Fusion]. Locked scenarios will be automatically unlocked within 2-4 hours. You can unlock scenarios manually, but it is not generally recommended.

Scenarios may be locked for a number of reasons:  

* Workfront Fusion does not support parallel processing of scheduled scenarios. These scenarios are locked at the beginning of the scenario execution and unlocked when it completes. If the execution is interrupted, the scenario may not unlock. This may occur when a user manually force-stops the scenario, or when there is a system issue.

* The Workfront Fusion engineering team may lock a scenario because it is causing performance or other issues.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] package</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] license</td> 
   <td> <p>New: [!UICONTROL Standard]</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] license**</td> 
   <td>
   <p>Current: No [!DNL Workfront Fusion] license requirement.</p>
   <p>Or</p>
   <p>Legacy: Any </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan: [!DNL Workfront Fusion] is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Access level configurations*</td> 
   <td> 
     <p>You must be a [!DNL Workfront Fusion] administrator for your organization.</p>
     <p>You must be a [!DNL Workfront Fusion] administrator for your team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/access-level-requirements-in-documentation.md).

<!--For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).-->

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
    ![](assets/unlock-scenario.png)