# `/realm members`

Displays official membership and blocklist information for one selected Realm.

## Syntax

`/realm members <realm> [filter] [name]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `realm` | Yes | The Realm whose members will be displayed. |
| `filter` | No | `Visitor`, `Member`, `Operator`, or `Banned`. |
| `name` | No | A gamertag to search for. |

Do not provide `filter` and `name` together.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with access to the Realm.
- The member must have `command.realm.members`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Member Categories

- **Visitor** - limited Minecraft Realm access.
- **Member** - standard player access.
- **Operator** - elevated in-game authority.
- **Banned** - players on the official Realm blocklist.

The command presents the results in interactive pages, normally with up to ten entries per page.

> **Current limitation:** A supplied filter or name can be accepted without being reflected correctly in the displayed list. Treat the unfiltered list as the most reliable output and verify filtered decisions in the official Realm member interface.

## Related Commands

- [`/realm players`](players.md)
- [`/realm permission`](permission.md)
- [`/banlist all`](../Banlist/all.md)
- [Command Troubleshooting](../troubleshooting.md)
