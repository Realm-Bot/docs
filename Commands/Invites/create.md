---
label: "/invites create"
description: Create a reusable Realm Bot managed web invite with optional usage and expiry limits.
order: 97
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/invites create`

Creates a Realm Bot managed `realmbot.link` URL for a selected Realm. This is not an official Minecraft Realm code.

## Syntax

`/invites create <realm> [max_users] [expires]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `realm` | Yes | The Realm the managed link will invite players to. |
| `max_users` | No | Maximum successful uses. `0` or omission means unlimited. |
| `expires` | No | A duration such as `1h` or `1d`. Omission means no configured expiry. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.invites.create`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Example

`/invites create realm:<selected Realm> max_users:5 expires:1d`

Realm Bot creates the managed record and returns a `realmbot.link` URL.

## Safety

Treat the link as an entry point to the Realm. When setting a limit, use a positive number; use `0` or omit the option only when unlimited use is intentional. Prefer short expiries for links shared publicly.

## Related Commands

- [`/invites temp`](temp.md)
- [`/invites list`](list.md)
- [`/invites delete`](delete.md)
- [Invite Links](<../../Server Dashboard/server-invites.md>)
- [Command Troubleshooting](../troubleshooting.md)
