---
label: "/realm unban"
description: Remove a player from the official blocklist of one or all connected Realms.
order: 96
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/realm unban`

Removes a resolved Minecraft player from the official blocklist for one or more connected Realms.

## Syntax

`/realm unban <user> [realm] [reason] [attachment] [silent]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `realm` | No | One Realm to target. If omitted, every connected Realm is targeted. |
| `reason` | No | The reason recorded for the unban. |
| `attachment` | No | Optional supporting evidence. |
| `silent` | No | Suppresses the configured Discord moderation-log message when enabled. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with permission to manage the Realm.
- The member must have `command.realm.unban`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Scope and Result

> **Warning:** Omitting `realm` targets every connected Realm. Select one Realm explicitly when a server-wide unban is not intended.

Realm Bot attempts to remove the official Realm block, records moderation context, and can send the configured player message. `silent:true` suppresses only the configured Discord log output.

This command does **not** remove a Realm Bot Global Ban. Verify the official blocklist afterwards before telling the player they can rejoin.

## Related Commands

- [`/realm ban`](ban.md)
- [`/banlist lookup`](../Banlist/lookup.md)
- [`/db report`](../Banlist/report.md)
- [Command Troubleshooting](../troubleshooting.md)
