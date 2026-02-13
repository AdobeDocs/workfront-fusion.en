---
title: Iterator module
description: An Iterator module is a special type of module that converts an array into a series of bundles. Each array item is outputted as a separate bundle.
author: Becky
feature: Workfront Fusion
exl-id: 43d39955-3dd7-453d-8eb0-3253a768e114
---
# [!UICONTROL Iterator] module

An [!UICONTROL Iterator] is a type of module that converts an array into a series of bundles. Each array item is outputted as a separate bundle.

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

## [!UICONTROL Iterator] module configuration

The general Iterator module has a single field, The [!UICONTROL Array] field. This field contains the array to be converted or split into separate bundles.

![Set up iterator](assets/set-up-iterator.jpg)

Other connectors may include iterator modules specific to that iterator. These contain a Source module field, which allows you to select that module that outputs the array that you want to iterate.

![Specialized iterators](assets/specialized-iterators.jpg)

For more information, see [Configure a module](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

>[!BEGINSHADEBOX]

**Examples:** 

* The below scenario shows how to retrieve emails with attachments and save the attachments as single files in a selected [!DNL Dropbox] folder.

   Emails can contain an array of attachments. The [!UICONTROL Iterator] module after the first module enables the scenario to handle each attachment separately. The [!UICONTROL Iterator] module splits the array of attachments into single bundles. Each bundle, with one attachment, is then saved one at a time in a selected [!DNL Dropbox] folder. The [!UICONTROL Array] field in the Iterator module should contain the `Attachments` array.

   ![Attachments array](assets/attachments-array.jpg)

>[!ENDSHADEBOX]


## Troubleshooting

### Problem: Mapping panel does not display mappable items under [!UICONTROL Iterator] module

When an [!UICONTROL Iterator] module does not have information about the structure of the array's items, the mapping panel in the modules following the [!UICONTROL Iterator] module displays only two items under the [!UICONTROL Iterator] module: `Total number of bundles` and `Bundle order position`.

![Mapping panel doesn't display](assets/mapping-panel-doesnt-display.png)

This is because each module is responsible for providing information about items it outputs, so that these items can be properly displayed in the mapping panel in the subsequent modules. However, several modules might be unable to provide this information in some cases. For example, [!UICONTROL JSON] > [!UICONTROL Parse JSON] or [!UICONTROL Webhooks] > [!UICONTROL Custom Webhook] modules with missing Data structure would not provide the information.

#### Solution

The solution is to manually execute the scenario. This forces the module to create output. Fusion can then apply the format of this output to later modules in the scenario. 

For example, a scenario includes a [!UICONTROL JSON] > [!UICONTROL Parse JSON] module without a Data structure.

![Parse JSON](assets/json-parse-json.png)

An [!UICONTROL Iterator] module connected to this JSON module cannot map the output of the module to the Array field in the setup panel of the [!UICONTROL Iterator] module.

![Connect iterator module](assets/connect-iterator-module.png)

To resolve this: 

Manually start the scenario in the scenario editor. 

>[!NOTE]
>
>To prevent the entire scenario from running, you can:
>
>* Unlink the modules after the [!UICONTROL JSON] > [!UICONTROL Parse JSON] module to prevent the flow from proceeding further. 
>   Or 
>* Right-click the [!UICONTROL JSON] > [!UICONTROL Parse JSON] module and choose **[!UICONTROL Run this module only]** from the context menu to execute only the [!UICONTROL JSON] > [!UICONTROL Parse JSON] module.

After the [!UICONTROL JSON] > [!UICONTROL Parse JSON] executes, it can then provide information about its outputs to all the subsequent modules, including the Iterator module. The mapping panel in the Iterator's setup then displays the items:

![Mapping panel displays items](assets/mapping-panel-displays-items.png)

in addition, the mapping panel in the modules that are connected after the [!UICONTROL Iterator] module display the items contained in the array:

![Items contained in array](assets/items-contained-in-array.png)
