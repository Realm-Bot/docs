---
label: "/allowlist add"
description: Add a Minecraft player to Realm Bot's server-level allowlist for supported automated systems.
order: 97
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/allowlist add`

Adds a player to Realm Bot's allowlist for the current Discord server. Supported automated systems can use this list to exempt trusted players from configured enforcement.

## Syntax

`/allowlist add <user>`

The required `user` argument is the player's Xbox gamertag. Realm Bot resolves it to the corresponding Microsoft/Xbox profile before saving the entry.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- Realm Bot Premium must be active.
- The member must have `command.allowlist.add`, or be a Discord Administrator.

## Example

`/allowlist add user:ExamplePlayer`

Realm Bot saves the resolved player together with basic audit information about who added them. If the player is already present, the command reports that no duplicate entry is needed.

## Scope

This is Realm Bot's server-level allowlist. It does not add the player as a Realm member or invite them to Minecraft.

Review the [Allowlist command overview](index.md) for the automated systems that can use exemptions.

## Common Issues

### The player cannot be found

Confirm the gamertag spelling and retry after any temporary Xbox profile service issue has cleared.

### The player is already allowlisted

Use [`/allowlist check`](check.md) or [`/allowlist list`](list.md) to confirm the existing entry.

## Related Commands

- [`/allowlist check`](check.md)
- [`/allowlist list`](list.md)
- [`/allowlist remove`](remove.md)
- [Command Troubleshooting](../troubleshooting.md)
