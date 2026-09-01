---
title: Initialize Storage
description: When a user navigates to Storage for the first time, they see an initialization screen that creates a secure connection to Adobe Storage on behalf of the team.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# Initialize Storage in Workfront Fusion

The Fusion Storage area must be initialized before you can view repositories, folders, and files in your Adobe cloud storage. 

For an overview of Storage, see [Storage overview](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

## Initialize Storage

1. In Workfront Fusion, click **Storage** in the left navigation. 
1. Click **Initialize Storage**.

Fusion automatically creates a secure connection to Adobe Storage on behalf of the team.

After the connection is established, Fusion loads the team's storage repositories.

## Troubleshooting initialization

| Message | Reason | What the user should do |
| -------- | -------- | ------------------------ |
| **Access Restricted** | The organization is not onboarded to Adobe IMS. | Contact the organization admin to complete IMS onboarding. |
| **Organization Mismatch** | The user is signed into a different Adobe organization than the one selected in Fusion. | Sign out, then sign back in with the correct Adobe IMS organization. |
| **Access Denied** | The user's account does not have the required permissions, or Adobe Storage is not available for the organization. | Verify account permissions with the organization admin. After resolving, click **Retry**. |
| **No Storage Found** | The connection was established but no repositories were found. | Verify Adobe Storage is provisioned for the organization. After verifying, click **Load Storage** to retry. |
