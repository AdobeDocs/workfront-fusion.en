---
title: "HTTP > Other modules"
description: The Adobe Workfront Fusion HTTP app provides various modules for communication based on Hypertext Transfer Protocol (HTTP) protocol. HTTP is the foundation of data communication for the World Wide Web. You can use the modules to download web pages and files, call webhooks and API endpoints, and so on.
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
---
# HTTP > Other modules

The Adobe Workfront Fusion [!UICONTROL HTTP] app provides various modules for communication based on Hypertext Transfer Protocol (HTTP) protocol. HTTP is the foundation of data communication for the World Wide Web. You can use the modules to download web pages and files, call webhooks and API endpoints, and so on.

The right choice of the module depends on the authentication/ authorization mechanism the resource you want to access employs. The following are examples of modules

* **Make a request**: Primarily intended for resources not using any type of authentication or authorization
* **Make a Basic Auth request**: For resources using [!DNL HTTP] Basic authentication (BA)
* **Make a OAuth 2.0 request**: For resources using the OAuth 2.0 authorization protocol
* **Make a Client Certificate Auth request**: For resources employing authorization protocol that requires a client-side certificate
* **Make an API Key authorization request**: For resources employing API Keys for authorization

>[!NOTE]
>
>If you are connecting to an Adobe product that does not currently have a dedicated connector, we recommend using the Adobe Authenticator module.
>
>For more information, see [Adobe Authenticator module](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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

## Request modules

See the following articles for specific request module instructions:

* [[!UICONTROL HTTP] > [!UICONTROL Make a request] module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make a Basic Authorization request] module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make a Client Certificate Authorization request] module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an API Key Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## Other action modules

* [[!UICONTROL Get a File]](#get-a-file)
* [[!UICONTROL Resolve a target URL]](#resolve-a-target-url)

### [!UICONTROL Get a File] 

This action module downloads a file from the specified URL. After the file is downloaded, you can further process the file (map the file data) using other modules in the scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx )] </td> 
   <td> <p>Use this option to set up error handling.</p> <p>For more information, see <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Error handling in Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Enter or map the URL of the file you want to download. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules] </td> 
   <td> <p>Enable this option if you want the cookies for this site to be available to other modules. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Resolve a target URL] 

This action module resolves a chain of HTTP redirects and returns a target URL.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Enter or map the URL you want to resolve, such as a [!DNL bit.ly] URL.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method] </td> 
   <td> <p>Select whether you want to use the [!UICONTROL HEAD] method or the [!UICONTROL GET] method.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Iterator modules

### [!UICONTROL Retrieve headers]

This module returns each header (name and value) from the specified HTTP module in a separate bundle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> Select the module you want to retrieve headers from.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Generating JSON Web Tokens (JWT)

It is possible to generate a JWT token with the help of built-in functions:

Header:

![JWT header](/help/workfront-fusion/references/apps-and-modules/assets/jwt-header-350x19.png)

Code for copy&paste:

```
{{replace(replace(replace(base64("{""alg"":""HS256"",""typ"":""JWT""}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Payload:

![JWT payload](/help/workfront-fusion/references/apps-and-modules/assets/jwt-payload-350x17.png)

Code for copy&paste:

```
{{replace(replace(replace(base64("{""iss"":""key"",""exp"":" + (timestamp + 60) + "}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Token:

![JWT token](/help/workfront-fusion/references/apps-and-modules/assets/jwt-token-350x15.png)

Code for copy&paste:

```
{{1.value}}.{{2.value}}.{{replace(replace(replace(sha256(1.value + "." + 2.value; "base64"; "secret"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```
