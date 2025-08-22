---
content-type: reference
title: 'Set up and managing organizations and teams: article index'
description: This section contains articles related to setting up and managing organizations and teams in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
---
# Delete users through the [!DNL Adobe Admin Console]

You can remove a user from Adobe Workfront Fusion only, leaving access to any other [!DNL Adobe] product profiles, or you can remove the user from the [!DNL Adobe Admin Console] entirely.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>Current: No Workfront Fusion license requirement.</p>
   <p>Or</p>
   <p>Legacy: Any </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] Workfront plan: Your organization must purchase Adobe Workfront Fusion.</li><li>[!UICONTROL Ultimate] Workfront plan: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Access level configurations*</td> 
   <td> 
     <p>You must be an [!DNL Adobe Admin Console] administrator for your organization.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Remove a user from Adobe Workfront Fusion only

You can remove a user from Workfront Fusion while leaving their other Adobe product permissions intact. 

For instructions, see "Remove users and user groups from a product" in the article [Manage products on Admin Console](https://helpx.adobe.com/enterprise/using/manage-products.html).

## Deactivate a user in all products in the [!DNL Adobe Admin Console]

To delete a user, you must deactivate the user through the [!DNL Adobe Admin Console].

A user is deactivated from the [!DNL Adobe Admin Console] when one of the following applies:

* The user is moved out from a product or product profile, and are not assigned to any other product or product profile.
* The user is removed from a group that is linked to a product profile, and is not included in any other group linked to a product profile.
* The user is removed from a product profile and is not assigned to another product profile.
* The user is deleted or deactivated in the organization that includes Workfront Fusion.

  For instructions, see the section "Remove users" in [Manage users individually](https://helpx.adobe.com/enterprise/using/manage-users-individually.html).

In Workfront Fusion, the deactivation affects the user in one of the following ways:

* If the user is in only one organization, the user is deactivated.
* If the user is in more than one organization, the user is removed from the organization that the user was modified in on the [!DNL Adobe Admin Console].
* Consider the following when deleting a user.

### Considerations when deleting a user in Workfront Fusion

Consider the following when deleting a user.

* When a user is deleted, the user's connections, keys, and webhooks are removed. 
* Any scenarios belonging to the user are transferred to the organization Owner. The connections in these scenarios must be updated, because the connections belonging to the user are no longer valid.
* If the deleted user owns any applications or public templates, the applications or public templates are transferred to the organization Owner. If there is not an organization Owner, the applications or public templates are transferred to another user.
