---
title: View and manage team roles
description: Each team has a Roles tab where you can view the team's roles, create your own roles, choose the permissions that each role includes, and update or delete roles.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
---
# View and manage team roles

Each team in Adobe Workfront Fusion has a **[!UICONTROL Roles]** tab. On this tab, you can view the roles available in the team, create your own roles, and choose exactly which permissions each role includes. You can also update and delete roles. You are no longer limited to a fixed set of roles.

With custom roles, you can:

* Give each person only the access that their job needs, which reduces the risk of accidental changes to critical scenarios.
* Set up access to match how your organization works, instead of fitting your teams into the predefined roles.
* Manage access yourself, without contacting support.

For an overview of organizations, teams, and the predefined team roles, see [Organization and team overview](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/org-and-team-overview.md). For the permissions included in the predefined roles, see [Organization and team roles](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

<!-- BECKY CHECK ME: The source material (the Slack announcement) says flexible permissions are live in QA and for internal customers, with a limited pilot with paid customers next, then general availability. Confirm availability at the 2026-11-12 release, and whether this article should say that custom roles are available only to some organizations. -->

## Access requirements

<!-- BECKY CHECK ME: This table is copied from other Fusion articles. The source says that anyone with the Manage members permission can create, update, delete, and assign users to roles. Confirm the access level configurations. -->

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
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Access level configurations</td> 
   <td> 
     <p>You must have the <b>[!UICONTROL Manage members]</b> permission in the team. In the predefined roles, this permission is included in the Team Admin and Organization Owner roles.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Who can manage team roles

Anyone with the **[!UICONTROL Manage members]** permission in a team can create, update, delete, and assign users to roles in that team.

* Organization Owners can create and manage roles in all teams.
* Organization Admins can manage roles only in the teams that they are members of and where they have the **[!UICONTROL Manage members]** permission.
* Team Admins can manage roles in their teams.

<!-- BECKY CHECK ME: Confirm that Team Admins can manage roles. The source says that the Manage members permission was given to the Team Admin and Org Owner roles in the legacy system, and that team admins and org admins can create roles only in the teams where they are admins. -->

## View the roles in a team

1. Open the team.

   <!-- BECKY CHECK ME: Confirm how users open a team (for example, select the team in the left navigation, or open it from the Teams list under Org overview). -->

1. Click the **[!UICONTROL Roles]** tab.

   The **[!UICONTROL Roles]** tab is next to the **[!UICONTROL Team]**, **[!UICONTROL Users]**, and **[!UICONTROL Notification options]** tabs. It lists the roles that are available in the team, including the predefined roles. For each role, the list shows the following:

   * **[!UICONTROL Name]**: The name of the role.
   * **[!UICONTROL Permissions]**: A summary of the permissions that the role includes. For example, a role might show "No permissions", the name of a set of permissions, such as "Member", or "Custom" and the number of permissions, such as "Custom · 19 permissions".
   * **[!UICONTROL Edit]** and **[!UICONTROL Delete]** buttons for the role.

1. (Optional) To find a role, enter text in the **[!UICONTROL Search]** field above the list, or in the search field in the **[!UICONTROL Name]** column.
1. (Optional) To sort the list by name, click the **[!UICONTROL Sort]** icon in the **[!UICONTROL Name]** column.
1. (Optional) To hide or display columns, click the **[!UICONTROL Columns]** icon near the upper-right corner of the list, then enable or disable columns.

<!-- BECKY CHECK ME: Confirm the label and function of the icons next to the Name column and above the list on the right (the sort icon and the columns icon). -->

## Create a role

1. Open the team's **[!UICONTROL Roles]** tab, as described in [View the roles in a team](#view-the-roles-in-a-team) in this article.
1. Click **[!UICONTROL Create role]**.

   The **[!UICONTROL Create role]** page opens.

1. Enter a name for the role in the **[!UICONTROL Role name]** field.
1. In the **[!UICONTROL Role template]** dropdown, select the template that you want to start from.

   The template sets the initial permissions for the role. The default template is **[!UICONTROL Viewer]**.

1. In the **[!UICONTROL Scoped permissions]** area, select the permissions that you want the role to include.

   Permissions are grouped by area, such as **[!UICONTROL Automations]**, **[!UICONTROL Connections]**, and **[!UICONTROL Team]**. For each area, you can do either of the following:

   * To set all of the permissions in an area at once, click **[!UICONTROL No access]**, **[!UICONTROL View only]**, or **[!UICONTROL Full access]** next to the name of the area.
   * To choose specific permissions, select or clear the checkbox for each permission.

   For a list of the permissions, see [Permissions that you can include in a role](#permissions-that-you-can-include-in-a-role) in this article.

1. Click **[!UICONTROL Save]**. To close the page without creating the role, click **[!UICONTROL Cancel]**.

<!-- BECKY CHECK ME: Confirm the options in the Role template dropdown and what each one selects. Confirm exactly what No access, View only, and Full access select in each area (in the screenshot, View only selects the view permissions). Confirm whether there is a Description field, and whether there are areas below Team on the page (the screenshots end at Team). -->

The role is available in the team. You can assign it to team members.

### Permissions that you can include in a role

<table style="table-layout:auto">
 <col>
 <col>
 <thead>
  <tr>
   <th>Area</th>
   <th>Permissions</th>
  </tr>
 </thead>
 <tbody>
 <tr>
   <td role="rowheader">[!UICONTROL Automations]</td>
   <td>View list, View details, View run history, Manage notifications, Reset statistics, Run once, Edit schedule, Activate, Deactivate, Create, Edit, Publish, Delete</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Incomplete executions]</td>
   <td>View, Manage</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Webhooks]</td>
   <td>View, View queue, Create, Edit, Manage queue, Change priority, Delete</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Connections]</td>
   <td>View, Create, Edit, Delete</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Keys]</td>
   <td>View, Create, Edit, Delete</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Data stores]</td>
   <td>View list, Browse records, Create, Edit, Delete</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Data structures]</td>
   <td>View, Create, Edit, Delete</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Templates]</td>
   <td>View list, View details, Create, Edit, Delete</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Team]</td>
   <td>View team, Edit team settings, Manage members, Delete team</td>
  </tr>
 </tbody>
</table>

<!-- BECKY CHECK ME: Confirm that this list is complete, and add a description of what each permission allows, if needed. The list is taken from the Create role page, which may have more areas below Team. -->

## Update a role

1. Open the team's **[!UICONTROL Roles]** tab.
1. Click **[!UICONTROL Edit]** in the row of the role that you want to update.

   The page for editing the role opens. It has the same fields as the **[!UICONTROL Create role]** page.

1. Change the name or the permissions of the role. For information about the fields, see [Create a role](#create-a-role) in this article.
1. Click **[!UICONTROL Save]**.

<!-- BECKY CHECK ME: The Edit button is confirmed by the screenshot, and it is available for the predefined roles as well as custom roles. Confirm the title of the edit page, whether you can rename the predefined roles, and what happens to users who already have the role. -->

## Delete a role

1. Open the team's **[!UICONTROL Roles]** tab.
1. Click **[!UICONTROL Delete]** in the row of the role that you want to delete.

<!-- BECKY CHECK ME: Confirm why the Delete button is unavailable (dimmed) for some roles, such as Team Operator, Team Member, and Team Admin in the screenshot, whether there is a confirmation prompt, and what happens to users who have the role. Update this procedure and add a note, if needed. -->

## Clone roles to another team

You can copy the roles in one team to another team, so that you do not have to re-create the same roles in each team.

1. Open the team's **[!UICONTROL Roles]** tab, as described in [View the roles in a team](#view-the-roles-in-a-team) in this article.
1. Click **[!UICONTROL Clone to team]**.

   The **[!UICONTROL Clone roles to another team]** page opens.

1. In the **[!UICONTROL Target team]** dropdown, select the team that you want to clone the roles to.

   A table appears that lists the roles in the current team.

1. For each role in the table, review and set the following:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Source role]</td> 
      <td> <p>The role in the current team, with a summary of its permissions.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Action]</td> 
      <td> <p>What to do with the role. For example, <b>[!UICONTROL Copy into existing role]</b> copies the permissions of the source role into a role that already exists in the target team.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Target]</td> 
      <td> <p>The role in the target team that the source role is copied into.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Changes]</td> 
      <td> <p>Whether the target role differs from the source role. For example, <b>[!UICONTROL Already in sync]</b> means that the target role already has the same permissions as the source role.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Users]</td> 
      <td> <p>Information about users who have the role. For example, <b>[!UICONTROL No matching users]</b> means that there are no users to include.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Status]</td> 
      <td> <p>The result for the role after you clone.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL Clone]**. To close the page without cloning, click **[!UICONTROL Cancel]**.

<!-- BECKY CHECK ME: The screenshot shows the Clone roles to another team page after a target team is selected. Confirm the options in the Action dropdown (for example, whether you can create a new role in the target team), the options in the Target dropdown, what the checkbox in the Users column does (for example, whether it also assigns the role to matching users in the target team) and what "matching users" means, what the Changes column shows when the roles differ, and what the Status column shows before and after you clone. -->

<!-- BECKY CHECK ME: Confirm whether the Target team dropdown lists all teams or only the teams that you can manage, and whether the Clone to team button is visible to everyone who can manage roles. -->

## Assign a role to a user

You assign a custom role the same way that you assign a predefined role. For instructions, see [Add a user to a team](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md) and [View or edit user roles](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md#view-or-edit-user-roles-for-a-team).

<!-- BECKY CHECK ME: Confirm that custom roles appear in the role dropdowns in both of these procedures. -->

## Considerations

* Organization permissions cascade. To give someone access to perform an action in all teams, assign an organization role instead of creating a team role. For more information, see [Organization and team roles](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).
* Roles that you create belong to one team.

<!-- BECKY CHECK ME: The Slack thread says that defining a role that is available in all teams was out of scope for the initial release. Confirm that a role belongs to a single team, and that you clone it to use it in another team. -->
