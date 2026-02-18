---
title: Model Context Protocol (MCP) modules
description: The Model Context Protocol (MCP) module allows you to process a user prompt using MCP.
author: Becky
feature: Workfront Fusion
hide: yes
hidefromtoc: yes
exl-id: 748055ad-d305-4513-9a5c-9c970b74a96e
---
# MCP Agent module

<!--SET UP REDIRECTS-->

Model Context Protocol (MCP) is a way to securely connect AI language models with other applications. You configure MCP servers, which allow the AI model to access the application. You can then send a prompt to the AI model, and it can return information from the application.

For example, you could configure a MCP server to connect an AI model with Gmail. When you send the prompt "Give me my last 5 emails from Gmail," it can access your Gmail and return the emails.

The Model Context Protocol (MCP) module allows you to process a user prompt using a language model and MCP servers.

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

## Prerequisites

* You must have configured any MCP servers that you intend to connect to.
* You must have an LLM key to the selected LLM (Large Language Model).

## Model Context Protocol module and its fields

### Process User Prompt

This action module processes a prompt, using the language model and MCP servers you specify.

>[!NOTE]
>
>This module must return an object. It does not return output such as strings or numbers.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>LLM key</td> 
   <td> Select an existing LLM key, or create a new one  by clicking <b>Add</b> and entering the following information: 
     <ul>
       <li><b>Key name</b>: Enter a name for the new key.</li>
       <li><b>LLM</b>: Select the large language model that this key is associated with.</li>
       <li><b>Key</b>: Enter or map your API key for the selected model.</li>
       <li><b>Model</b>: Select the LLM model that the key will use.</li>
       <li><b>Max Tokens</b>: Enter or map the maximum number of tokens that the LLM can generate in its response.<p>One token usually equals four characters, or .75 of a word in English. "Hello world" would equal two tokens, and "Authentication" would equal one to two tokens.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>MCP Servers</td> 
   <td> <p>For each MCP server that you want to connect to, click <b>Add</b> and enter the following information: </p> 
     <ul>
       <li><b>Connection</b>: Select the connection that Fusion will use to connect to the MCP server.</li>
       <li><b>MCP Server Host</b>: Enter the URL of the MCP server.</li>
       <li><b>MCP Server Name</b>: Enter or map a name for this MCP server.</li>
       <li><b>Headers</b>: Add any applicable headers.</li>
       <li><b>MCP Server Type</b>: Select the server type.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>Enter your prompt </td> 
   <td> <p>Enter or map the prompt that you want to process.</p> </td> 
  </tr> 
 </tbody> 
</table>


