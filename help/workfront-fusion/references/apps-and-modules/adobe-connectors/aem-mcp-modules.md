---
title: Adobe Experience Manager MCP modules
description: With the Adobe Experience Manager MCP module, you can send a plain-English prompt to Adobe Experience Manager's MCP server and let an AI model carry out the request.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# Adobe Experience Manager MCP modules

The Adobe Experience Manager MCP connector is a dedicated Fusion integration for Adobe Experience Manager's own Model Context Protocol (MCP) server. Unlike a typical connector, where each module performs one fixed action, this connector has a single module that accepts an open-ended, plain-English instruction and lets an AI model decide which Adobe Experience Manager operations — across areas like sites, digital assets, content fragments, folders, the content repository, and content AI — are needed to fulfill it.

This connector is dedicated to Adobe Experience Manager's own MCP server. It does not support other, unrelated MCP servers. For a connector you can point at any MCP server instead, see [MCP Agent module](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md).

>[!NOTE]
>
>Responses from this module are AI-generated and can occasionally be imperfect, even with every available safeguard in place. This module is appropriate for automation where a human isn't reviewing every run in real time, but it isn't a guarantee of the deterministic behavior you'd get from a traditional Adobe Experience Manager module.

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
   <td role="rowheader">Adobe Workfront Fusion license</td> 
   <td>
   <p>Operation-based: Available to organizations with operation-based licenses</p>
   <p>Connector-based (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

* You must have an Adobe Experience Manager account to use this module.

## Connect Adobe Experience Manager MCP to Workfront Fusion {#connect-adobe-experience-manager-mcp-to-workfront-fusion}

The Adobe Experience Manager MCP connector uses OAuth to connect to Adobe Experience Manager. There are no connection fields to fill in manually, such as a username, password, or API key.

To create a connection:

1. In the Adobe Experience Manager MCP module, click **[!UICONTROL Add]** next to the Connection field.
1. You are redirected to Adobe's login page. Log in and approve access.

You are redirected back to Workfront Fusion, and the new connection is available in the module.

## Adobe Experience Manager MCP module and its fields

Currently, there is only one module in the Adobe Experience Manager MCP connector.

### Process a user prompt

This action module sends a plain-English instruction to Adobe Experience Manager's MCP server and returns the AI's answer.

Each run of this module is a single, self-contained execution, similar to sending an email rather than having a live conversation. The AI cannot ask a follow-up question and wait for your reply — it makes its best judgment in one pass and returns a complete answer. If your prompt is ambiguous, the AI states any assumption it made as part of its answer, rather than stopping to ask you to clarify.

>[!IMPORTANT]
>
>This module only takes a write or delete action when your prompt actually asks for one. It doesn't take an extra action you didn't request, even in the same run where it's carrying out something else you did ask for.

Because each run is independent, the module has no memory of previous runs by itself. To create a multi-turn, conversational experience across several runs, store the previous question and answer (for example, in a [Data Store](/help/workfront-fusion/create-scenarios/data-stores/data-store-overview.md)) and include that history as text at the start of your next prompt, followed by the new question.

<table style="table-layout:auto"> 
 <col/>
 <col/>
 <tbody>
  <tr>
   <td role="rowheader">Connection</td>
   <td><p>For instructions about connecting your Adobe Experience Manager account to Workfront Fusion, see <a href="#connect-adobe-experience-manager-mcp-to-workfront-fusion" class="MCXref xref">Connect Adobe Experience Manager MCP to Workfront Fusion</a> in this article.</p></td>
  </tr>
  <tr>
   <td role="rowheader">User Prompt</td>
   <td><p>Enter or map the instruction, in plain English, that you want the AI to carry out.</p><p>Example: <i>Find all assets in the marketing folder that haven't been updated in 90 days.</i></p></td>
  </tr>
  <tr>
   <td role="rowheader">Read-only tools <i>(Optional)</i></td>
   <td><p>Restrict which read-only Adobe Experience Manager actions the AI is allowed to call — actions that only look something up, such as finding an asset or reading a page's content, and never change anything.</p><p>If you leave this field empty, all read-only actions are allowed.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Write/delete tools <i>(Optional)</i></td>
   <td><p>Restrict which write or delete Adobe Experience Manager actions the AI is allowed to call — actions that change something, such as updating a page, publishing content, or deleting an asset.</p><p>If you leave this field empty, all write and delete actions are allowed. To guarantee that an unattended scenario never takes a destructive action, we recommend leaving this field set to a deliberately empty selection rather than leaving it unrestricted.</p></td>
  </tr>
  <tr>
   <td role="rowheader">LLM key <i>(Optional, advanced)</i></td>
   <td><p>By default, this module processes your prompt using Adobe's own AI service, and you do not need to select a key.</p><p>To use your own AI provider instead, select an existing LLM key, or create a new one by clicking <b>Add</b> and entering the following information:</p>
    <ul>
     <li><b>Key name</b>: Enter a name for the new key.</li>
     <li><b>LLM</b>: Select the large language model that this key is associated with. Supported providers are OpenAI, Anthropic Claude, and Amazon Bedrock.</li>
     <li><b>Key</b>: Enter or map your API key for the selected provider.</li>
     <li><b>Model</b>: Select the LLM model that the key will use.</li>
     <li><b>Other fields</b>: Enter values for any other fields that your LLM requires.</li>
    </ul>
   </td>
  </tr>
 </tbody>
</table>

The module returns the following information, which you can map in subsequent modules in the scenario:

* **Response**: The AI's final answer, as text.
* **Audit Trail**: A record of what happened while producing that answer, including which tools were called, whether each call succeeded, and how long processing took.

<!-- BECKY CHECK ME: confirm the exact on-screen output field names (Response, Audit Trail) against the live module before publishing - the Slack request describes what's returned by behavior ("the AI's final answer as text, plus a full audit trail"), not by verified on-screen labels. -->
