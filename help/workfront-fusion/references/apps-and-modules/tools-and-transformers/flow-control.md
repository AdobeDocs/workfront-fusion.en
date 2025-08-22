---
title: Flow control
description: When you are creating or editing a scenario, you can configure settings to control the way data flows through it.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
---
# Flow control

When you are creating or editing a scenario, you can configure settings to control the way data flows through it.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current:  Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>No Workfront Fusion license requirement</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>Select or Prime Workfront package: Your organization must purchase Adobe Workfront Fusion.</li><li>Ultimate Workfront package: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Repeater

You can use a [!UICONTROL Repeater] module to repeat a task a given number of times. A [!UICONTROL Repeater] module generates bundles, one after another.


<table>
    <tr>
        <td>[!UICONTROL Initial value]</td>
        <td>Enter or map the value that you want the module to have in the first iteration. The default value is 1.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Repeats]</td>
        <td>Enter or map the number of times that you want the module to repeat. This number must be greater than or equal to 0, and less than or equal to 10,000.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Step]</td>
        <td>This is the number by which the module increases the value. The default value is 1.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

For example, you could use a [!UICONTROL Repeater] module to send five emails with the subjects "Hello 1," "Hello 2," and so on, by connecting the **[!UICONTROL Email] >[!UICONTROL Send me an email]** module to the [!UICONTROL Repeater] module.

1. Click the [!UICONTROL Flow Control] icon ![Flow control icon](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif) at the bottom of the screen, then click **[!UICONTROL Repeater]** in the menu that displays.
1. Click the [!UICONTROL Repeater] module, then click **[!UICONTROL Connect automatically]** in the box that displays.

   The Repeater module opens.

1. In the the **[!UICONTROL Repeats]** field, enter the number of repetitions (outputted bundles) you want the module to product.

   In this example, you would enter 5.

   ![Repeater](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   The value of the item increases in each repetition by this value specified in the **[!UICONTROL Step]** field, which you can view by selecting **[!UICONTROL Show advanced settings]**. This number is 1 by default.

1. Click **[!UICONTROL OK]** to close the **[!UICONTROL Flow Control]** box.

1. Click the app or service module connected to the [!UICONTROL Repeater] module.
1. In the box that appears, type the information that you want to repeat.

   In our email example, you would type Hello in the [!UICONTROL Subject] box, then map `i` from the repeater module.

   ![Repeater](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>The number of repeats is not determined by the value of `i`, as it would be in a loop in programming. The module will repeat the number of times indicated in the [!UICONTROL Repeats] field. The value `i` changes with each iteration of the [!DNL repeater] module, and can be mapped to later modules. The example above maps the value of `i` into the Hello message, resulting in messages that read "Hello 1," Hello 2," and so on.

>[!ENDSHADEBOX]

## [!UICONTROL Iterator]

An [!UICONTROL Iterator] is a special type of module that converts an array into a series of bundles. Each array item will be a separate bundle in the [!UICONTROL Iterator] module output. For more information, see [Iterator module](/help/workfront-fusion/references/modules/iterator-module.md).

## Array aggregator

An array aggregator is a special type of module which allows to merge several bundles into one single bundle. For more information, see [Aggregator module](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

The [!UICONTROL Router] module allows you to branch your flow into several routes and process the data within each route differently. Once a [!UICONTROL Router] module receives a bundle, it forwards it to each connected route in the order the routes were attached to the [!UICONTROL Router] module. For more information, see [Router module in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Directives

The error handling directives allow you to control how your scenario reacts to errors. 

For information on error handling directives, see [Directives for error handling](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

