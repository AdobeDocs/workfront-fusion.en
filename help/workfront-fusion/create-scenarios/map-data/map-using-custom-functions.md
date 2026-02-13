---
title: Map data using custom functions
description: When you map items, you can use functions to create simple or complex formulas.
author: Becky
feature: Workfront Fusion
---
# Map data using custom functions

You can create custom functions in the Functions area of Fusion. You then add these functions to your scenarios in the form of an Adobe App Builder module.

Because custom functions work through Adobe App Builder, your organization must have an Adobe App Builder license to use them.

Custom functions, like most scenario elements, are owned by teams.

Workfront Fusion also includes built-in functions that allow you to create simple or complex formulas. These functions cover a wide variety of use cases, including functions for arrays, strings, numbers, and data from previous modules.

For information and instructions on built-in functions, see [Map an item using built-in functions](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

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
   <p><ul><li>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li><li>You must have an Adobe App Builder license to use custom functions.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Configure a custom function

Custom functions are configured in the Functions area of Workfront Fusion. After a function is configured, you can add it to a scenario using the Adobe App Builder connector.

### Initialize your runtime environment

Before you can create custom functions, you must initialize your runtime environment. This needs to be done only if your team does not have any custom functions.

>[!IMPORTANT]
>
>Initialization can be performed only be a user with access to Adobe App Builder, either a developer or a system administrator within the IMS organization.
>
>After initialization is complete, all users on the team where initialization was performed are able to create and use functions.

1. Click the **Functions** ![Functions icon](assets/functions-icon.png) tab in the left panel.

   If you have not yet configured your runtime, you see the message "Runtime environment not configured."
1. Click **Initialize runtime**.

   After some time, a Functions list appears, with two sample functions.

### Create a custom function

After your runtime environment is configured, you can begin creating custom functions.

>[!IMPORTANT]
>
>* Your custom function **must** be a JavaScript function.
>* Your custom function **must** return an object. 
>* After you create a custom function, you cannot: 
>
>   * Change its name
>   * View the default parameter values

1. Click the **Functions** ![Functions icon](assets/functions-icon.png) tab in the left panel.
1. Click **Add function**.
1. Enter a name for the custom function. 

   You will not be able to change this name later.
1. Enter the code for the function.
1. For each default parameter value you want to add, click **Add Parameter** and enter the parameter name and default value.

   You can override default parameters when adding the function to a scenario.
1. Click **Save**

## Add a custom function to a scenario

To add a custom function to a scenario, use the Adobe App Builder connector.

For instructions, see [Adobe App Builder module](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

