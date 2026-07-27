---
label: "/banlist lookup"
description: Check a player's official blocklist status in one or all connected Minecraft Realms.
order: 96
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/banlist lookup`

Checks whether a resolved Minecraft player appears on the official blocklist for one or more connected Realms.

## Syntax

`/banlist lookup <user> [realm]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `realm` | No | One Realm to check. If omitted, every Realm associated with the connected server account is checked. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.banlist.lookup`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Example

`/banlist lookup user:ExamplePlayer realm:<selected Realm>`

Realm Bot reports the player's blocklist status for the selected Realm.

> **Current limitation:** An official Realm API failure can produce an incomplete result or make a blocked player appear unblocked. Verify important decisions against the Realm's official blocklist.

This command does not check Realm Bot Global Ban. Use [`/db report`](report.md) to submit evidence for Global Ban review.

## Related Commands

- [`/banlist all`](all.md)
- [`/realm ban`](../Realm/ban.md)
- [`/realm unban`](../Realm/unban.md)
- [Command Troubleshooting](../troubleshooting.md)
