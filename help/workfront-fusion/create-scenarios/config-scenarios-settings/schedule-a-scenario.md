---
content-type: reference
title: Schedule a scenario
description: By default, a scenario runs every 15 minutes. You can change this by defining when and how often an activated scenario runs. Fusion scenarios can be scheduled to run as often as every 5 minutes.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
---
# Schedule a scenario

By default, a scenario runs every 15 minutes. You can change this by defining when and how often an activated scenario runs. Fusion scenarios can be scheduled to run as often as every 5 minutes.

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

## Schedule a scenario

1. Click the **Scenario** tab in the left panel. 
1. Select the scenario you want to schedule. 
1. In the upper-right corner of the Scenario detail page, click **[!UICONTROL Options]** > **[!UICONTROL Scheduling]**

   Or

   Click the **[!UICONTROL Scheduling]** icon (clock) on the scenario's trigger module.

1. Enter information into the following fields:

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Run scenario]</td> 
      <td> <p>Select the frequency at which you want to run the scenario, then select the interval.</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL At regular intervals]</strong> </p> <p>Enter the number of minutes between executions. The default value is 15 minutes.</p> </li> 
        <li> <p><strong>[!UICONTROL Once]</strong> </p> <p>Enter the date and time that you want the scenario to run. Use the format <code>MM/DD/YYYY h:mm A</code>. Example: <code>06/25/2019 11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Every day]</strong> </p> <p>Enter the time at which you want the scenario to run. Use the format <code>h:mm A</code>. Example: <code>11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Days of the week]</strong> </p> <p>Days: Select the days of the week that you want the scenario to run. You can select one or more days.</p> <p>Time: Enter the time that you want the scenario to run on the selected days. Use the format <code>h:mm A</code>. Example: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Days of the month]</strong> </p> <p>Days: Select the days of the month that you want the scenario to run. You can select one or more days.</p> <p>Time: Enter the time that you want the scenario to run on the selected days. Use the format <code>h:mm A</code>. Example: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Specified dates]</strong> </p> <p>Months: Select the months that you want to run the scenario. You can select one or more months.</p> <p>Days: Select the days of the month that you want the scenario to run. You can select one or more days.</p> <p>Time: Enter the time that you want the scenario to run on the selected days. Use the format <code>h:mm A</code>. Example: <code>11:00 PM</code></p> </li> 
       </ul> <p>Note: A date must exist for a scenario to run on that date. For example, a scenario scheduled for only the 31st of the month will not run in February, April, June, September, or November, because those months do not have a 31st day.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Advanced scheduling]</td> 
      <td>You can define specific time intervals during which your scenario is to run. You can specify time-of-day intervals, weekdays or months. For each interval, click <strong>[!UICONTROL Add]</strong> and fill in the fields as described in the [!UICONTROL Run scenario] field.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Start]</td> 
      <td>Enter the date and time after which you want the scenario to run. Use the format <code>MM/DD/YYYY h:mm A</code>. Example: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL End]</td> 
      <td>Enter the date and time before which you want the scenario to run. Use the format <code>MM/DD/YYYY h:mm A</code>. Example: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL OK]** to save the schedule settings and return to the scenario.
