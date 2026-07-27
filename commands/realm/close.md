# `/realm close`

Requests that one or more connected Realms close to new player joins.

## Syntax

`/realm close [realm]`

The optional `realm` argument selects one Realm. If omitted, every Realm associated with the connected server account is targeted.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with access to manage the Realm.
- The member must have `command.realm.close`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Safety and Scope

> **Warning:** The action begins immediately and has no confirmation. Omitting `realm` closes every connected Realm.

Select one Realm explicitly and notify players before planned maintenance. Verify the actual Realm status after execution because a Discord response may appear before the external service state is fully confirmed.

## Related Commands

- [`/realm open`](open.md)
- [Command Troubleshooting](../troubleshooting.md)
