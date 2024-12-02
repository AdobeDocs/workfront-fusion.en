---
title: Map items using functions
description: When you map items, you can use functions to create simple or complex formulas.
author: Becky
feature: Workfront Fusion
---
# Map an item using functions

When you map items, you can use functions to create simple or complex formulas. The functions available are similar to functions in Excel and in some programming languages:

* They evaluate general logic, math, text, dates, and arrays. 
* They let you perform conditional logic and transformations of item values, such as converting a text to uppercase, trimming text, converting a date into a different format, and more. 

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan</td> 
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

<!--For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md).-->

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Insert functions into fields

To insert a function into a field:

1. Click the **[!UICONTROL Scenario]** tab in the left panel.
1. Select the scenario where you want to map data.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Click the field where you want to insert a function.
1. Select the tab in the mapping panel that contains the function you want to insert. 

   For information on mapping panel tabs, see [Mapping overview](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md)
   1. Click the function name.

      Or

      Drag the function into the field.
1. Configure the function parameters. 

    For an explanation of function parameters, hover over the function in the mapping panel. 

    For more information on functions and their parameters, see the articles under [Function references: article index](/help/workfront-fusion/references/mapping-panel/functions/functions-toc.md).

1. Continue configuring the module, or click **OK**.

>[!TIP]
>
>When you create a complex formula that you want to reuse in another field, you can click the field that contains the combination, use Cmd-A or Ctrl-A to select it, then copy and paste it into the other field.


>[!BEGINSHADEBOX]

   **Example:** Some data types prevent users from entering more than a certain number of characters. You can use the substring function to limit a value to a certain number of characters.

   In this example, the substring function limits project name to 50 characters.

   ![](/help/workfront-fusion/references/apps-and-modules/assets/example-meet-length-restriction-350x184.png)

>[!ENDSHADEBOX]

## Nesting functions

You can nest functions within each other.

>[!BEGINSHADEBOX]

   **Example:** 

   In this example, the substring function limits the trimmed project name to 50 characters.

   ![](/help/workfront-fusion/references/apps-and-modules/assets/trimmed-name-under-50.png)

>[!ENDSHADEBOX]

To nest a function:

1. Click the field where you are creating a formula.

   This opens the mapping panel.

1. Click the first function that you want to add. This is the function on the outside. If the following example, this is the `substring` function.
1. In that function, click where you want the nested function to go. In this example, the nested function goes in the place of the first parameter.
1. In the mapping panel, click the nested function. In this example, this is the `trim` function.
1. Continue configuring the function as desired.
1. Continue configuring the module, or click **OK**.

## Use [!DNL Google Sheets] functions

If [!DNL Workfront Fusion] does not feature a function you want to use, but it is featured by [!DNL Google Sheets], you can use it by following these steps:

1. In [!DNL Google Sheets], create a new empty spreadsheet.
1. In [!DNL Workfront Fusion], open your scenario.
1. Add the **[!DNL Google Sheets]** >**[!UICONTROL Update a cell]** module to the scenario.

1. Configure the module:

   1. Choose the newly created spreadsheet in the **[!UICONTROL Spreadsheet]** field.
   1. Insert your formula containing the [!DNL Google Sheets] function(s) into the **[!UICONTROL Value]** field.

      You can use the output of preceding modules as usual.

      ![](/help/workfront-fusion/references/apps-and-modules/assets/exploit-google-sheet-functions-350x218.png)

1. Insert the **[!UICONTROL Google Sheets] >[!UICONTROL Get a cell]** module to obtain the calculated result.
1. Configure the module, using the same Cell ID that you used in step 4.

   ![](/help/workfront-fusion/references/apps-and-modules/assets/exploit-google-sheet-functions-2-350x187.png)
