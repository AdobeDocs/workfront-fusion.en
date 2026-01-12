---
title: Math
description: In an Adobe Workfront Fusion scenario, you can use the math module to calculate math expressions.
author: Becky
feature: Workfront Fusion
---
# MCP (Model Context Protocol) modules

Model Context Protocol is a way to connect large language models with other applications, allowing you to use a prompt to generate an action or workflow in the application. The MCP Agent module brings this functionality into Workfront Fusion.

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

You must have Workfront Fusion connections to the applications that you are using the MCP Agent module to connect to.

## MCP Agent modules and their fields

The only available module for the MCP Agent transformer is the Process User Prompt module.

### Process user prompt

This transformer uses the selected large language model to connect to the specified servers, using a prompt.

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
       <li><b>Max Tokens</b>: </li>
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
   <td> <p>Enter or map the prompt that you want to process..</p> </td> 
  </tr> 
 </tbody> 
</table>
