---
title: Generate a scenario segment using AI
description: You can enter a text prompt to create an HTTP module configured to the prompt.
author: Becky
feature: Workfront Fusion
---
# Generate a scenario segment using AI 

<!--DO NOT DELETE - linked through CSH-->

<!--Check if this is in GA before repo goes live. If not, hide this article.-->

<!--Check if they need to have signed the rider and stuff-->

You can use AI to enter a text prompt describing what you need a segment of your scenario to do. Fusion then generates one or more modules that perform those actions, which you can use in your scenario.

Generated scenario segments contain modules for a single connector. To generate modules for a different connector, create a separate prompt, then join the scenario segments in your scenario. 

As with anything generated from AI, we recommend that you double check and test the generated modules to ensure that they are performing as intended.

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

1. Click the Generate with AI icon ![Generate with AI](assets/generate-with-ai-icon-beta.png) near the bottom of the scenario editor page.

   Or

   Begin adding a module and select **Generate with AI** from the list of applications. This option does not appear when adding the first (trigger) module to a scenario.

   The AI Assistant panel opens.
1. (Conditional) If this is the first time using AI to add a scenario segment, read the Agreement that appears and click **Agree**.
1. Enter a text prompt into the box. 

   For tips on prompts, see [Tips for creating prompts for scenario segments](#tips-for-creating-text-prompts) in this article.

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
