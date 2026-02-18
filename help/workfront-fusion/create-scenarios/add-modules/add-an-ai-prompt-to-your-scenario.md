---
title: Add an AI Prompt to Your Scenario
description: You can include an AI prompt in your scenario that connects to your
author: Becky
feature: Workfront Fusion
exl-id: d0ac0d0b-e3a0-46de-801d-e53c1c4d63ff
---
# Add an AI prompt to your scenario

You can include an AI prompt in your scenario using Model Context Protocol (MCP) combined with large language models (LLMs). By configuring these in the MCP Agent module, you can use artificial intelligence to set up workflows that are efficient, secure, and flexible.

>[!NOTE]
>
>This functionality is separate from the ability to add modules to a scenario using AI.
>
>For information on adding modules with AI, see [Generate a scenario segment using AI](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-with-ai.md).

## Overview of Model Context Protocol

Model Context Protocol (MCP) is a way to securely connect AI language models with other applications. You configure MCP servers, which allow the AI model to access the application. You can then send a prompt to the AI model, and it can return information from the application.

For example, you could configure a MCP server to connect an AI model with Gmail. When you send the prompt "Give me my last 5 emails from Gmail," to the large language model, it parses that prompt and sends it to the Gmail MPC server, which can then access your Gmail and return the emails.

The MCP Agent module allows you to process a user prompt using a language model and MCP servers.

## Benefits of using MCP in your Fusion scenarios

Using MCP in your scenarios offers the following benefits:

* Using MCP in your scenario reduces the need to think through all of the situations and possible variations of an action. By using a prompt, you eliminate the need to use regex or parse data to account for these variations.
* You can provide context to the prompt by using elements mapped from previous modules, or other functions in the mapping panel.
* Using a prompt can be more efficient and flexible than building a scenario with specific modules, because it can use reasoning on the prompt and select the best course of action from the available context.
* Because you configure the MCP servers that the module can connect to, you control the security for that server, and can be sure that the security fits the needs of your organization. 

>[!NOTE]
>
>Available functionality depends on the tools available in the MCP server, and is not controlled by Fusion.

## Add an AI prompt to your scenario

You can add an AI prompt to your scenario by using the MCP Agent module.

For instructions, see [MCP Agent module](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md).
