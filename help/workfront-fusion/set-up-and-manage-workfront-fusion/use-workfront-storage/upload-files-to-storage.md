---
title: Upload files to Storage
description: You can upload files to a folder in Storage directly, or create an automation scenario to handle the upload.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# Upload files to Storage

For an overview of Storage, see [Storage overview](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

Upload is available when browsing inside a folder (not at the top-level folder list).

## How to upload

1. Click the **"Upload File"** dropdown button
2. Select **"Upload File"** to upload directly, or **"Upload File in Scenario"** to create an automation scenario instead
3. For direct upload: a file picker opens — select the file to upload
4. A **progress banner** appears at the top-right showing:
   * File name
   * Upload progress percentage
   * Bytes transferred
   * A **Cancel** button to abort the upload

## Upload limits

* Maximum file size: **5 GB**
* If a file exceeds this limit, a toast notification appears: *"File too large — Maximum upload size is {max}. Selected file is {actual}."*

## After upload

* The file appears in the folder listing once the upload completes
* The **Size** column may temporarily show *"Processing…"* while Adobe Storage processes the file on the backend. The actual file size appears after processing completes (this can be verified by refreshing the page)

For instructions on creating an upload scenario, see [Create scenarios from Storage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/create-scenarios-from-storage.md).
