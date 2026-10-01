---
title: Adobe Marketo Engage MCP module
description: The Adobe Marketo Engage MCP module allows you to send a natural-language prompt to Adobe Marketo Engage's MCP (Model Context Protocol) server.
author: Becky
feature: Workfront Fusion
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
    internal-label: APIs
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
  - id: e14a7f57-c82c-4874-a495-5d036cbbdc3d
    internal-label: Resource management
subfeature_v2:
  - id: b70a979b-965d-47a9-a360-e7ec2a19b8c1
    internal-label: Digital content and documents
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Adobe Marketo Engage MCP module

The Adobe Marketo Engage MCP module allows you to send a natural-language prompt to Adobe Marketo Engage's MCP (Model Context Protocol) server, using an AI model to interpret the request and call Marketo's own tools to fulfill it. Unlike a traditional Marketo connector where each module does one fixed action, such as "Create a Lead", this connector has a single module that accepts an open-ended instruction in plain English and lets the AI decide which Marketo operations are needed to satisfy it.

This connector is for Marketo Engage's own MCP server specifically

To connect to MCPs for other applications, see see [Add an AI prompt to your scenario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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

* You must have an Adobe Marketo Engage account and a valid Marketo instance.

## Connect Adobe Marketo Engage MCP to Workfront Fusion {#connect-adobe-marketo-engage-mcp-to-workfront-fusion}

You can create a connection to your Marketo instance directly from inside the Adobe Marketo Engage MCP module.

1. In the Adobe Marketo Engage MCP module, click **Add** next to the **Connection** field.
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
          <p>Enter a name for the new connection.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Select whether you are connecting to a production or non-production environment.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Select whether you are connecting to a service account or a personal account.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>
          <p>Enter the Client ID for your Marketo REST API service, as created in Marketo LaunchPoint.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>
          <p>Enter the Client Secret for your Marketo REST API service, as created in Marketo LaunchPoint.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Munchkin ID]</td>
        <td>
          <p>Enter your Marketo instance's Munchkin ID (for example, `123-ABC-456`). The Munchkin ID is shown in Marketo under <b>Admin → Munchkin</b>.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Click **Continue** to create the connection and return to the module.

>[!IMPORTANT]
>
> * Use a dedicated API-only Marketo user with the minimum role and permissions required for the scenario, rather than reusing an administrator account.
> * Creating the connection does not validate the credentials. Fusion saves them without a test call, so the connection can appear to be created successfully even if a value is wrong or mistyped. If a credential is incorrect, the failure usually appears later when the module first tries to reach Marketo or when the tool lists fail to load.

## The module: "Process a user prompt"

This is the only module the connector provides. A scenario uses it by supplying:

1. **Connection** — the Marketo connection created above.
2. **Enter your prompt** — the instruction, in plain English (for example, "find every lead added to the Spring Webinar list in the last week and tell me which ones have no company name set").
3. **Tools** (optional) — described below. These fields only appear once a connection is selected.
4. **LLM key** (optional, advanced) — described below.

It returns the AI's final answer as text, plus a full audit trail of what happened while producing that answer.

### What comes back

The output is a single **Data** bundle containing three parts:

- **Response** — the AI's final answer, as text. This is what most scenarios will map into the next module.
- **Audit Trail** — the detailed record of the run: a session ID, the original prompt, start/end times, total duration, overall status, the final response, and a **Tool Calls** list. Each tool call entry records which Marketo tool ran, its arguments, its output, its start/end time and duration, whether it succeeded, and its order in the sequence.
- **Summary** — the same run condensed to counts: total tool calls, successful calls, failed calls, processing time, and status.

The audit trail is useful material for the docs: it's what lets a user see *how* the AI arrived at an answer and exactly which changes it made in Marketo — worth calling out for anyone running this unattended or needing a record for compliance.

### Which AI model answers the prompt

By default, **no configuration is needed at all** — the module uses Adobe's own managed AI service automatically, with no key or credentials to enter. This is the expected, zero-setup path for most users.

Advanced users can instead select a specific "LLM key" (a saved API credential) to use a different AI provider — OpenAI, Anthropic Claude, or Amazon Bedrock — if they have their own account with one of those and want to use it instead of Adobe's default service. The field is marked advanced and is optional; most users will never need it.

### Choosing which Marketo actions the AI is allowed to take

Once a connection is selected, the module asks the Marketo MCP server what tools it offers and presents them as multi-select lists, each showing how many tools it contains:

- **Read-only tools** — actions that only look something up (find a lead, list campaign members, read a program's details) and never change anything.
- **Write/delete tools** — actions that change something (create or update a lead, add someone to a list, activate a campaign, approve or send an email).
- **Other tools** — a third list that appears only if the Marketo server offers tools it hasn't labelled as read-only or not. These are shown separately rather than being assumed safe or unsafe. If the server labels everything, this list doesn't appear at all.

A user can leave the lists untouched to let the AI use anything it needs. Or they can restrict a list to specific actions — for example, selecting only 2 specific "write" actions while leaving "read-only" alone means the AI can look up whatever it needs freely, but can only make those 2 specific kinds of changes, nothing else. **Leaving a list empty means "all actions in that category are allowed," not "none"** — restricting the AI requires actively choosing which specific actions to allow in that category.

This exists so a cautious user (or a scenario meant to run unattended, without anyone watching) can guarantee the AI won't take an unexpected destructive action against live marketing data, while still letting it freely gather information.

Because the lists are read live from the Marketo server, the exact tools shown — and the counts in the field labels — can change as Adobe updates that server. Docs shouldn't promise a fixed list.

### One prompt, one answer — no back-and-forth

Each run of this module is a single, self-contained execution — like asking someone a question over email rather than a live phone call. The AI cannot ask a follow-up question and wait for a reply; it must make its best judgment and produce a complete, final answer in one pass. If a request is ambiguous, the AI will make a reasonable assumption, state that assumption as part of its answer, and proceed — it will not stop and ask the user to clarify, because there's no way for it to receive a reply within a single run.

The AI is also instructed to verify facts with a tool call rather than rely on memory — checking a lead's current state, a list's membership, or a campaign's status before acting — because Marketo data may have changed since anything it saw earlier.

And it is instructed to only take a write, update, or delete action when the prompt actually asked for one. It won't take an extra "helpful" action that wasn't requested — explicitly including activating or deactivating campaigns, creating or deleting leads and lists, and approving or sending emails — even in the same run where it's doing something else the user did ask for.

### Continuing a conversation across multiple runs

Because each run is independent, the AI has no memory of a previous run by itself. A scenario that wants a multi-turn, chat-like experience (for example, "ask a follow-up about the previous answer") has to explicitly provide that history as part of the new prompt — for example, by storing the previous question and answer (in Fusion's Data Store, or passed between modules) and including it as text at the start of the new prompt, followed by the new question. This is a scenario-design pattern, not something the module does automatically — there is no "session" or "conversation ID" that automatically remembers prior runs. (The session ID in the audit trail identifies one run for tracing; it is not a handle for resuming anything.)

## Good example prompts to draw from

These illustrate the intended range without naming internal tools:

- "List the leads that joined the 'Q3 Product Launch' program in the last 7 days and summarize which industries they're from."
- "Check whether the 'Welcome Series' smart campaign is currently active, and tell me how many people are in it."
- "Find the form used on our pricing page and tell me which fields are marked required."
- "Add the lead with email jane@example.com to the 'VIP Customers' static list."
- "Summarize the performance of every email in the 'Spring Newsletter' program."

## What a content writer should NOT claim

- **Don't describe the connection as an OAuth or "sign in with Adobe" flow.** It isn't one. It's three credential fields the user copies out of Marketo's LaunchPoint and Munchkin admin pages. Screenshots or steps borrowed from the AEM MCP connector docs would be wrong here.
- **Don't imply the connection form validates the credentials.** It saves them without testing them.
- Not a substitute for individual Marketo action-modules — it's a single, flexible AI-driven module, not a set of deterministic single-purpose modules.
- Results are AI-generated and can occasionally be imperfect, even with every safeguard above in place — appropriate for automation where a human isn't reviewing every single run in real time, but not a guarantee of 100% deterministic behavior the way a traditional Marketo module is. This deserves extra emphasis for Marketo specifically, because a write action here can email real customers or alter real lead records.
- The read/write tool split limits what categories of *Marketo actions* the AI can take — it is not a way to sandbox or limit what the AI is capable of reasoning about or discussing in its answer text.
- Don't name specific Marketo MCP tools/actions unless verified against the live tool list — this document intentionally describes capability areas (leads, lists, campaigns, programs, emails, forms, snippets, bulk operations) rather than exact tool names, since the server's exact tool set may evolve.
- Don't state Marketo API rate limits, quotas, or daily call caps as if this connector defines them. Any such limit comes from the user's own Marketo subscription and REST API allowance; verify with the Marketo team before publishing numbers.

## Reference links used while compiling this

- Adobe Marketo Engage MCP server (developer documentation):
  https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server
