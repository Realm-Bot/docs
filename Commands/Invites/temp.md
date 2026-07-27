---
label: "/invites temp"
description: Create a one-use Realm Bot managed invite link that expires after 24 hours.
order: 96
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/invites temp`

Creates a managed `realmbot.link` URL for controlled one-person onboarding. The link allows one successful use and expires after 24 hours.

## Syntax

`/invites temp <realm>`

The required `realm` argument selects the Realm the link will invite the user to.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.invites.temp`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Example

`/invites temp realm:<selected Realm>`

Share the returned URL only with its intended recipient. The link is separate from the Realm's official invite codes.

## Related Commands

- [`/invites create`](create.md)
- [`/invites list`](list.md)
- [Invite Links](<../../Server Dashboard/server-invites.md>)
- [Command Troubleshooting](../troubleshooting.md)
