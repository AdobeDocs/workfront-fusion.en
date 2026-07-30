---
name: fusion-release-notes
description: Create a new Workfront Fusion weekly release note page, and wire it into the release activity overview page and the TOC. Use when the user wants to write, add, or draft a new Fusion release note or weekly release page, or asks to document new Fusion features for a release. Do not use for Workfront (Quicksilver) release notes in product-announcements/product-releases — use release-notes-formatter for those.
---

# Fusion Release Notes

Creates a new weekly Adobe Workfront **Fusion** release note page in `help/workfront-fusion/fusion-product-releases/`, and links it from the two places that make it discoverable: the release activity overview page and `help/workfront-fusion/TOC.md`.

This is a different system from the Quicksilver (core Workfront) release notes handled by the `release-notes-formatter` skill:

| | Fusion release notes (this skill) | Quicksilver release notes (`release-notes-formatter`) |
|---|---|---|
| Cadence | Weekly | Quarterly |
| Directory | `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/` | `help/quicksilver/product-announcements/product-releases/` |
| Per-feature date callout | No — the page title carries the week | Yes — `>[!NOTE]` block per feature |
| Index page | `fusion-release-activity.md` (by year/month) | `{YY}-q{N}-release-overview.md` (by quarter) |

## Step 1: Gather the features

Ask the user (if not already provided) for the list of features/changes to document for the week, and for each one:

- A short feature title
- A plain description of what changed and why it matters
- The help article(s) it links to (verify the path exists — do not guess)
- Whether it requires user/admin action or is a deprecation (needs an `>[!IMPORTANT]` callout)

## Step 2: Determine the file name and date

- Find the Monday (or release date) for the week being documented and confirm it with the user if ambiguous.
- File path: `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md`
  - `{M}` and `{D}` have **no leading zeros**: `fusion-2026-7-20.md`, not `fusion-2026-07-20.md`.
  - If the year folder doesn't exist yet, create it.
- Check whether a page for that week already exists before creating a new one.

## Step 3: Write the page

### Frontmatter

```yaml
---
title: Workfront Fusion release activity Week of {Month} {Day}, {Year}
description: Workfront Fusion release activity Week of {Month} {Day}, {Year}
author: {Author}
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
```

Rules:
- `title` and `description` are identical.
- Always include the comma in the date (`July 20, 2026`), even though some older pages omit it — don't copy that inconsistency.
- **Use `hidefromtoc: true` for every new page. Do not add an `exl-id` or `TQID`.** Those are assigned later once the page is published; inventing one is wrong. (Pages from mid-2026 onward all follow this pattern — see `_fusion-release-notes-reference.md` if you need to check an example.)

### Body

```markdown
# Workfront Fusion release activity: Week of {Month} {Day}, {Year}

This page describes all enhancements made in Adobe Workfront Fusion the week of {Month} {Day}, {Year}.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/en/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## {Feature title}

Feature description paragraph(s) — what changed, why, and how it affects existing scenarios/configurations if relevant.

For more information, see [{Help article title}](/help/workfront-fusion/{path-to-article}.md).

## {Next feature title}

...
```

Notes:
- One H2 per feature, in the order the user gave them (no forced newest-first ordering within the page — it's a single week).
- No `>[!NOTE]` date callout per feature — the page title already carries the date.
- If a feature requires action or is a breaking change/deprecation, add an `>[!IMPORTANT]` callout directly under the H2, before the description:
  ```markdown
  ## {Feature title}

  >[!IMPORTANT]
  >
  >**Action Required: {short summary of what the user must do and by when}**
  >
  >{Details of the requirement.}

  {Regular description paragraph(s).}
  ```
- Every feature should end with a "For more information, see [...]" link to the relevant help article. Verify the link target exists in the repo.

## Step 4: Add the page to the overview index

Edit `help/workfront-fusion/fusion-product-releases/fusion-release-activity.md`:

- Find the `## Fusion releases in {current year}` section (it is **not** wrapped in a `+++` collapsible block — only past years are collapsed).
- Find or create the `### {Month} {Year}` heading for the release's month, directly under the year heading.
  - If the month heading doesn't exist yet, add it **above** the previous month (newest month first).
- Add the new page as the **first** bullet under that month heading (newest week first):
  ```markdown
  * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```
- If this is the first release of a new year, add a new `## Fusion releases in {YYYY}` heading above the previous year's heading, and wrap the *previous* year's section in a `+++ **Click to open**` / `+++` collapsible block if it isn't already (only the current year stays expanded).

## Step 5: Add the page to the TOC

Edit `help/workfront-fusion/TOC.md`:

- Find `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}` for the current year, nested under `* Fusion release activity {#fusion-release-activity}`.
- Add the new page as the **first** entry under that heading (newest first), matching existing indentation (8 spaces):
  ```markdown
        * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```
- If the current year's heading doesn't exist yet, add `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}` above the previous year's heading.
- **Do not** add the `{hide-from-toc}` prefix to new entries — that's only used for older entries once they age out of the visible nav (see Known Inconsistencies below).

### Known inconsistencies to watch for (don't replicate)

- Several early-2026 TOC entries are nested under the `Fusion releases - 2025` heading by mistake, even though the pages themselves are 2026 releases. When adding a new entry, always double check it lands under the heading matching **its own year**, not wherever the previous entry happens to sit.
- Some older page titles/H1s omit the comma before the year (`July 13 2026` instead of `July 13, 2026`). Always use the comma in new pages.

## Step 6: Final checklist

- [ ] File created at the correct path with no leading zeros in the date
- [ ] Frontmatter uses `hidefromtoc: true`, no invented `exl-id`/`TQID`
- [ ] Title/description match, date includes comma
- [ ] Each feature has a description and a verified "For more information" link
- [ ] Action-required/deprecation features have an `>[!IMPORTANT]` callout
- [ ] New page added as the newest entry in `fusion-release-activity.md`, under the correct year/month
- [ ] New page added as the newest entry in `TOC.md`, under the correct year heading
- [ ] New year/month headings created if needed, with the previous year collapsed in `fusion-release-activity.md`

## Additional resources

For full worked examples (a straightforward multi-feature week, and one with an `>[!IMPORTANT]` action-required callout), see `.claude/commands/_fusion-release-notes-reference.md`.
