---
title: AWS S3 modules
description: The [!DNL Adobe Workfront Fusion AWS] S3 modules let you perform operations on your S3 buckets.
author: Becky
feature: Workfront Fusion
exl-id: 6b2d9dd5-0b33-4297-aea0-aba26072b26a
---
# AWS S3 modules

The [!DNL Adobe Workfront Fusion AWS] S3 modules let you perform operations on your S3 buckets.

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

## Prerequisites

To use [!UICONTROL AWS S3] modules, you must have an [!DNL Amazon Web Service] account.

## AWS S3 API information

The AWS S3 connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td>https://s3.&#123;&#123;parameters.region&#125;&#125;.amazonaws.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.5.21</td> 
  </tr>
 </tbody> 
 </table>

## Connect [!DNL AWS] to Workfront Fusion {#connect-aws-to-workfront-fusion}

To connect [!DNL AWS S3] to Workfront Fusion you must connect your [!DNL AWS] account to Workfront Fusion. To do so, you'll first need to create an API user in [!DNL AWS] [!UICONTROL IAM].

1. Sign in to your [!DNL AWS] [!UICONTROL IAM] account.
1. Navigate to **[!UICONTROL Identity and Access Management]** > **[!UICONTROL Access Management]** > **[!UICONTROL Users]**.

1. Click **[!UICONTROL Add User]**.
1. Enter the name of the new user and select the **[!UICONTROL Programmatic access]** option in the [!UICONTROL Access type] section.
1. Click **[!UICONTROL Attach existing policies directly]**, then search for **[!UICONTROL AmazonS3FullAccess]** in the search bar. Click it when it appears, then click **[!UICONTROL Next]**.

1. Proceed through the other dialog screens, then click **[!UICONTROL Create User]**.
1. Copy the provided **[!UICONTROL Access key ID]** and **[!UICONTROL Secret access key]**.

1. Go to Workfront Fusion and open the [!DNL AWS S3] module's **[!UICONTROL Create a connection]** dialog.
1. Enter the [!UICONTROL Access key ID] and [!UICONTROL Secret access key] from step 7 to the respective fields and click **[!UICONTROL Continue]** to establish the connection.

The connection has been established. You can proceed with setting up the module.

## [!DNL AWS S3] modules and their fields

When you configure [!DNL AWS S3] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL AWS S3] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Searches](#searches)

### Actions 

* [[!UICONTROL Create Bucket]](#create-bucket)
* [[!UICONTROL Get File]](#get-file)
* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Upload File]](#upload-file)

#### [!UICONTROL Create Bucket]

This action module creates a bucket in AWS.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL AWS] account to Workfront Fusion, see <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connect [!DNL AWS] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Enter the name of the new bucket.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Select your regional endpoint. For more information, see <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">regional endpoints</a> in the AWS documentation.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get File] 

This action module downloads a file from a bucket.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL AWS] account to Workfront Fusion, see <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connect [!DNL AWS] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Select your regional endpoint. For more information, see <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">regional endpoints</a> in the [!DNL AWS] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Select the bucket you want to download the file from.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Path]</p> </td> 
   <td> <p>Enter the path to the file. Example: <code>/photos/2019/February/image023.jpg</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call] 

This action module makes a custom call to the AWS S3 API. 

For a detailed discussion of the [!DNL Amazon S3] API, see [[!DNL Amazon S3] [!UICONTROL REST] API Introduction](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL AWS] account to Workfront Fusion, see <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connect [!DNL AWS] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Region] </td> 
   <td> <p>Select your regional endpoint. For more information, see <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">regional endpoints</a> in the [!DNL AWS] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Enter a host URL. The path must be relative to<code> https://s3.&lt;selected-region>.amazonaws.com/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Select the [!UICONTROL HTTP] request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">[!UICONTROL HTTP] request methods in Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Add a request header. For each header you want to add, click <b>Add item</b> and enter the header. You can use the following common request headers. For more request headers refer to <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTCommonRequestHeaders.html">[!DNL AWS S3] API Documentation</a>.</p> <p>Workfront Fusion adds authorization headers automatically.</p> 
    <table style="table-layout:auto">
     <col> 
     <col> 
     <thead> 
      <tr> 
       <th>Header Name</th> 
       <th> <p> Description</p> </th> 
      </tr> 
     </thead> 
     <tbody> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Length]</p> </td> 
       <td> <p>Length of the message (without the headers) according to RFC 2616. This header is required for [!UICONTROL PUT]s and operations that load XML, such as logging and ACLs.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Type]</p> </td> 
       <td> <p>The content type of the resource, in case the request content is in the body. Example: <code>text/plain</code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-MD5]</p> </td> 
       <td> <p>The base64 encoded 128-bit MD5 digest of the message (without the headers) according to RFC 1864. This header can be used as a message integrity check to verify that the data is the same data that was originally sent. Although it is optional, we recommend using the [!UICONTROL Content-MD5] mechanism as an end-to-end integrity check. For more information about [!UICONTROL REST] request authentication, see <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html?r=1821">Signing and authenticating REST requests</a> in the AWS documentation.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Date]</p> </td> 
       <td> <p>The current date and time according to the requester. Example: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. When you specify the <code>Authorization </code>header, you must specify either the <code>x-amz-date</code> or the <code>Date </code>header.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Expect]</p> </td> 
       <td> <p>When your application uses [!UICONTROL 100-continue], it does not send the request body until it receives an acknowledgment. If the message is rejected based on the headers, the body of the message is not sent. This header can be used only if you are sending a body.</p> <p>Valid Values: [!UICONTROL 100-continue]</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
       <td> <p>For path-style requests, the value is <code>s3.amazonaws.com</code>. For virtual-style requests, the value is <code>BucketName.s3.amazonaws.com</code>. For more information, see <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/VirtualHosting.html">Virtual Hosting</a> in the AWS documentation.</p> <p>This header is required for HTTP 1.1 (most toolkits add this header automatically); optional for HTTP/1.0 requests.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-content-sha256]</p> </td> 
       <td> <p>When using signature version 4 to authenticate the request, this header provides a hash of the request payload. When uploading an object in chunks, set the value to <code>STREAMING-AWS4-HMAC-SHA256-PAYLOAD</code> to indicate that the signature covers only headers and that there is no payload. For more information, see <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-streaming.html">Signature Calculations for the Authorization Header</a> in the AWS documentation.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-date]</p> </td> 
       <td> <p>The current date and time according to the requester. Example: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. When you specify the <code>Authorization </code>header, you must specify either the <code>x-amz-date</code> or the <code>Date </code>header. If you specify both, the value specified for the <code>x-amz-date</code> header takes precedence.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-security-token]</p> </td> 
       <td> <p>This header can be used in the following scenarios:</p> 
        <ul> 
         <li>Provide security tokens for [!DNL Amazon DevPay] operations. Each request that uses [!DNL Amazon DevPay] requires two <code>x-amz-security-token</code> headers: one for the product token and one for the user token. When [!DNL Amazon S3] receives an authenticated request, it compares the computed signature with the provided signature. Improperly formatted multi-value headers used to calculate a signature can cause authentication issues.</li> 
         <li>Provide a security token when using temporary security credentials. When making requests using temporary security credentials you obtained from IAM, you must provide a security token using this header. To learn more about temporary security credentials, go to Making Requests.</li> 
        </ul> <p>This header is required for requests that use [!DNL Amazon DevPay] and requests that are signed using temporary security credentials.</p> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Add the desired query strings such as parameters or form fields.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:   <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload File] 

This action module uploads a file to an AWS S3 bucket.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL AWS] account to Workfront Fusion, see <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connect [!DNL AWS] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Select your regional endpoint. For more information, see <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">regional endpoints</a> in the [!DNL AWS] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Folder] </p> </td> 
   <td> <p>Specify the target folder that you want to upload a file to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers] (optional)</p> </td> 
   <td> <p> For each header you want to add, click <b>Add item</b> and enter the header's key and value.</p><p> For available headers, see <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a> in the AWS documentation.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Searches 

* [[!UICONTROL List Files]](#list-files)
* [[!UICONTROL List Folders]](#list-folders)

#### [!UICONTROL List Files] 

Returns a list of files from a specified location.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL AWS] account to Workfront Fusion, see <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connect [!DNL AWS] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Select your regional endpoint. For more information, see <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">regional endpoints</a> in the [!DNL AWS] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Select the [!DNL Amazon S3] bucket you want to search for files.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix]</p> </td> 
   <td> <p> Enter a path to a folder to look up files in, such as <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Folders] 

Returns a list of folders from a specified location.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL AWS] account to Workfront Fusion, see <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connect [!DNL AWS] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Select your regional endpoint. For more information, see <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">regional endpoints</a> in the [!DNL AWS] documentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Select the [!DNL Amazon S3] bucket you want to search for folders.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix] (optional)</p> </td> 
   <td> <p> Path to a folder to look up folders in, such as <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>
