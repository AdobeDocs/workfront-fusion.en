---
title: Archive modules
description: In a [!DNL Adobe Workfront Fusion] scenario, you can connect an archive, such as a zipped file, to multiple third-party applications and services. For example, you can configure a scenario that
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
---
# [!UICONTROL Archive] modules

In a [!DNL Adobe Workfront Fusion] scenario, you can use an archive, such as a zipped file, in your scenario, allowing you to use it in your automations or integrations.

For instructions on creating a scenario, see the articles under [Create scenarios: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

## [!UICONTROL Archive] modules and their fields

When you configure [!UICONTROL Archive] modules, [!DNL Workfront Fusion] displays the fields listed below. Along with these, additional [!UICONTROL Archive] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Aggregators](#aggregators)
* [Transformers](#transformers)

## Actions

### [!UICONTROL Extract an archive] 

This action module extracts a file you identify from an archive.

The module returns the ID of the  file and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>  <p>Select a source file from a previous module, or map the source data.</p></p>  </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Example:** Get the ZIP file from the defined [!DNL Dropbox] folder (for example, Archives), extract it using the [!UICONTROL Archive] module and send extracted files to the desired email address as attachments with the [!UICONTROL Email] or [!DNL Gmail] module.

![Example Dropbox](/help/workfront-fusion/references/apps-and-modules/assets/example-dropbox-350x134.png)

>[!ENDSHADEBOX]

## Aggregators

### [!UICONTROL Create an archive] 

This aggregator module adds the desired files to a [!UICONTROL ZIP], GZIP, or [!UICONTROL TAR] archive.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module]</td> 
   <td> <p> Select the module you want to retrieve the files from.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Select whether you want to add files to a [!UICONTROL ZIP], GZIP, or a [!UICONTROL TAR] archive.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Enter a comment that you would like to add to the archive.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Group by]</td> 
   <td> <p>Define an expression that you want to group the aggregated output by. This expression can contain one or more mapped items. The aggregated data will be then separated into groups using this expression's value. Each group outputs as a separate bundle with a key (the evaluated expression) and a value (the aggregated text). You can use the key as a filter in subsequent modules.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Select this option to stop the scenario when there are no results.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Archive name]</td> 
   <td> <p> Enter a name for the created archive. Do not add an extension.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Example:** Watch incoming emails using the [!DNL Gmail] >[!UICONTROL Watch emails] module. If an email is received, its attachments are iterated into individual bundles then archived to the [!DNL ZIP] file and saved to the defined Dropbox folder.

![Example Gmail](/help/workfront-fusion/references/apps-and-modules/assets/example-gmail-350x102.png)

>[!ENDSHADEBOX]

## Transformers

* [[!UICONTROL Deflate]](#deflate)
* [[!UICONTROL Inflate]](#inflate)

### [!UICONTROL Deflate] 

This transformer module compresses binary data using a deflation algorithm.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Enter or map the data you want to compress using the deflate function.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Inflate] 

This transformer module decompresses binary data using an inflation algorithm.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Enter or map the data you want to decompress using the inflate function.</p> </td> 
  </tr> 
 </tbody> 
</table>
