---
title: Use Mutual TLS in HTTP modules in Adobe Workfront Fusion
description: You can use Mutual TLS in your Adobe Workfront Fusion HTTP modules, allowing both sides of the information transaction to verify the other's identity.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
---
# Use Mutual TLS in HTTP modules in Adobe Workfront Fusion

## Mutual TLS overview

When you send data over the internet, it's important to ensure that it goes to or comes from the correct location and that only the intended recipient can read it. With TLS enabled, the client (computer requesting information) uses certificates to verify the identity of the server (computer providing information). This makes secure HTTP connections.

Mutual TLS allows this identity confirmation to go both ways. When the server sends its certificate to verify its identity to the client, it also requests the client's certificate. This ensures that the server does not send information to a site or user that would misuse it.

>[!INFO]
>
>**Example:**
>
>* **TLS**: When a person types "MyGreatBank.com" into a browser, they want to be sure that they are going to My Great Bank, not a website that might misuse or sell their banking information. They also want to be sure their bank account information is encrypted.
>
>   When the browser (the client) connects to MyGreatBank.com (the server), TLS requires a certificate from MyGreatBank.com to verify its identity. The certificate is provided by a certificate authority such as [!DNL DigiCert] or [!DNL Thawte]. Because the browser trusts the certificate authority, it allows the connection.
>
>* **Mutual TLS**: MySoftware.com is a software client that needs information from the MyGreatBank.com API. MyGreatBank allows only trusted clients to connect to their servers. So, in addition to the regular TLS verifying the identity of MyGreatBank.com, the TLS/certificate authority process also verifies the request from MySoftware.com.

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
   <p>Operation-based: No Workfront Fusion license requirement</p>
   <p>Connector-based (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Providing your Workfront Fusion public certificate

When you connect to a web service with an HTTP request, the web service usually requires a Workfront Fusion public certificate for verification. This allows the web service to compare the certificate presented in the HTTP request to the one on file, as a way to ensure that the certificate is on the web service's allowlist.

For instructions on uploading the Adobe Workfront Fusion public certificate to a web service, see the web service's documentation.

>[!NOTE]
>
>You may need to provide other information in addition to the certificate. For information on what a web service requires, see the web service's API documentation.

You can use the following links to download the Workfront Fusion public certificates. To locate your datacenter, see [Identify your datacenter](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md) in the article Configure IP Addresses for Fusion in your organization's allowlist. 

### Certificates for 2025

>[!IMPORTANT]
>
>* These Workfront Fusion public certificates expire on **March 2, 2027** (US and EU) or **March 8, 2027** (Azure). After yours expires you will need to upload a new certificate to the web service. We recommend that you:
>
>   * Make note of the expiration date and set a reminder for yourself to upload the certificate to your web service.
>   * Bookmark this page to easily find the new certificates.
>
>* These are non-wildcard mTLS certificates.

| Datacenter | Download link | Dates valid |
| --- | --- | --- |
| US Datacenter | [Download Workfront Fusion US Certificate 2026](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-us-mtls-certificate-2026.pem) | January 29, 2026 to March 2, 2027 |
| EU Datacenter | [Download Workfront Fusion EU Certificate 2026](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-eu-mtls-certificate-2026.pem) | January 29, 2026 to March 2, 2027 |
| Azure Cluster | [Download Workfront Fusion Azure Certificate 2026](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-eu-az-mtls-certificate-2026.pem) | February 4, 2026 to March 8, 2027 |


### Certificates for 2025

>[!IMPORTANT]
>
>* We recommend installing the certificates for 2026, available above.
>* These Workfront Fusion public certificates expire on **April 4, 2026** (US and EU) or **November 25, 2025** (Azure). After yours expires you will need to upload a new certificate to the web service. We recommend that you:
>
>   * Make note of the expiration date and set a reminder for yourself to upload the certificate to your web service.
>   * Bookmark this page to easily find the new certificates.
>
>* These are non-wildcard mTLS certificates.

| Datacenter | Download link | Dates valid |
| --- | --- | --- |
| US Datacenter | [Download Workfront Fusion US Certificate 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-us-mtls-certificate.pem) | March 3, 2025 to April 4, 2026 |
| EU Datacenter | [Download Workfront Fusion EU Certificate 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-eu-mtls-certificate.pem) | March 3, 2025 to April 4, 2026 |
| Azure Cluster | [Download Workfront Fusion Azure Certificate 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-az-mtls-certificate.pem) | October 24, 2024 to November 25, 2025 |

<!--

### Certificates for 2024

>[!IMPORTANT]
>
>* We recommend installing the certificates for 2025, available above.
>* These Workfront Fusion public certificates expire on **May 7, 2025**. After yours expires you will need to upload a new certificate to the web service. We recommend that you:
>
>   * Make note of the expiration date and set a reminder for yourself to upload the certificate to your web service.
>   * Bookmark this page to easily find the new certificates.
>
>* These are non-wildcard mTLS certificates.

| Datacenter | Download link | Dates valid |
|---|---|---|
| US Datacenter | [Download Workfront Fusion Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |
| EU Datacenter | [Download Workfront Fusion EU Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |

-->

## Enabling Mutual TLS&nbsp;in Workfront Fusion HTTP modules

All Workfront Fusion [!UICONTROL HTTP] request modules have the option to enable Mutual TLS.

To enable Mutual TLS in an [!UICONTROL HTTP] request module:

1. Add an [!UICONTROL HTTP] request module to your scenario.
1. Begin configuring the module.

   For instructions on configuring an [!UICONTROL HTTP] request module, see the appropriate article under [Universal connectors](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

1. Enable **[!UICONTROL Show advanced settings]** near the bottom of the module.
1. Enable **[!UICONTROL Use Mutual TLS]**.
