---
title: Configure the Adobe Workfront Fusion MCP server
description: Connect Adobe Workfront Fusion to an MCP-compatible AI agentic platform, or to Coworker (standalone or in the Fusion right rail).
---

# Configure the Adobe Workfront Fusion MCP server

The Adobe Workfront Fusion MCP server lets you work with your Fusion organization's' scenarios, executions, connections, webhooks, data stores, and more, through natural-language conversation in a supported AI agentic platform.

For a list of tools available in the Adobe Workfront Fusion MCP server, see [Adobe Workfront Fusion MCP server tools](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-fusion-mcp-server/fusion-mcp-server-tools.md).

## Supported AI agentic platforms

The Fusion MCP server works with any AI agentic platform that supports Model Context Protocol (MCP) and remote (Streamable HTTP) MCP servers with OAuth.

>[!NOTE]
>
> Adobe does not currently publish a Workfront Fusion connector in the Claude connectors directory or the ChatGPT app/plugin directory. To use Fusion with Claude, ChatGPT, or Microsoft Copilot, add it as a **custom MCP server** by URL, as described in this article.

This article walks through the connection steps for:

* [Adobe Coworker](#use-fusion-with-coworker): Coworker as a standalone and Coworker in the Fusion right rail
* [Claude](#connect-fusion-to-claude): Custom connector
* [ChatGPT](#connect-fusion-to-chatgpt): Custom MCP server
* [A custom MCP solution](#connect-fusion-to-a-custom-mcp-solution)

>[!IMPORTANT]
>
>If you use a different MCP-compatible platform such as Gemini, Cursor, or VS Code, follow that platform's documentation for adding a custom MCP server. When prompted for the MCP server URL, enter:
>
>```
>https://mcp.fusion.adobe.com/mcp
>```

## Prerequisites

Before you can connect Fusion to an AI agentic platform, you must:

* Have an active Adobe Workfront Fusion license and access to at least one Fusion organization.
* Have a Fusion user role and team roles that grant access to the data you want to work with.
* Sign in with an Adobe ID (Adobe Identity Management System, IMS).
* Have access to an MCP-compatible AI agentic platform, or to Coworker.

## Use Fusion with Coworker

Coworker is Adobe's AI agent. Fusion is built into Coworker, so you don't need to enter an MCP URL or register an OAuth app. You can use Coworker with Fusion in two places:

* [Coworker (standalone)](#use-fusion-in-coworker): Work with Fusion alongside your other Adobe apps.
* [Coworker in the Fusion right rail](#use-coworker-in-the-fusion-right-rail): Open Coworker in a panel inside the Fusion UI.

Both use the same Fusion MCP tools, your Adobe ID, and your Fusion permissions. The Read or Write MCP tools settings apply in both. Destructive actions, such as delete, clear queue, or overwrite, always ask for confirmation.

### Use Fusion in Coworker

1. Open Coworker.
2. Open **Customization** > **Integrations**
3. Find **fusion-mcp** and click **Test**.
4. If you have access to more than one Fusion organization it will be auto selected. You can ask Coworker to switch organization later if necessary.

### Use Coworker in the Fusion right rail

In Fusion, Coworker opens in the right rail

1. Sign in to Workfront Fusion.
2. Click the **Coworker** icon in the right rail.
3. Ask a question in the panel.

### Example prompts

* *Show me all scenarios that failed to execute in the last 24 hours.*
* *List all scenarios created or deleted this week, sorted by most recent first.*
* *What is this scenario doing?*
* *Why did this execution fail?*

## Connect Fusion to Claude

Add Fusion as a custom connector.

>[!NOTE]
>
> In Claude Team/Enterprise, you must be an owner to add a custom connector. For information, see [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp) in the Claude documentation..

1. Sign in to [Claude](https://claude.ai).
2. In the left menu, select **Customize**.
3. Select **Connectors**.
4. Select **+**, then **Add custom connector**.
5. Enter a name (for example, "Workfront Fusion") and the MCP server URL:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

6. Click **Connect**.
7. Sign in. Select a profile and Fusion organization.

For Claude Code, you can add the server from the command line:

```
claude mcp add --transport http fusion-mcp https://mcp.fusion.adobe.com/mcp
```

## Connect Fusion to ChatGPT

Add Fusion as a custom MCP server.

### ChatGPT Desktop or Codex

1. In ChatGPT, open **Settings**.
2. Click **Plugins**.
3. Click **Add server**.
4. Enter a name for the server.
5. For the type, select **Streamable HTTP**.
6. Enter the MCP server URL:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

7. Click **Save**.
8. Click **Authenticate** for the new server and sign in.
9. Make sure the toggle next to the server is on.

### ChatGPT on the web

1. Sign in to [ChatGPT](https://chatgpt.com).
2. Go to [https://chatgpt.com/plugins](https://chatgpt.com/plugins). (Developer mode may need to be enabled under **Settings**; on Business/Enterprise plans, an admin must allow custom connectors.)
3. Click **+**.
4. Enter a **Name**.
5. For **Connection**, select **Server URL** and enter the MCP server URL.
6. Leave **Authentication** set to **OAuth**.
7. Read the risk message and select the checkbox.
8. Click **Create**, then sign in with your.

## Connect Fusion to a custom MCP solution

If you're building your own application or agent, connect to the Fusion MCP server directly.

## Switch to a different Fusion organization

You don't need to disconnect to change organizations. The Fusion MCP server can switch the active organization within a session:

* _Which Fusion organizations do I have?_
* _Switch to the 1234 organization._

The agent uses `fusion_orgs_list` and `fusion_orgs_set`. The switch applies to the current conversation/session only. Organizations in different data-center zones (for example, US and EU) are all available through the same MCP URL.

## Troubleshoot setup and authentication

| Problem | Likely cause | Fix |
| --- | --- | --- |
| You can't find a Fusion connector in the Claude or ChatGPT directory. | Adobe doesn't publish a directory connector for Fusion. | Add Fusion as a custom MCP server using the URL in this article. |
| You can't add a custom connector in Claude or ChatGPT. | Your plan restricts custom connectors to owners or administrators. | Ask your Claude or ChatGPT administrator to add the connector or allow custom MCP servers. |
| You connected but see no data, or the wrong data. | The wrong Fusion organization is active. | Ask the agent to list your organizations and switch to the right one. |
| Authentication failed or the connection stopped working. | Session expired or connection error. | Disconnect and reconnect the server. |
| You see a message that MCP access is disabled. | MCP access is turned off for your Fusion organization. | Ask your Fusion administrator to enable it. |
| The agent can read scenarios but can't create, run, update, or delete them. | Write MCP tools are disabled, or your team role doesn't allow it. | Ask your Fusion administrator to enable write tools, or to grant you the required team role. |
| Custom app authentication is rejected. | Callback URL isn't on the authorized list. | Ask your administrator to add the exact callback URL. |
| Fusion isn't listed in Coworker, or Coworker is missing from the Fusion right rail. | Feature not enabled for your organization. <!-- BECKY CHECK ME: confirm whether this is the correct admin guidance before publishing. --> | Contact your Fusion administrator. |

## Frequently asked questions

### Is there an official Fusion connector for Claude or ChatGPT?

Not at this time. Use the custom MCP server URL. Coworker (standalone and in the Fusion right rail) has Fusion built in.

### Can I use more than one Fusion organization?

Yes. You can switch the active organization during a conversation without reconnecting.

### What can the agent do on my behalf?

The agent acts as you, using your Fusion role and team permissions. It can't access anything you can't access in Fusion. Destructive actions require explicit confirmation.

### Does the agent see my connection secrets?

No. Connection and key tools return metadata (name, type, scopes, expiration), not credentials or secret values.
