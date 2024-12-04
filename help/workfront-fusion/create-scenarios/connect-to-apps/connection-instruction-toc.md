---
title: Create connections in [!DNL Adobe Workfront Fusion]
description: A connection must adhere to the requirements set by the API of the app or web service it connects to. For this reason, instructions for setting up a connection vary based on the app or web service. This article can help you identify and locate the instructions for connecting [!DNL Adobe Workfront Fusion] to your chosen app or web service.
author: Becky
feature: Workfront Fusion
---
# Create connections in [!DNL Adobe Workfront Fusion]

A connection must adhere to the requirements set by the API of the app or web service it connects to. For this reason, instructions for setting up a connection vary based on the app or web service. This article can help you identify and locate the instructions for connecting [!DNL Adobe Workfront Fusion] to your chosen app or web service.

## Access requirements 

 You must have the following access to use the functionality in this article: 

 <table style="table-layout:auto"> 
 <col>  
 <col>  
 <tbody>  
  <tr>  
   <td role="rowheader">[!DNL Adobe Workfront] plan</td>  
   <td> <p>Any</p> </td>  
  </tr>  
  <tr data-mc-conditions="">  
   <td role="rowheader">[!DNL Adobe Workfront] license</td>  
   <td> <p>New: [!UICONTROL Standard]</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p> </td>  
  </tr>  
  <tr>  
   <td role="rowheader">[!DNL Adobe Workfront Fusion] license**</td>  
   <td> 
   <p>Current: No [!DNL Workfront Fusion] license requirement.</p> 
   <p>Or</p> 
   <p>Legacy: Any </p> 
   </td>  
  </tr>  
  <tr>  
   <td role="rowheader">Product</td>  
   <td> 
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] Plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] is included.</li></ul> 
   <p>Or</p> 
   <p>Current: Your organization must purchase [!DNL Adobe Workfront Fusion].</p> 
   </td>  
  </tr> 
 </tbody>  
</table> 

For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md). 

## Connect to an app or web service that does not require configuration

In most cases, you can use the module to create a connection with little or no extra information. [!DNL Workfront Fusion] handles the authentication automatically.

For instructions on creating a connection with no special considerations, see [Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions](../../workfront-fusion/connections/connect-to-fusion-general.md).

## Connect to an Adobe app or service

To connect to an Adobe app or service, you may need information from the Adobe Admin Console, such as your Org ID or Technical Account ID. 

You can also use the Adobe Authenticator module  to connect to any Adobe API, using a single connection. This allows you to more easily connect to Adobe products that do not yet have a dedicated Fusion connector.

For specific instructions, see [the article for the connector](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-adobe-products).

## Connect to a [!DNL Microsoft] app or web service

Most of the [!DNL Microsoft] apps in [!DNL Workfront Fusion] allow you to create a connection with no extra information.

The following circumstances do require extra steps in creating a connection:

* Using [!DNL Microsoft Dynamics 365] modules.

   For instructions, see [[!DNL Microsoft Dynamics 365] modules](../../workfront-fusion/apps-and-their-modules/microsoft-dynamics-365-modules.md).

* Connecting to the [!DNL Microsoft Graph API] using an [!UICONTROL HTTP] module

   For instructions, see [Call the [!DNL MS Graph REST API] via the [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] module](../../workfront-fusion/connections/call-the-ms-graph-rest-api.md).

## Connect to a [!DNL Google] app or web service

The process for connecting to [!DNL Google] apps may differ based on what kind of [!DNL Google] account you are using. In addition, [!DNL Google] security measures may require extra configuration when you are connecting to [!DNL Workfront Fusion].

For more information see:

* [Connect [!DNL Adobe Workfront Fusion] to [!DNL Google Services] using a custom OAuth client](../../workfront-fusion/connections/connect-fusion-to-google-using-oauth.md)
* [Connect [!DNL Adobe Workfront Fusion] to [!DNL Google Services] with updated security measures](../../workfront-fusion/connections/connect-to-google-with-new-security-measures.md)

## Other apps that require additional configuration

Some apps and services do not follow the basic configuration for [!DNL Workfront Fusion] connections. You can find instructions for connecting these apps in the article for that app.

For specific instructions, see [the article for the connector](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-third-party-applications).


