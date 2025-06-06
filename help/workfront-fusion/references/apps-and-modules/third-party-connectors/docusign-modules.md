---
title: DocuSign modules
description: The [!DNL Adobe Workfront Fusion DocuSign] modules enable you to monitor and retrieve envelope status, search and retrieve envelopes, or download and send a document to sign in your [!DNL DocuSign] account.
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
---
# DocuSign modules

The [!DNL Adobe Workfront Fusion] [!DNL DocuSign] modules enable you to monitor and retrieve envelope status, search and retrieve envelopes, or download and send a document to sign in your [!DNL DocuSign] account.

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

To use [!DNL DocuSign] modules, you must have a [!DNL DocuSign] account.

## DocuSign API information

The DocuSign connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>1.18.11</td> 
  </tr>
 </tbody> 
 </table>

## Connect [!DNL DocuSign] to [!DNL Workfront Fusion] {#connect-docusign-to-workfront-fusion}

To create a connection for your [!DNL DocuSign] modules:

1. Click **[!UICONTROL Add]** next to the [!UICONTROL Connection] box when you begin configuring the first [!DNL DocuSign] module.
1. Enter the following:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Enter a name for the new [!DNL DocuSign] connection.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td>Select whether you are connecting to a production on non-production environment.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Select whether you are connecting to a service account or a personal account.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Account type]</td> 
      <td>Select whether you the account you want to connect to is a production account or a demo account.</td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Continue** to save the connection and return to the module.

## [!DNL DocuSign] modules and their fields

When you configure [!DNL DocuSign] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL DocuSign] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Actions](#actions)

### Triggers

#### [!UICONTROL Watch envelopes]

This trigger module starts a scenario when an envelope is sent, delivered, signed, completed, or declined.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL DocuSign] account to [!DNL Workfront Fusion], see <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connect Docusign to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Select the account that contains the records you want to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p> Select the type of event that you want to watch.</p> 
    <ul> 
     <li>[!UICONTROL Document completed]</li> 
     <li>[!UICONTROL Document declined]</li> 
     <li>[!UICONTROL Document sent]</li> 
     <li>[!UICONTROL Document signed]</li> 
     <li>[!UICONTROL New document in Inbox]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Outputs]</p> </td> 
   <td> <p>Select the fields that you want to include in the module output.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Enter or map the maximum number of records you want the module to work with during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

### Actions 

* [[!UICONTROL Add a custom field]](#add-a-custom-field)
* [[!UICONTROL Add Recipient to Envelope]](#add-recipient-to-envelope)
* [[!UICONTROL Create a new envelope]](#create-a-new-envelope)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download a document]](#download-a-document)
* [[!UICONTROL Modify custom field]](#modify-custom-field)
* [[!UICONTROL Read an envelope]](#read-an-envelope)
* [[!UICONTROL Send envelope]](#send-envelope)
* [[!UICONTROL Upload a file to an envelope]](#upload-a-file-to-an-envelope)

#### [!UICONTROL Add a custom field]

This action module adds a custom field to the document

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL DocuSign] account to [!DNL Workfront Fusion], see <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connect [!DNL DocuSign] to [!DNL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Select the account that contains the document where you want to add a custom field.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Enter or map the ID of the envelope that contains the document where you want to add a custom field.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Enter or map a name for the new field that you want to add.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Enable this option if you want the added field to be a required field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Enable this option if you want the field to be visible.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Enter or map the value (contents) of the added field. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add Recipient to Envelope]

This action module adds one or more recipients to an existing envelope. If the envelope has already been sent, the recipient is sent an email. This module is not valid for envelopes that have already been completed.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>For instructions about connecting your DocuSign account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Account] </td>
   <td> <p>Select the account that contains the envelope where you want add recipients.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Envelope ID]</td>
    <td>Select the or map the ID of the envelope where you want to add the recipient.</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[!UICONTROL Recipient type]</td>
   <td> <p> Select the type of recipient that you want to add to the envelope.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agent]</p> </li> 
     <li> <p>[!UICONTROL Carbon copy]</p> </li> 
     <li> <p>[!UICONTROL Certified delivery]</p> </li> 
     <li> <p>[!UICONTROL In-person signer]</p> </li> 
     <li> <p>[!UICONTROL Intermediary]</p> </li> 
     <li> <p>[!UICONTROL Signer]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Email]</td>
   <td> <p>Enter or map the email address of the recipient you want to add to the envelope.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Name]</td>
   <td>Enter or map the name of the recipient you want to add to the envelope.</td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Routing order]</td>
   <td> <p>Enter or map the routing number for the recipient. Routing number determines the order in which recipients receive and sign your documents.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Email body]</td>
   <td>Enter or map the body (content) of the email that is sent to the recipent.</td> 
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Email subject]</td>
   <td>Enter or map the subject of the email that is sent to the recipient.</td> 
  </tr> 
    <td role="rowheader">[!UICONTROL Private message]</td>
   <td> If you want to send a private message to the recipient, enter or map the text of the message. <p>Only the selected recipient sees the private message, as well as the general message. The private message is limited to 1000 characters.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Authentication]</td> 
   <td> <p>Select the authentication method that you want to use to confirm the recipient's identity.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL None]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Access code]</strong> </p> <p>Enter or map the access code.</p> </li> 
     <li> <p><strong>[!UICONTROL Phone]</strong> </p> <p>Enter or map the phone number.</p> </li> 
     <li> <p><strong>[!UICONTROL SMS]</strong> </p> <p>Enter or map the phone number.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a new envelope]

This action module creates a new envelope from a template. It returns the new envelope's ID, as well as the status of the new envelope.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td>

<td> <p>For instructions about connecting your DocuSign account to Workfront Fusion, see the articles under <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Create a connection - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Account] </td>
   <td> <p>Select the account that contains the envelope where you want to upload a file.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template]</td>
   <td> <p> Select the template that you want to create the new envelope from. Templates are available based on the [!UICONTROL Account] you selected.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL After creation]
   </td> 
   <td> <p>Select whether you want to save the envelope as a draft or send it for signing.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template recipients]</td>
    <td>For each recipient that you want to add to this envelope, click <b>Add item</b> and enter the following details:
    <ul>
    <li><b>Access code</b><p>Enter or map the code that the recipient uses to access the envelope.<p></li>
    <li><b>Email</b><p>Enter or map the email address of the recipient.<p></li>
    <li><b>Name</b><p>Enter or map the name of the recipient.<p></li>
    <li><b>Role name</b><p>Enter or map the role name of the recipient.<p></li>
    <li><b>Routing order</b><p>Enter or map the routing number for the recipient. Routing number determines the order in which recipients receive and sign your documents.<p></li>
    </ul>
    </td>
    </tr>
  <tr> 
   <td role="rowheader">
     [!UICONTROL Allow Print and Sign]
   </td> 
   <td> <p>Enable this option to allow the recipient to print the document and sign the paper.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Allow Reassign]
   </td> 
   <td> <p>Enable this option if you want the recipient to be able to reassign the documents to another user.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Allow Recipient Recursion]
   </td> 
   <td> <p>Enable this option to allow recipient recursion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Authoritative copy]
   </td> 
   <td> <p>Enable this option to mark the documents in this envelope as authoritative copies.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Auto Navigation]
   </td> 
   <td> <p>Enable this option to set auto navigation for the recipient.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Brand ID]
   </td> 
   <td> <p>Enter or map the ID of the brand.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Markup Enabled]
   </td> 
   <td> <p>Enable this option to enable Document Markup.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Expire Enabled]
   </td> 
   <td> <p>Enable this option to set an expiration for this envelope. If you enable this option, fill in the following fields:<ul><li><b>Expire After</b><p>Enter or map the number of days after which this envelope expires.</p></li><li><b>Expire Warning</b><p>Enter or map the number of days before expiration that a reminder email is sent to the recipient.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Body]
   </td> 
   <td> <p>Enter or map the body (content) of the email that accompanies this envelope.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Subject]
   </td> 
   <td> <p>Enter or map the subject of the email that accompanies this envelope.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call] 

This action module allows you to perform a custom API call.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL DocuSign] account to [!DNL Workfront Fusion], see <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connect [!DNL DocuSign] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Account]</td> 
   <td>Enter or map the account that you want to use to access the [!DNL DocuSign] API.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Enter or map a path relative to <code>https://&lt;BASE_URI>/v2/accounts/&lt;ACCOUNT_ID>.</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object. This determines the content type of the request.</p> <p>For example,<code> {"Content-type":"application/json"}</code></p> <p>Note: If you're getting errors and it's difficult to determine their origin, consider modifying headers based on the [!DNL Workfront] documentation. If your Custom API Call returns a 422 HTTP Request Error, try using a "Content-Type":"text/plain" header.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Add the query for the API call in the form of a standard JSON object.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Enter or map the maximum number of results to be worked with during one execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Example:** List Envelopes

The following API call returns envelopes from the specified date in your [!DNL DocuSign] account:

**URL**: `/v2.1/accounts/{accountId}/envelopes/`

**Method**: `GET`

**Query String**:

* **Key**: `from_date`

* **Value**: `YYYY-MM-DD`

Specifies when the request begins checking for status changes for envelopes in the account.

![Example Docusign setup](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)

The result can be found in the module's Output under Bundle > Body > envelopes.

In our example, 6 envelopes were returned:

![Example docusign output](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

>[!ENDSHADEBOX]

#### [!UICONTROL Download a document]

This action module downloads a single document.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL DocuSign] account to [!DNL Workfront Fusion], see <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connect [!DNL DocuSign] to [!DNL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Select the account that contains the document you want to download.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Enter or map the ID of the envelope you want to download.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Document ID]</p> </td> 
   <td> <p>Enter or map the ID of the document you want to download.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Certificate]</td> 
   <td>Enable this option to include the envelope signing certificate in the download.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents by User ID]</td> 
   <td>Enable this option to allow recipients to retrieve documents by User ID. For example, if a user is included in two different routing orders with different visibilities, using this option returns all of the documents from both routings.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encrypt]</td> 
   <td>Enable this option if you want the PDF bytes returned in the response to be encrypted for all the key managers configured on your [!DNL DocuSign] account.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Select the language.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Changes]</td> 
   <td>Enable this option to highlight any changed fields for the returned PDF are highlighted in yellow, and outline optional signatures or initials in red.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watermark]</td> 
   <td> <p>Enable this option to enable the watermark feature. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify custom field]

This action module modifies a custom field using the field name.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL DocuSign] account to [!DNL Workfront Fusion], see <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connect [!DNL DocuSign] to [!DNL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Select the account that contains the document where you want to modify a custom field.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Enter or map the ID of the envelope that contains the document where you want to modify a custom field.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field ID]</td> 
   <td>Enter or map the ID of the field you want to modify.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Enter or map the name of the field you want to modify.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Enable this option if you want the modified field to be a required field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Enable this option if you want the field to be visible.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Enter or map the value (contents) of the modified field. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read an envelope]

This action module reads information about an envelope in [!DNL DocuSign] using the envelope ID.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL DocuSign] account to [!DNL Workfront Fusion], see <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connect [!DNL DocuSign] to [!DNL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Select the account that contains the document you want to read information from.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Enter or map the ID of the envelope that contains the document you want to read information from.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Select the properties that you want to appear in the module's output. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send envelope]

This action module sends a draft envelope to its recipients.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL DocuSign] account to [!DNL Workfront Fusion], see <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connect [!DNL DocuSign] to [!DNL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Select the account that contains the draft envelope that you want to send to its recipients.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Enter or map the ID of the draft envelope that you want to send to its recipients.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file to an envelope]

This module uploads a specified file to an existing envelope in DocuSign.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL DocuSign] account to [!DNL Workfront Fusion], see <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connect [!DNL DocuSign] to [!DNL Workfront Fusion]</a> in this article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Select the account that contains the envelope where you want to upload a file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Enter or map the ID of the envelope where you want to upload a file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or enter the source file's name and data.</td> 
  </tr> 
 </tbody> 
</table>
