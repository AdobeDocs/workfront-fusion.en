---
title: Fusion organizations and teams overview
description: Adobe Workfront Fusion's Organization and Teams features make it possible for enterprises to control access to scenarios and other features within Fusion.
author: Becky
feature: Workfront Fusion
xl-id: 601e937f-0286-4557-9a87-59aa9c0c22f1
---
# [!DNL Adobe Workfront Fusion] organizations and teams overview

[!DNL Adobe Workfront Fusion]'s Organization and Teams features make it possible for enterprises to control access to scenarios and other features within Fusion.

An organization is the largest entity in Adobe Workfront Fusion. For example, your Fusion organization may represent the Fusion account for your entire company. 

Teams are smaller groups within the organization, and share Fusion resources such as scenarios, connections, and templates. 

<!--

## Access requirements

You must have the following access to use the functionality in this article:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] plan*</td> 
   <td> <p>[!DNL Pro] or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] license**</td> 
   <td>
   <p>Current license requirement: No [!DNL Workfront Fusion] license requirement.</p>
   <p>Or</p>
   <p>Legacy license requirement: [!UICONTROL [!DNL Workfront Fusion] for Work Automation and Integration],  [!UICONTROL [!DNL Workfront Fusion] for Work Automation]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Current product requirement: If you have the [!UICONTROL Select] or [!UICONTROL Prime] [!DNL Adobe Workfront] Plan, your organization must purchase [!DNL Adobe Workfront Fusion] as well as [!DNL Adobe Workfront] to use functionality described in this article. [!DNL Workfront Fusion] is included in the [!UICONTROL Ultimate] [!DNL Workfront] plan.</p>
   <p>Or</p>
   <p>Legacy product requirement: Your organization must purchase [!DNL Adobe Workfront Fusion] as well as [!DNL Adobe Workfront] to use functionality described in this article.</p>
   </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Access level configurations*</td> 
   <td> 
     <p>You must be a [!DNL Workfront Fusion] administrator for your organization.</p>
     <p>You must be a [!DNL Workfront Fusion] administrator for your team.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

To find out what plan, license type, or access you have, contact your [!DNL Workfront] administrator.

<p>**For information on [!DNL Adobe Workfront Fusion] licenses, see <a href="../../workfront-fusion/get-started/license-automation-vs-integration.md" class="MCXref xref">[!DNL Adobe Workfront Fusion] licenses</a></p>

-->

## Organizations

[!DNL Workfront Fusion] users belong to an organization. 

Users must be added to an organization before they are added to a team. <!--For instructions, see []().-->

### Organization roles

A user has one of the following roles in an organization:

* **[!UICONTROL Owner]**: The owner has all permissions available in the organization.
* **[!UICONTROL Admin]**: Admins can create and manage teams and users for the organization, and can approve templates.
* **[!UICONTROL Member]**: Members are able to use [!DNL Workfront Fusion] but are unable to make organizational changes.
* **[!UICONTROL Accountant]**: Accountants can see license information on the organization dashboard, but cannot perform any actions.
* **[!UICONTROL App Developer]**: Functionality for this role is currently unavailable, and will be made available in the near future. We do not recommend assigning users to this role at this time.

<!--For information on specific actions available to users in each organization role, see [Organization and team roles](/help/workfront-fusion/references/).-->

## Teams

Teams are groups of users that share access to specific resources. These resources may include:

* Scenarios
* Connections
* Webhooks
* Keys
* Data stores
* Data structures
* Email notification settings

>[!NOTE]
>
>Because teams share resources, it is sometimes useful for a team to have only one member. For example, users in training may create connections to their individual [!DNL Workfront] accounts. Any team members would also be able to connect to the individual [!DNL Workfront] account. In this case we recommend that the user be the only member of a training team.

Organizations may have as many teams as they need, and users may belong to one or more teams.

Users can select their team from the dropdown list in the left navigation panel. Users only see teams that they are members of. Selecting a team will allow a user to access that team's resources.

### Team roles

A user has one of the following roles in each of their teams:

* **[!UICONTROL Team Admin]**: Admins can add, remove, or change the role of a team member. They can also perform any action available to the other team roles.
* **[!UICONTROL Team Member]**: The team member role allows users to create and execute scenarios.
* **[!UICONTROL Team Monitoring]**: The [!UICONTROL monitoring] role allows users to access execution information for scenarios, but they are unable to design scenarios or change their "Active" status.
* **[!UICONTROL Team Operator]**: The [!UICONTROL operator] role allows users to see execution data and change the "Active" status of scenarios.
* **[!UICONTROL Team Restricted Member]**: Functionality for this role is currently unavailable, and will be made available in the near future. We do not recommend assigning users to this role at this time.

<!--For information on specific actions available to users in each team role, see [Organization and team roles](/help/quicksilver/workfront-fusion/organizations/organization-roles.md).-->

