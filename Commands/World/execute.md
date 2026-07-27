---
label: "/world execute"
description: Execute a Minecraft command through the active Relay Account with its in-game authority.
order: 94
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/world execute`

Executes a Minecraft Bedrock command through the active Relay Account.

## Syntax

`/world execute <command> [realm]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `command` | Yes | The Minecraft command **without** a leading `/`. |
| `realm` | No | One Realm to target. If omitted, every connected Realm is targeted. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- Realm Bot Premium must be active.
- The member must have `command.world.execute`, or be a Discord Administrator.
- The Relay Account must be connected.
- The Relay Account needs the Minecraft operator permission required by the command.
- Cheats must be enabled where the Minecraft command requires them.

## Example

`/world execute command:time set day realm:<selected Realm>`

The command argument is `time set day`, without a leading slash.

## Output

Realm Bot displays the available output for each selected Realm and can attach an `output.txt` file. `No Response` can mean:

- The Minecraft command produced no output
- The syntax was invalid
- The Relay Account was offline
- The account lacked permission
- The Relay service timed out or failed

Verify the effect in-game rather than treating `No Response` as success.

## Safety and Targeting

> **Warning:** This command can execute destructive Minecraft operations and has no separate confirmation. Restrict `command.world.execute` to trusted technical administrators.

If `realm` is omitted, the command is sent to every connected Realm. Select one Realm explicitly.

Commands run with the Relay Account's authority. `@s` refers to the executing Relay Account, so use explicit targets when another player or entity is intended.

## Related Commands

- [`/world broadcast`](broadcast.md)
- [`/world join`](join.md)
- [Realm Console](<../../Realm Modules/realm-console.md>)
- [Command Troubleshooting](../troubleshooting.md)
