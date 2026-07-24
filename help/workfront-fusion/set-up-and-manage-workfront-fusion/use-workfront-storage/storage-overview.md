---
title: Storage overview
description: Storage is a page in Workfront Fusion that gives teams direct access to their Adobe Enterprise Storage Management (ESM) repositories, letting users browse folders, upload and download files, view version history, and create automation scenarios.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# Storage overview

<!--Add to navigation articles once this goes to production-->

The Storage area in Workfront Fusion gives teams direct access to their Adobe Enterprise Storage Management (ESM) repositories. Users can browse folders, upload and download files, view version history, and create automation scenarios, all without leaving Fusion.

Storage is owned by teams, and requires the organization to be onboarded to Adobe Identity Management System (IMS) with access to Adobe Storage.

For instructions on using Storage, see:

* [Initialize Storage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md)
* [View and manage Storage in Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-and-manage-storage-in-workfront-fusion.md)
* [Upload files to Storage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/upload-files-to-storage.md)
* [Download files from Storage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/download-files-from-storage.md)
* [Delete files from Storage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/delete-files-from-storage.md)
* [View file version history in Storage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-storage-file-version-history.md)
* [Create scenarios from Storage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/create-scenarios-from-storage.md)

## Storage prerequisites

To use the Workfront Fusion Storage area, the following must be true:

* The organization is onboarded to **Adobe Identity Management System (IMS)**
* The organization has **Adobe Storage** available
* The user is signed into the **correct Adobe IMS organization** (the one matching the selected Fusion organization)
* The user's account has **access to Adobe Storage**

## Glossary

When using 

| Term | Definition |
| ------ | ----------- |
| **Repository** | A top-level storage container in Adobe ESM, typically mapped to a project or workspace |
| **Connection** | A secure link between Fusion and Adobe Storage, created automatically during initialization. Uses Adobe IMS authentication with automatic token refresh |
| **ESM** | Enterprise Storage Management, Adobe's cloud file storage service |
| **IMS** | Adobe Identity Management System, Adobe's authentication and identity platform |

<!--

## UI Reference — Key Screens

### 1. Initialization Screen

* Cloud icon with **"Adobe Storage"** heading
* Description text explaining the feature
* **"Initialize Storage"** button (primary action)
* Error variants for access restriction, org mismatch, access denied, no storage found

### 2. Repository List

* Table with **Name** and **Region** columns
* **"Open"** action button per row

### 3. File Browser

* Breadcrumb navigation bar
* **"Upload File"** dropdown button (with "Upload File" and "Upload File in Scenario" options)
* File/folder table with **Name**, **Type**, **Size**, **Created** columns
* Floating action bar on file selection with: **Download**, **Download in Scenario**, **Versions**, **Delete**
* Upload/download progress banners (top-right corner)

### 4. Version History Panel

* Right-side slide-out panel
* Version list with date, version badge, and download button per entry
* **"current"** label on the latest version

-->
