---
title: Connect Adobe Workfront Fusion to Google Services with updated security measures
description: Google has introduced restrictions on how users can use their API. This article describes how to connect Adobe Workfront Fusion to Google, accounting for these update security measures.
author: Becky
feature: Workfront Fusion
---
# Connect Adobe Workfront Fusion to Google Services with updated security measures

Google has introduced restrictions on how users can use their API. This article describes how to connect Adobe Workfront Fusion to Google, accounting for these update security measures.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront plan</td> 
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

<!--For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md).-->

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Google Services restrictions

Google introduced restrictions on how users can use their API as of June 1st, 2020. These security measures protect Google users from leakage or misuse of their personal data on Google. 

These restrictions are related to the Gmail and Google Drive apps. 

For more information about these restrictions, see "Additional Requirements for Specific API Scopes" in the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy#additional_requirements_for_specific_api_scopes)

To access restricted scopes, the connected service (Adobe Workfront Fusion or any other service that accesses the user's data via the API) must be verified, and must have a Letter of Assessment to prove that the service is secure and transparent about how they use the data. Workfront Fusion complies with all of Google's requirements for access to restricted scopes. However, most of the third-party connected services in Workfront Fusion don't have the Letter of Assessment, and therefore don't comply with Google terms. Because of that, Workfront Fusion is not permitted to send data to these services.

## Exceptions to Google Services restrictions

There are a few exceptions that make it possible to send data to an unapproved third-party service that doesn't have the Letter of Assessment without violating any of the new restrictions. They differ based on Google Workspace with the Workfront Fusion OAuth client, Google Workspace with another OAuth client, or @gmail.com and @googlemail.com.

* [Google Workspace with Workfront Fusion OAuth client](#g-suite-with-workfront-fusion-oauth-client)
* [Google Workspace with another OAuth client](#g-suite-with-another-oauth-client)
* [@gmail.com and @googlemail.com](#gmailcom-and-googlemailcom)

### Google Workspace with Workfront Fusion OAuth client

Workfront Fusion uses the Domain-wide Installation exception. Domain-wide Installation is suited for Google Workspace users, and allows users to integrate unapproved services without any limitations. If you are a Google Workspace user, you don't have to perform any additional steps and can directly connect to unapproved services.

### Google Workspace with another OAuth client 

Google Workspace users that prefer to use their own OAuth client instead of using the Workfront Fusion OAuth client can connect to Google Services through the Internal Use approach. This option is intended for advanced users. For instructions, see [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

### @gmail.com and @googlemail.com {#gmailcom-and-googlemailcom}

Users that access Google Services through @gmail.com or @googlemail.com can connect to Google Services through the Personal Use approach. This option is intended for advanced users. For instructions, see [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## FAQ

* [What apps in Adobe Workfront Fusion are affected?](#what-apps-in-adobe-workfront-fusion-are-affected)
* [Do I have a Google Workspace account?](#do-i-have-a-g-suite-account)
* [What should I do if I'm a @gmail.com or @googlemail.com user?](#what-should-i-do-if-im-gmailcom-or-googlemailcom-user)
* [What should I do if I'm a Google Workspace user?](#what-should-i-do-if-im-a-g-suite-user)

### What apps in Adobe Workfront Fusion are affected? {#what-apps-in-adobe-workfront-fusion-are-affected}

Google Drive, Gmail, and Email (connected to Gmail account).

### Do I have a Google Workspace account? {#do-i-have-a-g-suite-account}

If your email address ends with @gmail.com or @googlemail.com, your account is not a Google Workspace account. If your Google account ends with a custom domain such as @my-company.com, then it is a Google Workspace account.

### What should I do if I'm @gmail.com or @googlemail.com user? {#what-should-i-do-if-im-gmailcom-or-googlemailcom-user}

These new restrictions only apply if you are integrating Google Drive or Gmail. If you want to connect to Google Drive or Gmail, you can

* Switch to Google Workspace

   or

* Create a custom OAuth client. This option is intended for advanced users.

   For instructions, see [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

If you want to integrate any other service than Google Drive or Gmail, these restrictions do not apply.

### What should I do if I'm a Google Workspace user? {#what-should-i-do-if-im-a-g-suite-user}

There is no required action.
