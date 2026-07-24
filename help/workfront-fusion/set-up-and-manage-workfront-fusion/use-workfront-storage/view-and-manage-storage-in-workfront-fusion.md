---
title: View and manage Storage in Workfront Fusion
description: The Storage area lists the repositories that are available, and lets you browse into folders and files.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# View and manage Storage in Workfront Fusion

The Storage area in Workfront Fusion allows you to view and interact with repositories in your Adobe cloud storage. 

For an overview of Storage, see [Storage overview](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

>[!TIP]
>
>Storage must be initialized before you can see repositories. For instructions, see [Initialize Storage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md).

## View repositories, folders, and files

1. In Workfront Fusion, click **Storage** in the left navigation. 
   A list of repositories opens.
   
   If there is only one repository available, the repository opens directly.

1. Click **Open** on any repository to browse its contents.

   Opening a repository shows Folders within the repository.
1. Click a folder to open it and display its Files.
1. To navigate back up through the folder structure, click the breadcrumbs.


>[!NOTE]
>
>An empty folder displays the message: *"This folder is empty"*

## Manage multiple Storage connections

A team can have multiple Adobe Storage connections.

1. In Workfront Fusion, click **Storage** in the left navigation. 
   When multiple connections exist, tabs appear at the top of the Storage page, labeled with each connection's name.
1. To switch to a different connection's repositories, click the tab for that connection.

If a connection becomes invalid, such as if its token expired and could not be refreshed, it is automatically filtered out and does not appear as a tab. Fusion's scheduled token refresh keeps connections valid automatically.

## File information

Each file in the table shows:

| Column | Description |
| -------- | ------------- |
| **Name** | File name with a document icon. |
| **Type** | File extension badge, such as PNG, PDF, or JPG. |
| **Size** | File size. Shows *"Processing…"* if the file was recently uploaded and the backend is still processing it. |
| **Created** | Creation date. |

Files also show a **version badge** (e.g., `v2`, `v3`) when multiple versions exist.

## Table controls

* **Search/filter**: Filter files by name using the global search bar.
* **Sorting**: Click column headers to sort.
* **Pagination**: Choose 10, 25, 50, or 100 items per page. The default is 25.
