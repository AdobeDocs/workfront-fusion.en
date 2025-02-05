---
title: Microsoft Office 365 Email
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use Microsoft Office 365 Email, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 5d4072ba-c598-4347-a42f-c59c7add0a1b
---
# [!DNL Microsoft Office 365 Email] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!UICONTROL Microsoft Office 365 Email], as well as connect it to multiple third-party applications and services.

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
   <p>Current: No Workfront Fusion license requirement.</p>
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

To use [!DNL Microsoft Office 365 Email] modules, you must have a [!DNL Microsoft Office 365 Email] account.

## Microsoft Office 365 Email API information

The Microsoft Office 365 Email connector uses the following:

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
   <td>v2.6.5</td> 
  </tr>
 </tbody> 
 </table>

## Connecting the [!DNL Office 365 Email] service to [!DNL Workfront Fusion]

For instructions about connecting your [!DNL Office 365 Email] account to [!UICONTROL Workfront Fusion], see [Create a connection to [!UICONTROL Adobe Workfront Fusion] - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Some Microsoft apps use the same connection, which is tied to individual user permissions. Therefore, when creating a connection, the permissions consent screen displays any permissions that were previously granted to this user's connection, in addition to any new permissions needed for the current application. 
>
>For example, if a user has "Read table" permissions granted via the Excel connector and then creates a connection in the Outlook connector to read emails, the permissions consent screen will show both the already granted "Read table" permission and the newly required "Write email" permission.

## [!DNL Microsoft Office 365 Email] modules and their fields

When you configure [!DNL Microsoft Office 365 Email] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Microsoft Office 365 Email] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Message](#message)
* [Draft Message](#draft-message)
* [Attachment](#attachment)
* [Other](#other)

### Message

* [[!UICONTROL Create and Send a Message (legacy)]](#create-and-send-a-message)
* [[!UICONTROL Delete a Message]](#delete-a-message)
* [[!UICONTROL Get a message]](#get-a-message)
* [[!UICONTROL Move a Message]](#move-a-message)
* [[!UICONTROL Search messages]](#search-messages)
* [[!UICONTROL Watch Messages]](#watch-messages)



#### [!UICONTROL Create and Send a Message (legacy)]

This action module creates and sends an email message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Enter or map the subject line of the message.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>Enter or map the message body text of the email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Select the importance of the email</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>For each recipient that you want to send the email to, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>For each recipient that you want to send a copy of the email to, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>For each recipient that you want to send a copy of the email to, without allowing other recipients to see their names or email addresses, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>For each attachment that you want to add to the email, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Select a source file from a previous module, or map the source file's name and data.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Internet Message Headers]</td> 
   <td> <p>For each header that you want to add to the email, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the header</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter a value for the header.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Message]

This action module deletes an existing email message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> To use a shared email address, enter the address here. The user whose credentials are used in the connection used for this module must have access to the shared folder.<p>Leave this field blank to use connection owner's own email address.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Select or map the ID of the message you want to delete.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a message]

This action module gets the metadata of a specific message

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> To use a shared email address, enter the address here. The user whose credentials are used in the connection used for this module must have access to the shared folder.<p>Leave this field blank to use connection owner's own email address.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Select or map the ID of the message you want to retrieve metadata for.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get MIME contents]</td> 
   <td>Enable this option to retrieve data about the MIME content of the message. [!UICONTROL MIME] content may include images, audio, video, or other types of files.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a Message]

This action module moves an email message to a selected folder in the mailbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Select or map the ID of the message you want to move to a different folder.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mail Folder] </td> 
   <td> <p>Select or map the ID of the folder where you want to move the message.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search messages]

This search module searches for messages based on specific criteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> To use a shared email address, enter the address here. The user whose credentials are used in the connection used for this module must have access to the shared folder.<p>Leave this field blank to use connection owner's own email address.</p></p> </td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Mail Folder]</td> 
   <td> <p>Select the folder that contains the messages you want to search.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>Enter your search query. For information on how to write a search query, see the [!DNL Microsoft] support article <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&amp;rs=en-us&amp;ad=us">Search Mail and People in [!DNL Outlook.com]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td> <p>Select how you want to order the results:</p> 
    <ul> 
     <li>[!UICONTROL Subject (Ascending or descending)]</li> 
     <li>[!UICONTROL Created Date Time (Ascending or descending)]</li> 
     <li>[!UICONTROL Last Modified Date Time (Ascending or descending)]</li> 
     <li>[!UICONTROL Received Date Time (Ascending or descending)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter the maximum number of messages [!DNL Workfront Fusion] should return during one scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Messages]

This trigger module starts a scenario when a new email message is sent or received.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Watch Messages]</p> </td> 
   <td> <p>Select the messages you want to watch:</p> 
    <ul> 
     <li>[!UICONTROL Only Unread]</li> 
     <li>[!UICONTROL Only read]</li> 
     <li>[!UICONTROL All]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mail Folder]</td> 
   <td> <p>Select the folder that contains the messages you want to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>Enter your search query. The module returns messages that match this query. For information on how to write a search query, see the [!DNL Microsoft] support article <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&amp;rs=en-us&amp;ad=us">Search Mail and People in [!DNL Outlook.com]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Enter the maximum number of messages [!DNL Workfront Fusion] should return during one scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Draft Message

* [Create a Draft Message](#create-a-draft-message)
* [Send a Draft Message](#send-a-draft-message)
* [Update a Message](#update-a-message)

#### [!UICONTROL Create a Draft Message] 

This action module creates a new email message as a draft.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Enter the subject line of the message.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body Content Type]</td> 
   <td>Select whether the body content of the message is HTML or Text.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>Enter or map the message body text of the email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Select the importance of the email</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>For each recipient that you want to send the email to, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>For each recipient that you want to send a copy of the email to, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>For each recipient that you want to send a copy of the email to, without allowing other recipients to see their names or email addresses, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>For each attachment that you want to add to the email, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Select a source file from a previous module, or map the source file's name and data.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> To use a shared email address, enter the address here. The user whose credentials are used in the connection used for this module must have access to the shared folder.<p>Leave this field blank to use connection owner's own email address.</p></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send a Draft Message]

This action module sends an email message that is currently in draft.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> To use a shared email address, enter the address here. The user whose credentials are used in the connection used for this module must have access to the shared folder.<p>Leave this field blank to use connection owner's own email address.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Draft Message ID]</td> 
   <td> <p> Select or map the Message ID of the draft you want to send.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Message]

This action module updates an existing message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> To use a shared email address, enter the address here. The user whose credentials are used in the connection used for this module must have access to the shared folder.<p>Leave this field blank to use connection owner's own email address.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a message ID]</td> 
   <td> <p>Select how you want to identify the message to update:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter Manually]</strong> </p> <p>Enter or map the message ID.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the folder that contains the message you want to update, then select the message</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Enter the subject line of the message.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>Enter the message body text of the email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Select the importance of the email</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>For each recipient that you want to send the email to, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>For each recipient that you want to send a copy of the email to, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>For each recipient that you want to send a copy of the email to, without allowing other recipients to see their names or email addresses, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>For each attachment that you want to add to the email, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Select a source file from a previous module, or map the source file's name and data.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark it as Read]</td> 
   <td>Enable this option to mark the updated message as read.</td> 
  </tr> 
 </tbody> 
</table>

### Attachment

* [[!UICONTROL Download an Attachment]](#download-an-attachment)
* [[!UICONTROL List Attachments]](#list-attachments)

#### [!UICONTROL Download an Attachment]

This module downloads the specified attachment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> To use a shared email address, enter the address here. The user whose credentials are used in the connection used for this module must have access to the shared folder.<p>Leave this field blank to use connection owner's own email address.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Select or map the ID of the message that contains the attachment you want to download.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment ID]</td> 
   <td> <p>Enter or map the ID of the attachment you want to download. You can locate this idea using the List Attachments module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Attachments]

This module retrieves a list of attachments belonging to the specified message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> To use a shared email address, enter the address here. The user whose credentials are used in the connection used for this module must have access to the shared folder.<p>Leave this field blank to use connection owner's own email address.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Select or map the ID of the message you want to retrieve attachments from.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of attachments you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Other

* [[!UICONTROL Add an Attachment]](#add-an-attachment)
* [Create and send a message](#create-and-send-a-message)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Add an Attachment]

This module adds a large attachment to a message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> To use a shared email address, enter the address here. The user whose credentials are used in the connection used for this module must have access to the shared folder.<p>Leave this field blank to use connection owner's own email address.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Select or map the ID of the message you want to add an attachment to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create and Send a Message]

This action module creates and sends an email message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Enter or map the subject line of the message.</p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>Enter or map the message body text of the email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Select the importance of the email</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>For each recipient that you want to send the email to, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>For each recipient that you want to send a copy of the email to, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>For each recipient that you want to send a copy of the email to, without allowing other recipients to see their names or email addresses, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter the email address of the contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>For each attachment that you want to add to the email, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Select a source file from a previous module, or map the source file's name and data.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Internet Message Headers]</td> 
   <td> <p>Add the message headers for the email.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the name of the header</p> </li> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Enter a value for the header.</p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> To use a shared email address, enter the address here. The user whose credentials are used in the connection used for this module must have access to the shared folder.<p>Leave this field blank to use connection owner's own email address.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
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
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Enter a path relative to <code>https://graph.microsoft.com</code>. Example:<code> /v1.0/me/messages</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
