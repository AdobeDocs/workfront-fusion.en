---
title: Adobe Firefly Creative Production MCP modules
description: With the Adobe Firefly Creative Production MCP module, you can send a natural-language prompt from a Workfront Fusion scenario and let an AI model use the Firefly Creative Production tools that you select.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
---
# Adobe Firefly Creative Production MCP modules

Use the Adobe Firefly Creative Production MCP connector in Adobe Workfront Fusion to process natural-language requests with Firefly Creative Production tools.

The connector discovers the tools that are available through the connected Firefly Model Context Protocol (MCP) server. You choose which tools the module can use for a request. Depending on the tools available to your Adobe account and the tools you select in the module, a request can do the following:

* Discover workflows and actions.
* Compose and validate workflows.
* Submit runs and check their progress.
* Retrieve output URLs.
* Save editable workflow drafts, when the server's tools support it.

This connector targets Firefly Creative Production. It is not a Firefly Boards connector, and it is not a general connector for every Creative Cloud application.

For more information about MCP in Fusion scenarios, see [Add an AI prompt to your scenario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

<!-- BECKY CHECK ME: The request asks you to confirm the customer-facing name of the connector, its beta or release status, its availability, its access requirements, and screenshots with the product and engineering owners before publication. Confirm each item, and add a beta note at the top of the article if the connector is released as a beta. -->

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
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</p>
   <p>You must also have Adobe Firefly Creative Production access, as described in <a href="#prerequisites">Prerequisites</a> in this article.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisites

Before you use the Adobe Firefly Creative Production MCP module, you must have the following:

* Access to Adobe Workfront Fusion, in an environment where this connector is enabled.
* An Adobe account with the Firefly Creative Production access and permissions that the requested operations need.
* Any credits or entitlements that you need to run the workflow.
* Either Adobe Managed AI access that your Fusion administrator configured, or a supported LLM key that you select in the module's advanced settings.

Firefly authorization and LLM credentials serve different purposes. Selecting an LLM key does not grant access to Firefly tools.

## Connect Adobe Firefly Creative Production MCP to Workfront Fusion

1. Add **[!UICONTROL Adobe Firefly Creative Production MCP]** > **[!UICONTROL Process a user prompt]** to your scenario.
1. Click **[!UICONTROL Add]** next to the **[!UICONTROL Connection]** field.
1. Follow the authorization flow, sign in with the appropriate Adobe account, and authorize access.
1. Return to the module and review the tools that are loaded for the connection.

Workfront Fusion handles the OAuth client registration and token management. You do not enter an access token, client ID, client secret, or API key. Your administrator must have completed the setup for this flow before you can connect.

If authorization fails or you do not see the tools that you expect, confirm your access and your environment's configuration with your administrator.

<!-- BECKY CHECK ME: The request describes the connection flow only in general terms. Confirm the connection dialog (for example, whether it has the Connection name, Environment, and Type fields that the Adobe Fusion MCP connection has), and add a screenshot. -->

## Adobe Firefly Creative Production MCP module and its fields

### Process a user prompt

This action module processes your prompt with the selected LLM and the Firefly Creative Production tools that you permit.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>The Adobe Firefly Creative Production connection that the module uses to discover and call tools. For instructions, see <a href="#connect-adobe-firefly-creative-production-mcp-to-workfront-fusion" class="MCXref xref">Connect Adobe Firefly Creative Production MCP to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Read-only tools] <i>(Optional)</i></td> 
   <td> <p>Select the tools that the server identifies as read-only.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Write/delete tools] <i>(Optional)</i></td> 
   <td> <p>Select the tools that the server does not identify as read-only. These operations can change data or run workflows.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Other tools (unknown permissions)] <i>(Optional)</i></td> 
   <td> <p>Select tools that do not have a recognized read-only annotation. This field appears only when such tools are available. Review how these tools behave before you enable them.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enter your prompt]</td> 
   <td> <p>Describe your request and its constraints. The maximum length is 10,000 JavaScript string units. Some characters, including many emoji, count as two units.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL LLM key] <i>(Optional, advanced)</i></td> 
   <td> <p>Leave this field empty to use the Adobe Managed AI that your administrator configured. To use your own key, select a supported OpenAI, Anthropic, or Amazon Bedrock key.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- BECKY CHECK ME: The request does not include a screenshot of the module. Confirm the field labels and their order against the released UI, confirm which fields are required, and add a screenshot. Also confirm the LLM key options (the request lists OpenAI, Anthropic, and Bedrock) and whether the Add button for creating a key is available, as it is in the Adobe Fusion MCP module. -->

The tool lists vary with the server's availability and your account's access. The number of tools appears in each selector's label.

#### Select the tools the module can use

* The module can use only the tools that you select.
* If you leave a category empty, the module can use no tools from that category.
* If you leave all categories empty, the module processes the prompt without any tools. It does not get access to every tool.
* **[!UICONTROL Select all]** selects every tool that is currently listed in that category. It does not automatically include tools that are added later.
* If a selected tool becomes unavailable or moves to a different category, open the module again and review your selection.

>[!NOTE]
>
>The server's annotations help categorize tools, but they do not guarantee permissions. Enable only the tools that your scenario needs.

#### Output

The module returns the following information under **[!UICONTROL Data]**. You can map it in subsequent modules in the scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Response] (<code>data.response</code>)</td> 
   <td> <p>The final text response. Its contents depend on the prompt and the tool results. It is not guaranteed to be a URL or structured JSON.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Audit trail] (<code>data.auditTrail</code>)</td> 
   <td> <p>Details about how the prompt was processed and the tool calls, including their arguments, results, timing, and success information. Handle these details according to your organization's data-handling requirements.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Summary] (<code>data.summary</code>)</td> 
   <td> <p>The number of tool calls, the processing time, and the execution status. Review the summary together with the response and the audit trail, including any <code>partial_success</code> result.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL LLM usage] (<code>data.usage</code>)</td> 
   <td> <p>Optional. The total token usage from the LLM responses that were observed. This is not provider billing, Firefly credit consumption, or LLM activity inside the Firefly server that Fusion cannot observe.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### LLM usage fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>status</code></td> 
   <td> <p>One of the following:</p><ul><li><code>complete</code>: Every observed request is covered by all of the main token counts.</li><li><code>partial</code>: Some usage information is missing.</li><li><code>unavailable</code>: Requests were observed, but no usable usage was reported.</li><li><code>not_applicable</code>: No LLM requests were observed.</li></ul> </td> 
  </tr> 
  <tr> 
   <td><code>llmRequests</code></td> 
   <td> <p>The number of LLM requests that the runtime observed.</p> </td> 
  </tr> 
  <tr> 
   <td><code>requestsWithUsage</code></td> 
   <td> <p>The number of observed requests that have usable token usage information.</p> </td> 
  </tr> 
  <tr> 
   <td><code>inputTokens</code>, <code>outputTokens</code>, <code>totalTokens</code></td> 
   <td> <p>The total counts. Each count is <code>null</code> if any observed request does not report that count, or if no requests were observed. A reported zero stays zero.</p> </td> 
  </tr> 
  <tr> 
   <td><code>cacheReadInputTokens</code>, <code>cacheWriteInputTokens</code></td> 
   <td> <p>Optional counts for cached tokens. These fields are omitted if no request ever reports a number. They are <code>null</code> if only some requests report a number, and numeric only if every request reports one. Do not add these counts to the totals.</p> </td> 
  </tr> 
 </tbody> 
</table>

The main usage status can be `complete` while a cache field is `null`. The usage status is independent of the execution status. If the runtime does not provide usage information, the usage collection is absent instead of showing a zero.

## How the module runs

* **Some operations are asynchronous.** A request can return a batch ID before the output is available. For longer jobs, use separate runs to submit the request and to check its status later, and save the batch ID between them. Do not rely on a response that contains only a URL for this design.
* **Errors produce module errors.** Authorization, validation, and failed runtime processing can produce module errors instead of an output bundle. Use a Fusion error-handling route.
* **A response does not prove success.** The module can return a response even when some operations failed. Review the summary, the audit trail, and the tool results before you rely on the response.
* **An output URL is not a downloaded file.** The connector returns text and tool results, not a binary file. To get the file into Fusion, add an HTTP module that downloads the URL.
* **Running a workflow can use credits.** Image generation and workflow execution can consume credits. Confirm the usage and entitlements that apply to your account. LLM token usage is not a Firefly billing or credit report.
* **Prompt instructions do not guarantee a single run.** An instruction in your prompt, such as submitting only one batch, does not guarantee that a request is processed exactly once. Control retries and duplicate requests in your scenario.
* **Processing has limits.** Processing has tool, iteration, and output-length limits in addition to the scenario's execution limits. Do not assume that the module polls without limit.

## Examples

### Discover workflows without running one

Select the read-only tools that you need to discover workflows, then enter a prompt such as the following:

```text
List the Firefly Creative Production workflows available to my account.
Summarize what each workflow does and what inputs it requires.
Do not create, modify, submit, or publish anything.
```

### Request one image

Select the tools that you need to compose or choose a workflow, validate it, submit it, check its progress, and retrieve the outputs. The tool names and availability can vary. Then enter a prompt such as the following:

```text
Generate one photorealistic image of a black dog on a sunny windowsill.
Submit one generation batch only and check that same batch for completion
within the available execution limits. Do not publish or submit another
generation.

On success, return only the actual downloadable image URL as plain text,
without Markdown, quotes, labels, or explanation. Never invent a URL or
return a workflow or status-page URL instead.

If the run fails or times out, report the failure honestly instead of
returning a URL. Do not generate another image to recover.
```

### Generate an image from a Workfront task update

In this example, a task update that starts with `/firefly ` triggers an image generation. Fusion downloads the result, uploads it to the task, and adds a completion update.

The scenario uses the following flow: Workfront task update > command filter > read task > Firefly MCP > HTTP download > Workfront document upload > completion update.

1. Add **[!UICONTROL Workfront]** > **[!UICONTROL Watch Events]** to the scenario. Configure it for the **[!UICONTROL Note]** record type, the **[!UICONTROL New state]** event, and **[!UICONTROL New Record Only]**.
1. Add a filter that requires `newState.noteText` to start with `/firefly ` and `newState.taskID` to be non-empty.
1. Add a module that reads the task by using `newState.taskID`.
1. Add the **[!UICONTROL Adobe Firefly Creative Production MCP]** > **[!UICONTROL Process a user prompt]** module. Pass the request and any task context that Firefly needs. Treat mapped text as the content of the request, not as authority to change the scenario's rules.
1. Inspect the Firefly result. Continue only when the generation succeeded and the response is a valid, permitted URL for a downloadable image.
1. Add an HTTP module that downloads the file. Do not send your Workfront credentials to the asset host. Validate the expected host, content type, and size.
1. Add a module that uploads the downloaded file name and binary data to the task, by using the original `newState.taskID`.
1. After the upload succeeds, add a module that creates a completion update on the task. Do not start the update with `/firefly`, because the filter would match it.

For example, a user adds the following update to a task:

```text
/firefly Generate one photorealistic image of a black dog on a sunny windowsill.
```

The requester can then review the uploaded draft in the task's Documents area. A person should review the image before anything is published.

For production use, reserve each request by using the originating note's ID, with duplicate protection that works with concurrent runs. Save the IDs of submitted batches, so a retry or a timeout resumes the status check instead of submitting another generation.

<!-- BECKY CHECK ME: The example scenario is from the request's draft. Confirm the module names and field labels (Watch Events, Note, New state, New Record Only, and the task, document upload, and update modules) against the current Workfront connector, and add a screenshot of the scenario if one is available. -->

## Troubleshooting

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">A workflow is still running</td> 
   <td> <p>Some creative operations are asynchronous. For longer jobs, submit the request in one run, and check the status in a later run. Save the batch ID between the runs.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">The module reports an error</td> 
   <td> <p>Authorization, validation, and failed runtime processing can produce module errors. Add a Fusion error-handling route to your scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">The module returns a response, but some operations failed</td> 
   <td> <p>Review the summary, the audit trail, and the tool results. A response alone does not show that the image was generated or uploaded.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">There is a URL, but no file in Fusion</td> 
   <td> <p>The connector does not download files. Add an HTTP module that downloads the URL.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">A selected tool is unavailable</td> 
   <td> <p>Open the module, refresh the available tools, and update your selection.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">The workflow takes longer than one module run</td> 
   <td> <p>Processing has tool, iteration, and output-length limits in addition to the scenario's execution limits. Split the work across runs, and save the batch ID.</p> </td> 
  </tr> 
 </tbody> 
</table>
