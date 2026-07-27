---
label: "/warn lookup"
description: Review a player's Realm Bot warning and warning-removal history.
order: 96
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/warn lookup`

Displays Realm Bot warning history for a resolved Minecraft player, grouped by reason and accompanied by a summary.

## Syntax

`/warn lookup <user> [realm]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `realm` | No | The intended Realm filter. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.warn.lookup`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Output

The response includes warning and warning-removal records, grouped by reason. Interactive controls display up to **five records per reason page** and can switch to a summary.

The response and pagination controls are public. Use a staff channel if moderation history should remain restricted.

> **Current limitation:** The optional Realm filter may not fully restrict the records displayed. Confirm the Realm attached to each record before acting on the result.

## Related Commands

- [`/warn add`](add.md)
- [`/warn remove`](remove.md)
- [Command Troubleshooting](../troubleshooting.md)
