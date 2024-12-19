---
title: Use cURL to add an HTTP module
description: You can paste a cURL request into your scenario, and Fusion creates an HTTP module configured from the cURL request.
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
---
# Use cURL to add an HTTP module

You can paste a cURL request into your scenario, and Fusion creates an HTTP module configured from the cURL request.

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

## Create an HTTP module from a cURL request


To create an HTTP module using cURL:

1. Create the text of the cURL request outside of Fusion, such as in a text editor.
1. Copy the cURL request to your clipboard.
1. Click the **[!UICONTROL Scenario]** tab in the left panel.
1. Select the scenario where you want to create the module.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Right click on any white space in the scenario editor and select **Paste**.

   Or

   Press Ctrl + V (Windows) or Cmd + V (Mac).
   

   An HTML module is created.
1. Drag the module to connect it to your scenario.

## Troubleshooting

If your cURL is not pasting into your scenario, check your browser settings to ensure that pasting from the clipboard is enabled.
