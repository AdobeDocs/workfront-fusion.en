---
title: Add a module to a scenario
description: This article describes the basic process of adding a module to a scenario.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
TQID: 'https://experienceleague.adobe.com/R2JCX7aaYzmYHgiLqj1WDlVFHI-s-qanltoOrycQ5JU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
---
# Add a module to a scenario

A scenario is comprised of a series of modules that indicate how data should be transformed within an app or transferred between apps and web services. You build a module by adding and configuring modules.

This article describes the basic process of adding a module to a scenario. For more specific instructions about ways to add a scenario, see the other articles under [Add modules: article index](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

>[!NOTE]
>
>Workfront Fusion is transitioning the scenario editor to a new experience. During this transition, both the classic and new experiences are available, and you can switch between them at any time. We recommend using the new experience. For more information, see [New and classic experiences](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) in the article Scenario editor.

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

## Add the first module to a scenario

The first module of a scenario is usually a trigger module.

For more information on trigger modules, see [Trigger modules](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) on the article Module overview.

* [Add the first module in the new experience (Recommended)](#add-the-first-module-in-the-new-experience-recommended)
* [Add the first module in the classic experience](#add-the-first-module-in-the-classic-experience)

### Add the first module in the new experience (Recommended)

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Begin creating a scenario by clicking **Create a new scenario** in the upper-right corner of the screen.

   The scenario editor opens, with a placeholder module and the list of available connectors.

   ![Placeholder module](/help/workfront-fusion/build-practice-scenarios/assets/new-placeholder-module.png)

   ![App and service picker](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. Select the connector or webhook that will start this scenario:

   * Browse by category using the panel on the left ([!UICONTROL Favorites], [!UICONTROL All apps], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative & Content], [!UICONTROL Adobe Cloud Services], [!UICONTROL Generative AI], or [!UICONTROL Built-in]), or
   * Enter a term in the search box. Results update as you type, and connector matches are listed before module name and description matches. 

1. Click the module that you want to add to the scenario.

1. Configure the module.

   The module's settings open in the panel on the right side of the canvas.

   For instructions on configuring specific modules, see the article for the chosen applications, listed in [Fusion applications and their modules references: article index](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>* In the list of connectors, badges identify private, premium, and beta apps. 
>* Modules for large apps are organized into groups. 
>* When you add an error handler, directives are listed first.
>* If a connector has more than one version, you will be able to select the version after selecting the connector.

>[!NOTE]
>
>If you have removed the first module from a scenario and want to replace it, click the placeholder module to open the list of connectors.

### Add the first module in the classic experience

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Begin creating a scenario by clicking **Create a new scenario** in the upper-right corner of the screen.

   The scenario editor opens, with a placeholder (question mark) module and the list of available connectors.

   ![Placeholder module](assets/placeholder-module.png)

1. Select the connector or webhook that will start this scenario. You can type the name of the connector in the search bar of the list to filter the list.
1. Configure the module.

   For instructions on configuring specific modules, see the article for the chosen applications, listed in [Fusion applications and their modules references: article index](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>If you have removed the first module from a scenario and want to replace it, click the placeholder (question mark) module to open the list of connectors.

## Add another module to a scenario

* [Add another module in the new experience (Recommended)](#add-another-module-in-the-new-experience-recommended)
* [Add another module in the classic experience](#add-another-module-in-the-classic-experience)

### Add another module in the new experience (Recommended)

1. If you are not in the scenario editor of the scenario where you want to add a module, click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Click anywhere on the scenario to enter the Scenario editor.
1. To add a module after another module, hover over the right edge of the module after which you want to add a module, then click **Add another module** when it appears.

    The list of connectors opens, showing any connectors already used in the scenario.

1. (Optional) To select another connector, click **Add another module** in the list, then select the connector:

   * Browse by category using the panel on the left ([!UICONTROL Favorites], [!UICONTROL All apps], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative & Content], [!UICONTROL Adobe Cloud Services], [!UICONTROL Generative AI], or [!UICONTROL Built-in]), or
   * Enter a term in the search box. Results update as you type, and connector matches are listed before module name and description matches.

1. Click the module that you want to add to the scenario.

1. Configure the module.

   The module's settings open in the panel on the right side of the canvas. 

   For instructions on configuring specific modules, see the article for the chosen applications, listed in [Fusion applications and their modules references: article index](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

### Add another module in the classic experience

1. If you are not in the scenario editor of the scenario where you want to add a module, Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Click anywhere on the scenario to enter the Scenario editor.
1. To add a module to another module, hover over the right handle of the module after which you want to add a module, then click **Add another module** when it appears.

    The list of connectors opens, showing any connectors already used in the scenario.

1. (Optional) To select another connector, click **Add another module** in the list, then select the connector. You can type the name of the connector in the search bar of the list to filter the list.
1. Configure the module.

   For instructions on configuring specific modules, see the article for the chosen applications, listed in [Fusion applications and their modules references: article index](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## Insert a module between existing modules in a scenario

* [Insert a module in the new experience (Recommended)](#insert-a-module-in-the-new-experience-recommended)
* [Insert a module in the classic experience](#insert-a-module-in-the-classic-experience)

### Insert a module in the new experience (Recommended)

1. If you are not in the scenario editor of the scenario where you want to add a module, click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Right-click the path between the modules where you want to insert a module, then select **Add a module**.

   ![Add a module between existing modules](assets/add-a-module-between-modules.png)

   The list of connectors opens, showing any connectors already used in the scenario.

1. (Optional) To select another connector, click **Add another module** in the list, then select the connector:

   * Browse by category using the panel on the left ([!UICONTROL Favorites], [!UICONTROL All apps], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative & Content], [!UICONTROL Adobe Cloud Services], [!UICONTROL Generative AI], or [!UICONTROL Built-in]), or
   * Enter a term in the search box. Results update as you type, and connector matches are listed before module name and description matches. 
   
1. Click the module that you want to add to the scenario.

1. Configure the module.

   The module's settings open in the panel on the right side of the canvas. 

   For instructions on configuring specific modules, see the article for the chosen applications, listed in [Fusion applications and their modules references: article index](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>To create a link to a specific module, add `?moduleId=<module-id>` to the URL when viewing the following pages:
>
>* Scenario edit page (URL ends in `/edit`)
>* A specific scenario execution (URL ends in `/logs/<log-id>`)
>
>`<module-id>` refers to the number next to the module label when viewing the scenario.
>
>This can be useful when debugging scenarios or copying module configuration.

### Insert a module in the classic experience

1. If you are not in the scenario editor of the scenario where you want to add a module, Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Click on the dotted path between the modules where you want to insert a module.
1. In the menu that appears, select **Add a module**.

The list of connectors opens, showing any connectors already used in the scenario.

1. (Optional) To select another connector, click **Add another module** in the list, then select the connector. You can type the name of the connector in the search bar of the list to filter the list.
1. Configure the module.

   For instructions on configuring specific modules, see the article for the chosen applications, listed in [Fusion applications and their modules references: article index](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>To create a link to a specific module, add `?moduleId=<module-id>` to the URL when viewing the following pages:
>
>* Scenario edit page (URL ends in `/edit`)
>* A specific scenarion execution (URL ends in `/logs/<log-id>`)
>
>`<module-id>` refers to the number next to the module label when viewing the scenario.
>
>This can be useful when debugging scenarios or copying module configuration.
