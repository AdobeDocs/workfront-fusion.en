---
title: HTTP > Make a JWT request module
description: The Adobe Workfront Fusion HTTP > Make a JWT request module sends an HTTP(S) request to a URL and authorizes it with a JSON Web Token that Fusion signs for you automatically.
author: Becky
feature: Workfront Fusion
exl-id: 2f8c0b0d-085a-4b49-b350-4fd4cca1d0a7
TQID: 'https://experienceleague.adobe.com/'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# [!UICONTROL HTTP] > [!UICONTROL Make a JWT request] module

The Adobe Workfront Fusion [!UICONTROL HTTP] > [!UICONTROL Make a JWT request] module sends an HTTP(S) request to a URL and authorizes it with a JSON Web Token (JWT) that the module signs for you on every call. The response is then processed the same way as in the standard [!UICONTROL HTTP] > [!UICONTROL Make a request] module.

This module behaves like the standard [!UICONTROL Make a request] module, with one main difference: it automatically signs a JWT from the claims you provide and adds it to the request, by default as `Authorization: Bearer <token>`.

Use this module to call any API that expects a signed JWT for authentication, such as services that require a short-lived bearer token signed with a shared secret (HMAC) or a private key (RSA/ECDSA), without creating the token in a separate step.

If the API uses OAuth 2.0, Basic authentication, an API key, or a client certificate, use the matching dedicated HTTP module instead.

>[!NOTE]
>
>If you are connecting to an Adobe product that does not currently have a dedicated connector, we recommend using the Adobe Authenticator module.
>
>For more information, see [Adobe Authenticator module](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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
   <p>Operation-based: Available to organizations with operation-based licenses</p>
   <p>Connector-based (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Create a JWT connection

The module requires a JWT connection. The connection stores the signing material so the secret or private key does not have to appear in the scenario.

### Create a JWT connection in Fusion

1. Add the [!UICONTROL HTTP] > [!UICONTROL Make a JWT request] module to your scenario.
1. Click **[!UICONTROL Add]** next to the **[!UICONTROL Connection]** field.
1. Configure the connection fields:

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader"><p>Connection name</p></td>
      <td><p>Enter a name for the connection.</p></td>
     </tr>
     <tr>
      <td role="rowheader"><p>Algorithm</p></td>
      <td>
       <p>Select the signing algorithm for the connection.</p>
       <ul>
        <li><code>HS256</code></li>
        <li><code>HS384</code></li>
        <li><code>HS512</code></li>
        <li><code>RS256</code></li>
        <li><code>RS384</code></li>
        <li><code>RS512</code></li>
        <li><code>PS256</code></li>
        <li><code>PS384</code></li>
        <li><code>PS512</code></li>
        <li><code>ES256</code></li>
        <li><code>ES384</code></li>
        <li><code>ES512</code></li>
       </ul>
      </td>
     </tr>
     <tr>
      <td role="rowheader"><p>Secret</p></td>
      <td>
       <p>Enter the signing key.</p>
       <ul>
        <li>For <code>HS*</code> algorithms, use the shared secret string.</li>
        <li>For <code>RS*</code>, <code>PS*</code>, and <code>ES*</code> algorithms, use the PEM-encoded private key.</li>
       </ul>
      </td>
     </tr>
    </tbody>
   </table>

1. Click **[!UICONTROL Continue]** to create the connection and return to the module.

>[!IMPORTANT]
>
>A JWT connection signs with one algorithm only. If your scenario requires more than one signing algorithm, create a separate connection for each algorithm. This matches the existing standalone JWT app behavior.

## [!UICONTROL HTTP] > [!UICONTROL Make a JWT request] module and its fields

When you configure the [!UICONTROL HTTP] > [!UICONTROL Make a JWT request] module, Adobe Workfront Fusion displays the fields listed below in the same order they appear in the module UI. A bolded title in a module indicates a required field. Fields marked as advanced are hidden unless you select **[!UICONTROL Show advanced settings]**.

<table style="table-layout:auto">
 <col>
 <col>
 <tbody>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Connection]</p></td>
   <td><p>Select an existing JWT connection or create a new one.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL URL]</p></td>
   <td><p>The target URL for the request.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Method]</p></td>
   <td><p>HTTP method such as GET, POST, PUT, PATCH, or DELETE.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Headers]</p></td>
   <td><p>Custom request headers in key/value format.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Query String]</p></td>
   <td><p>Query-string parameters in key/value format.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Body type]</p></td>
   <td><p>How the request body is encoded. Options include Raw, application/x-www-form-urlencoded, and multipart/form-data.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Parse response]</p></td>
   <td><p>When enabled, Fusion parses the response body based on the response content type.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL JWT Payload (Claims)]</p></td>
   <td><p>Key/value pairs included as claims in the JWT payload. The reserved claims <code>exp</code>, <code>iat</code>, and <code>nbf</code> must be a NumericDate — a number of seconds since the Unix epoch. Claim values keep their JSON type, so numbers stay numbers and booleans stay booleans.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Timeout] (advanced)</p></td>
   <td><p>Specify the request timeout in seconds (1-300). The default is 40 seconds.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Retry Count] (advanced)</p></td>
   <td><p>Specify how many times the request should retry if the request fails due to a retryable error.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Additional Retry Status Codes] (advanced)</p></td>
   <td><p>Specify additional HTTP status codes that should be treated as retryable.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Share cookies with other HTTP modules] (advanced)</p></td>
   <td><p>Enable this option to share cookies from the server with all HTTP modules in your scenario.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Self-signed certificate] (advanced)</p></td>
   <td><p>Upload your certificate if you want to use TLS using your self-signed certificate.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Reject connections that are using unverified (self-signed) certificates] (advanced)</p></td>
   <td><p>Enable this option to reject connections that are using unverified TLS certificates.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Follow redirect] (advanced)</p></td>
   <td><p>Enable this option to follow the URL redirects with 3xx responses.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Disable serialization of multiple same query string keys as arrays] (advanced)</p></td>
   <td><p>By default, Workfront Fusion handles multiple values for the same URL query string parameter key as arrays. For example, <code>www.test.com?foo=bar&amp;foo=baz</code> will be converted to <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>. Activate this option to disable this feature.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Request compressed content] (advanced)</p></td>
   <td><p>Enable this option to request a compressed version of the website. Adds an <code>[!UICONTROL Accept-Encoding]</code> header to request compressed content.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Use Mutual TLS] (advanced)</p></td>
   <td><p>Enable this option to use Mutual TLS in the HTTP request.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Sign Options] (advanced)</p></td>
   <td><p>Additional options passed to the JWT signer, such as <code>expiresIn</code>, <code>issuer</code>, <code>audience</code>, <code>subject</code>, and <code>keyid</code>. Duration values such as <code>expiresIn</code> are interpreted by the <code>jsonwebtoken</code> library. A plain number is treated as milliseconds, so use a unit string such as <code>"1h"</code> or <code>"3600s"</code> to be explicit. The algorithm is taken from the connection and cannot be overridden here.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Header Name] (advanced)</p></td>
   <td><p>Name of the request header that receives the signed JWT. Default: <code>Authorization</code>. The header name must not contain a dot (<code>.</code>), because dotted names are rejected and cannot be masked in request logs.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Token Type] (advanced)</p></td>
   <td><p>Authentication scheme placed before the token, such as <code>Bearer</code>. Leave this blank to send the raw token without a prefix.</p></td>
  </tr>
 </tbody>
</table>

## How the token is built

1. The module collects the claims in the [!UICONTROL JWT Payload (Claims)] field.
1. Reserved claims such as <code>exp</code>, <code>iat</code>, and <code>nbf</code> are converted to NumericDate values.
1. The module applies the [!UICONTROL Sign Options] and signs the token using the algorithm from the connection.
1. The signed token is placed in the request header defined by [!UICONTROL Header Name].
1. If [!UICONTROL Token Type] is set, the module adds the prefix before the token. For example, <code>Bearer eyJ...</code>.
1. The request is sent, and the response is processed the same way as the standard [!UICONTROL HTTP] > [!UICONTROL Make a request] module.

The signed token is automatically masked in debug and error logs so it is never exposed.

## Example

### Connection

- Algorithm: `HS256`
- Secret: `my-shared-secret`

### Module settings

- URL: `https://api.example.com/v1/orders`
- Method: `GET`
- JWT Payload (Claims):
  - `sub` = `service-account-42`
  - `iss` = `make-integration`
- Sign Options:
  - `expiresIn` = `1h`
- Header Name: `Authorization`
- Token Type: `Bearer`

### Result

The module sends the request with a header similar to:

```text
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

## FAQ / gotchas

### Why did my token expire so quickly?

You likely entered a bare number for `expiresIn` such as `3600`. The `jsonwebtoken` library interprets plain numbers as milliseconds. Use a unit string such as `"1h"` or `"3600s"` instead.

### Can I change the algorithm per request?

No. The algorithm is fixed by the connection. If you need a different algorithm, create a different JWT connection.

### Can I send the token in a custom header?

Yes. Set the [!UICONTROL Header Name] field to a custom name, but it cannot contain a dot (`.`).

### Can I send the raw token without `Bearer`?

Yes. Leave [!UICONTROL Token Type] empty.

### Is the token visible in logs?

No. The signed token is masked automatically in debug and error logs.


>[!NOTE]
>
>Technical note: signing uses the `jsonwebtoken` library and mirrors the standalone JWT app's signing behavior, so the same inputs produce the same token as the standalone JWT app.
