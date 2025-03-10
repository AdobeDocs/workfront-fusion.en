---
title: Encryptor
description: Adobe Workfront Fusion Encryptor modules allow you to encrypt any text data. They currently support message encryption via AES256 and PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
---
# Encryptor

[!DNL Adobe Workfront Fusion] [!UICONTROL Encryptor] modules allow you to encrypt any text data. They currently support message encryption via AES256 and PGP ([!UICONTROL OpenPGP]).

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

## Message encryption and decryption using PGP

When encrypting and decrypting via PGP, it is necessary to use a keychain and to create a private or public key (or both).

For more information on public and private keys, see [Adobe Workfront Fusion glossary](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md).

For more information on keys, see [Keys](/help/workfront-fusion/references/modules/keys.md).

## [!UICONTROL Encryptor] modules and their fields

When you are configuring [!UICONTROL Encryptor] modules, the following fields display. A bolded title in a module indicates a required field.

### AES Decrypt (advanced)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Select the key that you want the module to use. To create a key, click <b>Add</b> and enter the key's name, key, and encoding type.</td>
    </tr>
    <tr>
        <td>Bits</td>
        <td></td>
    </tr>
    <tr>
        <td>Input encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Data</td>
        <td></td>
    </tr>
    <tr>
        <td>Output encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Cipher algorithm</td>
        <td></td>
    </tr>
    <tr>
        <td>Initialization vector encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Authentication tag encoding</td>
        <td></td>
    </tr>
</table>

### AES Decrypt (simple)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Select the key that you want the module to use. To create a key, click <b>Add</b> and enter the key's name, key, and encoding type.</td>
    </tr>
   <tr>
        <td>Input encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Data</td>
        <td></td>
    </tr>
    <tr>
        <td>Output encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Secret key</td>
        <td></td>
    </tr>
</table>

### AES Encrypt (advanced)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Select the key that you want the module to use. To create a key, click <b>Add</b> and enter the key's name, key, and encoding type.</td>
    </tr>
    <tr>
        <td>Bits</td>
        <td></td>
    </tr>
    <tr>
        <td>Input encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Data</td>
        <td></td>
    </tr>
    <tr>
        <td>Output encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Cipher algorithm</td>
        <td></td>
    </tr>
    <tr>
        <td>Initialization vector encoding</td>
        <td></td>
    </tr>
</table>

### AES Encrypt (simple)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Select the key that you want the module to use. To create a key, click <b>Add</b> and enter the key's name, key, and encoding type.</td>
    </tr>
   <tr>
        <td>Input encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Data</td>
        <td></td>
    </tr>
    <tr>
        <td>Output encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Secret key</td>
        <td></td>
    </tr>
</table>


### Create digital signature

This module allows you to decrypt a message using public and private keys.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Enter the recipient's private key.</td>
    </tr>
    <tr>
        <td>Algorithm </td>
        <td></td>
    </tr>
   <tr>
        <td>Input encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Output encoding</td>
        <td></td>
    </tr>
    <tr>
        <td>Secret key</td>
        <td></td>
    </tr>
    <tr>
        <td>Data</td>
        <td></td>
    </tr>
</table>

### Decrypt a PGP message

This module allows you to decrypt a message using public and private keys.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Enter the recipient's private key.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Enter the recipient's public key. This can authenticate the sender's identity.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Map the message that you want to decrypt.</td>
    </tr>
</table>

### Encrypt a PGP message

This module allows you to encrypt a message using public and private keys.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Enter the sender's private key. This can authenticate the sender's identity.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Enter the recipient's public key.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Enter the message that you want to encrypt.</td>
    </tr>
    </table>
