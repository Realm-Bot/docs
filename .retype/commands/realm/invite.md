# `/realm invite`

Uses the official Realm membership service to add a resolved Minecraft player to one or more connected Realms.

## Syntax

`/realm invite <user> [realm]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `realm` | No | One Realm to target. If omitted, every connected Realm is targeted. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with permission to manage membership.
- The member must have `command.realm.invite`, or be a Discord Administrator.
- The gamertag must resolve successfully.
- Premium and an active Relay Account are not required.

## Example

`/realm invite user:ExamplePlayer realm:<selected Realm>`

Realm Bot attempts to add the player through the official membership API and reports a result for the selected Realm.

This command does not create a browser invite link. Use the [`/invites`](../Invites/index.md) commands for managed `realmbot.link` URLs.

## Common Issues

Existing membership, Realm capacity, expired account access, or a temporary Realm service failure can prevent the invitation. Verify the member list before retrying.

## Related Commands

- [`/realm kick`](kick.md)
- [`/invites create`](../Invites/create.md)
- [Command Troubleshooting](../troubleshooting.md)
