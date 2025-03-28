---
title: Email modules
description: In a [!DNL Adobe Workfront Fusion] scenario, you can connect your Email account to multiple third-party applications and services.This allows you to download emails via IMAP, send emails via SMTP, create new drafts, move and copy emails from one folder to another folder, mark emails as read or unread, and delete emails.
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
---
# Email modules

In a [!DNL Adobe Workfront Fusion] scenario, you can connect your Email account to multiple third-party applications and services.This allows you to download emails via IMAP, send emails via SMTP, create new drafts, move and copy emails from one folder to another folder, mark emails as read or unread, and delete emails.

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

## Connect your email to Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [Connect to Google](#connect-to-google)
* [Connect to other email services (IMAP)](#connect-to-other-email-services-smap)

### Connect to [!DNL Google]

Use this option to create scenarios with email modules that require a connection to your [!DNL Google] account. This is an account with restricted scopes.

You can create a connection to your [!DNL Google] account directly from inside an Email module.

1. In any Email module, click **[!UICONTROL Add]** next to the [!UICONTROL Connection] field.
1. Select **[!DNL Google]** as the connection type.
1. Enter a name for the connection.
1. (Optional) Enter your [!UICONTROL [!DNL Google] Client ID] and [!UICONTROL Client Secret].
1. Click **[!UICONTROL Continue]** to create the connection and go back to the module.

### Connect to other email services (IMAP)

IMAP connection allows you to access your mailbox remotely and read or manipulate messages in your mailbox. IMAP connection is used by most of the Email modules.

1. In any Email module, click **[!UICONTROL Add]** next to the [!UICONTROL Connection] field.
1. Select **[!UICONTROL Others (SMTP)]** as the connection type.
1. Enter a **[!UICONTROL Name]** for the connection.
1. Select your **[!UICONTROL Email provider]** from the list. If your email provider is not on the list, select Other.
1. Enter the  **[!UICONTROL User name]**, and your **[!UICONTROL Password]** for the email account.
1. (Conditional) If your provider is not on the list, enter your **[!UICONTROL SMTP server]** and **[!UICONTROL Port]**, and specify whether you want to **[!UICONTROL Use a secure connection (TLS)]**. To find this information, check the [!UICONTROL Help] section for your mailbox. If you don't have this information available, contact your email service provider.
1. To use a self-signed certificate, enable the **Reject unauthorized certificates** option and upload your self-signed certificate. For instructions, see [Upload a self-signed certificate](#upload-a-self-signed-certificate)
1. Click **[!UICONTROL Continue]** to create the connection and go back to the module.

#### Upload a self-signed certificate

To add a self-signed certificate:

1. Click **Extract**.
1. Select the type of file you are extracting.
1. Select the file that contains the or certificate. 
1. Enter the password for the file.
1. Click **Save** to extract the file and return to the module setup.

## [!UICONTROL Email] modules and their fields

When you configure [!UICONTROL Email] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

Some of the email fields might already contain data because you used them in another module in the scenario. See the email help documentation if you need information about them.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>The Unique Email ID known as '[!UICONTROL Email ID (UID)]' is the email's identifier. The Email ID is specific for each of the email's folders.

* [Triggers](#triggers)
* [Actions](#actions)
* [Iterators](#iterators)

### Triggers 

#### [!UICONTROL Watch Emails]

This trigger module starts a scenario when a new email is received for processing according to specified criteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your email account to [!UICONTROL Workfront Fusion], see <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connect your email to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Select the folder that contains emails you want to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Select the criteria by which you want to watch emails:</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>Enter the email address of the sender whose emails you want to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Enter the subject of the email you want to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Enter any keywords to watch only those emails containing the keywords.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched]</td> 
   <td> <p>Enable this option to mark the unread email as read after retrieving the details.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> Enter or map the maximum number of emails [!DNL Workfront Fusion] should return during one scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Copy an Email]](#copy-an-email)
* [[!UICONTROL Create a Draft]](#create-a-draft)
* [[!UICONTROL Delete an Email]](#delete-an-email)
* [[!UICONTROL Get Emails]](#get-emails)
* [[!UICONTROL Mark an Email as Read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an Email as Unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an Email]](#move-an-email)
* [[!UICONTROL Send an Email]](#send-an-email)

#### [!UICONTROL Copy an Email]

This action module copies an email or a draft into a selected folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your email account to [!UICONTROL Workfront Fusion], see <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connect your email to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Select the folder from which you want to copy the email. Example: Primary.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Select the folder to which you want to copy the email. Example: Work.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Enter the Email UID of the email you want to copy to the destination folder.</p> <p>You can get the UID of the email by using the [!UICONTROL Email] > [!UICONTROL Watch Email] module or [!UICONTROL Search Email] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Draft]

This action module creates and adds a new draft to a selected folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your email account to [!UICONTROL Workfront Fusion], see <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connect your email to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Select the folder in which you want to create the draft email.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>Enter or map the email address to which you want to send the email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Enter or map the subject line of the email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Enter or map the email content in HTML format using HTML tags, or in the plain text.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>For each attachment you want to add, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Enter the file name, including the extension. </p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Enter the path to the folder where you want to to upload the attachment.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Enter the content ID to insert the attachment (image) in the content.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>For each email address to which you want to send a copy of this email click <b>Add item</b> and enter the email address. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> For each email address to which you want to send a copy of this email without having the email address appear in the email, click <b>Add item</b> and enter the email address.</p> </td> 
  </tr> 
  <!--<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Enter or map the email address (and name, if needed) that appears in the [!UICONTROL From] field in the email. </p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code>.</p> <p>Note:  Normally, [!DNL Workfront Fusion] uses the email address that you entered when creating the connection as the sender address. If you enter any other email address, an error may occur when sending a message because your account may not have permission to send emails from a different address than your own. E.g. <code>test@mail.com</code> or "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Enter or map the email address that appears in the [!UICONTROL Sender] field in the email.</p> <p>Tip:  If you are unsure whether to use this field or the From field, we recommend choosing the From field.</p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> If you want replies to this email sent to a different address than the "[!UICONTROL from]" address, enter the email address where you want replies to this email sent.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> If you are replying to a specific email, enter or map the ID of the email you are replying to.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Enter the message IDs of all the replies in the thread.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Select the priority of the email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Add the headers:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Add the key. For example, Sender, Date, To, and so on.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter the value for the key.</p> </li> 
    </ul> </td> 
  </tr> -->
 </tbody> 
</table>

#### [!UICONTROL Delete an Email]

This action module removes an email or a draft from the selected folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your email account to [!UICONTROL Workfront Fusion], see <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connect your email to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Select the folder that contains the email you want to delete.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Enter the Email UID of the email you want to delete.</p> <p>You can get the UID of the email by using the Email > Watch Email module or [!UICONTROL Search Email] module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expunge]</td> 
   <td> <p>Enable this option to permanently remove all messages flagged as [!UICONTROL Deleted] in the currently open mailbox.</p> <p>Note: In [!DNL Gmail], this behavior is driven by the setting in the [!UICONTROL Settings] >[!UICONTROL Forwarding POP/IMAP in IMAP access] section.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Emails]

This module returns emails that match the specified criteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your email account to [!UICONTROL Workfront Fusion], see <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connect your email to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Select the folder that contains the emails you want to retrieve.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched] </td> 
   <td> <p>Enable this option if you want to mark the unread email as read after retrieving the details.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Select the criteria of the emails you want to retrieve:</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>Enter or map the email address of the sender whose emails you want to retrieve.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Recipient Email]</td> 
   <td> <p> Enter or map the email address of the recipient whose emails you want to retrieve.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From date] </td> 
   <td> <p>Enter or map the date to retrieve the emails processed on or after the specified date.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before date]</td> 
   <td> <p> Enter or map the date to retrieve the emails processed on or before the specified date.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Enter or map the subject of the email you want to retrieve.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Enter or map any keywords to retrieve only those emails containing those keywords.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Enter the Email ID (UID) of the email whose details you want to retrieve.</p> <p>You can get the UID of the email by using [!DNL Workfront Fusion]'s[!UICONTROL  Watch Email] module or [!UICONTROL Search Email] module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> The maximum number of emails [!DNL Workfront Fusion] should return during one scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p> Select if you want to continue to run the module even if there are no results returned.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Read]

This action module marks an email or a draft in a selected folder as read, by setting the [!UICONTROL Read] flag.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your email account to [!UICONTROL Workfront Fusion], see <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connect your email to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Select the folder that contains the email you want to mark as read.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Enter the Email UID of the email you want to mark as read.</p> <p>You can get the UID of the email by using the Email > Watch Email module or [!UICONTROL Search Email] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Unread] 

Marks an email or a draft in a selected folder as unread by setting the Unread flag.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your email account to [!UICONTROL Workfront Fusion], see <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connect your email to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Select the folder that contains the email you want to mark as unread. Example: Primary.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Enter the Email UID of the email you want to mark as unread.</p> <p>You can get the UID of the email by using the Email > Watch Email module or [!UICONTROL Search Email] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Email]

Moves a chosen email or a draft to a selected folder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your email account to [!UICONTROL Workfront Fusion], see <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connect your email to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Select the folder that contains the email you want to move. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Select the folder to which you want to add the email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Enter the Email UID of the email you want to move to the destination folder.</p> <p>You can get the UID of the email by using the Email > Watch Email module or [!UICONTROL Search Email] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send an Email] 

Sends a new email.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your email account to [!DNL Workfront Fusion], see <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connect your email to [!UICONTROL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save Message after Sending]</td> 
   <td>After the email message is sent, it will be saved in your mailbox. Enable this option if you want to save emails sent using [!DNL Workfront Fusion] to the <i>[!UICONTROL Sent mail]</i> folder or another folder in your mailbox. Some email services, such as [!DNL Gmail], save sent messages automatically.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>Add the email addresses you want to send the email to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Enter or map the subject line of the email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Content Type]</p> </td> 
   <td> <p>Select the [!UICONTROL content] type for the email:</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Plaintext]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Enter or map the email content in HTML format using HTML tags, or in the plain text, depending on what you chose in the [!UICONTROL Content Type] field.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>For each attachment you want to add, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Enter the file name, including the extension. </p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Enter the path to the folder where you want to to upload the attachment.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Enter the content ID to insert the attachment (image) in the content.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>For each email address to which you want to send a copy of this email click <b>Add item</b> and enter the email address. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> For each email address to which you want to send a copy of this email without having the email address appear in the email, click <b>Add item</b> and enter the email address.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Enter or map the email address that appears in the [!UICONTROL Sender] field in the email.</p> <p>Tip:  If you are unsure whether to use this field or the From field, we recommend choosing the From field.</p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> If you want replies to this email sent to a different address than the "from" address, enter the email address where you want replies to this email sent.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> If you are replying to a specific email, enter or map the ID of the email you are replying to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Enter the message IDs of all the replies in the thread.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Select the priority of the email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Add the headers:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Add the key. For example, [!UICONTROL Sender], [!UICONTROL Date], [!UICONTROL To], and so on.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter the value for the key.</p> </li> 
    </ul> </td> 
  </tr> 
<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Enter or map the email address (and name, if needed) that appears in the [!UICONTROL From] field in the email. </p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code>.</p> <p>Note:  Normally, [!DNL Workfront Fusion] uses the email address that you entered when creating the connection as the sender address. If you enter any other email address, an error may occur when sending a message because your account may not have permission to send emails from a different address than your own. E.g. <code>test@mail.com</code> or "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Iterators

#### [!UICONTROL Iterate Attachments]

Iterates received attachments one by one.

The email iterator module lets you manage email attachments separately. For example, you can set up to watch emails to iterate the emails with attachments and receive alerts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module]</td> 
   <td> <p>Select the module that outputs the email with the attachments that you want to iterate through.</p> </td> 
  </tr> 
 </tbody> 
</table>

For more information about iterators, see [Iterator module](/help/workfront-fusion/references/modules/iterator-module.md).
