---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: fusion
navigation-topic: workfront-fusion-navigation-topic
title: The Fusion context reference
description:  The Fusion context reference
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
---
# The Fusion context reference

>[!NOTE]
>
>This article assumes some familiarity with software development tools. 

When your UI calls `attach(...)`, Fusion shares a **context** object describing the current session. This page lists every field, what it means, and how the Fusion and Adobe IMS identifiers relate.

## How to read the context

* **Initial values:** `connection.sharedContext.get("<key>")`
* **Updates:** Listen for the `contextchange` event. The latest object arrives on `event.detail.context`.

For the full code pattern, see See [Build the custom extension UI](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).

```js
const organization = connection.sharedContext.get("organization");
const fusionOrgId  = organization?.id;        // Fusion's organization id
const imsOrgId     = connection.sharedContext.get("imsOrgId"); // Adobe IMS org id
```

## Top-level keys

| Key | Type | Description |
| ----- | ------ | ------------- |
| `imsToken` | string | The signed-in user's Adobe **IMS access token**. Use this as a `Bearer` token to call Adobe or Fusion APIs on the user's behalf. **Because this is sensitive, never log or display it.** |
| `imsOrgId` | string | The Adobe **IMS organization id**, in the form `XXXXXXXXXXXX@AdobeOrg`. |
| `imsUserId` | string | The Adobe **IMS user id** of the signed-in user. |
| `organization` | object | The **full active Fusion organization**. For more information, see [`organization` fields](#organization-fields) in this article. |
| `team` | object \| undefined | The **full active Fusion team**, when one is active (always relevant for `fusion/nav-team/1`). For more information, see [`team` fields](#team-fields) in this article. |
| `user` | object | The **full signed-in Fusion user**. For more information, see [`user` fields](#user-fields) in this article. |

### Fusion ID and IMS ID

Each entity has a **Fusion ID** (used by Fusion's own APIs) and, where it exists, an **Adobe IMS ID** (used by Adobe platform APIs):

| Entity | Fusion id | Adobe IMS id |
| -------- | ----------- | -------------- |
| Organization | `organization.id` | `imsOrgId` (also exposed as `organization.externalOrgId`) |
| Team | `team.id` | *(Teams are Fusion-only; no IMS id)* |
| User | `user.id` | `imsUserId` |

## `organization` fields

THese fields are found in the active organization record. Most extensions require only `id`, `name`, and the identifiers. 

| Field | Type | Description |
| ------- | ------ | ------------- |
| `id` | string | Fusion organization ID. |
| `name` | string | Organization display name |
| `externalOrgId` | string | Adobe IMS organization ID (same value as `imsOrgId`). |
| `externalId` | string | External identifier used by Fusion integrations |
| `countryId` | string | Country setting ID. |
| `timezoneId` | string | Time zone setting ID |
| `serviceName` | string | Service/plan identifier |
| `teamIds` | string[] | IDs of teams in this organization |
| `license` | object | Plan limits and entitlements, such as operations, data transfer, user seats, and feature flags |
| `scenariosCount` | number | Total scenarios in the organization |
| `activeScenarios` | number | Currently active scenarios |
| `activeApps` | number | Number of active apps or connections |
| `operations`, `operationsExt` | number | Operations usage counters |
| `transfer`, `transferExt` | number | Data-transfer usage counters |
| `isPaused` | boolean | Whether the organization is paused |
| `isDeleted` | boolean | Whether the organization is marked deleted |
| `imsEnabled` | boolean | Whether the organization is linked to Adobe IMS |
| `usersCount` | number | Number of users in the organization |
| `nextReset` | string (date) | When usage counters next reset. See [Dates](#dates) |

## `team` fields

These fields are present when a team is active. You must provide a fallback in case the team is `undefined` (for example on an organization-level screen with no team selected).

| Field | Type | Description |
| ------- | ------ | ------------- |
| `id` | string | Fusion team ID. |
| `name` | string | Team display name. |
| `organizationId` | string | Fusion ID of the organization this team belongs to. |
| `country` | string | Team country setting. |
| `timezone` | string | Team time zone. |
| `license` | object | Team-level limits and entitlements. |
| `activeScenarios` | number | Active scenarios in the team. |
| `activeApps` | number | Active apps or connections in the team. |
| `scenarioDrafts` | boolean | Whether scenario drafts are enabled. |
| `isDeleted` | boolean | Whether the team is marked deleted. |
| `created` | string (date) | When the team was created. See [Dates](#dates). |

## `user` fields

These fields apply to the signed-in Fusion user.

| Field | Type | Description |
| ------- | ------ | ------------- |
| `id` | string | Fusion user ID. |
| `name` | string | Full name. |
| `email` | string | Email address. |
| `avatar` | string | Avatar image URL. |
| `locale` | string | User locale , such as `en`. |
| `language` | string | Preferred language, when set. |
| `timezone` | string | Time zone name. |
| `timezoneId` | string | Time zone setting id. |
| `countryId` | string | Country setting ID. |
| `localeId` | string | Locale setting ID. |
| `features` | object | Per-user feature flags (e.g. `allow_apps`, `public_templates`). |
| `usersAdminsRoleId` | string | The user's admin role ID, when applicable. |

>[!NOTE]
>
> The `user` object may include additional internal fields. You should rely only on the fields documented her. Other fields can change without notice, and some authentication-related must never be logged or displayed.

## Dates 

The context is serialized before it reaches your extension, so **date fields arrive as strings** (ISO 8601, such as `"2026-06-24T00:00:00.000Z"`), not JavaScript `Date` objects. You can convert these if needed:

```js
const resetDate = new Date(context.organization.nextReset);
```

## Context updates

Fusion re-sends the whole context (via `contextchange`) when:

* the user **switches organization**,
* the user **switches teams**, or
* the **signed-in user's** information changes.

Always re-read all the keys you use inside your `contextchange` handler rather than assuming only one value changed.

## Security best practices

* **Never log, display, or persist `imsToken`.** Treat it like a password.
* Send the token only to trusted Adobe/Fusion endpoints, over HTTPS, as a `Bearer` token.
* Do not store personal data from the context beyond what your feature needs.

## Use the token to call APIs

To turn `imsToken` (plus `organization.id` / `team.id`) into real Workfront or
Fusion data, you cannot call those APIs directly from the browser, because CORS blocks
it. Route the call through a small App Builder runtime action instead. See
[Calling Workfront & Fusion APIs](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom%20extension-10-calling-apis.md).


To continue the process of creating a custom extension, see [Publish your extension](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
