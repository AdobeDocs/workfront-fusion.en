---
title: Generate a scenario segment using AI
description: You can use AI to enter a text prompt describing what you need a segment of your scenario to do. Fusion then generates one or more modules that perform those actions, which you can use in your scenario.
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
---
# Generate a scenario segment using AI 

<!--DO NOT DELETE - linked through CSH-->

<!--Check if this is in GA before repo goes live. If not, hide this article.-->

<!--Check if they need to have signed the rider and stuff-->

You can use AI to enter a text prompt describing what you need a segment of your scenario to do. Fusion then generates one or more modules that perform those actions, which you can use in your scenario.

Generated scenario segments contain modules for a single connector. To generate modules for a different connector, create a separate prompt, then join the scenario segments in your scenario. 

As with anything generated from AI, we recommend that you double check and test the generated modules to ensure that they are performing as intended.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any Adobe Workfront Workflow package and any Adobe Workfront Automation and Integration package</p><p>Workfront Ultimate</p><p>Workfront Prime and Select packages, with an additional purchase of Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront licenses</td> 
   <td> <p>Standard</p><p>Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisites

Your organization must meet the following prerequisites to use this functionality:

* Your organization must have participated in the Workfront AI Assistant Beta program.
* Adobe must have a signed Adobe Gen AI agreement on file for your organization.

   For more information on signing the agreement, see [Sign the Adobe Gen AI agreement](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview#sign-the-adobe-gen-ai-agreement) in the article AI Assistant overview in the Workfront documentation.

## Currently supported AI module applications

The Fusion AI can currently generate modules that connect to the following applications:

* Adobe Firefly
* Azure OpenAI
* Microsoft Graph 
* Adobe Workfront Planning
* Adobe Analytics
* Adobe PDF Services
* Adobe Marketo
* Adobe Frame.io
* Dropbox
* NetSuite
* Google Calendar
* Atlassian Jira
* GitLab
* Spotify
* Bitbucket
* OpenAI
* Slack

## Generate modules

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a module.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Click the **AI Assistant** icon ![AI Assistant icon](assets/ai-assistant-icon.png) near the upper-right corner of the screen.
1. Enter a text prompt into the AI Assistant panel. 

   For tips on prompts, see [Tips for creating prompts for scenario segments](#tips-for-creating-prompts-for-scenario-segments) in this article.

   AI Assistant generates the module or set of modules.
1. (Conditional) If necessary, add your API token for the application into the modules. 
1. Check the modules to ensure that they are configured for the appropriate application and action.
1. (Conditional) If the generated scenario section is not attached to your scenario, drag it into place.

We recommend testing the modules to ensure that they are performing as intended.

## Tips for creating prompts for scenario segments

Text prompts should include the following information at a minimum:

* The application that you are connecting to
* The action or actions that you want to perform

>[!IMPORTANT]
>
>You can generate more than one module at a time, but can only generate modules for one application at a time.  

>[!BEGINSHADEBOX]

**Examples**:

* `Delete the records 'xyz-123', 'xyz-456', 'xyz-789' from Adobe Workfront Planning`
This includes the application `Workfront Planning` and the action `delete records`. This prompt creates three modules, one for each record that will be deleted.
* `Change campaign summary of the record 'xyz-123' from Adobe Workfront Planning`
This includes the application `Workfront Planning` and the action `change campaign summary`.
* `Get all field details in the record type with ID 'test-record' from Adobe Workfront Planning`
This includes the application `Workfront Planning` and the action `get field details`.

The following example is NOT correct:

* `Generate an image in Adobe Firefly and upload it to Dropbox`

    This example is incorrect because it includes more than one application

>[!ENDSHADEBOX]

Consider the following when creating text prompts:

* Use direct, simple language.
* Check and test your scenario segment. If it does not perform as expected, refine your prompt and try again.
