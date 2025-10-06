---
title: SOAP module
description: You can use the SOAP module to connect to SOAP APIs in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
---
# [!UICONTROL SOAP] module

You can use the [!UICONTROL SOAP] module to connect to [!UICONTROL SOAP] APIs in [!UICONTROL Adobe Workfront Fusion].

## SOAP module and its fields

The SOAP connector includes only one module, Execute SOAP action

### Execute SOAP action

This action module executes the specified SOAP action.



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

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## SOAP module and its fields

When you configure SOAP modules, Workfront Fusion displays the fields listed below.  A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Execute SOAP action

This action module executes a SOAP action, based on WSDL you specify.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL WSDL]</td> 
   <td> Select the WSDL that you want the module to use. To create a WSDL, click <b>Add</b> next to the field and fill in the fields. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTTP headers]</td> 
   <td> For each HTTP header that you want to add, click <b>Add item</b> and enter the header's name and value.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL SOAP headers]</td> 
   <td> For each SOAP header that you want to add, click <b>Add item</b> and enter the header's name, value, namespace, and XMLNS.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Force SOAP headers]</td> 
   <td> Enable this option to configure headers for SOAP 1.2. </td> 
  </tr> 
  </tbody> 
</table>

## Limitations of the [!UICONTROL SOAP] module

>[!NOTE]
>
>Redirects are disabled during WDSL loading. This is a security feature, but may mean that unverified redirects are blocked when the module is run.

The [!UICONTROL SOAP] module is currently in beta and does not support:

* Redefine elements
* Fraction digits restrictions
* Total digits restrictions
* White space restrictions
* Multiple parts in input and output messages. Only single part messages are supported
* Custom XML Schema elements defined with the help of SOAP Encoding schemas and elements.

>[!BEGINSHADEBOX]

**Example:** 
  
The following would not be recognized correctly by [!UICONTROL Workfront Fusion]:

```
<complexType name="ArrayOfFloat">
   <complexContent>
      <restriction base="soapenc:Array">
         <attribute ref="soapenc:arrayType"
            wsdl:arrayType="xsd:integer[]"/>
      </restriction>
   </complexContent>
</complexType>
```

This example includes the `soapenc:Array`, `soapenc:arrayType` and `wsdl:arrayType` references, which are not yet supported in [!UICONTROL Workfront Fusion].

>[!ENDSHADEBOX]

## Workaround

If the [!UICONTROL SOAP] module refuses to process the WSDL file or throws various errors in the module's configuration, you may try using the universal **[!UICONTROL HTTP] > [!UICONTROL Make a request]** module instead:

1. In Workfront Fusion, create a new scenario.
1. Insert the **[!UICONTROL HTTP] > [!UICONTROL Make a request]** module in the scenario.
1. Open the module's configuration and fill in the following fields:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Method]</td> 
      <td> <p>[!UICONTROL POST]</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td role="rowheader">[!UICONTROL Body type]</td> 
      <td> <p>[!UICONTROL Raw]</p> </td>
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Content type]</td> 
      <td> <p>[!UICONTROL XML (application/xml)]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Parse response]</td> 
      <td>[!UICONTROL Enabled]</td> 
     </tr> 
    </tbody> 
   </table>

   <!--![Workaround](/help/workfront-fusion/references/apps-and-modules/assets/workaround-350x443.png)-->

1. Open a new web browser window or tab.
1. Paste the WSDL URL into the web browser's address bar and fetch the XML file.

   The WSDL URL usually ends with `?wsdl`, but not necessarily, for example `http://voip.ms/api/v1/server.wsdl`.

1. If the WSDL file does not display directly in the web browser, open the downloaded file in a text editor.
1. Search for the `<service>` or `<wsdl:service>` tag:

   <!--![Service](/help/workfront-fusion/references/apps-and-modules/assets/service-350x65.png)-->

1. Once located, copy the URL from the `location` attribute.
1. In Workfront Fusion, paste the URL into the HTTP module's **Request content** field.
1. Provide values for selected parameters by replacing the question marks with actual values.

   >[!NOTE]
   >
   > To get specific values from the WSDL file, use an online WSDL viewer.

   <!--![Request](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. Close the module's configuration by clicking **[!UICONTROL OK]**.
1. Execute the scenario or module.
