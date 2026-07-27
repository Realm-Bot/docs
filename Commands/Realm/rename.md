---
label: "/realm rename"
description: Change the actual Minecraft Bedrock Realm name shown to members.
order: 90
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

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
