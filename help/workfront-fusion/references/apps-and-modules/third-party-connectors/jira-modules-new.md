---
title: Jira modules
description: In an  Adobe Workfront Fusion scenario, you can automate workflows that use Jira Software, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
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

Your connection method is based on whether you are using Jira Cloud or Jira Server.

* [Connect Jira Cloud to Workfront Fusion](#connect-jira-cloud-to-workfront-fusion)
* [Connect Jira Server to Workfront Fusion](#connect-jira-server-to-workfront-fusion)

### Connect Jira Cloud to Workfront Fusion

Connect Jira Cloud to Workfront Fusion

To connect Jira to Workfront Fusion, you must create an API token and insert it together with your Service URL and Username to the Create a connection field in Workfront Fusion.

#### Create an API token in Jira 

1. Create an API token in Jira.

   For instructions, we recomments searching for "Create an API token" in the Jira documentation.
1. After creating the token, copy the token to a secure location.

   >[!IMPORTANT]
   >
   >You can't view the token again after closing this dialog.
1. Store the generated token in a safe place.
1. Continue with [Configure the Jira API token in Workfront Fusion](#configure-the-jira-api-token-in-workfront-fusion).

#### Configure the Jira API token in Workfront Fusion 

1. In any Jira Cloud module in Workfront Fusion, click **Add** next to the connection field.
1. Specify the following information:

   * **Environment**
   * **Type**
   * **Service URL:** This is the base URL that you use to access your Jira account. Example: `yourorganization.atlassian.net`
   * **Username**
   * **API token:**&nbsp;This is the API token you created in the [Create an API token in Jira](#create-an-api-token-in-jira) section of this article.

1. Click Continue to create the connection and return to the module.

### Connect Jira Server to Workfront Fusion

To authorize a connection between Workfront Fusion and Jira Server, you need your Consumer Key, Private Key, And Service URL. You may need to contact your Jira administrator for this information.

* [Generate Public and Private keys for your Jira connection](#generate-public-and-private-keys-for-your-jira-connection)
* [Configure the client app as a consumer in Jira](#configure-the-client-app-as-a-consumer-in-jira)
* [Create a connection to Jira Server or Jira Data Center in] Workfront Fusion(#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Generate Public and Private keys for your Jira connection 

To acquire a private key for your Workfront Fusion Jira connection, you need to generate public and private keys. This is done through your computer's terminal. You can locate your terminal by searching for terminal in your start menu or computer search bar (not your browser search bar.)

1. In your terminal, run the following `openssl` commands.

   * `openssl genrsa -out jira_privatekey.pem 1024`

      This command generates a 1024 bit private key.

   * `openssl req -newkey rsa:1024 -x509 -key jira_privatekey.pem -out jira_publickey.cer -days 365`

      This command creates an X509 certificate.

   * `openssl pkcs8 -topk8 -nocrypt -in jira_privatekey.pem -out jira_privatekey.pcks8`

      This command extracts the private key (PKCS8 format) to the `jira_privatekey.pcks8` file.

   * `openssl x509 -pubkey -noout -in jira_publickey.cer  > jira_publickey.pem`

      This command extracts the public key from the certificate to the `jira_publickey.pem` file.

      >[!NOTE]
      >
      >If you are using Windows, you may need to save the public key to the `jira_publickey.pem` file manually:
      >
      >1. In your terminal, run the following command:
      >   
      >   `openssl x509 -pubkey -noout -in jira_publickey.cer`
      >   
      >1. Copy the terminal output, including `-------BEGIN PUBLIC KEY--------` and `-------END PUBLIC KEY--------`.
      >   
      >1. Paste the terminal output into a file named `jira_publickey.pem`.


1. Continue to [Configure the client app as a consumer in Jira](#configure-the-client-app-as-a-consumer-in-jira)

#### Configure the client app as a consumer in Jira 

1. Log in to your Jira instance.
1. In the left navigation panel, click **Jira Settings** ![Jira settings icon](/help/workfront-fusion/references/apps-and-modules/assets/jira-settings-icon.png) > **Applications**> **Application links**.
1. In the **Enter the URL of the application you want to link** field, enter

   ```
   https://app.workfrontfusion.com/oauth/cb/workfront-jiraserver-oauth1
   ```

1. Click **Create new link**. Ignore the "No response was received from the URL you entered" error message.
1. In the **Link applications** window, enter values into the **Consumer key** and **Shared secret** fields.

   You can choose the values for these fields.

1. Copy the values of the **Consumer key** and **Shared secret** fields to a secure location.

   You will require these values later in the configuration process.

1. Fill in the URL fields as follows:

   | Field | Description |
   |---|---|
   | Request Token URL | `<Jira base url>/plugins/servlet/oauth/request-token` |
   | Authorization URL | `<Jira base url>/plugins/servlet/oauth/authorize` |
   | Access Token URL | `<Jira base url>/plugins/servlet/oauth/access-token` |

1. Select the **Create incoming link** checkbox.
1. Click **Continue**.
1. In the **Link applications** window, fill in the following fields:

   <table style="table-layout:auto"> 
    <col data-mc-conditions=""> 
    <col data-mc-conditions=""> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Consumer Key</p> </td> 
      <td> Paste in the consumer key that you copied to a secure location.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Consumer name</td> 
      <td>Enter a name of your choice. This name is for your own reference.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Public key</td> 
      <td>Paste in the public key from your <code> jira_publickey.pem</code> file.</td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Continue**.
1. Continue to [Create a connection to Jira Server or Jira Data Center in Workfront Fusion](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Create a connection to Jira Server or Jira Data Center in Workfront Fusion 

>[!NOTE]
>
>Use the Jira Server app to connect to Jira Server or Jira Data Center.

1. In any Jira Server module in Workfront Fusion, click **Add** next to the connection field.
1. In the Create a connection panel, fill in the following fields:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Connection name</p> </td> 
      <td> <p>Enter a name for the connection.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Environment</p> </td> 
      <td> <p>Select whther you are using a production or non-production environment.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Type</p> </td> 
      <td> <p>Select whether you are using a service account or a personal account.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Consumer Key</td> 
      <td>Paste in the consumer key that you copied to a secure location in <a href="#configure-the-client-app-as-a-consumer-in-jira" class="MCXref xref">Configure the client app as a consumer in Jira</a></td> 
     </tr> 
     <tr> 
      <td role="rowheader"> Private Key</td> 
      <td>Paste in the private key from the <code> jira_privatekey.pcks8</code> file you created in <a href="#generate-public-and-private-keys-for-your-jira-connection" class="MCXref xref">Generate Public and Private keys for your Jira connection</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> Service URL</td> 
      <td>Enter your Jira instance URL. Example: <code>yourorganization.atlassian.net</code></td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Continue** to create the connection and go back to the module.

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
