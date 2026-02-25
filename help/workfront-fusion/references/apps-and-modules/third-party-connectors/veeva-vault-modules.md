---
title: Veeva Vault modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Veeva Vault, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 2ef967b6-0a69-4801-8574-5f17c9ce991d
---
# Veeva Vault modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use Veeva Vault, as well as connect it to multiple third-party applications and services.

For instructions on creating a scenario, see the articles under [Create scenarios: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

## Access requirements

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
   <td role="rowheader">Adobe Workfront Fusion license</td> 
   <td>
   <p>Operation-based: No Workfront Fusion license requirement</p>
   <p>Connector-based (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

To use Veeva Vault modules, you must have a Veeva Vault account.

## Connect Veeva Vault to Workfront Fusion  

You can create a connection to your Veeva Vault account directly from inside a Veeva Vault module.

When creating a connection, you can select whether to use a password, or whether to use OAuth2 authentication.

### Connect to Veeva Vault using a username and password

1. In any Veeva Vault module, click **Add** next to the Connection field.
1. In the **Connection type** field, select `Veeva Username Password`.
1. Fill in the following fields.

    <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">Connection name</td> 
       <td> <p>Enter a name for the connection.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">Username</td>
        <td>
          <p>Enter the username for the Veeva Vault account.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Password</td>
        <td>
          <p>Enter the password for the Veeva Vault account.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">Vault DNS</td> 
       <td>Enter your Veeva Vault DNS (domain name).</p><p>To locate your Veeva Vault DNS, examine the URL that you use to access Veeva Vault.</p>For example, in the URL <code>https://my-dns.veevavault.com</code>, the DNS is <code>my-dns</code>. You do not need to enter the entire URL.</td> 
      </tr> 
     </tbody> 
    </table>

1. Click **[!UICONTROL Continue]** to create the connection and go back to the module.

### Connect to Veeva Vault using OAuth2 authentication

1. In any Veeva Vault module, click **Add** next to the Connection field.
1. In the **Connection type** field, select `Veeva Oauth 2`.
1. Fill in the following fields.

    <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">Connection name</td> 
       <td> <p>Enter a name for the connection.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader">Authorization Server Provider</td> 
       <td> <p>Select the provider that you want to use for this authentication.</p> 
       <p><b>NOTE:</b> The Veeva Vault uses Azure AD client credentials when Azure is selected as the Authorization Server Provider.</p>
       </td> 
      </tr> 
      <tr> 
       <td role="rowheader">Ping host</td> 
       <td> <p>If you are using PingFederate, enter the ping host.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">Scope</td>
        <td>
          <p>Enter the scope for this connection. The scope must be formatted as <code>{Application ID URI}/.default</code>. The application ID URI must belong to the resource or app that is exposing permissions.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Tenant ID</td>
        <td>
          <p>If you are using Azure AD/Microsoft Entra ID for your authorization server provider, enter the tenant ID for this connection.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Client ID</td>
        <td>
          <p>Enter the Client ID for the Veeva Vault application that this connection will use.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Client Secret</td>
        <td>
          <p>Enter the Client Secret for the Veeva Vault application that this connection will use.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Profile ID</td>
        <td>
          <p>Enter the ID of your OAuth2 / Open ID Connect profile.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">Vault DNS</td> 
       <td>Enter your Veeva Vault DNS (domain name).</p><p>To locate your Veeva Vault DNS, examine the URL that you use to access Veeva Vault.</p>For example, in the URL <code>https://my-dns.veevavault.com</code>, the DNS is <code>my-dns.veevavault.com</code>. </td> 
      </tr> 
      <tr>
        <td role="rowheader">Your session expiration time in minutes</td>
        <td>
          <p>Enter the expiration time of your session, in minutes..</p>
        </td>
      </tr>
     </tbody> 
    </table>

1. Click **[!UICONTROL Continue]** to create the connection and go back to the module.


## Veeva Vault modules and their fields

When you configure Veeva Vault modules, Workfront Fusion displays the fields listed below. Along with these, additional Veeva Vault fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Document](#document)
* [Object](#object)
* [Other](#other)

### Document

* [Create a single document](#create-a-single-document)
* [Create a single document relationship](#create-a-single-document-relationship)
* [Create multiple annotations](#create-multiple-annotations)
* [Create multiple documents](#create-multiple-documents)
* [Create multiple document relationships](#create-multiple-document-relationships)
* [Delete a single document](#delete-a-single-document)
* [Delete a single document relationship](#delete-a-single-document-relationship)
* [Delete multiple annotations](#delete-multiple-annotations)
* [Delete multiple document relationships](#delete-multiple-document-relationships)
* [Download a file](#download-file)
* [Export documents](#export-documents)
* [Get a single document](#get-a-single-document)
* [Get document annotations](#get-document-annotations)
* [Get document relationships](#get-document-relationships)
* [Initiate user action](#initiate-user-action)
* [List documents](#list-documents)
* [Retrieve document export results](#retrieve-document-export-results)
* [Update a single document](#update-a-single-document)
* [Update multiple annotations](#update-multiple-annotations)
* [Update multiple documents](#update-multiple-documents)

#### Create a single document

This module creates a single document, binder, or template.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to create a document, binder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Select fields</p> </td> 
   <td> <p>Select the fields that you want to enter data for, then enter the data into those fields.</td> 
  </tr> 
 </tbody> 
</table>

#### Create a single document relationship

This action module creates a relationship between two documents

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Document ID</p> </td> 
   <td> <p>Enter or map the ID of the document where you want the relationship to originate.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>Select or map the ID of the version that you want to create a relationship for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Target Document ID</p> </td> 
   <td> <p>Enter the ID of the document that the relationship points to.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Target major version</p> </td> 
   <td> <p>Enter the major version of the target document. This is the number before the point.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Target minor version</p> </td> 
   <td> <p>Enter the major version of the target document. This is the number after the point.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Relationship type</p> </td> 
   <td> <p>Enter or map the type of relationship that you want to create.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Create multiple annotations

This action module allows you to create up to 500 annotations.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Annotations</p> </td> 
   <td> <p>For each annotation you want to add, click <b>Add item</b> and fill in the data described in <a href="#annotation-fields" class="MCXref xref">Annotation fields</a> in this article.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### Annotation fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Annotation type </td> 
   <td> <p>Select the type of annotation that you want to create.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Enter or map the type of placemark that you want to use for this annotation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Page number</p> </td> 
   <td> <p>Enter or map the page number where you want this annotation to appear.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>X coordinate</p> </td> 
   <td> <p>Enter or map the X coordinate of the placemark.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Y coordinate</p> </td> 
   <td> <p>Enter or map the Y coordinate of the placemark.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Width</p> </td> 
   <td> <p>Enter or map the width of the placemark.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Height</p> </td> 
   <td> <p>Enter or map the height of the placemark.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Style</p> </td> 
   <td> <p>Enter or map the style of the placemark.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Reference</p> </td> 
   <td> <p>A reference allows the annotation to refer to an external source. For each reference that you want to add to the annotation, click <b>Add item</b> and enter the reference's type, document version ID, and an annotation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Select fields</p> </td> 
   <td> <p>Select the fields that you want to provide values for, then enter the values in each field. Available fields depend on the annotation type.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### Create multiple documents

This module creates multiple documents or templates using a CSV file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to create templates or documents.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>File data</p> </td> 
   <td> <p>Map the CSV file that will be used to create the documents.</td> 
  </tr> 
 </tbody> 
</table>

#### Create multiple document relationships

This action module configures multiple document relationships.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Input Type</p> </td> 
   <td> <p>Select the type of input that you are providing to create these relationships.</p> <ul><li>CSV</li><li>JSON</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>File data</p> </td> 
   <td> <p>If you are using a CSV file, enter or map the CSV file data.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Relationships data</p> </td> 
   <td> <p>If you are using JSON, for each relationship you want to add, click <b>Add item</b> and fill in the data described in <a href="#relationship-fields" class="MCXref xref">Relationship fields</a> in this article.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### Relationship fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Source document ID </td> 
   <td> <p>Enter or map the ID of the document where you want the relationship to originate.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Source major version</p> </td> 
   <td> <p>Enter the major version of the source document. This is the number before the point.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Source minor version</p> </td> 
   <td> <p>Enter the major version of the source document. This is the number after the point.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Target Document ID</p> </td> 
   <td> <p>Enter the ID of the document that the relationship points to.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Target major version</p> </td> 
   <td> <p>Enter the major version of the target document. This is the number before the point.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Target minor version</p> </td> 
   <td> <p>Enter the major version of the target document. This is the number after the point.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Relationship type</p> </td> 
   <td> <p>Enter or map the type of relationship that you want to create.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Delete a single document

This module deletes a single document, binder, or template.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to delete a document, binder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document ID / Binder ID / Template name</p> </td> 
   <td> <p>Select the item that you want to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### Delete a single document relationship

This action module deletes a relationship from a document

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Document ID</p> </td> 
   <td> <p>Enter or map the ID of the source document for the relationship you want to delete.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>Select or map the ID of the version that you want to delete a relationship for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Relationship ID</p> </td> 
   <td> <p>Enter or map the ID of the relationship that you want to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### Delete multiple annotations

This action module deletes annotations. The user must have permissions do delete annotations in Veeva Vault. You can delete up to 500 annotations.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Annotations</p> </td> 
   <td> <p>For each annotation you want to delete, click <b>Add item</b> and enter the following fields.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID</p> </td> 
   <td> <p>Enter or map the ID of the annotation that you want to delete.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document version ID</p> </td> 
   <td> <p>Enter or map the document's version number that contains the annotation that you want to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### Delete multiple document relationships

This action module deletes relationships from multiple documents

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Input Type</p> </td> 
   <td> <p>Select the type of input that you are providing to delete these relationships.</p> <ul><li>CSV</li><li>JSON</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>File data</p> </td> 
   <td> <p>If you are using a CSV file, enter or map the CSV file data.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Relationships data</p> </td> 
   <td> <p>If you are using JSON, for each relationship you want to add, click <b>Add item</b> and enter the relationship ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Download file

This module downloads a document, document version, or template from Veeva Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to download a document or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Download Type</p> </td> 
   <td> <p>Select whether you want to download a document or document version.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document ID / Template name</p> </td> 
   <td> <p>Enter or map the ID of the document or the name of the template you want to download.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Check out document</p> </td> 
   <td> <p>If you are downloading a document, enable this option to check out the document before you download it.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>If you are downloading a document version, select the version to download.</td> 
  </tr> 
 </tbody> 
</table>

#### Export documents

This module exports documents you specify, including sources, renditions, and text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to delete a document, binder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Source</p> </td> 
   <td> <p>Enable this option to include source files in the export.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Renditions</p> </td> 
   <td> <p>Enable this option to include renditions files in the export.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>All versions</p> </td> 
   <td> <p>Enable this option to include all versions of the document files in the export.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Text</p> </td> 
   <td> <p>Enable this option to include source document text in the export.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Get a single document

This module retrieves metadata for a single document, binder, or template.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to retrieve data for a document, binder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document ID / Binder ID / Template name</p> </td> 
   <td> <p>Select the fields that you want to retrieve data for.</td> 
  </tr> 
 </tbody> 
</table>

#### Get document annotations

This module retrieves annotations from a specific document version. You can retrieve all annotations or choose to retrieve only certain annotation types.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Document ID</p> </td> 
   <td> <p>Select or map the document that you want to retrieve annotations for. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>Select or map the ID of the version that you want to retrieve annotations for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned annotations</td> 
   <td>Enter or map the maximum number of annotations you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

#### Get document relationships

This module retrieves all relationships for a document.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Document ID</p> </td> 
   <td> <p>Select or map the document that you want to retrieve relationships for. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>Select or map the ID of the version that you want to retrieve relationships for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned relationships</td> 
   <td>Enter or map the maximum number of relationships you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

#### Initiate user action

This module initiates actions on documents and binder, such as sending a document for review or changing its state.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to perform an action on a document or a binder.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document / Binder</p> </td> 
   <td> <p>Select the document or binder that you want to perform the action on.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document version/ Binder version</p> </td> 
   <td> <p>Select the document or binder that you want to perform the action on.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Action</p> </td> 
   <td> <p>Select the action to perform on the document or binder.</td> 
  </tr> 
 </tbody> 
</table>

#### List documents

This module lists all documents of the selected type.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to list documents, binders, or templates.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

#### Retrieve document export results

This module returns the results of a previously requested document export.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Job ID</p> </td> 
   <td> <p>Enter or map the ID of the job that you want to return results for. </p> </td> 
  </tr> 
  </tbody> 
</table>

#### Update multiple annotations

This action module updates up to 500 annotations.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Annotations</p> </td> 
   <td> <p>For each annotation you want to update, click <b>Add item</b> and fill in the data described in <a href="#annotation-fields" class="MCXref xref">Annotation fields</a> in this article.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### Update multiple documents

This module updates multiple documents or templates using a CSV file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to create templates or documents</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>File data</p> </td> 
   <td> <p>Map the CSV file that will be used to create the documents.</td> 
  </tr> 
 </tbody> 
</table>

#### Update a single document

This module updates a single document, binder, or template.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to create a document, document version, binder, or template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID / Name</p> </td> 
   <td> <p>If you are updating a template, enter a new name for the template.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>New template Name</p> </td> 
   <td> <p>Enter or map the ID or name of the object that you want to update.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>Select fields</p> </td> 
   <td> <p>Select the fields that you want to enter data for, then enter the data into those fields.</td> 
  </tr> 
 </tbody> 
</table>

### Object

* [Create a single object record](#create-a-single-object-record)
* [Delete a single object record](#delete-a-single-object-record)
* [Get a single object](#get-a-single-object)
* [List objects records](#list-objects-records)
* [Update a single object record](#update-a-single-object-record)

#### Create a single object record

This module creates, copies, or deep copies a single object record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether to create or copy a record, or whether to deep copy a record.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Migration mode</td> 
   <td>If creating or copying a record, enable this option to create or update object records in a noninitial state and with minimal validation, create inactive records, and set standard and system-managed fields such as <code>createdby_v</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">No triggers</td> 
   <td>If set to true and migration mode is enabled, the module bypasses all system, standard, custom SDK triggers, and Action Triggers.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Object name</td> 
   <td>Enter or map the object name__v field value, such as <code>product__v</code>, <code>country__v</code>, or <code>custom_object__c</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record ID</td> 
   <td>If you are deep copying a record, select the record to copy.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record fields</td> 
   <td>If you are deep copying a record, select the fields that you want to provide values for, then provide those values.</td> 
  </tr> 
 </tbody> 
</table>

#### Delete a single object record

This module deletes or cascade deletes a single object record. Cascade deleting a record deletes the record and all its child objects.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether to delete a record, or cascade delete a record.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Object name</td> 
   <td>Select the object that you want to delete.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record ID</td> 
   <td>Select the ID of the record you want to delete.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">External ID</td> 
   <td>Instead of Record ID, you can use this user-defined document external ID.</td> 
  </tr> 
 </tbody> 
</table>

#### Get a single object  

This module retrieves metadata configured on a specific object record in your Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Object name</td> 
   <td>Select the object that you want to retrieve metadata for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record ID</td> 
   <td>Select the ID of the record you want to retrieve metadata for.</td> 
  </tr> 
 </tbody> 
</table>

#### List objects records

This module retrieves all Vault objects in the authenticated Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Retrieve localized labels</p> </td> 
   <td> <p>Select Yes to retrieve localized (translated) strings for the label and label_plural object fields.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Update a single object record-->

This module updates fields in an existing object record.

This module creates, copies, or deep copies a single object record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether to create or copy a record, or whether to deep copy a record.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Migration mode</td> 
   <td>Enable this option to create or update object records in a noninitial state and with minimal validation, create inactive records, and set standard and system-managed fields such as <code>createdby_v</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">No triggers</td> 
   <td>If migration mode is enabled, you can enable this option to bypass all system, standard, custom SDK triggers, and Action Triggers.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Object name</td> 
   <td>Enter or map the object name__v field value, such as <code>product__v</code>, <code>country__v</code>, or <code>custom_object__c</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record ID</td> 
   <td>Select the ID of the record to update.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">State</td> 
   <td>Specify the lifecycle state of the record when <code>X-VaultAPI-MigrationMode</code> is set to true.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">State label</td> 
   <td>Specify the lifecycle state type of the record when <code>X-VaultAPI-MigrationMode</code> is set to true. Use the format <code>base:object_lifecycle:</code> followed by the object state type.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record fields</td> 
   <td>If you are deep copying a record, select the fields that you want to provide values for, then provide those values.</td> 
  </tr> 
 </tbody> 
</table>

### Other

* [Make a custom API call](#make-a-custom-api-call)
* [Make a VQL query](#make-a-vql-query)
* [Read logs](#read-logs)

#### Make a custom API call

This action module makes a custom call to the Veeva Vault API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Enter a path relative to <code>baseurl/api/v</code>.  For example: <code>/objects/documents</code>. Do not include <code>baseurl/api/v/</code>, as it is already included.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Method</td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Headers</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion adds the authorization headers for you.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Query String</td> 
   <td> <p>Add the query for the API call in the form of a standard JSON object.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Body</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Make a VQL query

This module makes a query using Vault Query Language (VQL).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Select whether you want to create templates or documents</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>File data</p> </td> 
   <td> <p>Map the CSV file that will be used to create the documents.</td> 
  </tr> 
 </tbody> 
</table>

#### Read logs

This module returns data from audit trails

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection </td> 
   <td> <p>For instructions about connecting your Veeva Vault account to Workfront Fusion, see <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Connect Veeva Vault to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Audit type</p> </td> 
   <td> <p>Select the audit type that you want to retrieve data for.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Start date</p> </td> 
   <td> <p>Enter or map the start date for the audits that you want to retrieve.</p><p>For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>End date</p> </td> 
   <td> <p>Enter or map the end date for the audits that you want to retrieve.</p><p>For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Result URL </p> </td> 
   <td> <p>Select CSV if you want to get URL to download a CSV of the result.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum number of returned results</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>
