---
content-type: reference
title: Edit templates
description: This article describes how to edit Fusion templates. 
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
---

# Edit templates

Adobe Workfront Fusion templates are pre-built scenarios designed to automate and streamline various workflows. These templates can help you quickly set up integrations and automations without needing to build everything from scratch.

If you are an administrator, you have permission to view, modify, rename, publish, approve, and delete templates created by others.

## Access requirements 

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article: 

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] plan</td>
      <td><p>Any</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">[!DNL Adobe Workfront] license</td>
      <td><p>New: [!UICONTROL Standard]</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] license**</td>
      <td>
        <p>Current: No [!DNL Workfront Fusion] license requirement.</p>
        <p>Or</p>
        <p>Legacy: Any</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Product</td>
      <td>
        <p>New:</p>
        <ul>
          <li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] Plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li>
          <li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] is included.</li>
        </ul>
        <p>Or</p>
        <p>Current: Your organization must purchase [!DNL Adobe Workfront Fusion].</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md). -->

+++

## Edit [!DNL Workfront Fusion] templates as an administrator

1. Click **[!UICONTROL Administration]** in the left navigation panel to open the [!UICONTROL Administration] area.
1. Click **[!UICONTROL All Templates]** in the left navigation panel.
1. Click **[!UICONTROL Detail]** to the right of the template you want to edit. 
1. (Optional) Rename the template by clicking **Options** in the upper-right corner and selecting **Rename**.
1. (Optional) To change the language of your template, click **[!UICONTROL Create a new template]** ![](assets/fusion-scenario-settings-icon.png), and select the language from the Language drop-down.

   >[!IMPORTANT]
   >
   >The Languages selection corresponds to the languages available in the system settings and concerns only the name of the public template and its description. You can't change a template language once the template has been saved.

1. (Optional) To edit the template description, click **[!UICONTROL Set up a template]** ![](assets/fusion-scenario-settings-icon.png), and enter the description.
1. Add or edit apps, modules, and tools in the same way as you would do when creating a standard scenario.

   To add contextual help to the modules, see [Set up [!UICONTROL Wizard] functionality](#set-up-wizard-functionality) in this article.

   <!--For more information on building a scenario, see [Create a scenario in [!DNL Adobe Workfront Fusion]](../../../workfront-fusion/scenarios/create-a-scenario.md).-->

   >[!NOTE]
   >
   >If your template includes modules that require adding the connection, credentials, or other privacy-sensitive information, this information is not shared with the template users.

1. (Optional) Click **[!UICONTROL Run once]** to test the template.
1. Click the **[!UICONTROL Save]** icon ![](assets/save-icon.png).


## Set up [!UICONTROL Wizard] functionality

The [!DNL Workfront Fusion template] [!UICONTROL Wizard] allows you to provide future users of your template with instructions or information related to the specific fields used in modules.

1. Click the module added to the template to see the module's fields.
1. Locate the field where you want to add [!UICONTROL Wizard] information, and enable **[!UICONTROL Use in Wizard]** below that field.
1. Enter the information you want to make visible for users into the [!UICONTROL Help] field.
1. (Optional) To allow users to see this text when using the template, enable **[!UICONTROL Use as default value]**.
1. Repeat steps 2-4 for each field that you want to provide information for.
1. Click **[!UICONTROL OK]** to save changes and close the module.

The publishing process is the same as in the case of a standard user. For information, see [Publish and share templates](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md) section for more details.

## Template statuses

You can check the status on the template page under the template name.

The following statuses are available:

* **[!UICONTROL Private]**: This template is visible only for the template author and their team.
* **[!UICONTROL Published]**: This template is visible only for the template author and their team. Once published, you can send the template for approval if desired. You can also copy a shareable link.
* **[!UICONTROL Approved]**: This template is visible for all Workfront Fusion users in the [!UICONTROL Public templates] tab. You can also copy a shareable link by clicking [!UICONTROL Options] in the upper-right corner of the screen.

You can also check the status from the [!UICONTROL Team templates] tab. If a template is published, it will have an icon to the right of the template name.

* **Eye icon**: The template is published; it is visible for the team.
* **Yellow checkmark icon**: The template is published; it is visible only for the team; and it is pending approval to be added to the Public templates tab.
* **Green checkmark icon**: The template is available in the Public templates tab and is visible for any Workfront Fusion user. It is also still visible in the [!UICONTROL Team templates] tab. The template author or their team member can still edit it.

Templates without icons have [!UICONTROL Private] status. They are not published and are visible only to the team.

## Locate a template's SVG information

1. Click **[!UICONTROL Administration]** in the left navigation panel to open the [!UICONTROL Administration] area.
1. Click **[!UICONTROL Templates]** in the left navigation panel.
1. Click the template that you want to locate information for.
1. Click **Options** in the top-right corner.
1. Select *SVG Diagram*.

Here you can view the SVG diagram and the SVG code. 
