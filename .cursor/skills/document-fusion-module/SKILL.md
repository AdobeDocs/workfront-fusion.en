---
name: document-fusion-module
description: Document a new Adobe Workfront Fusion connector module by adding it to the appropriate connector article under help/workfront-fusion/references/apps-and-modules/. Use when the user asks to add, document, or describe a new Fusion module, or when the user provides screenshots of a Fusion module configuration panel and wants the corresponding article updated.
---

# Document a Fusion connector module

Use this skill to add one or more new modules to a Workfront Fusion connector article (for example, `adobe-firefly-modules.md`, `adobe-photoshop-modules.md`, `azure-dev-ops.md`).

## Required inputs (per module)

Before populating any module's fields, the user **must** provide all of the following. If any is missing, stop and ask for it before proceeding.

1. **The module name** — exactly as it appears in the Fusion UI (e.g., `Generate adaptive composite`).
2. **The connector article path** — the agent locates this and confirms with the user (see Phase 1).
3. **The API URL** for the underlying API operation. This is required so each field's purpose can be cross-referenced against the API spec.
4. **A screenshot of the module's configuration panel in standard view** (`Show advanced settings` **unchecked**).
5. **A screenshot of the module's configuration panel in advanced view** (`Show advanced settings` **checked**), or an explicit statement that the module has no advanced fields.

## Workflow

This is a multi-phase process. The pacing matters — work *with* the user, not ahead of them. Confirm progress at each phase boundary, and stay open to corrections at any time.

### Phase 1 — Scope the work

1. **Ask whether this is one module or multiple**: *"Are you adding a single module or multiple modules to a connector article?"*

2. **Gather every module name upfront**, based on the answer:
   - **Single module**: ask for its exact name as it appears in the Fusion UI.
   - **Multiple modules**: ask for all of the names at once, OR ask for a screenshot of the connector that lists them (for example, the connector overview screen in Fusion that shows tile labels for each module). Either way, end this step with a confirmed list of every new module to be added.

3. **Locate the connector article yourself** by searching `help/workfront-fusion/references/apps-and-modules/` based on the connector name implied by the module(s). Use the `Glob` or `Grep` tools.

4. **Confirm the article path with the user**: *"Based on the module name(s), this should go in `help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-firefly-modules.md`. Is that correct?"*

5. **Read the connector article** to learn its existing structure and conventions. Pay attention to:
   - Heading style (typically `### Module name` in sentence case)
   - Existing module ordering (typically alphabetical)
   - How `Connection` rows are worded
   - How nested fields are written (e.g., `Image > Source`)
   - Any existing footnote or annotation conventions

### Phase 2 — Place placeholders for every module up front

Even if there's only one new module, this gives the user a clear visual roadmap. If there are multiple new modules, place all of them now.

For each new module, insert a placeholder section in alphabetical position:

```markdown
### Module name

<!-- PLACEHOLDER: Add description of the Module name module here. -->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Connector Name], see <a href="#create-a-connection-to-connector-name" class="MCXref xref" >Create a connection to [!DNL Connector Name]</a> in this article.</td> 
  </tr> 
  <!-- PLACEHOLDER: Add field rows for the Module name module here. -->
 </tbody> 
</table>
```

Show the user the list of placeholders that were added (e.g., "Added placeholders for: Generate adaptive composite, Generate images with Image5, Generate precise composite, Generate video"). Then ask which to start with: *"Which would you like to start with?"*

### Phase 3 — Per-module documentation loop

For each module, complete this loop fully before moving on to the next:

#### 3a. Get the API URL

Ask the user for the API URL: *"Please share the API URL for `<module name>`'s underlying API operation."*

When you have it:
- Try `WebFetch` on the URL.
- If the page is empty/JS-rendered (common with Adobe Developer docs), look for a related feature guide page — typically at a `.../guides/how-tos/...` URL — and fetch that instead.
- If still no luck, fall back to `WebSearch` for the operation name.

Use whatever you learn as background context for field descriptions later. Don't dump it on the user; just acknowledge it briefly: *"Got the API context — ready for the standard view screenshot."*

#### 3b. Get the standard-view screenshot

Ask: *"Please share a screenshot of the module's configuration panel with `Show advanced settings` **unchecked**. After we work through the standard fields, I'll ask for the advanced view, but don't send that yet."*

#### 3c. Document the standard fields

Working from the standard-view screenshot, capture every visible field top to bottom. For each field:

1. Use the field's exact UI label as the row header. For grouped fields, join with ` > `:
   ```
   [!UICONTROL Background > Image > Source]
   ```
2. Read the helper text under the field in the screenshot (the gray/yellow caption). Use it as the basis for the description.
3. Cross-reference the API context from step 3a to identify what the field represents (for example, `background.fillAreaMask` is "the area of the background where the object will be placed").
4. Write the description by combining **what the field is** (from the API) with **how to provide it** (from the UI helper text and field type).

Skip any field that isn't visible in the screenshot, even if the API supports it. Don't invent fields.

After the standard fields are in place, briefly summarize them to the user (e.g., "Standard fields added: Connection, Prompt, Aspect Ratio, ..."), then move to step 3d.

#### 3d. Get the advanced-view screenshot

Ask: *"Now please share a screenshot of the module's configuration panel with `Show advanced settings` **checked**. If the module has no advanced fields, say so and we'll skip ahead."*

#### 3e. Document the advanced fields

Working from the advanced-view screenshot:

1. Identify the fields that *aren't* already in the standard view — those are the advanced fields.
2. For each advanced field, follow the same description process from step 3c.
3. Append `*` to the field name inside the `<td role="rowheader">`:
   ```html
   <td role="rowheader">[!UICONTROL Seeds]*</td>
   ```
4. After the closing `</table>`, add this footnote on its own line:
   ```markdown
   * These fields are advanced fields, and do not display unless you select **[!UICONTROL Show advanced settings]**.
   ```

If the user said the module has no advanced fields, skip steps 3d and 3e entirely.

#### 3f. Draft the module description

Now (not earlier), replace the description placeholder at the top of the section with a one-sentence draft based on the API context and what the fields imply. Always offer it as a draft for the user's review:

> *"I drafted this description: '...'. Want to use that, edit it, or replace it?"*

#### 3g. Per-module wrap-up

Give the user a final summary of the module's documented fields (standard + advanced), and surface any open questions:

- Were any fields cut off in the screenshots?
- Is the module description acceptable?
- Should anything be flagged as deprecated or note-worthy?

Wait for confirmation before saying the module is done. Then ask: *"Ready to move on to the next module?"* (or "We're all done with this connector article.")

### Phase 4 — Final verification

After all modules are documented, run through this checklist for each one:

- [ ] Module heading is `### ` (H3) and uses sentence case.
- [ ] Module appears in alphabetical order relative to its sibling modules.
- [ ] First row is `Connection` and uses the standard connection-link wording.
- [ ] Every documented field is visible in the user's screenshots.
- [ ] Advanced fields are marked with `*` and a single footnote exists below the table.
- [ ] No fields invented from the API alone.
- [ ] Source dropdown descriptions use the exact UI option labels (see "Source field convention" below).
- [ ] Module description is a one-sentence summary describing what the module does.

## Source field convention

Image source fields in Fusion connectors typically present a dropdown with two options. **Use the exact labels shown in the user's screenshot** — different generations of modules use different wording:

| If the dropdown shows... | Use this format |
|---|---|
| **Upload Image** and **Image URL** (newer modules) | `<ul><li><b>Upload Image</b><p>Upload the image, or map the image file from a previous module.</p></li><li><b>Image URL</b><p>Enter or map the URL of the image.</p></li></ul>` |
| **File** and **Presigned URL** (older modules) | `<ul><li><b>File</b><p>Select a source file from a previous module, or map the source file's reference image file name and reference image file.</p></li><li><b>Presigned URL</b><p>Enter or map the URL of the source image.</p></li></ul>` |

If the screenshot doesn't show the dropdown options open, ask the user to share them.

## Field description style

- Match the voice and structure of existing module entries in the same article.
- Keep descriptions brief: one or two sentences per field is usually enough.
- Use `[!UICONTROL ...]` markup for any UI field name referenced from another field.
- Use `<code>...</code>` for literal values (`<code>en-US</code>`, `<code>0.0</code>`).
- For numeric range fields, state the allowed range explicitly: *"Enter a number between 0 and 1..."*.
- For dropdowns with discrete options, enumerate them as a `<ul>` with `<b>Option</b>` followed by `<p>` description.

## Common fields and recommended descriptions

Reuse these for consistency across modules:

**Seeds** (when the field allows multiple seed values via Add item):
> Click **Add item** to add a seed value, then enter or map an integer. Use one seed per variation. The count of seed values must match the **Number of Variations** value if both are provided.

**Number of Variations** (replace the range with the actual range from the screenshot):
> Enter a number between [min] and [max]. The module generates this number of [output type] variations.

**Limit** (the standard Fusion execution-cycle limit; only include if visible in the screenshot):
> Enter or map the maximum number of results that you want the module to work with during one execution cycle.

**Locale**:
> Enter or map a language and region code to tailor the generated content to a specific country and language. Locale must be provided in ISO 639-1 language code and ISO 3166-1 region. Example: `en-US`

## Be open to corrections at any time

The user may correct earlier work mid-flow — Seeds wording, dropdown labels, field positioning, advanced/standard split, etc. Treat any correction as authoritative and update without pushback. After the correction, briefly summarize what was changed.

If the user introduces a new convention mid-flow (for example, "let's mark advanced fields with `*` and add a footnote"), adopt it for the rest of the session and apply it retroactively to any modules already documented.

## What to do if information is conflicting

When the API spec and the UI disagree (this happens often):

1. **Trust the UI**, because that's what the user actually sees in Fusion.
2. **Note the discrepancy** in your reply to the user so they can decide whether to investigate further.
3. **Don't invent an explanation** in the article body — keep it factual to what's in the UI.

If two screenshots from the user contradict each other (e.g., one shows `Blend`, another shows `Harmonization` for the same module), stop and ask which one is correct before writing. Identify which screenshot likely belongs to a different module by cross-referencing the API spec.
