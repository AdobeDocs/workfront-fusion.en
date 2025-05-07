---
title: Adobe Authenticator module
description: With the Adobe Authenticator module, you can connect to any Adobe product with an API, using a single connection.
author: Becky
feature: Workfront Fusion
exl-id: af4da661-eeee-4033-a2bb-a2196e446a3d
---
# Adobe Authenticator modules

The Adobe Authenticator module allows you to connect to any Adobe API, using a single connection. This allows you to more easily connect to Adobe products that do not yet have a dedicated Fusion connector.

The advantage over the HTTP modules is that you can create a connection, as in a dedicated app.

To see a list of available Adobe APIs, see [Adobe APIs](https://developer.adobe.com/apis). You may be able to use only the APIs to which you are assigned.

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

* You must have access to the Adobe product that you want the module to connect to.
* You must have access to the Adobe Developer Console.
* You must have a project on the Adobe Developer Console that includes the API that you want the module to connect to. You can:

   * Create a new project with the API.

       Or
   * Add the API to an existing project.

  For information on creating or adding an API to a project on the Adobe Developer Console, see [Create a project](https://developer.adobe.com/dep/guides/dev-console/create-project/) in the Adobe documentation.

## Adobe Authenticator API information

The Adobe Authenticator connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Create a connection

An Adobe Authenticator connection connects to a single project on the Adobe Developer Console. To use the same connection for more than one Adobe API, add the APIs to the same project, and create a connection to that project.

You can create separate connections to separate projects, but you cannot use a connection to access an API that is not on the project specified in that connection.

>[!IMPORTANT]
>
>With the Adobe Authenticator connector, you have the choice between making an OAuth Server-to-server connection, or a Service Account (JWT) connection. Adobe has deprecated JWT credentials, which will stop working after January 1, 2025. **Therefore, we highly recommend creating OAuth connections.**
>
>For more information on these types of connections, see [Server to Server authentication](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/) in the Adobe documentation

To create a connection:

1. In any Adobe Authenticator module, click **Add** next to the Connection field.
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
          <p>Select whether you want to create an OAuth Server-to-Server connection, or a service account (JWT) connection. We highly recommend creating OAuth connections.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Enter a name for this connection.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Enter your [!DNL Adobe] Client ID. This can be found in the [!UICONTROL Credentials details] section of the [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Enter your [!DNL Adobe] Client Secret. This can be found in the [!UICONTROL Credentials details] section of the [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>If you have selected an OAuth connection, enter the scopes needed for this connection.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>If you have selected a JWT connection, enter your [!DNL Adobe] Technical account ID. This can be found in the [!UICONTROL Credentials details] section of the [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>If you have selected a JWT connection, enter your [!DNL Adobe] Organization ID. This can be found in the [!UICONTROL Credentials details] section of the [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>If you have selected a JWT connection, enter the meta scopes needed for this connection. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>If you have selected a JWT connection, enter the private key that was generated when your credentials were created in the [!DNL Adobe Developer Console]. </p>
          <p>To extract your private key or certificate:</p>
          <ol>
            <li value="1">
              <p>Click <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Select the type of file you are extracting.</p>
            </li>
            <li value="3">
              <p>Select the file that contains the private key or certificate.</p>
            </li>
            <li value="4">
              <p>Enter the password for the file.</p>
            </li>
            <li value="5">
              <p>Click <b>[!UICONTROL Save]</b> to extract the file and return to the connection setup.</p>
            </li>
          </ol>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Base URLs]</td>
        <td>You must add the base URLs that you want this authenticator to allow. When using the Make a custom API call module later in the scenario, you will add a relative path to the chosen URL. By entering URLs here, you can control what the Make a custom API call module can connect to, which increases security.<p>For each base URL that you want to add to the authenticator, click <b>Add item</b> and enter the base URL.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentication URL]</td>
        <td>Leave this blank to use the standard Adobe IMS authentication URL of <code>https://ims-na1.adobelogin.com</code>. If you do not use Adobe IMS for authentication, enter the URL to use for authentication.</td>
      </tr>
    </tbody>
    </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.

## Modules

* [Make a custom API call](#make-a-custom-api-call)
* [Make a custom API call (Legacy)](#make-a-custom-api-call-legacy)

### Make a custom API call 

This action module allows you to make a call to any Adobe API. It supports large files, instead of text-only bodies.

This module was made available on November 14, 2024. Any Adobe Authenticator > Make a custom API call configured before this date does not handle large files, and is now considered the Make a custom API call (Legacy) module.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>For instructions on creating a connection to the Adobe Authenticator module, see <a href="#create-a-connection" class="MCXref xref" >Create a connection</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Base URL]</p>
      </td>
      <td>
        <p>Enter the base URL of the API point you want to connect to.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Enter the path relative to the base URL.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
      </td>
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
        <p>Enter the request query string.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body Type]</td>
   <td> Select the body type for this API request:
   <ul>
   <li>Raw</li>
   <li>application/x-www-form-urlencoded</li>
   <li>multipart/form-data</li>
   </ul>
      </td>
      </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output Type]  </td>
      <td>
        <p>Select the type of data that you want the module to output. If you do not select a type, the module selects a type automatically.</p>
      </td>
    </tr>
  </tbody>
</table>

### Make a custom API call (Legacy)

This action module allows you to make a call to any Adobe API.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>For instructions on creating a connection to the Adobe Authenticator module, see <a href="#create-a-connection" class="MCXref xref" >Create a connection</a> in this article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Base URL]</p>
      </td>
      <td>
        <p>Enter the base URL of the API point you want to connect to.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Enter the path relative to the base URL.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
      </td>
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
        <p>Enter the request query string.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
