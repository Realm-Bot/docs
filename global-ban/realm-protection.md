# Realm Protection

Global Ban protection lets a Realm owner apply active Realm Hub records to a connected Minecraft Realm. Each Realm keeps its own protection setting and category selection.

## Default State of the Realm Hub Database

Realm Hub protection is on by default. **Enabled** or **Disabled** means the owner has explicitly set a preference. If the dashboard shows **Temporarily unavailable**, refresh later rather than assuming protection has changed.

## Configure Protection

1. Sign in to the Realm Bot dashboard with Discord.
2. Select the Discord server containing the connected Realm.
3. If no Realm is connected, follow [Getting Started](../setup.md) and review the migration warning before connecting.
4. Select the Realm.
5. Open **Tools**, followed by **Banlist**.
6. Find the **Global Ban Database** card.
7. Confirm whether protection is enabled by default, enabled, or disabled.
8. Turn on the main switch if protection is disabled.
9. Select the categories the Realm should enforce.

The Banlist page is not a Premium-only feature.

## Protection Categories

Each category can be enabled or disabled independently.

| Category | Typical coverage |
|---|---|
| Nuking | Deliberate large-scale destruction of a Realm |
| Crashing | Deliberately disrupting or crashing a Realm |
| Cheating | Unfair gameplay modifications or prohibited advantages |
| Exploiting | Abuse of vulnerabilities, commands, packets, or game behaviour |
| Harassment | Targeted or repeated harmful behaviour |
| Threats | Credible threats against players, communities, or services |
| Ban Evasion | Returning through another account to avoid an existing ban |
| Other | Serious conduct that does not fit another category |

Use **Enable All** to select every category or **Disable All** to clear every category.

> **Important:** Leaving the Realm Hub Database switch enabled while disabling every category means no records from that database are enforced. Check custom source assignments separately.

## Assign a Saved List

1. [Preview and save the GitHub source](ban-list-explorer.md#save-to-my-ban-lists). Check the publisher, records and last successful refresh before using it to decide who may join.
2. As a manager, open the Discord server's **Realm > Tools > Ban List** for the intended Realm and select **Add Ban List**.
3. Choose your saved source. Select the categories to enforce and whether to include uncategorised records.
4. Enable protection for that source on the intended Realm.

A Realm supports up to **10 enabled custom lists**, and a user can have up to **100 active assignments**. Removing a list from **My Ban Lists** queues cleanup for its assignments. Do not assume immediate unbans; check the native banlist. This does not remove a different account's saved copy or change the publisher's file.

## How Realm Hub Enforcement Works

When protection is active, Realm Bot compares active Realm Hub records with the categories enabled for that Realm. Matching records are applied through the Realm's native ban system.

Processing is asynchronous. The dashboard can show entries under **In progress** while Realm operations are being applied.

The Banlist page provides:

- **Global bans** - database-derived entries associated with the Realm.
- **Database coverage** - relevant Realm Hub records and their current application state.
- **Needs attention** - updates that could not be completed.
- **Check Global Ban Database** - requests a fresh source check.
- **Check Realm** - compares the Realm's current ban state with the expected state.
- **Refresh bans** - reloads the information displayed on the page.

After any high-impact change, verify the result against the Realm's native banlist. A successful dashboard request does not by itself prove that every external Realm operation completed.

## Disabling Protection

Turning protection off stops new Global Ban entries from being applied. It does **not** remove bans already present in the Realm's native banlist.

Review existing entries separately before unbanning anyone. Use `/realm unban` only after confirming that removing the native ban is appropriate.

## Troubleshooting

### Protection is temporarily unavailable

- Refresh the page and try again later.
- Confirm the correct Discord server and Realm are selected.

### A Global Ban is not appearing

- Confirm the main protection switch is enabled.
- Confirm the record's category is enabled.
- Check that the public Realm Hub record is active.
- Select **Check Global Ban Database**.
- Select **Check Realm**.
- Review **Needs attention** for failed operations.
- Verify the Realm's native banlist after processing completes.

### A ban remains after protection is disabled

Disabling protection stops new bans; it does not remove existing ones. Review the record before removing a native ban.

### An entry remains in progress

- Allow time for asynchronous processing.
- Refresh the Banlist page.
- Confirm Realm Bot still has access to the Realm.
- Use **Check Realm** to compare the native ban state with the expected state.

## Related Pages

- [Global Ban Overview](overview.md)
- [Ban List Explorer](ban-list-explorer.md)
- [`/realm ban`](<../Commands/Realm/ban.md>)
- [`/realm unban`](<../Commands/Realm/unban.md>)
