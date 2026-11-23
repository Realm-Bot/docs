# `/realm lastseen`

Searches Xbox club/member information across the connected Realms for a player's most recent visible activity.

## Syntax

`/realm lastseen <user>`

Enter the player's Xbox gamertag.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.realm.lastseen`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Current Limitation

> **Current limitation:** The command may return `Never` even when the player has recent activity. Do not use this result as the only evidence in a moderation decision.

Xbox club/member visibility is also limited to approximately 1,000 members. Confirm activity with [`/realm recents`](recents.md), [`/realm sessions`](sessions.md), or the Realm Activity dashboard where available.

## Related Commands

- [`/realm recents`](recents.md)
- [`/realm sessions`](sessions.md)
- [`/realm playtime`](playtime.md)
- [Command Troubleshooting](../troubleshooting.md)
