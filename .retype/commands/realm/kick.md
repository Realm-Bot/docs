# `/realm kick`

Removes a player from official Realm membership. This is more than disconnecting the current play session, but it does not block or ban the player.

## Syntax

`/realm kick <user> [realm] [reason]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `realm` | No | One Realm to target. If omitted, every connected Realm is targeted. |
| `reason` | No | The reason recorded for the removal. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with permission to manage membership.
- The member must have `command.realm.kick`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Effect

Realm Bot attempts to remove the player's membership, writes the moderation record, and can send the configured player message and Discord log.

The player can be invited again later with [`/realm invite`](invite.md). Use [`/realm ban`](ban.md) instead when the player must be placed on the official blocklist.

> **Warning:** Omitting `realm` removes membership from every connected Realm. Select the intended Realm explicitly.

## Related Commands

- [`/realm invite`](invite.md)
- [`/realm ban`](ban.md)
- [Command Troubleshooting](../troubleshooting.md)
