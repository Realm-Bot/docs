---
label: "/realm nickname"
description: Change the local Realm label Realm Bot uses in Discord without renaming the Minecraft Realm.
order: 89
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/realm nickname`

Changes Realm Bot's local display label for a connected Realm. It does not change the actual Minecraft Bedrock Realm name shown to members.

## Syntax

`/realm nickname <realm> <nickname>`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `realm` | Yes | The connected Realm whose local label will change. |
| `nickname` | Yes | The new Realm Bot label, up to 32 characters. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.realm.nickname`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Example

`/realm nickname realm:<selected Realm> nickname:Survival`

The saved nickname is used by Realm Bot in Realm selection and Discord command displays. Command-list refresh can take a short time.

To rename the actual Minecraft Realm, use [`/realm rename`](rename.md).

## Related Commands

- [`/realm rename`](rename.md)
- [Command Troubleshooting](../troubleshooting.md)
