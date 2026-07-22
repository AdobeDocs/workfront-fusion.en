---
title: Create scenarios from Storage
description: Storage integrates with Fusion's scenario builder, so you can create pre-configured scenarios directly from the Storage page to download or upload files.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# Create scenarios from Storage

For an overview of Storage, see [Storage overview](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

Storage integrates with Fusion's scenario builder. Users can create pre-configured scenarios directly from the Storage page.

## Download in Scenario

1. Select a file and click **"Download in Scenario"** from the floating action bar
2. Fusion creates a new scenario named **"Download {fileName}"**
3. The scenario is pre-configured with:
   * The active connection
   * The repository, folder, and file pre-selected
   * A module to generate a presigned download URL
   * An HTTP module to fetch the file from that URL
4. The scenario opens in a **new browser tab** in the scenario designer

## Upload File in Scenario

1. While browsing inside a folder, click the **"Upload File"** dropdown
2. Select **"Upload File in Scenario"**
3. Fusion creates a new scenario named **"Upload to {folderName}"**
4. The scenario is pre-configured with:
   * The active connection
   * The repository and folder pre-selected
   * A module to generate a presigned upload URL with a placeholder filename
5. The scenario opens in a **new browser tab** for the user to customize (e.g., add a source module for the file data)

Both scenarios are created with a default scheduling interval of 15 minutes.
