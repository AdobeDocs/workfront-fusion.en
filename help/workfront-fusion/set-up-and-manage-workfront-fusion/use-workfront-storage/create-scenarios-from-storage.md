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

Storage integrates with Fusion's scenario builder. From the Storage page, users can create a scenario that will download the selected file.

## Download in Scenario

1. In Workfront Fusion, click **Storage** in the left navigation. 
1. Navigate to the repository that contains the file you want to download in a scenario.
1. Select a file, then click **"Download in Scenario"** from the action bar.

Fusion then creates a new scenario named **"Download {fileName}"**. This scenario opens in a separate browser tab.

The scenario is pre-configured with:

   * The active connection.
   * The repository, folder, and file pre-selected.
   * A module to generate a presigned download URL.
   * An HTTP module to fetch the file from that URL.
   * A default scheduling interval of 15 minutes.

## Upload File in Scenario

1. In Workfront Fusion, click **Storage** in the left navigation. 
1. Navigate to the repository and folder that contains the file you want to download in a scenario.
1. While browsing inside a folder, click the **"Upload File"** dropdown.
1. Select **"Upload File in Scenario"**.

Fusion then creates a new scenario named **"Upload to {folderName}"**. This scenario opens in a new browser tab. You must add modules to provide the file that you want to upload, such as the Workfront > Download document module.

The scenario is pre-configured with:

   * The active connection.
   * The repository and folder pre-selected.
   * A module to generate a presigned upload URL with a placeholder filename.
   * A default scheduling interval of 15 minutes.

