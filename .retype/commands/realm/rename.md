# `/realm rename`

Changes the actual Minecraft Bedrock Realm name through the official Realm service. The new name is visible to Realm members.

## Syntax

`/realm rename <realm> <new_name>`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `realm` | Yes | The Realm to rename. |
| `new_name` | Yes | The new name, up to 32 characters. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with permission to manage the Realm.
- The member must have `command.realm.rename`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Example

`/realm rename realm:<selected Realm> new_name:Community Survival`

Confirm the selected Realm and spelling before running the command. Use [`/realm nickname`](nickname.md) instead when only Realm Bot's local Discord label should change.

## Related Commands

- [`/realm nickname`](nickname.md)
- [Command Troubleshooting](../troubleshooting.md)
