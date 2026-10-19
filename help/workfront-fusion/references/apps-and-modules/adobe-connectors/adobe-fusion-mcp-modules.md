---
title: Adobe Fusion MCP modules
description: With the Adobe Fusion MCP module, you can send a plain-English prompt to Adobe Fusion's MCP server and let an AI model carry out the request.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
---
# Adobe Fusion MCP modules

The Adobe Fusion MCP connector sends one plain-English prompt to the Adobe Fusion Model Context Protocol (MCP) server. An AI model interprets your request and calls the Fusion tools needed to complete it.

The connector works only with the hosted Adobe Fusion MCP server. You cannot point it at another MCP server.

For more information about MCP in Fusion scenarios, see [Add an AI prompt to your scenario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Connect Adobe Fusion MCP to Workfront Fusion

The Adobe Fusion MCP connector uses OAuth 2.0 to connect to Adobe Fusion. You sign in through Adobe. You do not enter an access token or a server URL.

<!-- BECKY CHECK ME: Confirm whether the connection dialog has any fields, such as a connection name, and whether there is a production/non-production option. The source material describes only the Adobe sign-in. -->

To create a connection:

1. In the Adobe Fusion MCP module, click **[!UICONTROL Add]** next to the Connection field.
1. Enter a name for the connection, then click **[!UICONTROL Continue]**.
1. Sign in with your Adobe account and approve access.

You are redirected back to Workfront Fusion, and the new connection is available in the module.

## Adobe Fusion MCP module and its fields

### Process a user prompt

This action module sends a plain-English prompt to the Adobe Fusion MCP server. An AI model interprets the prompt, calls the Fusion tools needed to complete it, and returns the result.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting Adobe Fusion MCP to Workfront Fusion, see <a href="#connect-adobe-fusion-mcp-to-workfront-fusion" class="MCXref xref">Connect Adobe Fusion MCP to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>Read-only tools <i>(Optional)</i></td> 
   <td> <p>Select the read-only Fusion tools that the AI is allowed to call. These are the tools that the Fusion MCP server marks as read-only.</p> </td> 
  </tr> 
  <tr> 
   <td>Write/delete tools <i>(Optional)</i></td> 
   <td> <p>Select the write and delete Fusion tools that the AI is allowed to call.</p> </td> 
  </tr> 
  <tr> 
   <td>Other tools <i>(Optional)</i></td> 
   <td> <p>Select other Fusion tools that the AI is allowed to call. This field appears when the Fusion MCP server does not mark some tools as read-only or as write/delete.</p> </td> 
  </tr> 
  <tr> 
   <td>Enter your prompt</td> 
   <td> <p>Enter or map the instruction, in plain English, that you want the AI to carry out.</p> </td> 
  </tr> 
  <tr> 
   <td>LLM key <i>(Optional, advanced)</i></td> 
   <td> <p>By default, this module processes your prompt using Adobe Managed AI, and you do not need to select a key.</p> <p>To use your own AI provider instead, select an existing LLM key, or create a new one by clicking <b>Add</b> and entering the following information:</p>
     <ul>
       <li><b>Key name</b>: Enter a name for the new key.</li>
       <li><b>LLM</b>: Select the large language model that this key is associated with. Supported providers are OpenAI, Anthropic, and Amazon Bedrock.</li>
       <li><b>Key</b>: Enter or map your API key for the selected provider.</li>
       <li><b>Model</b>: Select the LLM model that the key will use.</li>
       <li><b>Other fields</b>: Enter values for any other fields that your LLM requires.</li>
      </ul>
    </td> 
  </tr> 
 </tbody> 
</table>

<!-- BECKY CHECK ME: Confirm the exact field labels and their order in the UI. Also confirm whether the same Adobe Managed AI model and monthly usage limit described in the Adobe Workfront MCP modules article apply here. -->

#### Restrict the tools the AI can call

You can limit which Fusion tools the AI can call by selecting tools in the Read-only tools, Write/delete tools, and Other tools fields.

* If you leave a field empty, the AI can call every tool in that category. This is true even if you select tools in a different category.
* If you leave all of the fields empty, the AI can call every tool on the Fusion MCP server.

To prevent an unattended scenario from taking a write or delete action, select only the tools you want to allow in the Read-only tools field, and select at least one tool in the Write/delete tools field that you are comfortable with the AI calling.

<!-- BECKY CHECK ME: There is currently no way to select "no write/delete tools" because an empty field allows all of them. Confirm the recommended guidance for preventing write/delete actions before publishing. -->

Tool names in the lists come from the Fusion MCP server.

#### How the module processes your prompt

* The module does not have a follow-up turn. If your prompt is unclear, the AI makes a reasonable assumption and states it in the response instead of asking you a question.
* The AI verifies information that can change by using the tools.
* The AI does not take any write or delete action beyond what your prompt requests.
* The module requires a valid connection. It does not run without one.

#### Output

The module returns the following information, which you can map in subsequent modules in the scenario:

* **Response**: The AI's final answer, as text.
* **Audit Trail**: A record of the session, including the tools called, their arguments and results, and timings.
* **Summary**: Totals for the session, including the number of successful tool calls and the final status.

<!-- BECKY CHECK ME: Confirm the exact output item names shown in the module (Response, Audit Trail, Summary). -->
