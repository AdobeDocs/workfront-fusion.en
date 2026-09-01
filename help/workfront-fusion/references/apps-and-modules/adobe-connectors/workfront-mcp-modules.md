---
title: Adobe Workfront MCP modules
description: With the Adobe Workfront MCP module, you can send a plain-English prompt to Adobe Workfront's MCP server and let an AI model carry out the request.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# Adobe Workfront MCP modules

The Adobe Workfront MCP connector is a dedicated Fusion integration for Adobe Workfront's own Model Context Protocol (MCP) server. Unlike a typical connector, where each module performs one fixed action, this connector has a single module that accepts an open-ended, plain-English instruction and lets an AI model decide which Workfront operations are needed to fulfill it.

For example, you could enter the prompt "Find all my active projects that are behind schedule and summarize their status," and the module returns a synthesized answer, instead of you having to chain together several Get and Filter modules.

You can restrict which Workfront actions the AI is allowed to take, so that even an unattended scenario can guarantee no unexpected destructive action is taken.

By default, this module uses Adobe Managed AI, which uses the `claude-sonnet-5` model. You can configure the module to use a different LLM, using a key and other credentials you provide.

>[!NOTE]
>
>Usage of Adobe Managed AI is limited to $25 per organization, per month.

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
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Connect Adobe Workfront MCP to Workfront Fusion

The Adobe Workfront MCP connector uses OAuth 2.0 to connect to Workfront. Unlike other Workfront connectors, there are no manual connection fields, such as a host, Client ID, or Client Secret, to fill in.

To create a connection:

1. In the Adobe Workfront MCP module, click **[!UICONTROL Add]** next to the Connection field.
1. Fill in the following fields:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Enter a name for this connection.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Select whether you are connecting to a production or non-production environment.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Select whether you are connecting to a service account or a personal account.</td>
      </tr>
    </tbody>
    </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.

   If you are not logged in to Workfront, you are directed to a login screen. Log in and approve access.

You are redirected back to Workfront Fusion, and the new connection is available in the module.

>[!NOTE]
>
>On first use, the connection automatically registers itself with Workfront's MCP server and reuses that registration for every subsequent connection you create.

## Adobe Workfront MCP module and its fields

### Process a user prompt

This action module processes a plain-English prompt against Workfront's MCP server, using the language model you specify, and returns the AI's answer.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 

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
  </tr>   <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-adobe-workfront-mcp-to-workfront-fusion" class="MCXref xref">Connect Adobe Workfront MCP to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>Read-only tools <i>(Optional)</i></td> 
   <td> <p>Restrict which read-only Workfront actions the AI is allowed to call. If no tools are selected, all read-only tools are allowed.</p> </td> 
  </tr> 
  <tr> 
   <td>Write/delete tools <i>(Optional)</i></td> 
   <td> <p>Enter the write or delete Workfront actions that the AI is allowed to call. If you leave this empty, all write and delete tools are allowed.</p> <p>To guarantee that an unattended scenario never takes a destructive action, we recommend leaving this field set to a deliberately empty selection rather than leaving it unrestricted.</p> </td> 
  </tr> 
  <tr> 
   <td>Enter your prompt</td> 
   <td> <p>Enter or map the instruction, in plain English, that you want the AI to carry out.</p> <p>Example: <i>Find all projects assigned to me that are behind schedule.</i></p> </td> 
  </tr>  </tbody> 
</table>

For a list of the tools you can select for the Read-only tools and Write/delete tools fields, see [Adobe Workfront MCP server tools](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-tools) in the Workfront documentation.

The module returns the following information, which you can map in subsequent modules in the scenario:

* **Response**: The AI's final answer, as text.
* **Audit Trail**: A record of the session, including the original prompt, start and end time, and details for each tool call the AI made, such as the tool name, arguments, whether it succeeded, duration, and output.
* **Summary**: Totals for the session, including the number of tool calls attempted, how many succeeded or failed, total processing time, and overall status.
