---
label: "/realm open"
description: Open one or all connected Realms to player joins.
order: 92
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/realm open`

Requests that one or more connected Realms open for players to join.

## Syntax

`/realm open [realm]`

The optional `realm` argument selects one Realm. If omitted, every Realm associated with the connected server account is targeted.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with access to manage the Realm.
- The member must have `command.realm.open`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Safety and Scope

> **Warning:** The action begins immediately and has no confirmation. Omitting `realm` opens every connected Realm.

Confirm maintenance or access restrictions are complete before reopening. Select one Realm explicitly and verify the actual Realm status after execution.

## Related Commands

- [`/realm close`](close.md)
- [Command Troubleshooting](../troubleshooting.md)
