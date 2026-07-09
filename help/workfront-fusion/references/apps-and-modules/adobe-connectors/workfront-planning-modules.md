---
title: Adobe Workfront Planning modules
description: With the [!DNL Adobe Workfront Planning] modules, you can start an Adobe Workfront Fusion scenario based on events in your [!DNL Adobe] Workfront Planning account, create, read, or update agreements and other records, search for records using criteria you set, and upload documents.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
TQID: https://experienceleague.adobe.com/QHOFWDOT-18-c0b3wLXsRV5cjGVxlcyLhvZdkev3GFg
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# [!DNL Adobe Workfront Planning] modules

With the [!DNL Adobe Workfront Planning] modules, you can trigger a scenario when events occur in Workfront Planning. You can also create, read, update, and delete records, or perform a custom API call to your [!DNL Adobe Workfront Planning] account.

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
   <td role="rowheader">Product</td> 
   <td>
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td>
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisites

You must have the following to access Workfront Planning:

* A new Workfront package and license. Workfront Planning is not available for legacy Workfront packages or licenses.
* A Workfront Planning package.
* Your organization's instance of Workfront must be onboarded to the Adobe Unified Experience.

## Adobe Workfront Planning API information

The Adobe Workfront Planning connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td><pre><code>https://&#123;&#123;connection.host&#125;&#125;/maestro/api/&#123;&#123;common.maestroApiVersion&#125;&#125;/</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Connect Workfront Planning to Workfront Fusion 

The Workfront Planning connector uses OAuth 2.0 to connect to Workfront Planning.

You can create a connection to your Workfront Planning account directly from inside a Workfront Planning Fusion module.

* [Connect to Workfront Planning using Client ID and Client secret](#connect-to-workfront-planning-using-client-id-and-client-secret)
* [Connect to Workfront Planning using a Server-to-Server connection](#connect-to-workfront--planning-using-a-server-to-server-connection)

### Connect to Workfront Planning using Client ID and Client secret

1. In any Adobe Workfront Planning module, click **Add** next to the Connection field.
1. Fill in the following fields:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Select <b>Adobe Workfront auth</b> connection.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Enter a name for the new connection.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Enter your Workfront Client ID. This can be found in the OAuth2 Applications area of the Setup area in Workfront. Open the specific application you are connecting to to see the Client ID.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Enter your Workfront Client secret. This can be found in the OAuth2 Applications area of the Setup area in Workfront. If you do not have a Client Secret for your OAuth2 application in Workfront, you can generate another. For instructions, see the Workfront documentation.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentication URL]</td>
        <td>This can remain the default value, or you can enter the URL of your Workfront instance, followed by <code>/integrations/oauth2</code>. <p>Example: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>In most cases, this value should be <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.

   If you are not logged in to Workfront Planning, you are directed to a login screen. After you log in, you can allow the connection.

>[!NOTE]
>
>* OAuth 2.0 connections to the Workfront API no longer rely on API keys. 
>* To create a connection to a Workfront Sandbox environment, you must create an OAuth2 application in that environment, and then use the Client ID and Client Secret generated by that application in your connection. 

### Connect to Workfront  Planning using a Server-to-Server connection

1. In any Adobe Workfront Planning module, click **Add** next to the Connection field.
1. Fill in the following fields:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Select <b>Adobe Workfront Server-to-Server connection</b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Enter a name for the new connection.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance name]</td>
        <td>
          <p>Enter the name of your instance, also known as your domain.</p><p>Example: if your URL is <code>https://example.my.workfront.com</code>, enter <code>example</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance lane]</td>
        <td>
          <p>Enter the environment type that this connection will connect to.</p><p>Example: if your URL is <code>https://example.my.workfront.com</code>, enter <code>my</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Enter your Workfront Client ID. This can be found in the OAuth2 Applications area of the Setup area in Workfront. Open the specific application you are connecting to to see the Client ID.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Enter your Workfront Client secret. This can be found in the OAuth2 Applications area of the Setup area in Workfront. If you do not have a Client Secret for your OAuth2 application in Workfront, you can generate another. For instructions, see the Workfront documentation.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>Enter any applicable scopes for this connection.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>In most cases, this value should be <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.

   If you are not logged in to Workfront Planning, you are directed to a login screen. After you log in, you can allow the connection.

>[!NOTE]
>
>* OAuth 2.0 connections to the Workfront API no longer rely on API keys. 
>* To create a connection to a Workfront Sandbox environment, you must create an OAuth2 application in that environment, and then use the Client ID and Client Secret generated by that application in your connection. 

## [!DNL Adobe Workfront Planning] Version 2 modules and their fields

>[!IMPORTANT]
>
>The modules in this section belong to the Workfront Planning V2 connector.
>For modules in the Workfront Planning V1 connector, see [[!DNL Adobe Workfront Planning] Version 1 modules and their fields](#adobe-workfront-planning-version-1-modules-and-their-fields).

When you configure Workfront Planning  modules, Workfront Fusion displays the fields listed below. Along with these, additional Workfront fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

### Triggers (V2)

#### Watch Events (V2)

This trigger module starts a scenario when a record, record type, or workspace is created, updated, or deleted in Workfront Planning.

>[!IMPORTANT]
>
>You can edit this module later, which will edit the webhook.
>
>Consider the following when updating a webhook:
>
>* The edited webhook is treated by Workfront event subscriptions as a new subscription. Event subscription history is not preserved for the previous webhook configuration, because that is considered a separate event subscription.
>* The switch from old to new event subscription may not be perfectly synchronized. It is therefore possible to receive an event twice (if the new subscription begins running before the old one stops) or to miss an event (if the old subscription stops before the new one begins running). 
>
>For more information on editing webhooks, see [Edit webhooks](/help/workfront-fusion/manage-scenarios/edit-webhooks.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Select the webhook that you want to use, or click Add to create a new one.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>Select whether you want to watch records, record types, or workspaces.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>Select whether you want to watch new records, updated records, both new and updated records, or deleted records.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Configuration type]</td>
      <td>Select whether you want simple configuration or advanced configuration. <p>For more information on advanced configuration, see <a href="#example-of-advanced-logic-in-the-watch-events-module" class="MCXref xref" >Example of advanced logic in the watch Events module</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>Select whether you want to watch the old state or the new state.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Trigger a scenario when the record changes <b>to</b> a given value.</p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Trigger a scenario when the record changes <b>from</b> a given value.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>If watching records, select the Workspace you want to watch for records.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>If watching records, select the type of record you want to watch for.</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>You can set filters to watch for only records that meet criteria you select.</p> <p>For each filter, enter the field you want the filter to evaluate, the operator, and the value that you want the filter to allow. You can use more than one filter by adding AND rules.</p> <p>Note: You cannot edit filters in existing Workfront webhooks. To set up different filters for Workfront event subscriptions, remove the current webhook and create a new one.</p> <p>For more information on event filters, see <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Event subscription filters in the Workfront &gt; [!UICONTROL Watch Events] modules</a> in the Workfront modules article.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>Select whether you want to watch for new. updated, new and updated, or deleted records.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Exclude updates made by this connection]</p>
      </td>
      <td>Enable this option to prevent the scenario from triggering when a change is made by the connection used by this module. This prevents another instance of the scenario being triggered if this scenario performs a triggering action.</td> 
    </tr>
  </tbody>
</table>

For an example of using advanced logic on this module, see [Example of advanced logic in the watch Events module](#example-of-advanced-logic-in-the-watch-events-module).

### Actions (V2)


#### Create a record (V2)

This action creates a single record in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>Select the workspace where you want to create a record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Select the type of record that you want to create.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Other fields</p>
      </td>
      <td>Enter the values that you want the new record to have. These fields are based on the record type you selected, and are unique to your Workfront Planning organization.</td> 
    </tr>
  </tbody>
</table>

#### Create a field (V2)

This action module creates a new field on the specified record type.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>Select the workspace where you want to create a field.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Select the record type that you want to create a field for.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Display name</p>
      </td>
      <td>Enter or map a name for the new field.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Description</p>
      </td>
      <td>Enter or map a description for the new field.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Field type</p>
      </td>
      <td>Select the data type for the field.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Other fields</p>
      </td>
      <td>Other fields specific to the selected field type may be available. Fill in values for these fields.</td> 
    </tr>
  </tbody>
</table>

#### Create a record type (V2)

This action module creates a new record type in the selected workspace.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>Select the workspace where you want to create a record type.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Display name</p>
      </td>
      <td>Enter or map a name for the new record type.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Description</p>
      </td>
      <td>Enter or map a description for the new record type.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Icon</p>
      </td>
      <td>Map the icon that you want to use for this record type.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Color</p>
      </td>
      <td>Select the color that you want to use to represent the new record type</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Source record type</p>
      </td>
      <td>If you are using another record type to copy as a starting point, select that record type.</td> 
    </tr>
  </tbody>
</table>

#### Create a view (V2)

This action module creates a new view for the selected record type.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>Select the workspace where you want to create a view.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Select the record type that you want to create a view for.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>View name</p>
      </td>
      <td>Enter or map a name for the new view.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>View type</p>
      </td>
      <td>Select whether the new view is a table, timeline, or calendar view.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Start date field</p>
      </td>
      <td>If the view will be a timeline or calendar view, select the field that the view will use to place the record on the timeline.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>End date field.</p>
      </td>
      <td>If the view will be a timeline or calendar view, select the field that the view will use to determine the end date on the timeline.</td> 
    </tr>
  </tbody>
</table>

#### Create a workspace (V2)

This action module creates a new workspace in Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace name]</p>
      </td>
      <td>Enter or map a name for the new workspace.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Description</p>
      </td>
      <td>Enter or map a description for the new workspace/td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Color</p>
      </td>
      <td>Select the color that you want to use to represent the new record type</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Icon</p>
      </td>
      <td>Map the icon that you want to use for this record type.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Owner</p>
      </td>
      <td>Enter or map the Adobe IMS user ID of the user that you want to own the workspace.</td> 
    </tr>
  </tbody>
</table>

#### Delete a record (V2)

This action module deletes a single record, specified by ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Enter or map the ID of the record that you want to delete.</td> 
    </tr>
  </tbody>
</table>

#### Delete a record type (V2)

This action module deletes a single record type, specified by ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Enter or map the ID of the record type that you want to delete.</td> 
    </tr>
  </tbody>
</table>

#### Delete a field (V2)

This action module deletes a single field, specified by ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Field ID]</p>
      </td>
      <td>Enter or map the ID of the field that you want to delete.</td> 
    </tr>
  </tbody>
</table>

#### Delete a view (V2)

This action module deletes a single view, specified by ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL View ID]</p>
      </td>
      <td>Enter or map the ID of the view that you want to delete.</td> 
    </tr>
  </tbody>
</table>

#### Delete a workspace (V2)

This action module deletes a single workspace, specified by ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace ID]</p>
      </td>
      <td>Enter or map the ID of the workspace that you want to delete.</td> 
    </tr>
  </tbody>
</table>

#### Dismiss access requests (V2)

This action module dismisses one or more access requests, specified by ID.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resource type]</p>
      </td>
      <td>Enter or map the ID of the Workspace that you want to delete.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resource ID]</p>
      </td>
      <td>Enter or map the ID of the resource that you want to dismiss access requests for.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Request IDs]</p>
      </td>
      <td>For each access request that you want to dismiss, click <b>Add item</b> and enter the request ID.</td> 
    </tr>
  </tbody>
</table>

#### Get a record (V2)

This action module retrieves a record, specified by its ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace ID]</p>
      </td>
      <td>Enter or map the ID of the record that you want to retrieve.</td> 
    </tr>
  </tbody>
</table>

#### Get auth ID from Workfront ID (V2)

This module takes a Workfront user ID and returns the matching authorization ID that Planning uses.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workfront User ID]</p>
      </td>
      <td>Enter or map the Workfront ID of the user that you want to retrieve an authorization ID for.</td> 
    </tr>
  </tbody>
</table>

#### Get the current user's effective permissions on a resource (V2)

This module returns the current user's view, edit, delete, and add permissions for a given resource.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resource type]</p>
      </td>
      <td>Select the resource type that you want to retrieve permissions for.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resource ID]</p>
      </td>
      <td>Enter or map the ID of the resource that you want to retrieve permissions for.</td> 
    </tr>
  </tbody>
</table>

#### Get a field (V2)

This module retrieves a field by its ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Field ID]</p>
      </td>
      <td>Enter or map the ID of the field that you want to retrieve.</td> 
    </tr>
  </tbody>
</table>

#### Get a record type (V2)

#### Get a view (V2)

#### Get a workspace (V2)

#### Make a custom API call (V2)

#### Move records (V2)

#### Request access to a resource (V2)

#### Update a field (V2)

#### Update a record (V2)

#### Update a record type (V2)

#### Update a view (V2)

#### Update a workspace (V2)

### Searches (V2)

#### Get all member and their roles for a resource (V2)

#### Get all workspaces (V2)

#### Get fields by record type (V2)

#### Get global record types (V2)

#### Get record types (V2)

#### Get records by record type (V2)

#### Get views by record type (V2)

#### List pending access requests for a resource (V2)

#### Search records (V2)








## [!DNL Adobe Workfront Planning] Version 1 modules and their fields

>[!IMPORTANT]
>
>The modules in this section belong to the Workfront Planning V1 connector.
>For modules in the Workfront Planning V2 connector, see [[!DNL Adobe Workfront Planning] Version 2 modules and their fields](#adobe-workfront-planning-version-2-modules-and-their-fields).

When you configure Workfront Planning  modules, Workfront Fusion displays the fields listed below. Along with these, additional Workfront fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Actions](#actions)
* [Searches](#searches)
* [Uncategorized](#uncategorized)

### Triggers

#### Watch Events

This trigger module starts a scenario when a record, record type, or workspace is created, updated, or deleted in Workfront Planning.

>[!IMPORTANT]
>
>You can edit this module later, which will edit the webhook.
>
>Consider the following when updating a webhook:
>
>* The edited webhook is treated by Workfront event subscriptions as a new subscription. Event subscription history is not preserved for the previous webhook configuration, because that is considered a separate event subscription.
>* The switch from old to new event subscription may not be perfectly synchronized. It is therefore possible to receive an event twice (if the new subscription begins running before the old one stops) or to miss an event (if the old subscription stops before the new one begins running). 
>
>For more information on editing webhooks, see [Edit webhooks](/help/workfront-fusion/manage-scenarios/edit-webhooks.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Select the webhook that you want to use, or click Add to create a new one.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>Select whether you want to watch records, record types, or workspaces.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>Select whether you want to watch the old state or the new state.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Trigger a scenario when the record changes <b>to</b> a given value.</p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Trigger a scenario when the record changes <b>from</b> a given value.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>If watching records, select the Workspace you want to watch for records.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>If watching records, select the type of record you want to watch for.</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>You can set filters to watch for only records that meet criteria you select.</p> <p>For each filter, enter the field you want the filter to evaluate, the operator, and the value that you want the filter to allow. You can use more than one filter by adding AND rules.</p> <p>Note: You cannot edit filters in existing Workfront webhooks. To set up different filters for Workfront event subscriptions, remove the current webhook and create a new one.</p> <p>For more information on event filters, see <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Event subscription filters in the Workfront &gt; [!UICONTROL Watch Events] modules</a> in the Workfront modules article.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>Select whether you want to watch for new. updated, new and updated, or deleted records.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Exclude updates made by this connection]</p>
      </td>
      <td>Enable this option to prevent the scenario from triggering when a change is made by the connection used by this module. This prevents another instance of the scenario being triggered if this scenario performs a triggering action.</td> 
    </tr>
  </tbody>
</table>

For an example of using advanced logic on this module, see [Example of advanced logic in the watch Events module](#example-of-advanced-logic-in-the-watch-events-module).

### Actions

* [Delete a record type](#delete-a-record-type)
* [Make a custom AI call](#make-a-custom-api-call)

#### Delete a record type

This action module deletes a single record type in Workfront Planning by its ID.

>[!WARNING]
>
>Deleting a record type in Workfront Planning also deletes all records in the record type table. 

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Enter or map the ID of the record type you want to delete.</td> 
    </tr>
  </tbody>
</table>

#### Make a custom API call

This module makes a custom API call to the [!DNL Adobe Workfront Planning] API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Enter a path relative to <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Add the headers of the request in the form of a standard JSON object.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion adds authorization headers automatically.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>For each key/value pair that you want to add to the query string, click <b>Add item</b> and enter the key and value.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>


### Searches

#### Search records

This action module retrieves a list of records based on criteria you specify.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>Enter or map the Workspace that contains the records that you want to search.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Select the record type that you want to search.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record Fields]</p>
      </td>
      <td>For each field that you want to use in your search, locate that field, select the operator, and enter or map the value that you want to search for. Field are available based on the record type selected.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Condition for filters]</p>
      </td>
      <td>Select the condition for your filters:<ul><li><b>AND</b><p>The module returns records that meet <b>all</b> of the field values you selected.</p></li><li><b>OR</b><p>The module returns records that meet <b>any</b> of the field values you selected.</p></li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Limit]</p>
      </td>
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
    </tr>
  </tbody>
</table>


### Uncategorized


#### Create a record

This action creates a single record in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Enter or map the type of record you want to create. Available record types are based on your Workfront Planning account.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Other fields</p>
      </td>
      <td>Enter the values that you want the new record to have. These fields are based on the record type you selected.</td> 
    </tr>
    <tr>
  </tbody>
</table>

### Delete a record

This action module deletes the specified record in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Enter or map the ID of the record you want to delete.</td> 
    </tr>
  </tbody>
</table>

### Get a record

This action module retrieves a single record from [!DNL Adobe Workfront Planning], specified by its ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record ID]</td>
      <td>Enter or map the ID of the record you want to retrieve.</td>
    </tr>
  </tbody>
</table>

### Get records by record type

This action module retrieves all records of the specified type.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Select or map the workspace that contains the records you want to retrieve.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Select the type of record that you want to retrieve.</td>
    </tr>
    <!--
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
    -->
  </tbody>
</table>

### Get record types

This action module retrieves a list of record types in an [!DNL Adobe Workfront Planning] account.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Select or map the workspace that contains the record types you want to retrieve.</td>
    </tr>
  </tbody>
</table>

### Update record

This action updates a single record in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Enter or map the type of record you want to update . Available record types are based on your Workfront Planning account.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Other fields</p>
      </td>
      <td>Enter the new values that you want the record to have. These fields are based on the record type you selected.</td> 
    </tr>
    <tr>
  </tbody>
</table>


## Use JSONata for readable `record-types` breakdown

The following JSONata expression creates a human-readable output of the Planning query that gives you the record-types breakdown. This makes the record type name, field names, and field option names (where applicable) human readable by a name, and keeps the rest of the structure intact. 

```
(
    $s0 := ({"data":$ ~> | fields | {"options":(options){name:$}} |});
    $s1 := ({"data":$s0.data ~> | **.fields | {"options_name":(options.*){displayName:$}} | });
    $s2 := $s1 ~> | data | {"fields":(fields){displayName:$}} |; 
    $s2.data{displayName:$}
)
```

For information on using JSONata modules, see [JSONata modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/jsonata-module.md).

## Example of advanced logic in the watch Events module

This is an example of the format that advanced logic takes when using the Workfront Planning > Watch Events module.

```
[
  {
    "fieldName": "recordTypeId",
    "fieldValue": "Rt68c886502d4b5554ee80896b",
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "planning"
    },
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "active"
    },
    "comparison": "eq",
    "state": "newState"
  }
]
```

Consider the following when using advanced logic in the Watch Event module:

* The first `"fieldvalue":` entry is the Planning Record Type ID pulled from the URL. In this example, the Planning Record Type ID is `Rt68c886502d4b5554ee80896b`.
* Planning data is returned inside an array called `data `, which appears in this example as `"fieldName": "data"`.
* Planning fieldNames are returned as IDs that start with `F`.
* Because this example is evaluating against an `OR` filter connector, it has two entries for the same field (`F68c886502d4b5554eec808975`).  The two drop down options that the module is filtering against are `"planning"` and `"active"`.
