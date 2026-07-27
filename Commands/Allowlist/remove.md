---
label: "/allowlist remove"
description: Remove a Minecraft player from Realm Bot's server-level automation allowlist.
order: 94
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/allowlist remove`

Removes a player from Realm Bot's allowlist for the current Discord server.

## Syntax

`/allowlist remove <user>`

The required `user` argument is the player's Xbox gamertag. Realm Bot resolves the profile before looking for the stored allowlist entry.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- Realm Bot Premium must be active.
- The member must have `command.allowlist.remove`, or be a Discord Administrator.

## Example

`/allowlist remove user:ExamplePlayer`

After removal, supported automated systems no longer treat the player as allowlisted. If no matching entry exists, Realm Bot reports that the player is not in the allowlist.

## Scope

Removing an exemption does not remove the player from any Minecraft Realm and does not alter their official Realm permission.

## Related Commands

- [`/allowlist add`](add.md)
- [`/allowlist check`](check.md)
- [`/allowlist list`](list.md)
- [Command Troubleshooting](../troubleshooting.md)
