---
content-type: reference
title: "Set up and managing organizations and teams: article index"
description: This section contains articles related to setting up and managing organizations and teams in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
---

# Delete users through the [!DNL Adobe Admin Console]

<!-- audited: 9/2024)-->

>[!IMPORTANT]
>
>The functionality in this article is available only if your organization's instance of [!DNL Adobe Workfront Fusion] has been onboarded to the [!DNL Adobe Business Platform].
>
><!--For a list of procedures that differ based on whether your organization has been onboarded to the [!DNL Adobe Business Platform], see [Platform-based administration differences ([!DNL Adobe Workfront Fusion]/[!DNL Adobe Business Platform])](../../workfront-fusion/fusion-in-admin-console/fusion-adobe-admin-console.md).-->

<!--Check this note - when all are moved to Adobe Admin Console, remove-->

You can remove a user from [!DNL Adobe Workfront Fusion] only, leaving access to any other [!DNL Adobe] product profiles, or you can remove the user from the [!DNL Adobe Admin Console] entirely.

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
     <p>You must be an [!DNL Adobe Admin Console] administrator for your organization.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<!--For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md).-->

<!--For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->

+++

## Remove a user from [!DNL Adobe Workfront Fusion] only

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

In [!DNL Workfront Fusion], the deactivation affects the user in one of the following ways:

* If the user is in only one organization, the user is deactivated.
* If the user is in more than one organization, the user is removed from the organization that the user was modified in on the [!DNL Adobe Admin Console].
<!--* For other considerations when deleting a user in [!DNL Workfront Fusion], see [Considerations when deleting a user in [!DNL Workfront Fusion]](../../workfront-fusion/organizations/manage-fusion-users.md#consider)-->



