---
label: "/realm lastseen"
description: Search connected Realms for a player's most recent Xbox club activity record.
order: 83
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/realm lastseen`

Searches Xbox club/member information across the connected Realms for a player's most recent visible activity.

## Syntax

`/realm lastseen <user>`

The required `user` argument is the player's Xbox gamertag. The command searches across all Realms associated with the connected server account.

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
