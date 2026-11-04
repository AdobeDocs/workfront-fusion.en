---
title: View and manage time zones
description: Learn how to view and manage time zone settings in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9910d9b4-5a7a-4f4a-9e66-8600d3b6c785
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
---
# View and manage time zones

Adobe Workfront Fusion includes controls for time zones on the organization and on the user level.

* Organization time zones: Scenarios use organization time zones to determine when a scheduled event occurs. 

* User time zones: User time zones determine the time that displays to a user. 

>[!BEGINSHADEBOX]

Example:

An organization is based in New York City, and the organization time is set to UTC-5 (America/New York). Scenario A is owned by this organization, and is scheduled to run at 9:00 AM every day. The scenario runs at 9:00 AM in the New York time zone.

A user in this organization lives in Los Angeles, and has their user time zone set to UTC-8 (America/Los Angeles). When this user views the scenario execution history for Scenario A, they see that the scenario ran at 6:00 AM. Even though the scenario ran according to the time in New York, the user sees the time as converted into their own time zone.

>[!ENDSHADEBOX]



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
  <tr> 
   <td role="rowheader">Access level</td> 
   <td> You must be an owner or an administrator for an organization to edit the time zone for that organization. </td>
   </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## View and manage your user time zone

1. In Fusion, click your Adobe Profile icon at the extreme upper-right of the screen.
1. In the menu that opens, select **Fusion Profile**.
1. Select the **Time Zone Options** tab. Tabs are located directly under your name.
   The Time Zone Options list opens.
1. In the Web area of the Time Zone Options list, locate your name.

   Your current user time zone setting is displayed to the right of your name.
1. To edit the time zone, click Edit ![Edit time zone](assets/edit-timezone-icon.png) next to the time zone.
1. In the Change details window, in the **Timezone** field, select the timezone that you want to set for yourself.
1. Click **Save**.


## View and manage your organization's time zone

>[!NOTE]
>
>You must be an owner or an administrator for an organization to edit the time zone for that organization.

1. In Fusion, click your Adobe Profile icon at the extreme upper-right of the screen.
1. In the menu that opens, select **Fusion Profile**.
1. Select the **Time Zone Options** tab. Tabs are located directly under your name.
   The Time Zone Options list opens.
1. In the Scenarios area of the Time Zone Options list, locate the organization that you want to view or manage the time zone for.

   The organization's current time zone setting is displayed to the right of the organization name.
1. To edit the time zone, click Edit ![Edit time zone](assets/edit-timezone-icon.png) next to the time zone.
1. In the Change details window, in the **Timezone** field, select the timezone that you want to set for your organization.
1. Click **Save**.


