---
title: MariaDB modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL MariaDB], as well as connect it to multiple third-party applications and services.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 41179cfe-c0f9-4d18-ab7e-374670ac688b
---
# [!DNL MariaDB] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL MariaDB], as well as connect it to multiple third-party applications and services.

For instructions on creating a scenario, see the articles under [Create scenarios: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td> <p>New: Standard</p><p>Or</p><p>Current:  Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>Current: No Workfront Fusion license requirement</p>
   <p>Or</p>
   <p>Legacy: Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>Select or Prime Workfront package: Your organization must purchase Adobe Workfront Fusion.</li><li>Ultimate Workfront package: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

To use [!DNL MariaDB] modules, you must have a [!DNL MariaDB] account.

## Connect [!DNL MariaDB] to [!DNL Workfront Fusion] 

You can create a connection to your [!DNL MariaDB] account directly from inside a [!DNL MariaDB] module.

1. In any [!DNL MariaDB] module, click **[!UICONTROL Add]** next to the [!UICONTROL Connection] field.
1. Configure the following fields:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Enter a name for the new connection.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Select whether this connection is for a production or non-production environment.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Select whether you are connecting to a service account or a personal account.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Host]</td> 
      <td> <p>Enter the IP address or host name of your database instance. This host must be accessible from outside your network.</p> <p>Example: <code>[!DNL mariadb.hwoh2j5h.us-east-1.rds.amazon.com]</code></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Port]</td> 
      <td>The default port is 3306. If you are using a non-standard port, set this number to your port. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Database ]</td> 
      <td>Enter the name of the database you want to interact with.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL User]</td> 
      <td>Enter your username.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Password]</td> 
      <td>Enter your password.</td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL Continue]** to create the connection and go back to the module.

## [!DNL MariaDB] Modules and their fields

When you configure [!DNL MariaDB] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL MariaDB] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Execute a query (advanced)

This action module retrieves information from your database, based on a query you supply.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions about connecting your [!DNL MariaDB] account to [!DNL Workfront Fusion], see <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Connect [!DNL MariaDB] to [!DNL Workfront Fusion]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Enter the SQL query that you want the module to use to retrieve data.</p> <p>Important: Variables used in the query are not sanitized. Make sure you sanitize variables properly to prevent SQL injection.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Select rows from a table (advanced)]

This module reads record from your database.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions about connecting your [!DNL MariaDB] account to [!DNL Workfront Fusion], see <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Connect [!DNL MariaDB] to [!DNL Workfront Fusion]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table]</td> 
   <td> <p>Select the table that contains the records you want to read.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Set up the filter by which you want to select rows</p> 
    <ul> 
     <li> <p>Select the field that you want to search by</p> </li> 
     <li> <p>Select the operator that you want to use for your search</p> </li> 
     <li> <p>Enter or map the value that you want to search for.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort] </td> 
   <td> <p>For each level that you want your results sorted by, click <strong>[!UICONTROL Add item]</strong>, then select the field that you want to sort the results by and whether you want to sort ascending or descending</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>
