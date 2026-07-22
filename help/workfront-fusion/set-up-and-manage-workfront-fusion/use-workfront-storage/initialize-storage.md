---
title: Initialize Storage
description: When a user navigates to Storage for the first time, they see an initialization screen that creates a secure connection to Adobe Storage on behalf of the team.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# Initialize Storage

For an overview of Storage, see [Storage overview](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md). For requirements before you begin, see [Storage prerequisites](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-prerequisites.md).

When a user navigates to **Storage** for the first time (or if no valid connection exists), they see an initialization screen.

## Steps

1. The user clicks **"Initialize Storage"**
2. Fusion automatically creates a secure connection to Adobe Storage on behalf of the team
3. A subtitle shows **"Creating connection"** while the connection is being set up
4. Once the connection is established, Fusion loads the team's storage repositories

## What can go wrong

| Screen | Reason | What the user should do |
|--------|--------|------------------------|
| **Access Restricted** | The organization is not onboarded to Adobe IMS | Contact the organization admin to complete IMS onboarding |
| **Organization Mismatch** | The user is signed into a different Adobe organization than the one selected in Fusion | Sign out, then sign back in with the correct Adobe IMS organization |
| **Access Denied** | The user's account does not have the required permissions, or Adobe Storage is not available for the organization | Verify account permissions with the organization admin; click **Retry** after resolving |
| **No Storage Found** | The connection was established but no repositories were found | Verify Adobe Storage is provisioned for the organization; click **Load Storage** to retry |
