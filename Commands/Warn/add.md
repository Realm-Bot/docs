---
label: "/warn add"
description: Record a player warning and evaluate the configured count threshold for Realm enforcement.
order: 97
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/warn add`

Creates a Realm Bot warning record for a Minecraft player. If the configured warning-count threshold is reached, Realm Bot can attempt to ban the player from the relevant Realm.

## Syntax

`/warn add <user> <reason> [realm]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `reason` | Yes | A configured warning reason or accepted typed reason. |
| `realm` | No | One Realm to target. If omitted, every connected Realm is processed. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.warn.add`, or be a Discord Administrator.
- Warning presets and thresholds should be configured in the dashboard.
- Premium and an active Relay Account are not required.

## Threshold Behaviour

The configured threshold is based on the number of warning records, not weighted points. At the threshold, Realm Bot may attempt an official Realm ban and can write audit and Discord log output where configured.

> **Important:** Verify the player's official blocklist status after a threshold action. The warning response alone is not proof that the external Realm ban completed.

Omitting `realm` evaluates the warning across all connected Realms. Select one Realm explicitly for targeted moderation.

## Related Commands

- [`/warn lookup`](lookup.md)
- [`/warn remove`](remove.md)
- [`/realm ban`](../Realm/ban.md)
- [Warning Configuration](<../../Server Dashboard/server-warnings.md>)
- [Command Troubleshooting](../troubleshooting.md)
