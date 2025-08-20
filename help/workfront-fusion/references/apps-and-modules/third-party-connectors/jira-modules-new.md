---
title: Jira modules
description: In an  Adobe Workfront Fusion scenario, you can automate workflows that use Jira Software, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: b74a3618-c4a1-4965-a88d-1643bfab12db
---
# Jira modules

>[!NOTE]
>
>These instructions apply to the new version of the Jira connector, which is simply labeled Jira. For instructions about the legacy Jira Cloud and Jira Server connectors, see [Jira software modules](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md).

In an  Adobe Workfront Fusion scenario, you can automate workflows that use Jira, as well as connect it to multiple third-party applications and services.

The Jira connector can be used for both Jira Cloud and Jira Data Server.

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

For information on  Adobe Workfront Fusion licenses, see [ Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

To use Jira modules you must have a Jira account.

## Connect Jira to Workfront Fusion 

You can create a connection to your Jira account directly from inside a Jira module.

>[!IMPORTANT]
>
>* To create a basic connection to Jira Data Center, you will need a Jira Personal Access Token.
>* To create a basic connection to Jira Cloud, you will need a Jira API token
>* To create an OAuth 2 connection to Jira Cloud or Jira Data Center, you will need a Jira Client ID and Client Secret.
>
>For instructions on creating any of these, see the Jira documentation.

1. In any Jira module, click **Add** next to the Connection field.
1. Configure the following fields:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Connection type</p> </td> 
      <td> <p>Select whether you are creating a basic connection or an OAuth 2 connection.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Connection name</p> </td> 
      <td> <p>Enter a name for the new connection.</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">Service URL</td>
      <td>Enter your Jira instance URL. This is the URL you use to access Jira.</td>
     </tr>
     <tr>
      <td role="rowheader">Jira account type</td>
       <td>Select whether you are connecting to Jira Cloud or Jira Data Center.</td>
     </tr>
     <tr> 
      <td role="rowheader">Client ID</td> 
      <td> <p>If you are creating an OAuth 2 connection, enter your Jira Client ID</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Client Secret</td> 
      <td> <p>If you are creating an OAuth 2 connection, enter your Jira Client Secret</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Email</td> 
      <td>If you are creating a basic connection to Jira Cloud, enter your email address.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API Token</td> 
      <td>If you are creating a basic connection to Jira Cloud, enter your API Token.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Personal Access Token</td> 
      <td>If you are creating a basic connection to Jira Data Center, enter your Personal Access Token.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API version</td> 
      <td>Select the Jira API version that you want this connection to connect to.</td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL Continue]** to create the connection and go back to the module.


## Jira modules and their fields

When you configure Jira modules, Workfront Fusion displays the fields listed below. Along with these, additional Jira fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Actions](#actions)
* [Searches](#searches)

### Triggers

#### Watch for records

This trigger module starts a scenario when a record is added, updated, or deleted.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Webhook</td> 
   <td> <p>Select the webhook that you want to use to watch for records, or create a new webhook. </p> <p>To create a new webhook:</p> 
    <ol> 
     <li>Click <strong>Add</strong></li> 
     <li>Enter a name for the webhook.</li> 
     <li> Select the connection you want to use for your webhook. <p>For instructions about connecting your Jira account to Workfront Fusion, see <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Jira to Workfront Fusion</a> in this article.</p> </li> 
     <li> <p>Select the record type that you want the software to watch for:</p> 
      <ul> 
       <li>Issue</li> 
       <li>Comment </li> 
       <li>Worklog </li> 
       <li>Project </li> 
       <li>Sprint</li> 
       <li>Attachment </li> 
      </ul> </li> 
     <li>Select one or more event types that will trigger this scenario.</li> 
     <li>Enter a Jira Query Language filter for this module.<p>For more information on JQL, see <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a> at the Atlassian help site. </p></li>
     <li>Click <b>Save</b> to save the webhook. 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [Add issue to sprint](#add-issue-to-sprint)
* [Create a Record](#create-a-record)
* [Custom API Call](#custom-api-call)
* [Delete a record](#delete-a-record)
* [Download an attachment](#download-an-attachment)
* [Read a record](#read-a-record)
* [Update a record](#update-a-record)

#### Add issue to sprint

This action module adds one or more issues to a sprint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Jira account to Workfront Fusion, see <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Jira to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sprint ID</td> 
   <td>Enter or map the Sprint ID of the sprint that you want to add an issue to.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Issue ID or keys</td> 
   <td>For each issue or key that you want to add to the sprint, click <b>Add item</b> and enter the issue ID or key. You can enter up to 50 in one module.</td> 
  </tr> 
 </tbody> 
</table>

#### Create a Record

This action module creates a new record in Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Jira account to Workfront Fusion, see <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Jira to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record Type</td> 
   <td> <p>Select the type of record you want the module to create.</p> 
    <ul> 
     <li>Attachment</li> 
     <li>Comment</li> 
     <li>Issue</li> 
     <li>Project</li> 
     <li>Sprint </li> 
     <li>Worklog</li> 
     <li>User</li> 
     <li>Board</li> 
     <li>Category</li> 
     <li>Filter</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Other fields</td> 
   <td> Fill in the other fields. Fields are available depending on the selected record type. </td> 
  </tr> 
 </tbody> 
</table>

#### Custom API Call

This action module lets you make a custom authenticated call to the Jira API. 

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Jira account to Workfront Fusion, see <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Jira to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Enter a path relative to<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Method</td> 
   td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Headers</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion adds the authorization headers for you.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Query String</td> 
   <td> <p>Add the query for the API call in the form of a standard JSON object.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Body</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### Delete a record

This action module deletes the specified record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Jira account to Workfront Fusion, see <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Jira to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record type</td> 
   <td> <p>Select the type of record you want the module to delete. </p> 
    <ul> 
     <li>Comment</li> 
     <li>Issue</li> 
     <li>Project</li> 
     <li>Sprint </li> 
     <li>Worklog</li> 
     <li>Attachment</li> 
     <li>Board</li> 
     <li>Category</li> 
     <li>Filter</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Record type)ID</td> 
   <td>Enter or map the ID or key of the record you want to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### Download an attachment

This action module downloads the specified attachment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Jira account to Workfront Fusion, see <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Jira to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td>Enter or map the ID of the attachment you want to download.</td> 
  </tr> 
 </tbody> 
</table>

#### Read a record

This action module reads data from the specified record in Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Jira account to Workfront Fusion, see <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Jira to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record Type</td> 
   <td> <p>Select the type of Jira record you want the module to read.</p> 
    <ul> 
     <li>Attachment</li> 
     <li>Comment</li> 
     <li>Issue</li> 
     <li>Project</li> 
     <li>Sprint </li> 
     <li>Worklog</li> 
     <li>User</li> 
     <li>Board</li> 
     <li>Category</li> 
     <li>Filter</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Outputs</td> 
   <td>Select the outputs that you want to receive. Output options are available based on the type of record selected in the "Record Type" field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Record type) ID</td> 
   <td> <p>Enter or map the unique Jira ID of the record that you want the module to read.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Update a record

This action module updates an existing record, such as an issue or project.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Jira account to Workfront Fusion, see <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Jira to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record Type</td> 
   <td> <p>Select the type of record you want the module to update. When you select a record type, other fields specific to that record type appear in the module.</p> 
    <ul> 
     <li>Comment</li> 
     <li>Issue</li> 
     <li>Project</li> 
     <li>Sprint </li> 
     <li>Transition issue</li> 
     <li>Category </li> 
     <li>Filter </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID or Key</td> 
   <td>Enter or map the ID or key of the record you want to update.</td> 
  <tr> 
   <td role="rowheader">Other fields</td> 
   <td> Fill in the other fields. Fields are available depending on the selected record type. </td> 
  </tr> 
 </tbody> 
</table>

### Searches 

#### Search for records

This search module looks for records in an object in Jira that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For instructions about connecting your Jira account to Workfront Fusion, see <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Jira to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Record Type</td> 
   <td> <p>Select the type of record you want the module to search for. When you select a record type, other fields specific to that record type appear in the module.</p> 
    <ul> 
     <li>Issue</li> 
     <li>Project</li> 
     <li>User</li> 
     <li>Sprint</li> 
     <li>Board</li> 
     <li>Worklog</li> 
     <li>Comment</li> 
     <li>Transition Issue</li> 
     <li>Category</li> 
    </ul> </td> 
  <tr> 
   <td role="rowheader"> <p>Max Results</p> </td> 
   <td> <p>Enter or map the maximum number of records you want the module to retrieve during each scenario execution cycle.</p> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Enter or map the ID of the first item you want to retrieve details for. This is a way to paginate the records. If you enter the 5000th item as the offset, the module would return items 5000-9999.</td> 
   </tr>
  <tr> 
   <td role="rowheader">Other fields</td> 
   <td> Fill in the other fields. Fields are available depending on the selected record type. </td> 
  </tr> 
 </tbody> 
</table>
