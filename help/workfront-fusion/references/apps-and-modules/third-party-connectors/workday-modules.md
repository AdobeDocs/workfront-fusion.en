---
filename: workday-modules
title: Workday modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use [!DNL Workday], as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 77237a1b-2acd-4350-9cc0-ec43b8b08137
---
# [!DNL Workday] modules

In an [!DNL Adobe Workfront Fusion] scenario, you can automate workflows that use [!DNL Workday], as well as connect it to multiple third-party applications and services.

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

To use the [!DNL Workday] modules, you must:

* Have a [!DNL Workday] account.

* Create an OAuth application in [!DNL Workday]. For instructions, see the [!DNL Workday] documentation.

## Workday API information

The Workday connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td>https://&#123;&#123;connection.servicesUrl&#125;&#125;/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.6.4</td> 
  </tr>
 </tbody> 
 </table>

## Connect [!DNL Workday] to [!DNL Workfront Fusion]

1. In any [!DNL Workfront Fusion] module, click [!UICONTROL Add] next to the [!UICONTROL Connection] field

2. Fill in the following fields:

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Connection name]</p>
                </td>
                <td>Enter a name for the connection.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Workday host]</td>
                <td>Enter the address of your [!DNL Workday] host without <code>https://</code>. For example: <code>mycompany.workday.com</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Services URL]</td>
                <td>Enter the address of your [!DNL Workday] web services without <code>https://</code>. For example: <code>mycompany-services.workday.com</code>.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Tenant name]</td>
                <td>Enter the tenant for this [!DNL Workday] account. Your tenant is your organization's identifier, and can be seen in the URL you use to log into Workday. Example: in the address <code>https://www.myworkday.com/mycompany</code>, the tenant is <code>mycompany</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Client ID]</td>
                <td>Enter the Client ID for the [!DNL Workday] application that this connection uses. You obtain this when you create the application in [!DNL Workday].</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Client Secret]</td>
                <td>Enter the Client Secret for the [!DNL Workday] application that this connection uses. You obtain this when you create the application in [!DNL Workday].</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Session timeout (min)]</td>
                <td >Enter the number of minutes after which your authorization token expires.</td>
            </tr>
        </tbody>
    </table>


3. Click [!UICONTROL Continue] to save the connection and return to the module

## [!DNL Workday] modules and their fields

When you configure [!DNL Workday] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!DNL Workday] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Action](#action)

* [Search](#search)


### Action

* [[!UICONTROL Create a record]](#create-a-record)

* [[!UICONTROL Delete a record]](#delete-a-record)

* [[!UICONTROL Make a custom API call]](#make-a-custom-api-call)

* [[!UICONTROL Update a record]](#update-a-record)


#### [!UICONTROL Create a record]

This action module creates a single record in [!DNL Workday].

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>For instructions about connecting your [!DNL Workday] account to Workfront Fusion, see <a href="#Connect" class="MCXref xref" >Connect [!DNL Workday] to [!DNL Workfront Fusion]</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record Type]</td>
            <td>Select the type of record that you want to create.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Enter or map the ID of the record you want to create.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Subresource ID]</td>
            <td >Enter or map the ID of the subresource you want to create.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL Delete a record]

This action module deletes a single record in [!DNL Workday].

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>For instructions about connecting your [!DNL Workday] account to [!DNL Workfront Fusion], see <a href="#Connect" class="MCXref xref" >Connect [!DNL Workday] to [!DNL Workfront Fusion]</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record type]</td>
            <td>Select the type of record that you want to delete.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Specific record type]</td>
            <td>Select the specific type of record that you want to delete. These are based on the record type that you chose.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Subresource ID]</td>
            <td>Enter or map the ID of the subresource you want to delete.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >Enter or map the ID of the record you want to delete.</td>
        </tr>
    </tbody>
</table>


### [!UICONTROL Make a custom API call]

This action module lets you make a custom authenticated call to the [!DNL Workday] API. This way, you can create a data flow automation that can't be accomplished by the other [!DNL Workday] modules.

When you are configuring this module, the following fields display.

The module returns the a status code, along with the headers and body of the API call.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Connection]</p> </td> 
            <td>For instructions about connecting your [!DNL Workday] account to [!DNL Workfront Fusion], see <a href="#Connect" class="MCXref xref" >Connect [!DNL Workday] to [!DNL Workfront Fusion]</a>.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Enter a path relative to <code style="color: #ff1493;">https://&lt;tenantHostname>/api/&lt;serviceName>/&lt;version>/&lt;tenant></code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] adds the authorization headers for you.</p> </td> 
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

#### [!UICONTROL Update a record]

This action module updates a single record in [!DNL Workday].

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>For instructions about connecting your [!DNL Workday] account to Workfront Fusion, see <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect [!DNL Workday] to Workfront Fusion]</a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record Type]</td>
            <td>Select the type of record that you want to update.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Enter or map the ID of the record you want to update.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Subresource ID]</td>
            <td >Enter or map the ID of the subresource you want to update.</td>
        </tr>
    </tbody>
</table>

### Search

* [[!UICONTROL Read a record]](#read-a-record)

* [[!UICONTROL List records]](#list-records)


#### [!UICONTROL Read a record]

This action module reads a single record.

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>For instructions about connecting your [!DNL Workday] account to Workfront Fusion, see <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect [!DNL Workday] to Workfront Fusion]</a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record type]</td>
            <td>Select the type of record that you want to delete.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Specific record type]</td>
            <td>Select the specific type of record that you want to read. These are based on the record type that you chose.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >Enter or map the ID of the record you want to delete.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL List records]

This search module retrieves a list of records of the specified type.

<table style="table-layout:auto"> 
      <col/>
      <col/>
      <tbody>
          <tr>
              <td role="rowheader">[!UICONTROL Connection]</td>
              <td>For instructions about connecting your [!DNL Workday] account to [!DNL Workfront Fusion], see <a href="#Connect" class="MCXref xref" >Connect [!DNL Workday] to [!DNL Workfront Fusion]</a></td>
          </tr>
          <tr>
              <td  role="rowheader">[!UICONTROL Record Type]</td>
              <td>Select the type of record that you want to retrieve.</td>
          </tr>
          <tr>
              <td role="rowheader">[!UICONTROL Limit]</td>
              <td >
                  <p>Enter or map the maximum number of records you want the module to retrieve during each scenario execution cycle.</p>
              </td>
          </tr>
      </tbody>
  </table>
