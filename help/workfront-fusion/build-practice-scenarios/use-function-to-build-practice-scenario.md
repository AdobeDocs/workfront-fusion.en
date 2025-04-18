---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Use a function to update a project in a basic scenario
description: Learn how to add a function to update a work item in Workfront.
author: Becky
feature: Workfront Fusion
exl-id: aa082ac8-48e8-4569-880e-024dd77feaa1
---
# Use a function to update a project in a basic scenario

Updating a Workfront work item is a common use case for Workfront Fusion. In this example, you will use a function to change the name of a project to be in uppercase letters.

Fusion includes many types of functions that allow you to transform and perform conditional logic on your data. For more information on using functions, see [Function overview](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md).

This example modifies the scenario created in [Create a basic scenario](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

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

## Prerequisites

You must create the scenario described in [Create a basic scenario](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) before following this procedure.

## Use a function to update a project

### Add the Update Record module to your scenario

1. Open the scenario in the scenario editor.
1. Hover over the partial circle to the right of the of the second module, then click **[!UICONTROL Add another module]**. 
1. Select [!DNL Adobe Workfront] from the list of applications, then choose the module **[!UICONTROL Update Record]**.
1. In the ID field, select the ID block that is under the Convert object module. This is the ID of the project that was output by that module. 

   ![ID from Convert object](assets/id-convert-object.png)

1. In the Record Type field, select Project, because the object to be updated is a project.
1. In the Select Fields to Map area, select Name. 

    A Name field will open.
1. Continue to [Map the function for the name update](#map-the-function-for-the-name-update).

### Map the function for the name update

When this scenario converts a request to a project, the project's name is the same as the request. The function here takes that name and capitalizes all of the letters in it. 

1. Click the **Name** field. 

   The mapping panel opens.
1. In the mapping panel, click the **Text and binary functions** icon. ![Text functions icon](assets/toolbar-icon-text&binary-functions.png)
1. Select the function **upper**.

   The function appears in the Name field, including the formatting for the input it expects.

   The input for this example is the name of the issue the project was converted from.

1. Move your cursor between the parentheses, because this is where the input will go.
1. In the mapping panel, click the **Module output** icon. ![Module output icon](assets/toolbar-icon-functions-you-map-from-other-modules.png) 
1. Select the name block that was output by your first module.

   The name block appears in the function.

   ![Name block in function](assets/map-name.png)

1. Click **OK** to save the module settings.

### Test and activate

1. Test the scenario by clicking **Run once** in the lower-left corner of the screen.
1. Examine the output to ensure that the scenario ran as expected.
1. When you are satisfied that the scenario is working as expected, click the **Scheduling** toggle in the lower-left of the screen to **On**.

   This activates the scenario. Active scenarios run according to the schedule set in the trigger module.
1. In [!DNL Workfront Fusion], click **[!UICONTROL Save]** near the lower-left corner to save your progress on the scenario.

   >[!IMPORTANT]
   >
   >Save often as you hone and test a scenario.

## Resources

* [Map items using functions](/help//workfront-fusion/create-scenarios/map-data/map-using-functions.md)
