---
title: Connect Adobe Workfront Fusion to a web service that uses API token authorization
description: Some services do not allow integration solutions such as Adobe Workfront Fusion to create an app that you can easily use in your scenario.
author: Becky
feature: Workfront Fusion
exl-id: 4a8ac816-52de-41e8-96d7-1c8cde2ebe32
---
# Connect Adobe Workfront Fusion to a web service that uses API token authorization

Some services do not allow integration solutions such as Adobe Workfront Fusion to create an app that you can easily use in your scenario.

The workaround to this situation is to connect the desired service (app) to Workfront Fusion using the HTTP > Make a Request module.

This article explains how to connect almost any web service to Workfront Fusion using an API Key/API token.

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
   <p>Current: No Workfront Fusion license requirement</p>
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

## Connect to a web service that uses an API token

The procedure of connecting the service via an API token is similar for most web services.

1. Create an application on the web service's website, as explained in the section [Create a new application and obtain the API token](#create-a-new-application-and-obtain-the-api-token) in this article.
1. Obtain the API Key or API token.
1. Add Workfront Fusion's  HTTP >  Make a Request module to your scenario.
1. Set up the module according to the web service's API documentation and running the scenario, as explained in the section [Set up the  HTTP module](#set-up-the-http-module) in this article.

>[!NOTE]
>
>This example connects to the Pushover notification service.

## Create a new application and obtain the API token 

>[!NOTE]
>
>There are many different ways that web services create and distribute API keys or API tokens. For instructions on obtaining an API key and token for your desired web service, go to the service's website and search for "API key" or "API token."
>
>We are including instructions for obtaining a Pushover API key only as an example of what you might find.

1. Log in to your Pushover account.
1. Click **Create an Application/API Token** at the bottom of the page.
1. Fill in the Application Information and click **Create an Application**.
1. Store the provided API token in a safe place. You will need it for the Workfront Fusion HTTP > Make a Request module to connect to the desired web service (Pushover, in this case).

## Set up the  HTTP module 

To connect a web service to your Workfront Fusion scenario, you need to use the  HTTP > Make a request module in the scenario and set up the module according to the web service's API documentation.

1. Add the  HTTP > Make a Request module to your scenario.
1. To push a message using Workfront Fusion, set up the HTTP module as follows.

   >[!NOTE]
   >
   >These module settings correspond to the Pushover web service API documentation. Settings may be different for other web services. For example, the API token may be inserted to the  Header and not to the Body field.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> URL</td> 
      <td> <p><code>https://api.pushover.net/1/messages.json</code> </p> <p>The URL field contains the endpoint that you can find in the web service's API documentation.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> Method</td> 
      <td> <p><code>POST</code> </p> <p>The used method depends on the corresponding endpoint. The Pushover endpoint for pushing messages uses the POST method.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Headers</p> </td> 
      <td> <p>Some web services may use Headers to specify the API token authentication or other parameters. This is not the case in our example as the Pushover's endpoint for pushing messages uses Body (see below) for all request types.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Query String</p> </td> 
      <td> <p>Some web services may use a Query String to specify other parameters. This is not the case in our example as the Pushover web service uses  Body (see below) for all request types.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Body Type</p> </td> 
      <td> <p><code>Raw</code> </p> <p>This setting allows you to select the JSON content type in the  Content Type field below.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Content Type</p> </td> 
      <td> <p><code>JSON (application/json)</code> </p> <p>JSON is the required content type by the  Pushover app. This may differ from other web services.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Request Content</p> </td> 
      <td> <p>Enter the  Body request content in the JSON format. You can use the  JSON > Create JSON module as explained in <a href="#map-the-json-body-using-the-json--create-json-module" class="MCXref xref">Map the JSON body using the JSON > Create JSON module</a> in this article. Or you can enter the JSON content manually, as explained in <a href="#enter-the-json-body-manually" class="MCXref xref">Enter the JSON body manually</a> in this article.</p> <p>See the web service's API documentation for the required parameters for that web service.</p> </td> 

     </tr> 
    </tbody> 
   </table>

## Enter the JSON body manually

Specify parameters and values in the JSON format.

>[!BEGINSHADEBOX]

**Example:**

```
{"user":"12345c2ecu1hq42ypqzhswbyam34",
"token":"123459evz8aepwtxydndydgyumbfx",
"message":"Hello World!",
"title":"The Push Notification"}
```

>[!ENDSHADEBOX]

This example includes the following information.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p> user</p> </td> 
   <td> <p>Your USER_KEY. This can be found in your Pushover dashboard.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> token </td> 
   <td> <p>Your API token/API Key that was generated you created your Pushover app.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> message </td> 
   <td> <p>The text content of the push notification that is sent to the device(s).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> title </td> 
   <td> <p>(Optional) Your message's title. If no value is entered, your app's name is used. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Map the JSON body using the JSON > Create JSON module

The Create JSON module makes the specifying JSON easier. It also gives you the possibility to define values dynamically.

For more information about the JSON modules, see [JSON modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/json-modules.md).

1. Enter or map the values you want to create JSON from.

   ![JSON values](/help/workfront-fusion/create-scenarios/connect-to-apps/assets/json-values-350x288.png) 

1. Connect the  JSON > Create JSON module to the HTTP > Make a Request module.
1. Map the JSON string from the Create JSON module to the  Request content field in the  HTTP > Make a Request module.

When you run the scenario, the push notification is sent to the device that has been registered in your Pushover account.
