# Ban List Explorer

Use the **Ban List Explorer** to review public Realm Hub records or inspect a custom GitHub list before deciding whether to use it on your Realm.

Open `/ban-list` on the Realm Bot website to access the Explorer. Public sources appear only when enabled and configured for public display.

## Explorer Capabilities

Depending on the selected source, the Explorer can:

- Search by Microsoft/Xbox gamertag or XUID.
- Switch between available public sources.
- Filter supported records by status, duration, appeal state, or ban type.
- Sort records when the selected source provides sortable dates.
- Open detailed Realm Hub case pages.
- View source details for entries in saved lists.
- Export the currently displayed page where supported.

Not every provider supplies every field. The Explorer shows only the filters, columns, links, and export fields supported by the selected source.

## Available Sources

| Source | Ownership and behaviour |
|---|---|
| Realm Hub Database | Native reviewed records managed through Realm Hub reporting, review, publication, and appeals |
| Custom GitHub lists | Publisher-managed JSON records available to preview. Signed-in users can save a source to their account. |

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

## External Records

External sources remain independent from the Realm Hub Database:

- Their provider controls record accuracy, publication, and correction.
- Realm Hub reports do not modify them.
- Realm Hub appeals cannot be used for them.
- Their available fields and detail links can differ from native Realm Hub records.

## Custom GitHub Lists

Choose **Load** to preview a publisher's public JSON file. A preview does not import records, endorse the source, enable appeals or take action on a Realm.

See [Custom Ban List Format](custom-ban-list-format.md) for the schema and validation rules.

## Save to My Ban Lists

1. Sign in and load a public GitHub JSON file. Review the records and their publisher.
2. Select **Save to My Ban Lists** after previewing, or use **Load & save** when loading the file. Confirm a name (1 to 100 characters) and an optional description (up to 500 characters).
3. Open **My Ban Lists** at `/ban-list/lists` to check the record count, sync health and last successful refresh. You can save up to **20 lists**.

Saving keeps a reference to the source URL. Accounts saving the same URL may see the same accepted records, but each manages its own saved entry. The collection is not a public endorsement directory, and saving a source does not make its file or evidence private.

If the first refresh fails, check the list's sync health before adding it again. Sources normally refresh about every **30 minutes**. You can refresh manually once every **five minutes**, up to **ten times per hour**.

**Saving does not ban anyone.** To use a saved source for enforcement, follow [Assign a Saved List](realm-protection.md#assign-a-saved-list) for the intended Realm. Removing a saved entry queues cleanup for its assignments; it does not delete another account's copy.

## Search and Filter Guidance

- Use the exact 16-digit XUID when gamertag search is ambiguous.
- Confirm the selected source before interpreting a result.
- Clear filters if an expected record does not appear.
- Treat missing fields as provider limitations rather than proof that the underlying event did not occur.
- Open the record detail page or public evidence before making a moderation decision.

## Exporting Records

Where supported, an export includes only the displayed page and fields, not the entire database.

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

Contact the publisher that owns the source. Realm Hub cannot correct the publisher's records.

### A record is under appeal but still active

Enforcement continues while an appeal is pending.

## Related Pages

- [Global Ban Overview](overview.md)
- [Realm Protection](realm-protection.md)
- [Appeals](appeals.md)
- [Custom Ban List Format](custom-ban-list-format.md)
