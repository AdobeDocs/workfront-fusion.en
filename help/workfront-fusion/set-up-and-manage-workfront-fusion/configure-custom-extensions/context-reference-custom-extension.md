# 6. The Fusion context reference

When your UI calls `attach(...)`, Fusion shares a **context** object describing the current session. This page lists every field, what it means, and how the Fusion and Adobe IMS identifiers relate.

## How to read the context

* **Initial values:** `connection.sharedContext.get("<key>")`
* **Updates:** listen for the `contextchange` event; the latest object arrives on `event.detail.context`.

See [Build the UI](./05-build-the-ui.md) for the full code pattern.

```js
const organization = connection.sharedContext.get("organization");
const fusionOrgId  = organization?.id;        // Fusion's organization id
const imsOrgId     = connection.sharedContext.get("imsOrgId"); // Adobe IMS org id
```

## Top-level keys

| Key | Type | Description |
|-----|------|-------------|
| `imsToken` | string | The signed-in user's Adobe **IMS access token**. Use it as a `Bearer` token to call Adobe or Fusion APIs on the user's behalf. **Sensitive â€” never log or display it.** |
| `imsOrgId` | string | The Adobe **IMS organization id**, in the form `XXXXXXXXXXXX@AdobeOrg`. |
| `imsUserId` | string | The Adobe **IMS user id** of the signed-in user. |
| `organization` | object | The **full active Fusion organization**. See table below. |
| `team` | object \| undefined | The **full active Fusion team**, when one is active (always relevant for `fusion/nav-team/1`). See table below. |
| `user` | object | The **full signed-in Fusion user**. See table below. |

### Fusion id vs. IMS id at a glance

Each entity has a **Fusion id** (used by Fusion's own APIs) and, where it exists, an **Adobe IMS id** (used by Adobe platform APIs):

| Entity | Fusion id | Adobe IMS id |
|--------|-----------|--------------|
| Organization | `organization.id` | `imsOrgId` (also exposed as `organization.externalOrgId`) |
| Team | `team.id` | *(teams are Fusion-only; no IMS id)* |
| User | `user.id` | `imsUserId` |

## `organization` fields

The active organization record. Most extensions need only `id`, `name`, and the identifiers; the rest is available if useful.

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Fusion organization id. |
| `name` | string | Organization display name. |
| `externalOrgId` | string | Adobe IMS organization id (same value as `imsOrgId`). |
| `externalId` | string | External identifier used by Fusion integrations. |
| `countryId` | string | Country setting id. |
| `timezoneId` | string | Time zone setting id. |
| `serviceName` | string | Service/plan identifier. |
| `teamIds` | string[] | Ids of teams in this organization. |
| `license` | object | Plan limits and entitlements (operations, data transfer, user seats, feature flags, etc.). |
| `scenariosCount` | number | Total scenarios in the organization. |
| `activeScenarios` | number | Currently active scenarios. |
| `activeApps` | number | Number of active apps/connections. |
| `operations`, `operationsExt` | number | Operations usage counters. |
| `transfer`, `transferExt` | number | Data-transfer usage counters. |
| `isPaused` | boolean | Whether the organization is paused. |
| `isDeleted` | boolean | Whether the organization is marked deleted. |
| `imsEnabled` | boolean | Whether the organization is linked to Adobe IMS. |
| `usersCount` | number | Number of users in the organization. |
| `nextReset` | string (date) | When usage counters next reset. See [Dates](#a-note-on-dates). |

## `team` fields

Present when a team is active. Always provide a fallback in case it is `undefined` (for example on an organization-level screen with no team selected).

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Fusion team id. |
| `name` | string | Team display name. |
| `organizationId` | string | Fusion id of the organization this team belongs to. |
| `country` | string | Team country setting. |
| `timezone` | string | Team time zone. |
| `license` | object | Team-level limits and entitlements. |
| `activeScenarios` | number | Active scenarios in the team. |
| `activeApps` | number | Active apps/connections in the team. |
| `scenarioDrafts` | boolean | Whether scenario drafts are enabled. |
| `isDeleted` | boolean | Whether the team is marked deleted. |
| `created` | string (date) | When the team was created. See [Dates](#a-note-on-dates). |

## `user` fields

The signed-in Fusion user.

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Fusion user id. |
| `name` | string | Full name. |
| `email` | string | Email address. |
| `avatar` | string | Avatar image URL. |
| `locale` | string | User locale (e.g. `en`). |
| `language` | string | Preferred language, when set. |
| `timezone` | string | Time zone name. |
| `timezoneId` | string | Time zone setting id. |
| `countryId` | string | Country setting id. |
| `localeId` | string | Locale setting id. |
| `features` | object | Per-user feature flags (e.g. `allow_apps`, `public_templates`). |
| `usersAdminsRoleId` | string | The user's admin role id, when applicable. |

> The `user` object may include additional internal fields. Rely only on the ones documented here; others can change without notice and some (authentication-related) must never be logged or displayed.

## A note on dates

The context is serialized before it reaches your extension, so **date fields arrive as strings** (ISO 8601, e.g. `"2026-06-24T00:00:00.000Z"`), not JavaScript `Date` objects. Convert them yourself if needed:

```js
const resetDate = new Date(context.organization.nextReset);
```

## When updates arrive

Fusion re-sends the whole context (via `contextchange`) when:

* the user **switches organization**,
* the user **switches team**, or
* the **signed-in user's** information changes.

Always re-read all the keys you use inside your `contextchange` handler rather than assuming only one value changed.

## Security reminders

* **Never log, display, or persist `imsToken`.** Treat it like a password.
* Send the token only to trusted Adobe/Fusion endpoints, over HTTPS, as a `Bearer` token.
* Do not store personal data from the context beyond what your feature needs.

Next: [Publish your extension â†’](./07-publish.md)
