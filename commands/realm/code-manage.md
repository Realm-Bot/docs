# `/realm code-manage`

Opens an interactive manager for a selected Realm's official Minecraft invite codes. These codes are separate from Realm Bot managed `realmbot.link` invitations.

## Syntax

`/realm code-manage <realm>`

The required `realm` argument selects one Realm.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with permission to manage the Realm.
- The member must have `command.realm.code-manage`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Available Actions

The interface displays and supports up to **five codes**. Depending on the selected code, you can:

- Create another code when the flow and limit allow it
- Enable or disable a code
- Remove its expiry to make it permanent
- Set an expiry of `30m`, `1h`, `6h`, `12h`, `1d`, or `7d`
- Permanently delete the code

Only the member who ran the command can use its controls. The controls expire after approximately 60 seconds.

## Safety

> **Warning:** Anyone with an active official Realm code can use it as a join path. Code deletion is immediate, permanent within this flow, and has no separate confirmation.

Confirm the selected code before changing or deleting it. Use Realm Bot's [Invite Links](<../../Server Dashboard/server-invites.md>) when you need a managed web link with usage and expiry controls.

> **Current limitation:** If the Realm has no existing codes, the interface may not offer the action needed to create its first code. Use the official Realm management interface or contact support.

## Related Commands

- [`/invites create`](../Invites/create.md)
- [`/invites list`](../Invites/list.md)
- [Command Troubleshooting](../troubleshooting.md)
