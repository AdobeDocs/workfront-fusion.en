---
title: Datadog modules
description: In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use Datadog, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
---
# [!DNL Datadog] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Datadog], as well as connect it to multiple third-party applications and services.

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

To use [!DNL Datadog] modules, you must have a [!DNL Datadog] account.

## Datadog API information

The Datadog connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>1.0.11</td> 
  </tr>
 </tbody> 
 </table>

## Connect [!DNL Datadog] to [!DNL Workfront Fusion] {#connect-datadog-to-workfront-fusion}

### Retrieve your API key and application key {#retrieve-your-api-key-and-application-key}

To connect your [!DNL Datadog] account to [!DNL Workfront Fusion] you need to retrieve an API Key and an application key from your [!DNL Datadog] account.

1. Log in to your [!DNL Datadog] account.
1. In the left navigation panel, click **[!UICONTROL Integrations]**, then click **[!UICONTROL APIs]**.
1. On the main screen, click **[!UICONTROL API Keys]**.
1. Hover over the purple bar to reveal the API key.
1. Copy the API key to a secure location.
1. On the main screen, click **[!UICONTROL Application Keys]**.
1. Hover over the purple bar to reveal the application key.
1. Copy the application key to a secure location.

### Create a connection to [!DNL Datadog] in [!DNL Workfront Fusion]

You can create a connection to your [!DNL Datadog] account directly from inside a [!UICONTROL Datadog] module.

1. In any [!UICONTROL Datadog] module, click **[!UICONTROL Add]** next to the [!UICONTROL Connection] field.
1. Fill the module's fields as follows:

    <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection Name]</td> 
      <td> <p> Enter a name for the connection.</p> </td> 
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
      <td role="rowheader">[!UICONTROL Domain] </td> 
      <td> <p>Select the domain you want to connect to (US or EU).</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key Location] </td> 
      <td> <p>Select whether to include the API key in the header or in the query string.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td> <p> Enter your [!DNL Datadog] API key. </p> <p>For instructions on retrieving the API key, see <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">Retrieve your API key and application key</a> in this article.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL Continue]** to create the connection and go back to the module.

## [!DNL Datadog] modules and their fields

When you configure [!DNL Datadog] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Datadog] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Actions

* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Post Timeseries Points]](#post-timeseries-points)

#### [!UICONTROL Make an API Call]

This action module allows you to perform a custom API call.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Datadog] account to [!DNL Workfront Fusion], see <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Connect [!DNL Datadog] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Dedicated Domain]</td> 
   <td>Some of Datadog API endpoints which expect a lot of incoming traffic are running on thier dedicated domains. Check this box to use the dedicated domain for your API call.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Enter a path relative to <code>https://api.datadoghq.com/api/</code>. Example:<code> /v1/org</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion adds the authorization headers for you.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Add the query for the API call in the form of a standard JSON object.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
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

**Example:** The following API call returns the all dashboards in your [!DNL Datadog] account:

URL: `/v1/dashboard`

Method: `GET`

![Datadog API call example](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-example.png)

The result can be found in the module's Output under Bundle > Body > dashboards.

In our example, 3 dashboards were returned:

![Datadog API response](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-response-example.png)

#### [!UICONTROL Post Timeseries Points]

The module allows you to post time-series data that can be graphed on [!DNL Datadog]'s dashboards.

The limit for compressed payloads is 3.2 megabytes (3200000), and 62 megabytes (62914560) for decompressed payloads.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Datadog] account to [!DNL Workfront Fusion], see <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Connect [!DNL Datadog] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> Select the type of metric you want to use. 
   <ul>
   <li>Gauge</li>
   <li>Rate</li>
   <li>Count</li>
   </ul>
   </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL Interval]</td> 
   <td> If the type of the metric is rate or count, define the corresponding interval.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Points]</td> 
   <td><p>Add points relating to a metric.</p> <p>This is a JSON array of points. Each point has the format: <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>Note:  <p>The timestamp must be in seconds.</p> <p>The timestamp must be current. Current is defined as not more than 10 minutes in the future or more than 1 hour in the past.</p> <p> The numeric value format should be a float value.</p> </p> <p>This field must contain at least 1 item.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Host]</td> 
   <td>Enter the name of the host that produced the metric. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> For each tag that you want to add to the metric, click <b>Add item</b> and enter the tag's value.</td> 
  </tr> 
 </tbody> 
</table>
