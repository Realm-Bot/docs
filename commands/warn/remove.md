# `/warn remove`

Records a warning-removal event for a Minecraft player. It preserves moderation history rather than deleting an earlier record.

## Syntax

`/warn remove <user> <reason> [realm]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `reason` | Yes | The reason associated with the removal record. |
| `realm` | No | One Realm to process. If omitted, every connected Realm is processed. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.warn.remove`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Current Limitation

> **Current limitation:** The command does not necessarily deactivate or delete the original warning in the current implementation. It may therefore leave threshold totals unchanged.

After recording a removal, use [`/warn lookup`](lookup.md) and verify the player's warning totals before relying on the change. Select one Realm explicitly to avoid unintended all-Realm scope.

## Related Commands

- [`/warn lookup`](lookup.md)
- [`/warn add`](add.md)
- [Command Troubleshooting](../troubleshooting.md)
