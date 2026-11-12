---
title: Adobe App Builder module
description: The Adobe App Builder connector allows you to use custom functions in your scenarios.
author: Becky
feature: Workfront Fusion
exl-id: 92661a0c-436b-4fbd-808a-a4fbe3cd2339
---
# Adobe App Builder module

You can create custom functions in the Functions area of Fusion. You then add these functions to your scenarios in the form of an Adobe App Builder module.

Because custom functions work through Adobe App Builder, your organization must have an Adobe App Builder license to use them.

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

## Create a connection to Adobe App Builder

The connection uses the Adobe I/O Runtime credentials of an App Builder project workspace. Before you create the connection, get these credentials from the Adobe Developer Console.

### Get your Runtime credentials

1. Sign in to the [Adobe Developer Console](https://developer.adobe.com/console) with the organization that has your App Builder license.
1. Open the App Builder project that contains your functions, then select the workspace you want to connect to (for example, **Production**).
1. Click **Download all** in the upper-right corner to download the workspace configuration JSON file.
1. Open the file and locate the `runtime` section. It contains:

   * `namespace`: the value to enter in the **Namespace** field
   * `auth`: a value in the format `username:password`. The part before the colon is the **Username**, and the part after the colon is the **Password**.

   >[!NOTE]
   >
   >You can also find the namespace and auth values by running `aio runtime namespace get` or `aio app use` in the Adobe I/O CLI.

### Create the connection

1. In the module, click **Add** next to the **Connection** field.
1. Fill in the following fields:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name]</td> 
      <td>Enter a name for this connection.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Environment]</td> 
      <td>Select whether you are connecting to a production or non-production environment.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Type]</td> 
      <td>Select <b>Service account</b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Username]</td> 
      <td>Enter the username from the <code>auth</code> value of your workspace (the part before the colon).</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Password]</td> 
      <td>Enter the password from the <code>auth</code> value of your workspace (the part after the colon).</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Namespace]</td> 
      <td>Enter the <code>namespace</code> value from the <code>runtime</code> section of your workspace configuration file.</td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Continue** to save the connection.

## Adobe App Builder modules

### Run a custom code block

This module allows you to run a code block. You configure the code block when you set up the module, and it is run when the module runs during a scenario execution.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Select the connection that contains the custom function that you want to run. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Code block]</td> 
   <td>Enter the block of code that you want the module to run.<p>To format the code for easier reading, click the <b>Format code</b> icon.</td> 
  </tr> 
   </tbody> 
</table>

### Run a custom function from package

This module runs a function from a package.

For information on packages, see [Use custom function packages](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Select the connection that contains the custom function that you want to run. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package]</td> 
   <td>Select the package that includes the function that you want to run in the scenario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable] </td> 
   <td>Select the function that you want to run in the scenario.</p></td> 
  </tr> 
   </tbody> 
</table>

### Use variable from package

This module brings a variable configured in a package into your scenario.

For information on packages, see [Use custom function packages](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Select the connection that contains the custom function that you want to run. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package]</td> 
   <td>Select the package that includes the variable that you want to bring into the scenario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable] </td> 
   <td>Select the variable that you want to bring into the scenario.</p></td> 
  </tr> 
   </tbody> 
</table>

### Run a custom function or code block

This module allows you to use a previously configured custom JavaScript function stored in the Functions area.

For instructions on configuring a custom function, see [Map data using custom functions](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Select the connection that contains the custom function that you want to run. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Select the custom function that you want to run.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parameters] </td> 
   <td>Enter the values for the function parameters. Available parameters are based on the parameters configured when the function was created.<p>If a parameter has a default value, you will not see it in the field, but can override it by entering or mapping a value into the field.</p></td> 
  </tr> 
   </tbody> 
</table>


