---
title: Create new templates
description: You can create new scenario templates in [!DNL Adobe] Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 9cb9bd04-e9ae-4162-a1b9-d71566582b7a
---
# Create new templates

You can create new scenario templates in [!DNL Adobe] Workfront Fusion.

>[!TIP]
>
>Before creating a new template, you can check the [!UICONTROL Public templates] tab to ensure that the template you want to create is not already available.

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
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Create a new template

You can build a template in a process similar to building a scenario. Fusion administrators can also create templates from existing scenarios.

* [Build a template](#build-a-template)
* [Create a template from a scenario](#create-a-template-from-a-scenario)

### Build a template

1. Click **[!UICONTROL Templates]** ![](assets/templates-icon.png) in the left navigation panel.
1. Click **[!UICONTROL Create a new template]** in the upper-right corner.
1. (Optional) Rename the template by replacing the default **[!UICONTROL New template name]** in the upper-left corner.
1. (Optional) To change the language of your template, click **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) and select the language from the Language drop-down.

   >[!IMPORTANT]
   >
   >The Languages selection corresponds to the languages available in the system settings and concerns only the name of the public template and its description. You can't change a template language once the template has been saved.

1. (Optional) To enter a description of the template, click **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png ) and enter the description.
1. Add apps, modules, and tools, using the same processes as adding modules to a scenario.

   For instructions, see the articles under [Add modules](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   To add contextual help to the modules, see [Set up Wizard functionality](#set-up-wizard-functionality) in this article.

   For more information on building a scenario, see [Create a scenario](/help/workfront-fusion/create-scenarios/plan-a-scenario/create-a-scenario-workflow.md).

   >[!NOTE]
   >
   >If your template includes modules that require adding the connection, credentials, or other privacy-sensitive information, this information is not shared with the template users.

1. (Optional) Click **[!UICONTROL Run once]** to test your template.
1. Click the **[!UICONTROL Save]** icon ![](assets/save-icon.png) to save the template.

When you save your template, it becomes visible to your team members. If you want your template to be accessible outside of your team, you must submit a request to have it approved and published. The request is sent to the Adobe Workfront Fusion team for approval. After it is approved, the template is accessible by others outside of your team.

For information on publishing templates, see [Publish and share [!DNL Adobe Workfront Fusion] templates](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md).

### Create a template from a scenario

>[!NOTE]
>
>You must be a Fusion administrator to create a template from a scenario. 

1. Click the **[!UICONTROL Scenario]** tab in the left panel.
1. Select the scenario that you want to create a template from.
1. Click the **Admin** drop down near the upper-right corner of the page.
1. Select **Clone as template**.
   
   The scenario is copied into a New template page.
1. (Optional) Rename the template by replacing the default **[!UICONTROL New template name]** in the upper-left corner.
1. (Optional) To change the language of your template, click **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) and select the language from the Language drop-down.

   >[!IMPORTANT]
   >
   >The Languages selection corresponds to the languages available in the system settings and concerns only the name of the public template and its description. You can't change a template language once the template has been saved.

1. (Optional) To enter a description of the template, click **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) and enter the description.
1. Edit apps, modules, and tools as desired, using the same processes as adding modules to a scenario.

   For instructions, see the articles under [Add modules](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   To add contextual help to the modules, see [Set up [!UICONTROL Wizard] functionality](#set-up-wizard-functionality) in this article.

   >[!NOTE]
   >
   >If your template includes modules that require adding the connection, credentials, or other privacy-sensitive information, this information is not shared with the template users.

1. (Optional) Click **[!UICONTROL Run once]** to test your template.
1. Click the **[!UICONTROL Save]** icon ![](assets/save-icon.png).

## Set up [!UICONTROL Wizard] functionality {#set-up-wizard-functionality}

The [!DNL Workfront Fusion template] [!UICONTROL Wizard] allows you to provide future users of your template with instructions or information related to the specific fields used in modules.

1. While creating a template, click a module added to the template to see the module's fields.
1. Locate the field where you want to add [!UICONTROL Wizard] information, and enable **[!UICONTROL Use in Wizard]** for that field.
1. Enter the information you want to make visible for users into the [!UICONTROL Help] field.
1. (Optional) To allow users to see this text when using the template, enable **[!UICONTROL Use as default value]**.
1. Repeat steps 2-4 for each field that you want to provide information for.
1. Click **[!UICONTROL OK]** to save changes and close the module.
