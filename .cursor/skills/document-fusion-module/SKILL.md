---
name: document-fusion-module
description: Document a new Adobe Workfront Fusion connector module by adding it to the appropriate connector article under help/workfront-fusion/references/apps-and-modules/. Use when the user asks to add, document, or describe a new Fusion module, or when the user provides screenshots of a Fusion module configuration panel and wants the corresponding article updated.
---

# Document a Fusion connector module

Use this skill to add a new module to a Workfront Fusion connector article (for example, `adobe-firefly-modules.md`, `adobe-photoshop-modules.md`, `azure-dev-ops.md`).

## Required inputs

Before writing any documentation, the user **must** provide all three of the following. If any is missing, stop and ask for it.

1. **The connector article path** — for example, `help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-firefly-modules.md`. If the user gives only the connector name, infer the path from the directory layout under `help/workfront-fusion/references/apps-and-modules/`.
2. **The API URL** for the underlying API operation (for example, an Adobe developer docs URL). This is required so each field's purpose can be cross-referenced against the API spec.
3. **Two screenshots** of the module's configuration panel in Fusion:
   - **Standard view** — `Show advanced settings` checkbox **unchecked**.
   - **Advanced view** — `Show advanced settings` checkbox **checked**.

If the module has no advanced fields, the user must say so explicitly. Don't assume.

## Workflow

Follow these phases in order. Don't skip ahead.

### Phase 1 — Place the placeholder

1. Read the connector article to understand its existing structure and conventions.
2. Find the alphabetical position for the new module among the existing `### Module name` headings.
3. Insert a placeholder section in that position with this shape:

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

4. Confirm the placeholder is correctly positioned before continuing.

### Phase 2 — Capture each visible field

Work through the screenshots top to bottom. For each visible field:

1. Use the field's exact UI label as the row header. For grouped fields (e.g., `Background → Image → Source`), join with ` > `:
   ```
   [!UICONTROL Background > Image > Source]
   ```
2. Read the helper text under the field in the screenshot (the gray/yellow caption). Use it as the basis for the description.
3. Cross-reference the API URL the user provided to identify what the field represents in the underlying API call (for example, `background.fillAreaMask` is "the area of the background where the object will be placed").
4. Write the description by combining both: **what the field is** (from the API) plus **how to provide it** (from the UI helper text and field type).

Skip any field that isn't visible in the screenshots, even if the API supports it. Don't invent fields.

### Phase 3 — Mark advanced fields

For every field that only appears in the advanced view (not the standard view):

1. Append `*` to the field name inside the `<td role="rowheader">`:
   ```html
   <td role="rowheader">[!UICONTROL Seeds]*</td>
   ```
2. After the closing `</table>`, add this footnote on its own line (or reuse it if the article already has one for another module):
   ```markdown
   * These fields are advanced fields, and do not display unless you select **[!UICONTROL Show advanced settings]**.
   ```

### Phase 4 — Verify against the conventions checklist

Before declaring the module done, confirm:

- [ ] Module heading is `### ` (H3) and uses sentence case.
- [ ] Module appears in alphabetical order relative to its sibling modules.
- [ ] First row is `Connection` and uses the standard connection-link wording.
- [ ] Every documented field is visible in the user's screenshots.
- [ ] Advanced fields are marked with `*` and a single footnote exists below the table.
- [ ] No fields invented from the API alone.
- [ ] Source dropdown descriptions use the exact UI option labels (see "Source field convention" below).
- [ ] Module description at the top is one sentence, written in third person, describing what the module does.

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

## What to do if information is conflicting

When the API spec and the UI disagree (this happens often):

1. **Trust the UI**, because that's what the user actually sees in Fusion.
2. **Note the discrepancy** in your reply to the user so they can decide whether to investigate further.
3. **Don't invent an explanation** in the article body — keep it factual to what's in the UI.

If two screenshots from the user contradict each other, stop and ask which one is correct before writing.

## What to ask the user before finishing

Before declaring the work complete, ask the user to confirm:

1. Whether there are any fields above or below the visible screenshot area you didn't capture.
2. The proposed module description at the top of the section.
3. Whether the module has any deprecation status (a deprecated predecessor or an upcoming deprecation note).
