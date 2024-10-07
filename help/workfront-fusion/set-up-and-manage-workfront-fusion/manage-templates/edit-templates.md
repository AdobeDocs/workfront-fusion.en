---
content-type: reference
title: Edit templates
description: This article describes how to edit Fusion templates. 
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
---

# Approve or disapprove templates

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
1. Click **[!UICONTROL Templates]** in the left navigation panel.
1. Click **[!UICONTROL Detail]** to the right of the template you want to edit. For information about specific template options that you can edit, see <!--[Create new templates in [!DNL Adobe Workfront Fusion]](../../../workfront-fusion/scenarios/templates/create-new-fusion-templates.md).-->

    >[!NOTE]
    >
    >In the [!UICONTROL Options] in the top-right corner, there is one additional option - the SVG diagram that provides you with the SVG code. Also, the publishing process is the same as in the case of a standard user, refer to the Publishing and sharing templates section for more details.
1. Click the **[!UICONTROL Publish]** button in the upper-right corner of the screen.<!-- - if admin does this, does it need to be approved?-->


## Template statuses

You can check the status on the template page under the template name.

The following statuses are available:

* **[!UICONTROL Private]**: This template is visible only for the template author and their team.
* **[!UICONTROL Published]**: This template is visible only for the template author and their team. Once published, you can send the template for approval if desired. You can also copy a shareable link.
* **[!UICONTROL Approved]**: This template is visible for all Workfront Fusion users in the [!UICONTROL Public templates] tab. You can also copy a shareable link by clicking [!UICONTROL Options] in the upper-right corner of the screen.

You can also check the status from the [!UICONTROL Team templates] tab. If a template is published, it will have an icon to the right of the template name.

* **Eye icon**: The template is published; it is visible only for the team; and an approval request was not sent.
* **Yellow checkmark icon**: The template is published; it is visible only for the team; and it is pending approval to be added to the Public templates tab.
* **Green checkmark icon**: The template is available in the Public templates tab and is visible for any Workfront Fusion user. It is also still visible in the [!UICONTROL Team templates] tab. The template author or their team member can still edit it.

Templates without icons have [!UICONTROL Private] status. They are not published and are visible only to the team.
