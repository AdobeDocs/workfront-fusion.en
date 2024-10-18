---
title: Delete a user in Workfront Fusion
description: Manage [!DNL Adobe Workfront Fusion] users in your organization
author: Becky
feature: Workfront Fusion
---
# Delete a user in Workfront Fusion

Adobe Workfront Fusion administrators can delete users inside Workfront Fusion.

>[!IMPORTANT]
>
>The procedure described on this page applies only to organizations that have not yet been onboarded to the Admin Console. If your organization has been onboarded to the Adobe Admin Console, you must perform this action through the Adobe Admin Console.
>
>For instructions on deleting a user in the Adobe Admin Console:
>
>* See [Delete users through the [!DNL Adobe Admin Console]](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/delete-users-admin-console.md).
>* Contact your Adobe Admin Console Administrator.
>
<!--
>For a list of procedures that differ based on whether your organization has been onboarded to the Adobe Admin Console, see [Platform-based administration differences (Adobe Workfront Fusion/Adobe Business Platform)](../../workfront-fusion/fusion-in-admin-console/fusion-adobe-admin-console.md).-->


>[!NOTE]
>
>If your organization is currently in the process of moving to the Adobe Admin Console, you cannot manage users in Workfront (adding or deleting users.) You can perform these actions in the Adobe Admin Console after your migration is complete.

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
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] Plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] is included.</li></ul>
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

<!--<!--For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md).-->-->

<!--<!--For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->-->

+++

## Delete a user 

[!DNL Adobe Workfront Fusion] administrators can delete users.

1. While logged in as a [!DNL Workfront Fusion] administrator, select **[!UICONTROL All users]** in the left navigation.
1. Click **[!UICONTROL Details]** in the row of the user that you want to view.
1. (Optional) To update the user's details, click **[!UICONTROL Options]** in the upper-right corner of the screen, then select **[!UICONTROL Delete]**.

### Considerations when deleting a user in Workfront Fusion

Consider the following when deleting a user.

* When a user is deleted, the user's connections, keys, and webhooks are removed. 
* Any scenarios belonging to the user are transferred to the organization Owner. The connections in these scenarios must be updated, because the connections belonging to the user are no longer valid.
* If the deleted user owns any applications or public templates, the applications or public templates are transferred to the organization Owner. If there is not an organization Owner, the applications or public templates are transferred to another user.
