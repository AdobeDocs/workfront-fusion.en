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

For an overview of Storage, see [Storage overview](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

The Storage area lists the repositories that are available.

>[!TIP]
>
>Storage must be initialized before you can see repositories. For instructions, see [Initialize Storage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md).

## Repository list

Clicking on the Storage area opens a list of available repositories.

If a team only has one repository, opening the Storage area opens the repository directly.

To open a repository from the list, click **Open** next to the repository you want to open.

* If the team only has **one repository**, Fusion opens it automatically
* If the team has **multiple repositories**, a table lists them with columns: **Name** and **Region**
* Click **Open** on any repository to browse its contents

## Navigating folders and files

* The top-level view shows **Folders** within the repository
* Clicking a folder opens it and displays its **Files**
* A **breadcrumb trail** at the top shows the current location; click any breadcrumb to navigate back
* An empty folder displays the message: *"This folder is empty"*

## File information

Each file in the table shows:

| Column | Description |
| -------- | ------------- |
| **Name** | File name with a document icon |
| **Type** | File extension badge (e.g., PNG, PDF, JPG) |
| **Size** | File size. Shows *"Processing…"* if the file was recently uploaded and the backend is still processing it |
| **Created** | Creation date |

Files also show a **version badge** (e.g., `v2`, `v3`) when multiple versions exist.

## Table controls

* **Search/filter**: Filter files by name using the global search bar
* **Sorting**: Click column headers to sort
* **Pagination**: Choose 10, 25, 50, or 100 items per page (default: 25)
