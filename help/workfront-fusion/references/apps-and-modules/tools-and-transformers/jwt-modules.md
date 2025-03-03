---
title: JWT modules
description: The [!DNL Adobe Workfront Fusion] [!UICONTROL JWT] app provides a module that creates JWT tokens based on the provided algorithm.
author: Becky
feature: Workfront Fusion
exl-id: 380f60db-b2ec-411a-86ee-0d5699f19b41
---
# [!UICONTROL JWT] module

The [!DNL Adobe Workfront Fusion] [!UICONTROL JWT] app provides a module that creates JWT tokens based on the provided algorithm.

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
   <p>No Workfront Fusion license requirement.</p>
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

## JWT API information

The JWT connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
   <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.1.5</td> 
  </tr>
 </tbody> 
 </table>

## JWT module and its fields

### Generate JWT

This module generates a JWT based on the selected algorithm. 

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Algorithm]</td> 
   <td> <p>Select algorithm with which you want to generate the JWT.</p> <ul>
   <li><b>HS256</b>: HMAC using SHA-256 hash algorithm</li>
   <li><b>HS384</b>: HMAC using SHA-384 hash algorithm</li>
   <li><b>HS512</b>: HMAC using SHA-512 hash algorithm</li>
   <li><b>RS256</b>: RSASSA-PKCS1-v1_5 using SHA-256 hash algorithm</li>
   <li><b>RS384</b>: RSASSA-PKCS1-v1_5 using SHA-384 hash algorithm</li>
   <li><b>RS512</b>: RSASSA-PKCS1-v1_5 using SHA-512 hash algorithm</li>
   <li><b>PS256</b>: RSASSA-PSS using SHA-256 hash algorithm (only Node ^6.12.0 OR >=8.0.0)</li>
   <li><b>PS384</b>: RSASSA-PSS using SHA-384 hash algorithm (only Node ^6.12.0 OR >=8.0.0)</li>
   <li><b>PS512</b>: RSASSA-PSS using SHA-512 hash algorithm (only Node ^6.12.0 OR >=8.0.0)</li>
   <li><b>ES256</b>: ECDSA using P-256 curve and SHA-256 hash algorithm</li>
   <li><b>ES384</b>: ECDSA using P-384 curve and SHA-384 hash algorithm</li>
   <li><b>ES512</b>: ECDSA using P-521 curve and SHA-512 hash algorithm</li>
   </ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload] </td> 
   <td> <p>For each payload item you want to add, click <b>Add item</b> and enter the item's key and value.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Options] </td> 
   <td> <p>For each option item you want to add, click <b>Add item</b> and enter the item's key and value.</p> <p>The following keys are available:
   <ul>
   <li><b>algorithm</b>: (default: RS256)</li>
   <li><b>expiresIn</b>: Expressed in seconds or a string describing a time span (e.g., 2 days, 10h, 7d). A numeric value is interpreted as a seconds count. If you use a string, be sure to provide the time units (days, hours, etc.), otherwise milliseconds unit is used by default (120 is equal to 120ms).</li>
   <li><b>notBefore</b>: Expressed in seconds or a string describing a time span (e.g., 2 days, 10h, 7d). A numeric value is interpreted as a seconds count. If you use a string, be sure to provide the time units (days, hours, etc.), otherwise milliseconds unit is used by default (120 is equal to 120ms).
</li>
   <li><b>audience</b></li>
   <li><b>issuer</b></li>
   <li><b>jwtid</b></li>
   <li><b>subject</b></li>
   <li><b>noTimestamp</b></li>
   <li><b>header</b></li>
   <li><b>keyid</b></li>
   <li><b>mutatePayload</b>: If <code>true</code>, the sign function will modify the payload object directly. This is useful if you need a raw reference to the payload after claims have been applied to it but before it has been encoded into a token.</li>
   <li><b>allowInsecureKeySizes</b>: If <code>true</code>, allows private keys with a modulus below 2048 to be used for RSA.</li>
   <li><b>allowInvalidAsymmetricKeyTypes</b>: If <code>true</code>, allows asymmetric keys which do not match the specified algorithm. This option is intended only for backward compatibility and should be avoided.</li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>
