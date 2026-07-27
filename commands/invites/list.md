# `/invites list`

Displays Realm Bot managed invite-link records for the current Discord server.

## Syntax

`/invites list`

This command has no arguments.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.invites.list`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Information Shown

Where available, each record includes:

- Status
- Current and maximum uses
- Expiration
- Target Realm
- Link slug

The list can include enabled, disabled, expired, or exhausted records even if older command wording refers only to active invitations.

> **Current limitation:** The command has no pagination and long output can be truncated. Use the [Invite Links dashboard](<../../Server Dashboard/server-invites.md>) for a fuller management view.

## Related Commands

- [`/invites create`](create.md)
- [`/invites temp`](temp.md)
- [`/invites delete`](delete.md)
- [Command Troubleshooting](../troubleshooting.md)
