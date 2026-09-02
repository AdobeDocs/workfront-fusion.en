---
name: fusion-doc-request
description: Handle a Fusion documentation request from the #fusion-documentation Slack template - update the relevant Fusion docs article(s) in this repo, then create a matching task in the Product Documentation Workfront project with the feature description and a formatted release note filled in on the custom form. Use when the user shares a Slack documentation-request thread/message for a Fusion feature, or says something like "please update and create a task" for one.
---

# Fusion Documentation Request

Handles the recurring "New documentation request from {person}" pattern posted in the `#fusion-documentation` Slack channel: read the request, update the docs, then create a tracking task on the same Workfront custom form used for every prior request of this kind.

This is a different workflow from the `fusion-release-notes` skill. This skill updates a reference article and creates a Workfront task; it does not create or update a weekly Fusion release note page in this repo, even if the request says "Needs announcement: Yes". Only use `fusion-release-notes` if the user separately asks for a weekly release note.

## Step 1: Get the request details

If given a Slack link, parse the `channel_id` and `message_ts` out of the URL and fetch the thread (`slack_get_thread_replies` or `slack_read_thread`, depending on which Slack MCP tool is connected - try both if one fails). Keep the thread's permalink/URL - it's needed in Step 3.

Slack connections in this environment are flaky (expired tokens, disconnects mid-session). If a fetch fails:
- Retry once.
- If it still fails, tell the user plainly that the fetch failed and ask them to paste the request content directly. Don't guess at the content, and don't silently give up without saying so.

The request template has these fields - extract each one:

* **Feature Title**
* **Description**
* **Points to be added to documentation** *(sometimes present - specific sections/details the requester wants covered; treat these as required, not optional, if given)*
* **Expected release date**
* **Needs announcement** *(Yes/No - informational only; see the note above. Do not act on this field.)*

If the request links to a Confluence wiki page with the full spec, fetch it (`get_wiki_content`) before writing documentation. Don't rely on the Slack summary alone for technical details (exact field names, steps, UI labels) - pull those from the wiki spec when one is linked.

## Step 2: Update the documentation

Find the relevant existing article(s) in this repo (grep for related module names, UI labels, or settings names - don't guess the file). Update them to reflect the change, following that article's existing structure, heading level, and house style.

* Do not invent technical details (exact field names, permission scopes, config steps) that aren't in the Slack request or linked wiki spec. If something is unconfirmed, flag it inline as an HTML comment (e.g. `<!-- BECKY CHECK ME: confirm the exact permission scope before publishing -->`) rather than guessing - never as a visible callout. It must not render on the published page.
* If this requires a brand-new article file (not just an edit to an existing one), follow this repo's standing conventions: no fabricated `exl-id`/`TQID` in frontmatter, wire the new page into the relevant TOC, and convert the file to CRLF/no-BOM after creating it (the `Write` tool defaults to LF).

## Step 3: Create the Workfront task

Project: **Product Documentation tasks - for development Issues that require messaging**. Resolve its ID with `insights_find_id_by_name` (entity `project`) rather than hardcoding it, in case it ever changes - see Known values below for the last resolved ID.

Task fields:

| Field | Value |
|---|---|
| `name` | `Becky - {Feature Title}` |
| `projectID` | from the project lookup above |
| `assignedToID` | the current user, from `insights_get_current_user` |
| `categoryID` | the Product Documentation custom form ID - see Known values below. If it's ever unclear, query `task.task_categoryID` on any recent sibling task in this project to confirm. |
| `description` | the **complete Slack message text** (all fields from the request template, not a paraphrase), followed by a link to the Slack conversation |
| `DE:Release notes` | a formatted release note, see format below |
| `DE:Preview Date Known` | `Yes`, by default |
| `DE:Preview Date` | the request's **Expected release date**, by default |

Set the preview date fields as part of this same create call - don't leave them for later or wait to be asked. If the user gives a different date later, or says the date isn't actually known yet, update accordingly, but default to filling them in every time.

Release note format for the `DE:Release notes` field. Always start with `***FUSION***` on its own line, then a blank line, then the title - this marks the note as belonging to Fusion (as opposed to core Workfront) at a glance:

```markdown
***FUSION***

## {Feature Title}

{Description of what changed and why it matters, in second person. A sentence or two is enough for a simple change - use multiple paragraphs and/or a bulleted list for anything with several parts or steps, the same way a full weekly release note would.}

For more information, see [{Article title}](/help/workfront-fusion/{path-to-article}.md).
```

Before the create call, call `read_workflow_docs` with `workfront://tools/create-any-object` - this call sets custom fields and an enum value (`DE:Preview Date Known`), which requires it per the MCP server's rules.

## Step 4: Confirm back to the user

Report plainly:

* Which doc file(s) you changed and what you added.
* The task name and URL.
* The exact field values you set, including the preview date fields.
* Anything you weren't fully confident about - e.g. Slack was unreachable and you worked from pasted text only, the target doc article was ambiguous, or a technical detail wasn't in the source material and got flagged instead of guessed.

## Known values (from prior runs)

Confirm these still resolve rather than assuming they're permanent:

* Project "Product Documentation tasks - for development Issues that require messaging" maps to ID `5e69583f00236b9f767c3e3944100ee4`
* Product Documentation custom form (`categoryID`) is `5d7275b9000514604bd969d418725843`
* Custom fields used: `DE:Release notes`, `DE:Preview Date Known`, `DE:Preview Date`
