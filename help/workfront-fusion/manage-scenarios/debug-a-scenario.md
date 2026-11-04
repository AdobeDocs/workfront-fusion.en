---
title: Debug a scenario
description: The Adobe Workfront Fusion Devtool allows you to understand and troubleshoot scenarios. The Devtool adds an extra panel to the Chrome Developer Tools. Using this debugger panel, you can check all the manual runs of your scenario, review all the performed operations, and see the details of every API call performed. You can see which module, operation, or single response caused the error, and use that knowledge to refine your scenario.
author: Becky
feature: Workfront Fusion
exl-id: 34215370-27e3-4c28-8bd1-a16268900b86
TQID: 'https://experienceleague.adobe.com/7NXYVXxbQvgKnqvRUNV-ySBApe9kl-Kn57sSKCh4NLE'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
---
# Debug a scenario

The Adobe Workfront Fusion Devtool helps you to understand and troubleshoot scenarios. Using the Devtool, you can check all the manual runs of your scenario, review all the performed operations, and see the details of every API call performed. You can see which module, operation, or single response caused the error, and use that knowledge to refine your scenario.

>[!NOTE]
>
>Logging in the debugger panel will be limited or unavailable for confidential scenarios, automatic executions, and successful operations.

>[!NOTE]
>
>In the new experience, several DevTool tools are built into the scenario editor, so you can use them without opening the DevTool:
>
>| Tool | Where to find it in the new experience |
>| ---------- | ---------- |
>| Get app metadata | Right-click a module and select **App metadata**. |
>| Copy mapping | Right-click the source module, select **Copy mapping**, then paste it on a compatible module. |
>| Copy filter | Right-click the filtered link, select **Copy filter**, then paste it on another link. |
>| Copy module name | Right-click a module and select **Copy module name** or **Paste module name**. |
>| Swap connection | Open Find and replace, then use the **Connection** tab. |
>| Swap variable | Open Find and replace, then use the **Variable** tab. |
>| Remap source | Open Find and replace, then use the **Source** tab. |
>
>These tools are also still available on the **Tools** tab of the DevTool, along with Focus a module, Find modules by mapping, and Base 64. You can also use the `base64()` and binary-conversion functions in mappings.
>
>You can also view request and response details directly from [Live Trail](/help/workfront-fusion/manage-scenarios/live-trail.md) and execution history in the scenario editor. For more information about Find and replace, see [Find and replace variables, sources, and connections in a scenario](/help/workfront-fusion/manage-scenarios/find-and-replace.md).
<!-- BECKY CHECK ME: DevTool screenshots (10/27/26) show all ten tools still on the Tools tab, so this note now says the seven built-in tools are available in both places. The release notes implied only Focus a module, Find modules by mapping, and Base 64 would remain. Confirm after release whether the other seven are removed from the DevTool, and update this note and the Tools section if so.  -->
<!-- BECKY CHECK ME: note added from the 10/23/26 release notes; the DevTool is NOT being removed. This article still needs a fuller restructure (new/classic split for the seven tools, Live Trail section or separate article). Confirm the menu labels. -->

For a video introduction and walkthrough of the Fusion Devtool, see 

* [Fusion Development Tool](https://video.tv.adobe.com/v/3427031/){target=_blank}
* [Devtool walkthrough](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/fusion/troubleshooting-and-error-handling/dev-tool-walkthrough.html?lang=en)

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

## Access the Devtool

If you use Fusion in the Adobe Unified Shell, or have updated to the new Fusion experience, you can access the Devtool from the Scenario editor.

### Access the Devtool in the new experience

1. Go to the Scenario editor for the scenario you want to debug.

   To locate the Scenario editor, see [The scenario editor](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Click the three-dot icon in the Controls area, then select **DevTool**.

Or:

1. Go to the Scenario editor for the scenario you want to debug.
1. Right-click in an empty area of the page (not on a module).
1. Select **Open Devtool**.

The DevTool opens in a panel below the canvas.

<!-- BECKY CHECK ME: new-experience access steps from your 10/27/26 notes (three-dot menu in Controls, or right-click). Confirm the menu label ('DevTool') and the 'panel below the canvas' description, and add a screenshot. I assumed the Helper tools icon steps below apply to the classic experience only; confirm. -->

### Access the Devtool in the classic experience

1. Click the **Helper tools** ![Helper tools](assets/debugger-icon.png) icon near the bottom of the screen.

Or: 

1. Go to the Scenario editor for the scenario you want to debug. 
  
   To locate the Scenario editor, see [The scenario editor](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Right click in an empty area of the page (not on a module).
1. Select **Open Devtool**.

## Use the Workfront Fusion Devtool

Workfront Fusion Devtool is divided into 3 main sections, plus a help link. You can find these in the left panel of your Devtool window.

* [Live Stream](#live-stream) 
* [Scenario Debugger](#scenario-debugger) 
* [Tools](#tools)
* **DevTool help**: Click the question mark icon to open the article about the DevTool.

<!-- BECKY CHECK ME: the DevTool left panel now has a fourth item, 'DevTool help' (question mark icon), per your 10/27/26 screenshots. Confirm the label, that it opens this article or another one, and whether to apply this to the classic experience too. Retake the left-panel screenshot. -->

### Live Stream 

Live Stream displays what is happening in the background when you click Run once in your scenario.

<!-- BECKY CHECK ME: HOLD: in the new experience, Live Stream shows a 'no events available' message even while a scenario is running, which may be a bug. No updates have been made to this section. Re-test after release before changing anything here. If it is intended behavior, this section may need to point to Live Trail instead. -->

1. Click the **[!UICONTROL Live Stream]** icon ![Live stream icon](assets/live-stream-icon.png) to open the Live Stream section.
1. Do any of the following:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Action</th> 
      <th>Instructions</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td role="rowheader">View request information</td> 
      <td> <p>You can view the following information for each module in your scenario</p> 
       <ul> 
        <li> <p>Request Headers (API endpoint URL, http method, time and date the request was called, request headers, and query string)</p> </li> 
        <li> <p>Request Body</p> </li> 
        <li> <p>Response Headers</p> </li> 
        <li> <p>Response Body</p> </li> 
       </ul> <p>To view this information, click the appropriate tab in the right panel of the Workfront Fusion Devtool.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Search events by content</p> </td> 
      <td> <p>Enter the search term into the search field in the left panel of the Workfront Fusion Devtool to display only requests that contain the search term.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Clear list of requests </p> </td> 
      <td> <p>Click the trash bin icon in the top-right corner of the Devtool's left panel to clear the list of requests recorded by the Workfront Fusion Devtool. </p> </td> 
     </tr> 
     <!--
     <tr>
      <td role="rowheader"> <p>Enable Console Logging</p> </td> 
      <td> <p>Click the computer icon <img src="assets/console-computer-icon.png"> in the top-right corner of the Devtool's left panel.</p> <p>Logging in the console is enabled when the computer icon is green.</p> </td> 
     </tr>
     -->
     <tr> 
      <td role="rowheader"> <p>Retrieve the Request in the Raw JSON Format or cURL</p> </td> 
      <td> 
       <ul> 
        <li> <p><strong>Raw JSON</strong> </p> <p>Click <strong>[!UICONTROL Copy RAW]</strong> in the upper-right corner of the Devtool's right pane.</p> </li> 
        <li> <p><strong>cURL</strong> </p> <p>Click <strong>[!UICONTROL Copy cURL]</strong> in the upper-right corner of the Devtool's right pane.</p> </li> 
       </ul> </td> 
     </tr> 
    </tbody> 
   </table>

### Scenario Debugger 

>[!NOTE]
>
>To quickly go to the debugger from a scenario that has errored out, you can click **Get details** in the error message in the module output.
>
>![Get details in module output](assets/go-to-debugger.png)

The Scenario Debugger is useful for more complex scenarios. It displays the history of the scenario runs and enables you to search modules by their name or ID.

1. Click the **[!UICONTROL Scenario Debugger]** icon ![Debugger icon](assets/scenario-debugger-icon.png) to open the Scenario Debugger.

   The Scenario Debugger lists the modules in your scenario. Each module shows its name, the app and action, and a numbered badge with the module ID.

1. (Optional) Enter the search term (name or module ID) in the **Search modules by Name or ID** field.
1. Click the module name.

   The cycles of the module's most recent run are listed next to the module list. If the module has no run data, the Scenario Debugger displays **No Result found**.

1. Expand a cycle, then click an operation.

   Each operation shows whether it succeeded and how long it took, for example **Operation 1** with a duration of 0 ms.

1. Review the details of the request. Use the tabs to view:

   * **Request Headers**: The API endpoint URL, the HTTP method, when the request was called, and the request headers.
   * **Request Body**
   * **Response Headers**
   * **Response Body**

1. (Optional) To copy the request, click **Copy RAW** or **Copy cURL**.

<!-- BECKY CHECK ME: Scenario Debugger steps expanded from your 10/27/26 new-experience DevTool screenshots. Confirm: (1) the 'Search modules by Name or ID' label; (2) that the module list sub-labels, badge (module ID), cycle/operation layout, and 'No Result found' state are described correctly; (3) the tab names, since Response Body was partly hidden behind the Copy buttons in the screenshot; (4) whether Copy RAW and Copy cURL copy the request only or the request and response; (5) whether the classic experience's Scenario Debugger looks the same, or this needs a new/classic split. The screenshot also shows a collapsed 'Live trail' tab with an event count on the right edge of the editor; see the Live Trail article. Retake the Scenario Debugger screenshots. -->

### Tools

The Workfront Fusion Devtool features tools that make setting up your scenario easier.

1. Click the **[!UICONTROL Tools]** icon ![Console tools icon](assets/console-tools-icon.png) to open the Tools. 
1. (Optional) To find a tool, enter its name in the **Search tool by name** field.
1. Select the tool you want to use
1. Configure the fields as detailed below.
1. Click **[!UICONTROL Run]**.

Until you select a tool, the right side of the panel prompts you to select one. A link at the bottom of the Tools tab takes you to the article about the DevTool.

<!-- BECKY CHECK ME: added from your 10/27/26 screenshots: the 'Search tool by name' field, the select-a-tool prompt, and the link to the DevTool article. Confirm the field label and link destination; retake the Tools screenshot. -->

Tools and their fields:

* [Focus a Module](#focus-a-module) 
* [Find Modules by Mapping](#find-modules-by-mapping) 
* [Get App Metadata](#get-app-metadata) 
* [Copy Mapping](#copy-mapping) 
* [Copy Filter](#copy-filter) 
* [Copy Module Name](#copy-module-name) 
* [Swap Connection](#swap-connection) 
* [Swap Variable](#swap-variable) 
* [Base 64](#base-64) 
* [Remap Source](#remap-source) 

#### [!UICONTROL Focus a Module]

Opens settings of the specified module by ID.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Module ID]</td>
        <td>Enter the ID of the module to open its settings.</td>
    </tr>
</table>

#### [!UICONTROL Find Modules by Mapping]

Allows you to search modules' values for a specified term. The output contains IDs of modules that contain the term you have searched for.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword]</td> 
   <td> <p> Enter the term you want to search for. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Use Only Values]</p> </td> 
   <td> <p>Enable this option to only search in module fields' values.</p> <p>Disable this option to also search in module fields' names.</p> <p>The search is performed through the name and label parameters.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get App Metadata]

Retrieves metadata of the app by the app's module name or ID. This is useful, for example, when you need to know the version of the app used in your scenario.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Select the module for which you want to retrieve metadata.</td>
    </tr>
</table>

#### [!UICONTROL Copy Mapping]

Copies values from the source module to the target module.

>[!CAUTION]
>
>Make sure you set the correct source and target modules. If you select a different type of module, values in the target module will be deleted.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> Select the module or enter the ID of the module from which you want to copy field values.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>Select the module or enter the ID of the module into which you want to insert the source module values.</p> <p>Important: Values in the target module will be overwritten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy Filter]

Copies the filter settings from the source module to the target module.

>[!NOTE]
>
>The copy action is performed on the filter placed on the left side of the selected module.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> Select the module or enter the ID of the module from which you want to copy filter values.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>Select the module or enter the ID of the module into which you want to insert the filter values from the source module.</p> <p>Important: Values in the target module will be overwritten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Preserve Fallback Route setting]</p> </td> 
   <td> <p>The source filter is set as the fallback route. Enable this option to also set the the target filter is set as the fallback route.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Copy Module Name]

Copies the name of the selected module to your clipboard.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Module] </td> 
   <td> <p>Select the module that you want to copy the name of.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Swap Connection]

Duplicates a connection from the source module to every module in the scenario of the same app.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Select the module or enter the ID of the module from which you want to duplicate the connection.</td>
    </tr>
</table>

#### [!UICONTROL Swap Variable]

Searches for specified variables in the scenario and replaces them with a new variable.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable to Find]</td> 
   <td> <p> Locate the variable pill that you want to replace from the variable module in your scenario and copy it to this ([!UICONTROL Variable to Find]) field. In the field, it appears with double curly brackets. Example: <code>&#123;&#123;5.value&#125;&#125;</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Replace With]</p> </td> 
   <td> <p>Locate the variable pill that you want to replace the variable with from the variables module in your scenario and copy it to this ([!UICONTROL Variable to Find]) field. In the field, it appears with double curly brackets. Example: <code>&#123;&#123;5.value&#125;&#125;</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Module]</p> </td> 
   <td> <p>Select the variables module in which you want to replace the variable. If no module is selected, the variable will be replaced in the entire scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Base 64]

Allows you to encode the entered data to Base64 or to decode Base64. Some requests are encoded to Base64. This tool can be useful when you want to search for particular data in the encoded request.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation] </td> 
   <td> <p>Select whether you want to encode the data from the [!UICONTROL Raw Data] field to Base64 or decode Base64 to Raw Data.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Raw Data]</p> </td> 
   <td> <p> Enter the data you want to encode to Base64, or Base64 if you want to decode to raw data, depending on the option selected in the [!UICONTROL Operation] field above.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remap Source]

Allows you to change the mapping source from one module to another.

You must first add the module you want to use as a source module to the route in your scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module] </td> 
   <td> <p> Select the module you want to be replaced as the mapping source for other modules in your scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>Select the module you want to use as a new mapping source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Module to Edit]</p> </td> 
   <td> <p>Select the module you want to change the mapping for if you don't want to change the mapping in the entire scenario. </p> </td> 
  </tr> 
 </tbody> 
</table>
