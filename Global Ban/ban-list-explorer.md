---
label: Ban List Explorer
description: Search, filter, inspect, and export supported public Realm Hub and external-provider ban records.
order: 98
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Ban List Explorer

The **Ban List Explorer** provides a public view of supported moderation sources. It can display native Realm Hub records, supported external-provider records, and compatible custom GitHub lists.

Open `/global-bans` to access the Explorer.

## Explorer Capabilities

Depending on the selected source, the Explorer can:

- Search by Microsoft/Xbox gamertag or XUID.
- Switch between available public sources.
- Filter supported records by status, duration, appeal state, or ban type.
- Sort records when the selected source provides sortable dates.
- Open detailed Realm Hub case pages.
- Open supported external-provider record pages.
- Export the currently displayed page where supported.

Not every provider supplies every field. The Explorer shows only the filters, columns, links, and export fields supported by the selected source.

## Available Sources

| Source | Ownership and behaviour |
|---|---|
| Realm Hub Database | Native reviewed records managed through Realm Hub reporting, review, publication, and appeals |
| ARAS / Realms+ | Independent public records owned by the external provider |
| Custom GitHub lists | Publisher-managed JSON records loaded for preview without import or automatic enforcement |

Realm Hub cannot correct, revoke, or appeal an external provider's record. Contact the provider that owns the source when an external entry appears incorrect.

## Realm Hub Records

A public Realm Hub record may display:

- Case number.
- Player profile and gamertag.
- XUID.
- Public reason.
- Ban type.
- Effective date.
- Duration or expiry.
- Current status.
- Evidence approved for public display.

Possible public statuses include:

| Status | Meaning |
|---|---|
| Active | The record is active |
| Temporary | The record has a defined expiry |
| Under Appeal | An appeal is being considered; enforcement remains active |
| Expired | The temporary record has reached its end |
| Revoked | The record was withdrawn or overturned |

An appeal does not suspend a record. **Under Appeal** records remain active until an appeal decision revokes them.

## External Records

External sources remain independent from the Realm Hub Database:

- Their provider controls record accuracy, publication, and correction.
- Realm Hub reports do not modify them.
- Realm Hub appeals cannot be used for them.
- Their available fields and detail links can differ from native Realm Hub records.

## Custom GitHub Lists

Custom GitHub lists are public JSON files supplied by third-party publishers. Loading one:

- Creates a temporary Explorer preview.
- Does not import records into the Realm Hub Database.
- Does not approve the publisher as a trusted source.
- Does not automatically enforce bans.
- Does not create Realm operations.
- Does not enable Realm Hub case pages or appeals.

See [Custom Ban List Format](custom-ban-list-format.md) for the complete schema and validation rules.

## Search and Filter Guidance

- Use the exact 16-digit XUID when gamertag search is ambiguous.
- Confirm the selected source before interpreting a result.
- Clear filters if an expected record does not appear.
- Treat missing fields as provider limitations rather than proof that the underlying event did not occur.
- Open the record detail page or public evidence before making a moderation decision.

## Exporting Records

Where supported, exports contain the fields available on the currently displayed page. An export is not a complete database synchronisation and does not make an external or custom source trusted.

Review exported data before redistributing it. Public availability does not remove the publisher's responsibility to handle evidence and personal information appropriately.

## Troubleshooting

### A known record does not appear

- Confirm the correct source is selected.
- Search by XUID.
- Clear status, type, duration, and appeal filters.
- Confirm the record is public and supported by that provider.

### Filters or columns are missing

The selected source may not provide the required fields. Custom-list capabilities depend on the fields present in the loaded JSON file.

### An external record is incorrect

Contact the provider that owns the source. Realm Hub cannot modify ARAS / Realms+ or custom-list records.

### A record is under appeal but still active

This is expected. An appeal does not pause enforcement while a decision is pending.

## Related Pages

- [Global Ban Overview](overview.md)
- [Realm Protection](realm-protection.md)
- [Appeals](appeals.md)
- [Custom Ban List Format](custom-ban-list-format.md)
