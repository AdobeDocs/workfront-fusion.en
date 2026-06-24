---
title: View and manage scenario versions
description: You can view, restore, rename, or download blueprints for previous versions of a scenario.
author: Becky
feature: Workfront Fusion
exl-id: e7fd0351-b840-422c-b861-82ae110c703b
TQID: https://experienceleague.adobe.com/xVihxZH-fwPCIkryQAQEOWgeShtPTMXth4jEl5OLdbo
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# View and manage scenario versions

Adobe Workfront Fusion saves a version of your scenario every time it changes.

You can view, restore, rename, or download blueprints for previous versions of a scenario.

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

## View and manage a scenario's version history

1. Click **[!UICONTROL Scenarios]** ![Scenarios icon](assets/scenarios-icon.png) in the left panel, then click the scenario to open it.
1. Click the [!UICONTROL More] icon ![More icon](assets/more-icon.png) at the bottom of the screen, then click **[!UICONTROL Previous Versions]**.

   A list of previous versions displays.
1. (Optional) To rename the version, click the More menu ![More menu](assets/more-icon-vertical.png) on the line for that version, select **Edit**, and enter a name into the field. Click **Save** to save the new name.

   We recommend giving a name that describes changes made for this version.
1. (Optional) To download the blueprint for a previous version, click the More menu ![More menu](assets/more-icon-vertical.png) on the line for that version, then select **Download**.
1. (Optional) To compare changes between two versions, click **View changes** for that version.

   For details and instructions for comparing versions, see [Compare scenario versions](#compare-scenario-versions) in this article.
1. (Optional) To restore the version, click **Restore** on the line for that version


   >[!NOTE]
   >
   >The restored version of the scenario is not automatically saved. If you want to save the restored version of the scenario, you must save it manually.


## Compare scenario versions
​
View changes functionality shows what is different between two scenario versions, side by side, so you can see exactly what changed before you decide to restore an older one.

1. Click **[!UICONTROL Scenarios]** ![Scenarios icon](assets/scenarios-icon.png) in the left panel, then click the scenario to open it.
1. Click the [!UICONTROL More] icon ![More icon](assets/more-icon.png) at the bottom of the screen, then click **[!UICONTROL Previous Versions]**.

   A list of previous versions displays.
​
1. Click **View changes** for the scenario version that you want to view..
1. The **Review changes** view opens and compares that version with your current scenario.

   The Review changes panel opens to a side-by side view of two scenario versions.

   * On the left, you see the current version.
   * On the right, you see the version that you clicked. This is the version that you can restore.

   To understand changes, see [Examine changes](#examine-changes) in this article.

1. To select another version for either side, click the **Compare from** or **Compare to** dropdown near the top of the panel and select another scenario version.
1. To swap sides, click the **⇄** button between the scenarios.
1. To revert to the scenario on the right side, click **Revert to selected version**

   Restored versions are saved as new versions, and can therefore be reverted in the future.

   To revert to the scenario that is currently on the left side, swap sides so it is on the right, then click **Revert to selected version**.


### Examine changes

​
Each change is shown on the side it belongs to, and colored by what restoring would
do:

* Red (left): This change is not in the version on the right, and would be removed if the version was restored.
* Green (right): This change is in the version on the right, and would be added if the version was restored.

If something was changed, instead of removed or added, the value displays in red on the left, and in green on the right.
​
Changes are grouped into sections:
​

* **Scenario**: Name, description, and type.
* **Scenario settings**: Schedule and processing options.
* **Modules**: Modules added, removed, moved, or reconfigured.
* **Flows**: Banches added, removed, or reordered.
* **Router routes**: Routes and their contents.
* **Error handlers**: Error-handling branches.
* **Orphan groups**: Disconnected modules on the canvas.
​
If the two versions are identical, the view displays the message/ **No differences found**.
​
