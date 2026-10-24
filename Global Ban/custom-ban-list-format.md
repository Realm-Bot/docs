---
label: Custom Ban List Format
description: Prepare a public GitHub JSON ban list for preview in Realm Bot's Ban List Explorer.
order: 95
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Custom Ban List Format

This guide explains how to create, publish, maintain, and preview a custom ban list in Realm Bot's **Ban List Explorer**.

A compatible custom list is:

- A publicly accessible JSON file.
- Stored in a public GitHub repository.
- Structured as an array of ban records.
- Limited to supported fields and values.
- Suitable for public viewing.
- Loaded through the **Custom GitHub List** option in the Ban List Explorer.

> **Important:** A custom list is preview-only. Loading one will not import it into the Realm Hub Database, approve it as a trusted source, enforce its bans, create Realm operations, or enable appeals.

Realm Bot identifies a successful custom-list preview internally as `github-compatible-v1`. Do not add a format wrapper to the source file. The root of the file must be the ban-record array itself.

## Compatibility Levels

A custom list can provide extensive Explorer functionality, but it is not equivalent to a native Realm Hub Database source.

| Feature | Custom GitHub preview |
|---|---:|
| Display players and reasons | Yes |
| Search by gamertag or XUID | Yes |
| Ban-type filtering | Yes, when `type` is supplied |
| Status filtering | Yes, when `status` is supplied |
| Duration filtering | Yes, when `expiresAt` is supplied |
| Recorded-date sorting | Yes, when `effectiveAt` is supplied |
| Reported Realm column | Yes, when `reportedRealm` is supplied |
| Public evidence links | Yes, when `evidence` is supplied |
| CSV export fields | Yes, based on available fields |
| Profile avatars resolved by Realm Bot | No |
| Realm Hub public case numbers | No |
| Realm Hub record detail pages | No |
| Account-owned appeals | No |
| Staff report and evidence-review workflow | No |
| Automatic Global Ban enforcement | No |
| Realm ban operations | No |
| Trusted source registration | No |
| Database import or synchronisation | No |

There is no JSON property that can turn a custom preview into an enforced Realm Hub source. Trusted source integration requires a separate Realm Bot staff review and implementation process.

## Quick Start

To create a compatible list:

1. Create a public GitHub repository or use an existing public repository.
2. Create a file ending in `.json`, such as `ban-lists/community-bans.json`.
3. Make the root value a JSON array.
4. Add one object per ban record.
5. Include `xuid`, `username`, and `reason` in every record.
6. Add supported optional fields where needed.
7. Commit and push the file to GitHub.
8. Open Realm Bot's **Ban List Explorer**.
9. Select **Custom GitHub List**.
10. Paste the public GitHub file URL.
11. Select **Load List**.
12. Check the records, filters, dates, durations, and evidence links.

A successful preview validates the current file. It does not permanently register or enable the list.

## Minimal Valid List

The smallest supported record contains `xuid`, `username`, and `reason`.

```json
[
  {
    "xuid": "2535431508056414",
    "username": "ExamplePlayer",
    "reason": "Example public moderation reason"
  }
]
```

A minimal list displays:

- Player name.
- XUID.
- Public reason.
- Basic gamertag or XUID search.

It does not enable status, type, duration, date, Realm, or evidence columns.

## Full Compatibility Example

This example enables every optional custom-list capability.

```json
[
  {
    "xuid": "2535431508056414",
    "username": "ExamplePlayer",
    "reason": "Destructive activity affecting multiple areas of the Realm.",
    "type": "nuking",
    "status": "active",
    "effectiveAt": "2026-08-01T12:00:00.000Z",
    "expiresAt": null,
    "updatedAt": "2026-08-02T09:15:00.000Z",
    "reportedRealm": "Example Realm",
    "evidence": [
      {
        "url": "https://example.com/public-evidence/example-player-1.png",
        "title": "Public Screenshot",
        "caption": "Staff-approved screenshot associated with the moderation record."
      }
    ]
  },
  {
    "xuid": "2535431508056415",
    "username": "AnotherPlayer",
    "reason": "Use of prohibited gameplay modifications.",
    "type": "cheating",
    "status": "expired",
    "effectiveAt": "2026-07-01T18:30:00Z",
    "expiresAt": "2026-08-01T18:30:00Z",
    "updatedAt": "2026-08-01T18:30:00Z",
    "reportedRealm": "Example Realm",
    "evidence": []
  }
]
```

The first record is permanent because `expiresAt` is explicitly `null`.

The second record is temporary because `expiresAt` contains a date. Its `status` is separately marked as `expired`.

The Explorer does not infer `status` from `expiresAt`. Publishers must keep these fields consistent.

## Root Structure

The JSON root must be an array:

```json
[
  {
    "xuid": "2535431508056414",
    "username": "ExamplePlayer",
    "reason": "Example reason"
  }
]
```

Do not wrap the records in an object:

```json
{
  "records": [
    {
      "xuid": "2535431508056414",
      "username": "ExamplePlayer",
      "reason": "Example reason"
    }
  ]
}
```

The wrapped version is invalid.

Standard JSON rules also apply:

- Do not include comments.
- Do not leave trailing commas.
- Use double quotes around property names and strings.
- Escape quotation marks inside strings.
- Save the file as valid UTF-8.
- Keep the `.json` file extension.

An empty array, `[]`, is valid and displays zero records.

## Record Fields

| Field | Required | Accepted value | Limit and behaviour |
|---|---:|---|---|
| `xuid` | Yes | String containing exactly 16 digits | Must be quoted. Numeric values are rejected. |
| `username` | Yes | Non-empty string | Maximum 64 characters. Displayed as the player's gamertag. |
| `reason` | Yes | Non-empty string | Maximum 2,000 characters. |
| `type` | No | Supported ban-type identifier | Enables the Ban Type column and filter. |
| `status` | No | `active`, `expired`, or `revoked` | Enables the Status column and filter. |
| `effectiveAt` | No | ISO 8601 date-time or `null` | A non-null value enables the Recorded column and date sorting. |
| `expiresAt` | No | ISO 8601 date-time or `null` | Enables Duration and Expiry support. |
| `updatedAt` | No | ISO 8601 date-time or `null` | Retained as source metadata. It does not replace `effectiveAt` for Recorded sorting. |
| `reportedRealm` | No | String, `null`, or empty value | Maximum 160 characters. A non-empty value enables the Reported Realm column. |
| `evidence` | No | Array of evidence objects | Maximum eight evidence entries per record. |

Although the website calls the displayed value a gamertag, the required JSON property is `username`, not `gamertag`.

Control characters are removed from text fields and surrounding whitespace is trimmed. Use readable text without embedded control characters or multiline formatting.

Unknown record properties are ignored. They do not create new columns or Realm Bot capabilities and should not be relied upon.

## XUID Requirements

Every record must use a 16-digit Xbox User ID:

```json
"xuid": "2535431508056414"
```

These examples are invalid:

```json
"xuid": 2535431508056414
```

```json
"xuid": "253543150805641"
```

```json
"xuid": "PlayerName"
```

Always store the XUID as a quoted string. This prevents JSON and JavaScript number-precision problems.

Use the XUID as the stable player identity. Gamertags can change, but the XUID should remain associated with the same Xbox account.

## Supported Ban Types

Use the exact lowercase identifier in the `type` field.

| Display name | JSON value | Suggested use |
|---|---|---|
| Nuking | `nuking` | Large-scale destructive activity |
| Crashing | `crashing` | Deliberately disrupting clients, Realms, or services |
| Cheating | `cheating` | Prohibited unfair gameplay modifications or tools |
| Exploiting | `exploiting` | Abusing software, game, command, or system flaws |
| Harassment | `harassment` | Targeted abusive or intimidating conduct |
| Threats | `threats` | Credible or serious threatening conduct |
| Ban Evasion | `ban_evasion` | Returning through another account or bypassing enforcement |
| Other | `other` | Conduct that does not fit another supported category |

Example:

```json
"type": "ban_evasion"
```

Values such as `Ban Evasion`, `ban-evasion`, `Nuking or Crashing`, and `unknown` are not accepted.

If `type` is omitted, the Explorer treats the record as legacy or untyped and displays it as **Other**. An omitted type does not enable the Ban Type capability when every record omits it.

Use `"type": "other"` explicitly when the record is intentionally categorised as Other.

Realm Bot does not infer a type from the reason text.

## Supported Status Values

| Status | Meaning |
|---|---|
| `active` | The moderation record is currently active |
| `expired` | A temporary record has reached its end |
| `revoked` | The record was withdrawn or overturned |

Example:

```json
"status": "active"
```

If `status` is omitted, the record is treated as having an unknown status. Do not supply `"unknown"` because it is not an accepted source status.

`null`, an empty string, uppercase values, and custom status names are rejected.

The Explorer does not calculate status from the dates. Update `status` when a temporary record expires or when a decision is revoked.

## Dates and Durations

Dates must use a complete ISO 8601 date-time with a timezone.

Accepted examples:

```json
"effectiveAt": "2026-08-01T12:00:00Z"
```

```json
"effectiveAt": "2026-08-01T12:00:00.000Z"
```

```json
"effectiveAt": "2026-08-01T13:00:00+01:00"
```

Date-only values and date-times without a timezone are rejected:

```json
"effectiveAt": "2026-08-01"
```

```json
"effectiveAt": "2026-08-01T12:00:00"
```

Realm Bot accepts zero to three fractional-second digits. The date must end with `Z` or a timezone offset such as `+01:00`.

### `effectiveAt`

`effectiveAt` represents the date used by the Explorer's **Recorded** column and recorded-date sorting.

A valid non-null `effectiveAt` enables recorded-date support for the list.

### `expiresAt`

The presence and value of `expiresAt` determine duration:

| Source value | Explorer duration |
|---|---|
| Field omitted | Unknown |
| `"expiresAt": null` | Permanent |
| Valid date-time | Temporary |

Use explicit `null` for permanent records:

```json
"expiresAt": null
```

Use a timestamp for temporary records:

```json
"expiresAt": "2026-09-01T12:00:00.000Z"
```

Do not use an empty string.

### `updatedAt`

`updatedAt` records when the source entry was last changed:

```json
"updatedAt": "2026-08-02T09:15:00.000Z"
```

It is validated and retained as metadata. The custom-list Explorer uses `effectiveAt` for its Recorded column and recorded-date sorting.

## Public Evidence

Evidence is an optional array of up to eight objects per record.

```json
"evidence": [
  {
    "url": "https://example.com/public-evidence/case-1.png",
    "title": "Public Screenshot",
    "caption": "Screenshot approved for public release."
  }
]
```

### Evidence Fields

| Field | Required | Limit | Behaviour |
|---|---:|---:|---|
| `url` | Yes | 2,048 characters | Must be an absolute HTTPS URL without embedded credentials |
| `title` | No | 120 characters | Used as the evidence link label |
| `caption` | No | 500 characters | Retained as supplementary evidence metadata |

When `title` is omitted, Realm Bot generates a label such as `Evidence 1`.

The Explorer primarily presents the evidence title as a link. Evidence files are not copied into Realm Bot storage.

Evidence URLs should:

- Be publicly accessible without signing in.
- Use HTTPS.
- Remain available over time.
- Open the intended evidence directly or on a clear public evidence page.
- Avoid expiring signatures and temporary access tokens.
- Avoid internal network addresses.
- Avoid embedded usernames or passwords.

Publish only information approved for public release. Do not publish:

- Reporter identities unless explicitly authorised.
- Private Discord messages without appropriate approval.
- Internal staff notes.
- Microsoft, Discord, or API tokens.
- Session cookies.
- Private evidence links.
- Personal addresses or unrelated identifying information.
- Material that exposes victims or uninvolved users.
- Evidence that your community is not entitled to redistribute.

Removing a file from GitHub may not remove it from commit history, forks, downloads, or caches.

## Explorer Capability Activation

Optional columns and filters are activated at the list level.

| Explorer capability | Activation condition |
|---|---|
| Player and Reason | Always available because the fields are required |
| Ban Type | At least one valid, non-empty `type` |
| Status | At least one valid `status` |
| Duration and Expiry | At least one record contains the `expiresAt` key |
| Recorded Date | At least one non-null valid `effectiveAt` |
| Reported Realm | At least one non-empty `reportedRealm` |
| Evidence | At least one record contains the `evidence` key |

For consistent results, include an enabled optional field on every applicable record.

For example, if one record includes `expiresAt` but other records omit it, the Duration column appears and the omitted records display an unknown duration.

An empty evidence array is valid:

```json
"evidence": []
```

Because the `evidence` key is present, it still enables the list's Evidence capability.

Custom lists never enable profile-avatar resolution, public case numbers, native detail pages, appeals, or enforcement.

## Duplicate Records

Realm Bot normalises records before comparing them.

Exact duplicate records are removed from the preview and counted as duplicates. The displayed record count can therefore be lower than the number of input objects.

Different records sharing the same XUID are retained and marked as related provider records. This permits multiple incidents for one player:

```json
[
  {
    "xuid": "2535431508056414",
    "username": "ExamplePlayer",
    "reason": "First recorded incident",
    "type": "harassment"
  },
  {
    "xuid": "2535431508056414",
    "username": "ExamplePlayer",
    "reason": "Separate later incident",
    "type": "ban_evasion"
  }
]
```

Avoid accidental duplicate objects. Unknown custom properties do not make two otherwise identical records distinct because Realm Bot ignores unsupported properties.

## Publish on GitHub

### GitHub Website

1. Open or create a public GitHub repository.
2. Select **Add file**.
3. Select **Create new file**.
4. Enter a path such as `ban-lists/community-bans.json`.
5. Paste the JSON array.
6. Confirm that every XUID is quoted.
7. Confirm that the file contains no comments or trailing commas.
8. Commit the file.
9. Open the committed `.json` file.
10. Copy the normal GitHub file URL or select **Raw** and copy the raw URL.
11. Load that URL through **Custom GitHub List**.

### Git

```powershell
git add ban-lists/community-bans.json
git commit -m "Add public Realm Bot ban list"
git push
```

The repository and file must remain public. Realm Bot will not authenticate with private repositories for custom previews.

## Supported GitHub URLs

### Standard GitHub File URL

```text
https://github.com/OWNER/REPOSITORY/blob/main/ban-lists/community-bans.json
```

### Raw GitHub URL

```text
https://raw.githubusercontent.com/OWNER/REPOSITORY/main/ban-lists/community-bans.json
```

### GitHub Contents API URL

```text
https://api.github.com/repos/OWNER/REPOSITORY/contents/ban-lists/community-bans.json?ref=main
```

If the Contents API URL omits `ref`, Realm Bot uses `main`.

The file path must end in `.json`. Use a simple branch, tag, or commit reference such as `main`, `v1`, or a commit hash. Branch names containing `/` may not be interpreted correctly by the current URL parser.

The following are not supported:

- Repository home-page URLs.
- Folder URLs.
- GitHub issue or release URLs.
- Private GitHub files.
- GitHub links that do not use `/blob/` for a file.
- URL shorteners.
- Redirecting links.
- Arbitrary non-GitHub JSON hosts.
- URLs containing credentials.
- URLs containing fragments.
- Production HTTP URLs.

## Load the List

To load a custom list:

1. Open the public **Ban List Explorer**.
2. Select **Custom GitHub List**.
3. Paste the URL into **GitHub List URL**.
4. Select **Load List**.
5. Wait for validation and retrieval to finish.
6. Review the displayed record count.
7. Test gamertag and XUID search.
8. Test all enabled filters.
9. Open each public evidence link.
10. Confirm dates, statuses, and durations are coherent.

The preview is fetched without being stored as a trusted source. Reload the list after publishing GitHub changes.

## Validation Limits

| Limit | Current value |
|---|---:|
| Maximum JSON response size | 2 MiB, or 2,097,152 bytes |
| Maximum input records | 5,000 |
| Maximum evidence entries per record | 8 |
| Maximum `username` length | 64 characters |
| Maximum `reason` length | 2,000 characters |
| Maximum `reportedRealm` length | 160 characters |
| Maximum evidence title length | 120 characters |
| Maximum evidence caption length | 500 characters |
| Maximum evidence URL length | 2,048 characters |
| Maximum custom-list URL length | 2,048 characters |
| Remote request timeout | 8 seconds |
| Preview rate limit | 5 attempts per 60 seconds per requester |

The 5,000-record limit applies before exact duplicates are removed.

The whole list uses all-or-nothing validation. One malformed record or evidence object rejects the complete preview.

When the remote server declares a content type, Realm Bot accepts:

- `application/json`
- `text/plain`
- `application/octet-stream`

The response must decode as valid UTF-8 JSON. Redirect responses are rejected rather than followed.

If the preview limit is reached, wait at least one minute before trying again.

## Common Errors

| Error or symptom | Likely cause | Resolution |
|---|---|---|
| JSON root must be an array | File uses `{ "records": [...] }` | Remove the wrapper and use the array directly |
| Invalid 16-digit XUID | XUID is numeric, too short, too long, or contains other characters | Use a quoted string containing exactly 16 digits |
| Record requires a username | File uses `gamertag` instead of `username` | Rename the property to `username` |
| Unsupported ban type | Display label or unknown value was supplied | Use an exact supported lowercase type identifier |
| Unsupported status | Invalid, uppercase, null, or unknown status | Use `active`, `expired`, or `revoked`, or omit the field |
| Invalid ISO 8601 date-time | Date is missing a time or timezone | Use a complete value ending in `Z` or an offset |
| Invalid evidence list | Evidence is not an array or exceeds eight entries | Use an array containing no more than eight objects |
| Evidence requires a URL | Evidence object has no usable `url` | Add a non-empty absolute HTTPS URL |
| List is too large | File exceeds 2 MiB or 5,000 entries | Split or reduce the list |
| Unsupported URL | Link points to a repository, folder, private file, or unsupported host | Use a public GitHub `.json` file URL |
| List could not be reached | GitHub or the network did not respond within eight seconds | Verify the URL and retry |
| Fewer records than expected | Exact duplicate records were removed | Remove duplicates or verify that records are genuinely distinct |
| Optional filters do not appear | Relevant optional fields are absent | Add supported fields to the records |
| Too many preview attempts | More than five attempts were made within one minute | Wait one minute and retry |
| One bad record blocks everything | Validation is all-or-nothing | Correct the indicated record and reload |

## Publishing Checklist

Before sharing a custom list, confirm:

- The repository is public.
- The file path ends in `.json`.
- The JSON root is an array.
- Every record is an object.
- Every XUID is a quoted 16-digit string.
- Every record has a non-empty `username`.
- Every record has a non-empty `reason`.
- Every `type` uses a supported identifier.
- Every `status` is `active`, `expired`, or `revoked`.
- Every date includes a time and timezone.
- Permanent records use `"expiresAt": null`.
- Temporary records use a valid expiry date.
- Expired records have an appropriate `status`.
- Evidence arrays contain no more than eight objects.
- Every evidence URL is public HTTPS.
- Evidence contains no secrets or private information.
- The file is below 2 MiB.
- The file contains no more than 5,000 input records.
- The standard GitHub or Raw URL opens without authentication.
- The list loads successfully in the Ban List Explorer.
- All enabled filters behave correctly.
- Every evidence link works in a logged-out browser.

## Maintenance

Use Git history to document legitimate list changes.

When maintaining a record:

- Keep the XUID stable.
- Update `username` when the player changes gamertag.
- Update `updatedAt` when public record data changes.
- Change `status` to `expired` when a temporary action ends.
- Change `status` to `revoked` when the action is withdrawn.
- Remove or replace broken evidence links.
- Keep `reason` factual, concise, and suitable for public display.
- Avoid recreating identical records.
- Review public evidence before every publication.
- Test the list after structural changes.
- Preserve a moderation policy explaining how records are reviewed and corrected.

A custom list should not be treated as proof that Realm Bot endorses, verifies, imports, or enforces its contents. Responsibility for accuracy, publication, evidence rights, corrections, and list governance remains with the publisher.

## Copy-Paste Template

```json
[
  {
    "xuid": "0000000000000000",
    "username": "PlayerGamertag",
    "reason": "Public moderation reason",
    "type": "other",
    "status": "active",
    "effectiveAt": "2026-08-01T12:00:00.000Z",
    "expiresAt": null,
    "updatedAt": "2026-08-01T12:00:00.000Z",
    "reportedRealm": "Realm Name",
    "evidence": [
      {
        "url": "https://example.com/public-evidence/file.png",
        "title": "Public Evidence",
        "caption": "Optional public description."
      }
    ]
  }
]
```

Replace every example value before publishing. In particular, `0000000000000000` is only a structural placeholder and must be replaced with the real 16-digit XUID.

## Related Pages

- [Global Ban Overview](overview.md)
- [Ban List Explorer](ban-list-explorer.md)
- [Realm Protection](realm-protection.md)
