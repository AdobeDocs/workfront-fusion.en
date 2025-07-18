---
title: SharePoint modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use Microsoft SharePoint Online, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
---
# Microsoft SharePoint Online modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use Microsoft SharePoint Online, as well as connect it to multiple third-party applications and services.

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

To use Microsoft SharePoint Online modules, you must have a Microsoft SharePoint Online account.

## SharePoint API information

The SharePoint connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API version</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.14.2</td> 
  </tr>
 </tbody> 
 </table>

## Connect Microsoft SharePoint Online to [!DNL Workfront Fusion] {#connect-microsoft-sharepoint-online-to-workfront-fusion}

* [Connect Microsoft SharePoint Online to [!DNL Workfront Fusion] using a [!DNL Microsoft] account](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-a-microsoft-account)
* [Connect Microsoft SharePoint Online to [!DNL Workfront Fusion] using advanced settings](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-advanced-settings)
* [Connect Microsoft SharePoint Online to [!DNL Workfront Fusion] using certificate authorization](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-certificate-authorization)

### Connect Microsoft SharePoint Online to [!DNL Workfront Fusion] using a [!DNL Microsoft] account 

You can use your [!DNL Microsoft] account to create a connection to Microsoft SharePoint Online. For instructions about connecting your [!DNL Sharepoint] account to [!DNL Workfront Fusion], see [Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### Connect Microsoft SharePoint Online to [!DNL Workfront Fusion] using advanced settings

To include credentials in the connection, enable the Show advanced settings option. For this type of connection,  you need a Client ID, Client Secret, and Tenant ID.

1. In any SharePoint module, click **[!UICONTROL Add]** near the Connection field to open the **[!UICONTROL Create a connection]** box.
1. Click **[!UICONTROL Show advanced settings]**.
1. Fill in the following fields:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection type]</p> </td> 
      <td>To use client credentials, select <b>Microsoft 365 Email</b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Enter a name for the connection.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client ID]</p> </td> 
      <td>Enter the client ID for the SharePoint app you are connecting to. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client secret]</p> </td> 
      <td>Enter the client secret for the SharePoint app you are connecting to.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Tenant ID]</p> </td> 
      <td>Enter the tenant ID of the SharePoint app you are connecting to.</td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Continue** to save the connection and return to the module.

### Connect Microsoft SharePoint Online to [!DNL Workfront Fusion] using certificate authorization

You can use certificate authorization to connect to SharePoint.

>[!IMPORTANT]
>
>To use certificate authorization, you must first create an app in Microsoft Entra and upload the certificate there.
>
>For instructions, see [How to configure certificate authorities for Microsoft Entra certificate-based authentication](https://learn.microsoft.com/en-us/entra/identity/authentication/how-to-configure-certificate-authorities) in the Microsoft documentation.

1. In any SharePoint module, click **[!UICONTROL Add]** near the Connection field to open the **[!UICONTROL Create a connection]** box.
1. Click **[!UICONTROL Show advanced settings]**.
1. Fill in the following fields:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection type]</p> </td> 
      <td>To use certificate authorization, select <b>Microsoft SharePoint Online (Cert Auth)</b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Enter a name for the connection.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client ID]</p> </td> 
      <td>Enter the client ID for the SharePoint app you are connecting to. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Thumbprint]</p> </td> 
      <td>Enter the thumbprint for the SharePoint app you are connecting to.</td> 
     </tr> 
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Enter the certificate or  private key that was generated when your credentials were created in Microsoft. </p>
          <p>To extract your private key or certificate:</p>
          <ol>
            <li>
              <p>Click <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li>
            <p>Select whether you are extracting a certificate or a private key.</li>
            <li>
              <p>Select the type of file you are extracting.</p>
            </li>
            <li>
              <p>Select the file that contains the private key or certificate.</p>
            </li>
            <li>
              <p>Enter the password for the file.</p>
            </li>
            <li>
              <p>Click <b>[!UICONTROL Save]</b> to extract the file and return to the connection setup.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody> 
   </table>

1. Click **Continue** to save the connection and return to the module.

## Microsoft SharePoint modules and their fields

When you configure Microsoft SharePoint Online modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional Microsoft SharePoint Online fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Drive item](#drive-item)
* [Item](#item)
* [List](#list)
* [Page (Beta)](#page-beta)
* [Site](#site)
* [Other](#other)

### Drive item

* [Create a file](#create-a-file)
* [Create a folder](#create-a-folder)
* [Get a file](#get-a-file)
* [Get a folder](#get-a-folder)
* [Update a folder or a file](#update-a-folder-or-a-file)
* [Watch folder items](#watch-folder-items)

#### Create a file

This module returns changes that have been made in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Select how you want to identify the location of the folder that you want to retrieve changes in.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong>, and <strong>[!UICONTROL Folder ID]</strong> of the location where you want to create the file.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Select the location where you want to create the file. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
      <p>Select a source file from a previous module, or map the source file's name and data.</p>
  </tr>  </tbody> 
</table>

#### Create a folder

This action module creates a new folder in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Select how you want to identify the location of the folder you want to create.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong>, and <strong>[!UICONTROL Folder ID]</strong> of the location where you want to create the folder.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Select the location where you want to create the folder. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder name]</td> 
   <td>Enter or map a name for the new folder.</td> 
  </tr>
  </tbody> 
</table>

#### Get a file

This action module retrieves the specified SharePoint file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Select how you want to identify the location of the file you want to get.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong>, and <strong>[!UICONTROL File ID]</strong> for the file that you want to retrieve.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Select the location of the file. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Get a folder

This module retrieved details about the specified folder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and File                IDs]</td> 
   <td> <p>Select how you want to identify the location of the file you want to get.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong>, and <strong>[!UICONTROL Folder path]</strong> for the folder that you want to retrieve.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Select the location of the folder. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Update a folder or a file

This action module updates the metadata of a folder or a file

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and File                IDs]</td> 
   <td> <p>Select how you want to identify the location of the file you want to get.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong>, and <strong>[!UICONTROL Folder or item ID]</strong> for the folder or file that you want to retrieve.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Select the location of the folder. </p> </li> 
    </ul> </td> 
  </tr> 
  </tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>For each metadata field that you want to update, click <b>Add item</b> and enter the field's path and value.</td> 
  <tr>
</tbody> 
</table>

#### Watch folder items

This trigger module starts a scenario when an item is updated in a folder you select.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Select how you want to identify the location of the file you want to get.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong>, and <strong>[!UICONTROL folder ID]</strong> in the fields that appear.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Select the location of the folder you want to watch. </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Enter the maximum number of items [!DNL Workfront Fusion] should return during one scenario execution cycle.</td> 
  <tr>
  </tr>
</tbody> 
</table>

### Item

* [[!UICONTROL Copy an item]](#copy-an-item)
* [[!UICONTROL Create an item]](#create-an-item)
* [[!UICONTROL Delete an item]](#delete-an-item)
* [[!UICONTROL Get an Item]](#get-an-item)
* [Get Details](#get-details)
* [[!UICONTROL List Items]](#list-items)
* [[!UICONTROL Move an Item]](#move-an-item)
* [[!UICONTROL Update an Item]](#update-an-item)
* [[!UICONTROL Watch Items] (Scheduled)](#watch-items-scheduled)


#### [!UICONTROL Copy an Item]

This action module copies an existing item in a SharePoint list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enter Site, Drive, and Folder IDs</td> 
   <td> <p>Select how you want to identify the site and drive that contain the item you want to copy.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong>, and <strong>[!UICONTROL Item ID]</strong> of the item you want to copy.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>In the Item Type field, select whether you are moving a field or a folder.  Select the site that contains the item you want to copy, then select the list, then select the item. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> Enter or map the ID of the folder you want to copy the item to. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>Enter or map a name for the new copy of the item. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an item]

This action module creates a new item in a SharePoint list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Create an Item]</td> 
   <td> <p>Select how you want to identify the site and drive where you want to create an item.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong> and <strong>[!UICONTROL List ID]</strong> where you want to create the item.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the list where you want to create an item, then select the list. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>For each field that you want to set for the new item, click <b>Add item</b> and enter the field's key (which identifies the field) and the value that you want the new item to have for that field.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an item]

This action module deletes an existing item in a SharePoint list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Select how you want to identify the site and list that contain the item you want to delete.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong>, and <strong>[!UICONTROL Item ID]</strong> of the item you want to delete.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the item you want to delete, then select the list, then select the item. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Item]

This action module returns the data of a specified item.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get an Item]</td> 
   <td> <p>Select how you want to identify the site and list that contain the item you want to get.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong>, and <strong>[!UICONTROL Item ID]</strong> of the item that you want to return data for.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the list you want to retrieve an item from, then select the list, then select the item. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Get details

This module gets item details from the specified URL.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Web URL</td> 
   <td> Enter or map the URL of the item that you want to retrieve details for. </td> 
  </tr> 
</tbody> 
</table>

#### [!UICONTROL List Items]

This action module retrieves a list of all items in a specified list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Items]</td> 
   <td> <p>Select how you want to identify the list that you want to retrieve items from.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong> and <strong>[!UICONTROL List ID]</strong> for the list that you want to list items for.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the list you want to retrieve items from, then select the list. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of items you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Item]

This action module copies an existing item in a SharePoint list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enter Site, Drive, and Folder IDs</td> 
   <td> <p>Select how you want to identify the site and list that contain the item you want to move.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong>, and <strong>[!UICONTROL Item ID]</strong> for the item that you want to move.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>In the Item Type field, select whether you are moving a field or a folder. Select the site that contains the item you want to copy, then select the list, then select the item. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> Enter or map the ID of the folder you want to move the item to. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>Enter or map a name for the moved item. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an item]

This action module updates an existing item in a SharePoint list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Select how you want to identify the site and list that contain the item you want to update.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong>, and <strong>[!UICONTROL Item ID]</strong> of the item you want to update.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the item you want to update, then select the list, then select the item. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>For each field that you want to update for the new item, click <b>Add item</b> and enter the field's key (which identifies the field) and the new value that you want the item to have for that field.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Items] (Scheduled)

This trigger module starts a scenario when an item is created or modified.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Select whether you want to watch lists by creation time (new items) or by modification time (updated items).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>Select how you want to identify the site and list that you want to watch.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong> and <strong>[!UICONTROL List ID]</strong> that you want to watch.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Select the site that you want to watch, then select the list. These drop-downs only retrieve followed sites.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of items you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### List

* [[!UICONTROL Create a List]](#create-a-list)
* [[!UICONTROL Get a List]](#get-a-list)
* [[!UICONTROL List Lists]](#list-lists)
* [[!UICONTROL Watch Lists]](#watch-lists)

#### [!UICONTROL Create a List]

This action module creates a new list in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Site ID]</td> 
   <td> <p>Select how you want to identify the site where you want to create a list.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong> where you want to create a list.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site where you want to create a list. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display Name]</td> 
   <td>Enter or map a name for the new list.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the new list.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Add Columns]</td> 
   <td>For each column that you want to set for the new list, click <b>Add item </b>, enter a <strong>[!UICONTROL Name]</strong> for the field, and select the <strong>[!UICONTROL Type]</strong> of value that you want the new column to have.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a List]

This action module returns the data of a specified list.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a List]</td> 
   <td> <p>Select how you want to identify the site and list that contain the item you want to get.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong> and <strong>List ID</strong> that you want to return.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the list you want to retrieve, then select the list. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Lists]

This action module retrieves a list of all items in a specified site.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Lists]</td> 
   <td> <p>Select how you want to identify the site that you want to retrieve lists from.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong> that contains the lists you want to return.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the lists you want to retrieve. The drop-down retrieves only sites you follow.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of lists you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Lists]

This trigger module starts a scenario when a list is created or modified.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Select whether you want to watch lists by creation time (new items) or by modification time (updated items).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site ID]</td> 
   <td> <p>Select how you want to identify the site that you want to watch for lists.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong> where you want to watch lists.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Select the site that you want to watch. The drop-down only retrieves site you follow.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of lists you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Page (Beta)

>[!NOTE]
>
>APIs in the `beta` version in [!DNL Microsoft Graph] are subject to change. The use of these APIs in production applications is not supported.

* [Get a Page](#get-a-page)
* [List Pages](#list-pages)
* [Publish a Page](#publish-a-page)
* [Watch Pages](#watch-pages)

#### [!UICONTROL Get a Page]

This action module returns the data of a specified page.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Page]</td> 
   <td> <p>Select how you want to identify the page that you want to retrieve.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>and <strong>[!UICONTROL Page ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the page you want to retrieve, then select the page.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### List Pages

This module retrieves a list of all pages.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Pages]</td> 
   <td> <p>Select how you want to identify the pages that you want to list.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong> of the site that contains the pages you want to list.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the pages you want to list.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of pages you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Publish a Page

This action module publishes the latest version of the selected page.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Publish a page]</td> 
   <td> <p>Select how you want to identify the page that you want to publish.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>and <strong>[!UICONTROL Page ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the page you want to publish, then select the page.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Watch Pages

This trigger module starts a scenario when a page is modified on the specified site.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site ID]</td> 
   <td> <p>Select how you want to identify the pages that you want to list.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong> of the site that contains the pages you want to watch.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Select the site that contains the pages you want to watch.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of pages you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Site

* [[!UICONTROL Get a Site]](#get-a-site)
* [[!UICONTROL Search Sites]](#search-sites)

#### [!UICONTROL Get a Site]

This action module returns the data of a specified site.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Site]</td> 
   <td> <p>Select how you want to identify the page that you want to retrieve.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that you want to retrieve.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Sites]

This action module searches for sites by a parameter you specify.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword of Display Name]</td> 
   <td> <p>Enter or map the search term that you want to search the sites for.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of sites you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Other

* [Get Changes](#get-changes)
* [Make an API Call](#make-an-api-call)
* [Watch Events](#watch-events)

#### Get Changes

This module retrieves additions, updates, and deletions made in the SharePoint folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Select how you want to identify the site and drive that contain the item you want to update.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Enter or map the <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong>, and <strong>[!UICONTROL Folder ID]</strong> in the fields that appear.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the site that contains the item you want to update, then select the drive, then select the folder. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> The token identifies from what point the module should begin retrieving changes.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

This module allows you to perform a custom API call.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Enter a path relative to <code>https://graph.microsoft.com</code>. Example:<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object. For example, <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] adds the authorization headers for you.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Add the query for the API call in the form of a standard JSON object.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Select the type of data that you want to send in your API call.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Watch events

This instant trigger module starts a scenario when an item is added, updated, or deleted in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
  <!--
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Select an existing webhook, or click Add and enter the connection to create a new webhook.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
