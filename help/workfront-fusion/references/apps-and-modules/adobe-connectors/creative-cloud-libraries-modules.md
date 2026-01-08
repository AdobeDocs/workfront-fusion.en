---
title: Adobe Creative Cloud Libraries modules
description: With the [!DNL Adobe Workfront Fusion Adobe Creative Cloud] Libraries modules, you can start a scenario when an element or library is created or updated. You can also upload, retrieve, archive, or list elements, or make a call to the [!DNL Adobe Creative Cloud Libraries] API.
author: Becky
feature: Workfront Fusion
exl-id: 85607e4e-538a-427f-8a99-a0ab65a75ac2
---
# Adobe Creative Cloud Libraries Modules

With the Adobe Workfront Fusion [!DNL Adobe Creative Cloud Libraries] modules, you can start a scenario when an element or library is created or updated. You can also upload, retrieve, archive, or list elements, or make a call to the [!DNL Adobe Creative Cloud Libraries] API.

If you need instructions on creating a scenario, see the articles under [Create a scenario: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

>[!IMPORTANT]
>
>Connection creation is currently not available in the Creative Cloud Libraries connector. Existing connections work as expected.

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

To use [!DNL Adobe Creative Cloud Libraries] modules, you must have an [!UICONTROL Adobe Creative Cloud] account.

## Adobe Creative Cloud Libraries API information

The Adobe Creative Cloud Libraries connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td>https://cc-libraries.adobe.io/api/v1</td> 
  </tr>
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.1.7</td> 
  </tr>
 </tbody> 
 </table>

## [!UICONTROL Adobe Creative Cloud Libraries] modules and their fields

When you configure [!UICONTROL Adobe Creative Cloud Libraries] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Adobe Creative Cloud Libraries] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Elements](#elements)

* [Libraries](#libraries)

* [Other](#other)


### Elements

* [[!UICONTROL Archive an Element]](#archive-an-element)

* [[!UICONTROL Get an Element]](#get-an-element)

* [[!UICONTROL List Elements]](#list-elements)

* [[!UICONTROL Upload an Element]](#upload-an-element)

* [!UICONTROL [Watch New Element in Library]](#watch-new-element-in-library)

* [[!UICONTROL Watch Updated Elements]](#watch-updated-elements)


#### [!UICONTROL Archive an Element]

This action module archives an element from a library.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Select an existing Creative Cloud Libraries connection. Connection creation is currently not available in the Creative Cloud Libraries connector. Existing connections work as expected.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Select or map the library that contains the element you want to archive.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Element ID]</td>
      <td>Select or map the element that you want to archive.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an Element]

This action module returns a single element from a library.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Select an existing Creative Cloud Libraries connection. Connection creation is currently not available in the Creative Cloud Libraries connector. Existing connections work as expected.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td>Select or map the library that contains the element you want to retrieve.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Element ID]</td>
      <td>Enter or map the ID of the element that you want to retrieve.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selector]</td>
      <td>
        <p>Select the type of information that the module returns. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL Default]</b>
            </p>
            <p>Base data</p>
          </li>
          <li>
            <p><b>[!UICONTROL Details]</b>
            </p>
            <p>All available data</p>
          </li>
          <li>
            <p><b>[!UICONTROL Representations]</b>
            </p>
            <p>A flattened list of assets associated with the library element</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Elements]

This action module retrieves a list of elements in a library.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Select an existing Creative Cloud Libraries connection. Connection creation is currently not available in the Creative Cloud Libraries connector. Existing connections work as expected.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Select or map the library that you want to list elements from.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Order by]</td>
      <td>Select whether you want to order results by name, or by the last date the element was modified.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Type]</td>
      <td >Enter or map a MIME type to limit results to elements identified with the specified MIME type. Example: <code>string</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selector]</td>
      <td>
        <p>Select the type of information that the module returns. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL Default]</b>
            </p>
            <p>Base data</p>
          </li>
          <li>
            <p><b>[!UICONTROL Details]</b>
            </p>
            <p>All available data</p>
          </li>
          <li>
            <p><b>[!UICONTROL Representations]</b>
            </p>
            <p>A flattened list of assets associated with the library element</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Watch New Element in Library]

This trigger module starts a scenario when an element is added to a library.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Select an existing Creative Cloud Libraries connection. Connection creation is currently not available in the Creative Cloud Libraries connector. Existing connections work as expected.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Select the library that you want to watch for updated elements.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL Watch Updated Elements]

This trigger module starts a scenario when an element in a library is updated.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Select an existing Creative Cloud Libraries connection. Connection creation is currently not available in the Creative Cloud Libraries connector. Existing connections work as expected.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Select the library that you want to watch for new elements.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
  </tbody>
</table>

### Libraries

* [[!UICONTROL Watch New Libraries]](#watch-new-libraries)

* [[!UICONTROL Watch Updated Libraries]](#watch-updated-libraries)


#### [!UICONTROL Watch New Libraries]

This trigger module starts a scenario when a new library is created.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Select an existing Creative Cloud Libraries connection. Connection creation is currently not available in the Creative Cloud Libraries connector. Existing connections work as expected.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Watch Updated Libraries]

This trigger module starts a scenario when an existing library is updated.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Select an existing Creative Cloud Libraries connection. Connection creation is currently not available in the Creative Cloud Libraries connector. Existing connections work as expected.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
  </tbody>
</table>

### Other

* [Make an API Call](#make-an-api-call)
* [Upload an Asset](#upload-an-asset)

#### [!UICONTROL Make an API Call]

This module makes a custom API call to the [!DNL Adobe Creative Cloud Libraries] API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>For instructions about connecting your Adobe Creative Cloud account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions.</a></p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Enter a path relative to <code>https://cc-libraries.adobe.io/api</code>.</p>
    <p>For example <code>/v1/libraries</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL API version]</td>
      <td>
        <p>Select the version of the [!DNL Adobe Analytics] API that you want to connect to.</p>
      </td>
    </tr>    <tr>
      <td role="rowheader">[!UICONTROL Method]</td>
      <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP request methods</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Add the headers of the request in the form of a standard JSON object.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion adds the authorization headers for you.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]</td>
      <td>
        <p>Add the query for the API call in the form of a standard JSON object.</p>
        <p>For example: <code>{"name":"something-urgent"}</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
       <tr>
      <td role="rowheader">[!UICONTROL Upload a transient document]</td>
      <td>
      <p>If you want to upload a transient document, enter the source file for the document you want to upload.</p>
      <p>Select a source file from a previous module, or map the source file's name and data.</p>
    </td>
    </tr>
</tbody>
</table>


#### [!UICONTROL Upload an Asset]

This action module uploads a small file asset to an existing library. Maximum file size is 1 GB.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Select an existing Creative Cloud Libraries connection. Connection creation is currently not available in the Creative Cloud Libraries connector. Existing connections work as expected.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Select the library that you want to upload an asset to.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Invocation Mode]</td>
      <td>
        <p>Select the processing mode to invoke this request process with.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL sync]</b>
            </p>
            <p>The API call is processed synchronously. The response is delivered when processing is complete (unless the call times out.)</p>
          </li>
          <li>
            <p><b>[!UICONTROL async]</b>
            </p>
            <p>The async monitor response is immediately returned, and request processing occurs asynchronously. The calling is responsible for polling the endpoint until completion.</p>
          </li>
          <li>
            <p><b>[!UICONTROL sync,async]</b> (Default)</p>
            <p>Synchronous processing of the request is attempted. When the processing extends past 5000 ms, the async monitor response is returned. The monitor URL should be polled until the request is complete.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Element Type]</td>
      <td >Select the type of element that you want to upload</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File Type]</td>
      <td >Enter or map the MIME type of the uploaded file.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Source File]</td>
      <td>
        <p>Select a source file from a previous module, or map the source file's name and data.</p>
      </td>
    </tr>
  </tbody>
</table>





