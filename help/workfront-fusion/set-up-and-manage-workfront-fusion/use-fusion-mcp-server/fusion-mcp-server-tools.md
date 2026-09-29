---
title: Adobe Workfront Fusion MCP server tools
description: Reference list of the tools that the Adobe Workfront Fusion MCP server exposes to AI agentic platforms and Coworker.
---

# Adobe Workfront Fusion MCP server tools


This article lists the tools that the Adobe Workfront Fusion MCP server exposes to a connected AI agent. The agent calls these tools on your behalf when you ask it to find, inspect, create, run, update, or delete Fusion items.

The same tools are available in every supported surface: custom MCP connections in Claude, ChatGPT, Copilot, or your own agent; and Coworker, both standalone and in the Fusion right rail. For setup, see [Configure the Adobe Workfront Fusion MCP server](configure-fusion-mcp-server.md).

The agent acts in Fusion using your Adobe ID, your Fusion organization role, and your team roles. A tool only works if you have the corresponding permission in Fusion. Adobe is not responsible for changes the agent makes to your Fusion data.

## Read and write actions

Each tool is classified as:

* **Read** — retrieves information without changing anything (for example, listing scenarios or getting an execution).
* **Write** — creates, changes, runs, or deletes Fusion data (for example, cloning a scenario or clearing a webhook queue).

## Organization tools

The active organization applies to all other tools in the current session.

| Tool | Name | Action | Description |
| --- | --- | --- | --- |
| List organizations | `fusion_orgs_list` | Read | Lists the Fusion organizations you can access, with ID, region (zone), and label. |
| Set active organization | `fusion_orgs_set` | Session | Switches the active organization for the current session. Doesn't change any Fusion data. |

## Scenario tools

### Scenarios

| Tool | Name | Action | Description |
| --- | --- | --- | --- |
| List scenarios | `fusion_scenarios_list` | Read | Lists scenarios in the organization. |
| Get scenario | `fusion_scenarios_get` | Read | Returns a scenario, including its full blueprint. |
| Get scenario dependencies | `fusion_scenarios_getDependencies` | Read | Returns the connections, keys, data stores, data structures, and webhooks the scenario's blueprint references. |
| Find dependent scenarios | `fusion_scenarios_dependents` | Read | Finds scenarios that reference a given webhook, data store, data structure, connection, key, or scenario. Useful for impact analysis before changing or deleting a resource. |
| Validate blueprint | `fusion_scenarios_validate_blueprint` | Read | Structurally validates a blueprint against a team (module references, connections, required fields) without saving anything. |
| Create scenario | `fusion_scenarios_create` | Write | Creates a scenario in a team from a blueprint, with optional name, description, folder, scheduling, and sequential processing. |
| Clone scenario | `fusion_scenarios_clone` | Write | Clones a scenario into the same or a different team. When cloning across teams, you map each connection, webhook, data store, data structure, and key to a target resource. Optionally continues from the last processed record. |
| Update scenario | `fusion_scenarios_update` | Write | Changes name, description, folder, scheduling, or active state (activate/deactivate). Can also restore a deleted scenario. |
| Run scenario once | `fusion_scenarios_execute` | Write | Runs a scenario once and waits (up to a timeout) for the result, returning status and any error message. Not supported for instant (webhook-triggered) scenarios. |
| Delete scenario | `fusion_scenarios_delete` | Write | Deletes a scenario. Deleted scenarios can be restored with **Update scenario**. |

Example prompts:

* _Which active scenarios in the Marketing team haven't been edited in 6 months?_
* _What connections does the "Salesforce → Workfront sync" scenario use?_
* _Clone "Lead intake" into the Sales team and swap in the Sales Salesforce connection._
* _Validate this blueprint before I import it._
* _Run "Nightly report" once and tell me if it succeeds._

### Scenario versions

| Tool | Name | Action | Description |
| --- | --- | --- | --- |
| List scenario versions | `fusion_scenario_versions_list` | Read | Lists saved versions of a scenario. Filter by `version`, `createdAt`, `comment`. |
| Get scenario version | `fusion_scenario_versions_get` | Read | Returns the blueprint and metadata for a specific version. |

Example prompts:

* _What changed between version 12 and version 14 of this scenario?_

### Folders

| Tool | Name | Action | Description |
| --- | --- | --- | --- |
| List folders | `fusion_folders_list` | Read | Lists scenario folders, with scenario counts. |
| Create folder | `fusion_folders_create` | Write | Creates a folder in a team. |
| Rename folder | `fusion_folders_update` | Write | Renames a folder. |
| Delete folder | `fusion_folders_delete` | Write | Deletes a folder. |

## Execution tools

| Tool | Name | Action | Description |
| --- | --- | --- | --- |
| List executions | `fusion_executions_list` | Read | Lists executions for a scenario or for an incomplete execution. Filter by `status` (for example `status==3` for errors, `status==2` for warnings), `timestamp`, `duration`, `bundles`, `operations`, `transfer`. Optionally includes check runs. |
| Get execution | `fusion_executions_get` | Read | Returns a single execution and metadata about its scenario or incomplete execution. |

Example prompts:

* _Show me failed runs of "Invoice sync" from yesterday and summarize the errors._
* _Which execution of this scenario used the most operations this week?_

## Operations (usage) tools

| Tool | Name | Action | Description |
| --- | --- | --- | --- |
| Get operations | `fusion_operations_get` | Read | Returns an operations time series (by day or month) for a date range of up to 1 year. Filter by team, scenario, or package; group by module, package, scenario, or team. |
| Get operations summary | `fusion_operations_summary_by_org` | Read | Returns total operations per scenario and team for a date range, plus the overall total. |

Example prompts:

* _Top 10 scenarios by operations last month._
* _How many operations did the Salesforce app use in Q3?_

## Connection and key tools

These tools return metadata only. They don't return credentials, tokens, or secret values. `[TBD: confirm]`

| Tool | Name | Action | Description |
| --- | --- | --- | --- |
| Search connections | `fusion_connections_search` | Read | Lists connections. Filter by `name`, `accountName`, `accountType`, `expire`, `teamId`, `scopesCount`, `editable`, `environmentType`, `authenticationType`. |
| Get connection | `fusion_connections_get` | Read | Returns details for a single connection. |
| Search keys | `fusion_keys_search` | Read | Lists keys. Filter by `name`, `typeName`, `teamId`. |
| Get key | `fusion_keys_get` | Read | Returns details for a single key. |

Example prompts:

* _Which connections expire in the next 30 days, and which scenarios use them?_

## Webhook tools

### Webhooks

| Tool | Name | Action | Description |
| --- | --- | --- | --- |
| List webhooks | `fusion_hooks_list` | Read | Lists webhooks (hooks). Filter by `name`, `teamId`, `type`, `enabled`, `gone`, `typeName`, `scenarioId`, `priority`, `detached`, and more. |
| Get webhook | `fusion_hooks_get` | Read | Returns a webhook's configuration, owner binding, and external references. |
| Find dependent webhooks | `fusion_hooks_dependents` | Read | Finds webhooks that reference a given connection. |

### Webhook queue

| Tool | Name | Action | Description |
| --- | --- |--------| --- |
| Get queue stats | `fusion_queue_stats` | Read   | Returns the number of queued events, the queue limit, and whether the webhook is enabled. |
| List queue | `fusion_queue_list` | Read   | Lists received webhook events waiting to be processed. |
| Get queue item | `fusion_queue_get` | Read   | Returns a single queued event, including its decoded payload. |
| Delete queue items | `fusion_queue_delete` | Write  | Deletes specific queued events (up to 50) or clears the queue, optionally excluding some events. Events currently processing can't be deleted. |

Example prompts:

* _Is the "Form submissions" webhook backing up?_
* _Show me the payload of the oldest queued event._

## Data store and data structure tools

| Tool | Name | Action | Description |
| --- | --- | --- | --- |
| List data stores | `fusion_datastores_list` | Read | Lists data stores with record count, size, and maximum size. |
| Get data store | `fusion_datastores_get` | Read | Returns a data store's metadata and usage, linked data structure, and strict-validation setting. |
| List data store records | `fusion_data_list` | Read | Reads records (key + JSON data) from a data store, with offset paging. |
| Find dependent data stores | `fusion_datastores_dependents` | Read | Finds data stores that use a given data structure. |
| Search data structures | `fusion_data_structures_search` | Read | Lists data structures. Filter by `name`, `strict`, `teamId`. |
| Get data structure | `fusion_data_structures_get` | Read | Returns a data structure, including its full field specification. |

Example prompts:

* _Which data stores are over 80% full?_
* _Show me the first 20 records in the "Customer map" data store._

## Activity log tools

| Tool | Name | Action | Description |
| --- | --- | --- | --- |
| List activity logs | `fusion_activity_logs_list` | Read | Lists audit events for the organization (who did what, to which entity, when). Filter by `entity` (for example `scenario`, `connection`, `webhook`, `data store`, `user`), `action` (for example `created`, `deleted`, `updated`, `transferred ownership`), user, team, and timestamp. |
| Export activity logs | `fusion_activity_logs_export` | Read | Exports activity logs as CSV or XLSX, using the same filters. |

Example prompts:

* _Who deleted scenarios in the last 7 days?_
* _Export all connection changes this quarter to Excel._

## Coworker

All tools in this article are available in Coworker, both standalone and in the Fusion right rail, subject to the same Read/Write settings and your permissions. `[TBD: list any tools that are hidden or behave differently in these surfaces, e.g. org switching in Coworker in the Fusion right rail follows the org selected in the UI]`

## How tools are updated

When Adobe releases a new version of the Fusion MCP server, connected agents pick up the updated tool set automatically. You don't need to reconnect.

