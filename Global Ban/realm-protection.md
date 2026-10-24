---
label: Realm Protection
description: Configure which active Realm Hub Global Ban categories Realm Bot applies to a connected Realm.
order: 99
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Realm Protection

Global Ban protection lets a Realm owner apply active Realm Hub records to a connected Minecraft Realm. Each Realm keeps its own protection setting and category selection.

## Default State

Protection is enabled by default when a connected Realm has no previously saved Global Ban setting.

The dashboard distinguishes:

- **Enabled by default** - no custom setting has been saved and default protection is active.
- **Enabled** - the owner has explicitly enabled protection.
- **Disabled** - the owner has explicitly disabled protection.
- **Temporarily unavailable** - the current protection state could not be loaded.

If the state is temporarily unavailable, refresh and try again later. Do not assume the setting changed.

## Configure Protection

1. Sign in to the Realm Bot dashboard with Discord.
2. Select the Discord server containing the connected Realm.
3. If no Realm is connected, link the required Microsoft account and run `/connect` in the Discord server.
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

> **Important:** Leaving the main switch enabled while disabling every category results in no Global Ban records being enforced.

## How Enforcement Works

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
- Leave the existing configuration unchanged until its saved state can be loaded.

### A Global Ban is not appearing

- Confirm the main protection switch is enabled.
- Confirm the record's category is enabled.
- Check that the public Realm Hub record is active.
- Select **Check Global Ban Database**.
- Select **Check Realm**.
- Review **Needs attention** for failed operations.
- Verify the Realm's native banlist after processing completes.

### A ban remains after protection is disabled

This is expected. Disabling protection does not remove existing native Realm bans. Review the record and remove the Realm ban separately only when appropriate.

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
