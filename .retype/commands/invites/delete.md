# `/invites delete`

Permanently removes one Realm Bot managed invite-link record from the current Discord server.

## Syntax

`/invites delete <slug>`

The required `slug` is the final identifying portion of the managed `realmbot.link` URL.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.invites.delete`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Safety

> **Warning:** Deletion is immediate and has no separate confirmation. Verify the slug with `/invites list` before running the command.

Deleting the managed record does not delete or rotate an official Minecraft Realm code.

## Related Commands

- [`/invites list`](list.md)
- [`/invites create`](create.md)
- [`/realm code-manage`](../Realm/code-manage.md)
- [Command Troubleshooting](../troubleshooting.md)
