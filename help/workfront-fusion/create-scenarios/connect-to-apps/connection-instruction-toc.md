---
title: Create connections
description: A connection must adhere to the requirements set by the API of the app or web service it connects to. For this reason, instructions for setting up a connection vary based on the app or web service. This article can help you identify and locate the instructions for connecting [!DNL Adobe Workfront Fusion] to your chosen app or web service.
author: Becky
feature: Workfront Fusion
exl-id: 281403a6-6f88-4976-8a10-1d0848ef9b35
---
# Create connections

A connection must adhere to the requirements set by the API of the app or web service it connects to. For this reason, instructions for setting up a connection vary based on the app or web service. This article can help you identify and locate the instructions for connecting [!DNL Adobe Workfront Fusion] to your chosen app or web service.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current: Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>Current: No Workfront Fusion license requirement.</p>
   <p>Or</p>
   <p>Legacy: Any </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>Select or Prime Workfront Plan: Your organization must purchase Adobe Workfront Fusion.</li><li>Ultimate Workfront Plan: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Connect to an app or web service that does not require configuration

In most cases, you can use the module to create a connection with little or no extra information. [!DNL Workfront Fusion] handles the authentication automatically.

For instructions on creating a connection with no special considerations, see [Create a connection - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

## Connect to an Adobe app or service

To connect to an Adobe app or service, you may need information from the Adobe Admin Console, such as your Org ID or Technical Account ID. 

You can also use the Adobe Authenticator module  to connect to any Adobe API, using a single connection. This allows you to more easily connect to Adobe products that do not yet have a dedicated Fusion connector.

For specific instructions, see [the article for the connector](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-adobe-products).

## Connect to a [!DNL Microsoft] app or web service

Most of the [!DNL Microsoft] apps in [!DNL Workfront Fusion] allow you to create a connection with no extra information.

The following circumstances do require extra steps in creating a connection:

* Using Microsoft Dynamics 365 modules.

   For instructions, see [Microsoft Dynamics 365 modules](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).

* Connecting to the Microsoft Graph API using an HTTP module

   For instructions, see [Call the MS Graph REST API](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md).

## Connect to a [!DNL Google] app or web service

The process for connecting to [!DNL Google] apps may differ based on what kind of [!DNL Google] account you are using. In addition, [!DNL Google] security measures may require extra configuration when you are connecting to [!DNL Workfront Fusion].

For more information see:

* [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)
* [Connect Adobe Workfront Fusion to Google Services with updated security measures](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-google-with-new-security-measures.md)

## Other apps that require additional configuration

Some apps and services do not follow the basic configuration for [!DNL Workfront Fusion] connections. You can find instructions for connecting these apps in the article for that app.

For specific instructions, see [the article for the connector](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-third-party-applications).
