---
title: Gmail modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use Gmail, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
---
# [!DNL Gmail] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Gmail], as well as connect it to multiple third-party applications and services.

For instructions on creating a scenario, see the articles under [Create scenarios: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

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

To use [!DNL Gmail] modules, you must have a [!DNL Gmail] account.

## Connect [!DNL Gmail] to [!DNL Workfront Fusion] {#connect-gmail-to-workfront-fusion}

* [Connect [!DNL Gmail] to [!DNL Workfront Fusion] using [!DNL Google Workspace]](#connect-gmail-to-workfront-fusion-usinggoogle-workspace)
* [Connect [!DNL Gmail] to [!DNL Workfront Fusion] using [!DNL gmail.com] or [!DNL googlemail].com](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### Connect [!DNL Gmail] to [!DNL Workfront Fusion] using[!DNL  Google Workspace]

For instructions about connecting your [!DNL Google Workspace] account to [!UICONTROL Workfront Fusion], see [Create a connection - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

### Connect [!DNL Gmail] to [!DNL Workfront Fusion] using [!DNL gmail.com] or [!DNL googlemail].com 

If you are [!DNL @gmail.com] or [!DNL @googlemail.com] user you must create an OAuth client on [the [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) in order to obtain a [!UICONTROL Client ID] and [!UICONTROL Client Secret].

For step-by-step instructions on how to create the OAuth client and obtain a [!UICONTROL Client ID] and [!UICONTROL Client Secret], see [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## [!DNL Gmail] modules and their fields

When you configure [!DNL Gmail] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Gmail] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Actions](#actions)
* [Iterators](#iterators)

### Triggers 

#### [!UICONTROL Watch emails]

This trigger module executes a scenario when a new email is received to be processed.

The module returns all standard fields associated with the record or records, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on connecting your [!DNL Gmail] account to [!DNL Workfront Fusion], see <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connect [!DNL Gmail] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Select the email folder you want to watch.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter type] </td> 
   <td> <p>Select the filter type you want to use to watch emails</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Simple filter]</strong> </p> <p>Fill out the [!UICONTROL Criteria], [!UICONTROL Sender Email Address], [!UICONTROL Subject], and [!UICONTROL Search Phrase] fields</p> </li> 
     <li> <p> <strong>[!UICONTROL Gmail filter]</strong> </p> <p>In the [!UICONTROL Query] field, enter the query that you want to use to filter emails.</p> <p>For more information on [!DNL Gmail] filters, see <a href="https://support.google.com/mail/answer/7190">Refine searches</a> in the [!DNL Gmail] documentation.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteria]</td> 
   <td>Select whether you want to watch [!UICONTROL all email], [!UICONTROL only read emails], or [!UICONTROL only unread] emails.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sender email address]</td> 
   <td> <p> Enter an email address to watch only emails sent from that address.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>Enter a text string to watch only emails that have that text string in the subject.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search phrase]</td> 
   <td>Enter a text string to watch only emails that have that text string anywhere in the email.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mark email message(s) as read when fetched]</td> 
   <td> <p> Enable this option to mark retrieved emails as read.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of results]</td> 
   <td> <p> Set the maximum number of results that [!DNL Workfront Fusion] will work with during one cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

<!--* [Add labels](#add-labels)-->
* [[!UICONTROL Copy an email]](#copy-an-email)
* [[!UICONTROL Create a draft]](#create-a-draft)
* [[!UICONTROL Delete an email]](#delete-an-email)
<!--* [Delete labels](#delete-labels)-->
* [[!UICONTROL Mark an email as read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an email as unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an email]](#move-an-email)
* [[!UICONTROL Modify email labels]](#modify-email-labels)
* [[!UICONTROL Send an email]](#send-an-email)
<!--* [Set labels](#set-labels)-->

<!--#### Add labels-->

#### [!UICONTROL Copy an email] 

This action module copies an email or email draft into a folder you specify.

You specify the folder, the destination folder, and the ID of the email..

The module returns the ID of the email and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on connecting your [!DNL Gmail] account to [!DNL Workfront Fusion], see <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connect [!DNL Gmail] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Select the [!DNL Gmail] source folder that contains the email you want to copy.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p>Select the [!DNL Gmail] target folder you want to copy the email to.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p>Enter or map the Email ID of the email you want to copy.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a draft] 

This action module creates a new email draft and adds it to a folder you specify.

You specify the folder where you want to create a draft.

The module returns the ID of the email draft and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on connecting your [!DNL Gmail] account to [!DNL Workfront Fusion], see <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connect [!DNL Gmail] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Select the [!DNL Gmail] folder you want to create a draft in.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Click <strong>[!UICONTROL Add]</strong>, then enter or map the email address for each recipient.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Enter or map the email subject.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Enter or map the email content (message body). HTML tags are allowed.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Click <strong>[!UICONTROL Add]</strong> to add an attachment. You can map a file from the previous modules.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Click <strong>[!UICONTROL Add]</strong>, then enter or map the email address for each copy recipient.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Click <strong>[!UICONTROL Add]</strong>, then enter or map the email address for each blind copy recipient.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an email] 

This action module removes an email or an email draft from a folder you specify.

The module returns the ID of the  email and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on connecting your [!DNL Gmail] account to [!DNL Workfront Fusion], see <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connect [!DNL Gmail] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] Message ID]</p> </td> 
   <td> <p>Enter or map the Email ID of the email you want to delete.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Permanently] </td> 
   <td> <p>Enable this option to allow the module to permanently delete the email, instead of moving it to the trash folder.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Delete labels-->



#### [!UICONTROL Mark an email as read]

This action module marks an email as read.

You specify the ID of the email and its folder.

The module returns the ID of the  email and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on connecting your [!DNL Gmail] account to [!DNL Workfront Fusion], see <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connect [!DNL Gmail] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Select the [!DNL Gmail] folder that contains the email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Enter or map the Email ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as unread] 

This action module marks an email or an email draft as unread.

You specify the ID of the email and its folder.

The module returns the ID of the  email and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on connecting your [!DNL Gmail] account to [!DNL Workfront Fusion], see <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connect [!DNL Gmail] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Select the [!DNL Gmail] folder that contains the email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)] </td> 
   <td> <p>Enter or map the Email ID of the email you want to mark as unread.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify email labels]

This action module modifies the label on an email message you specify.

The module returns the ID of the  email and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on connecting your [!DNL Gmail] account to [!DNL Workfront Fusion], see <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connect [!DNL Gmail] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] Message ID]</td> 
   <td> <p> Enter or map the Email ID of the email you want to delete.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Labels to add]</p> </td> 
   <td> <p>Select or map the label you want to add to the selected email message.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Labels to remove]</td> 
   <td> <p> Select or map the label you want to remove from the selected email message.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!UICONTROL Label to add] and [!UICONTROL Label to remove] fields load only user-created labels.

#### [!UICONTROL Move an email] 

This action module moves an email or an email draft to a folder you specify.

You specify the folder, the destination folder, and the ID of the email..

The module returns the ID of the  email and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on connecting your [!DNL Gmail] account to [!DNL Workfront Fusion], see <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connect [!DNL Gmail] to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Select the [!DNL Gmail] source folder that contains the email you want to move.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p> Select the [!DNL Gmail] target folder you want to move the email to.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Enter or map the Email ID of the email you want to move.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send an email] 

This action module sends a new email.

You specify the recipient of the email.

The module returns the ID of the email and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions on connecting your [!DNL Gmail] account to [!DNL Workfront Fusion], see <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connect [!DNL Gmail] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL From]</td> 
   <td> <p>Enter or map a sender email address.</p> <p>Note:  If you enter an incorrect email address, an error may occur when sending a message because your account may not have permission to send emails from an address different than your own.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Click <strong>[!UICONTROL Add]</strong>, then enter or map the email address for each recipient.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Enter or map the email subject.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Enter or map the email content (message body). HTML tags are allowed.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Click <strong>[!UICONTROL Add]</strong> to add an attachment. You can map a file from the previous modules.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Click <strong>[!UICONTROL Add]</strong>, then enter or map the email address for each copy recipient.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Click <strong>[!UICONTROL Add]</strong>, then enter or map the email address for each blind copy recipient.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Set labels-->

### Iterators

#### [!UICONTROL Iterate attachments]

You can iterate email attachments. Each attachment is a separate bundle in the module's output. For more information, see [Iterator module](/help/workfront-fusion/references/modules/iterator-module.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> <p>Select the module you want to iterate attachments from. </p> </td> 
  </tr> 
 </tbody> 
</table>
