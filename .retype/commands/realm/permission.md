# `/realm permission`

Changes a player's official Minecraft permission in one or more connected Realms.

## Syntax

`/realm permission <user> <permission> [realm]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `permission` | Yes | `Visitor`, `Member`, or `Operator`. |
| `realm` | No | One Realm to target. If omitted, every connected Realm is targeted. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with permission to manage members.
- The member must have `command.realm.permission`, or be a Discord Administrator.
- The target normally needs to be a Realm member.
- Premium and an active Relay Account are not required.

## Permission Levels

- **Visitor** limits normal building and interaction privileges.
- **Member** grants standard player access.
- **Operator** grants significant in-game administrative authority.

> **Warning:** Grant Operator only to highly trusted players. If `realm` is omitted, Realm Bot attempts to apply the permission across every connected Realm.

Minecraft Realm permission is separate from Discord permissions and Realm Bot command permissions. Verify the player's permission in the official Realm member list after the command.

## Related Commands

- [`/realm members`](members.md)
- [`/realm invite`](invite.md)
- [Server Permissions](<../../Server Dashboard/server-permissions.md>)
- [Command Troubleshooting](../troubleshooting.md)
