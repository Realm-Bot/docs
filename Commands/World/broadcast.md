---
label: "/world broadcast"
description: Send a prefixed announcement to in-game chat through the active Relay Account.
order: 95
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/world broadcast`

Sends a formatted `[BROADCAST]` message to players through the active Relay Account.

## Syntax

`/world broadcast <message> [realm]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `message` | Yes | The announcement text sent in-game. |
| `realm` | No | One Realm to target. If omitted, every connected Realm is targeted. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- Realm Bot Premium must be active.
- The member must have `command.world.broadcast`, or be a Discord Administrator.
- The Relay Account must be connected to the target Realm.
- The Relay Account needs sufficient Minecraft permission, with cheats enabled where required for `tellraw`.

## Example

`/world broadcast message:Server restart in 10 minutes realm:<selected Realm>`

Use straightforward text. Until robust command formatting is confirmed, avoid unusual characters or formatting sequences that could make the Minecraft command invalid.

> **Current limitation:** A Discord success response may not prove that players received the message. Confirm important announcements in-game.

## Related Commands

- [`/world execute`](execute.md)
- [`/world join`](join.md)
- [Command Troubleshooting](../troubleshooting.md)
