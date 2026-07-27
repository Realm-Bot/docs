---
label: "/world leave"
description: Disable persistent joining and disconnect the Relay Account from one or all selected Realms.
order: 96
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/world leave`

Disables persistent standard joining for the selected Realm rows and requests that the Relay Account disconnect.

## Syntax

`/world leave [realm]`

The optional `realm` argument selects one Realm. If omitted, every Realm associated with the connected server account is targeted.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- Realm Bot Premium must be active.
- The member must have `command.world.leave`, or be a Discord Administrator.

## Operational Impact

> **Warning:** There is no confirmation. Omitting `realm` disables joining and requests disconnection for all connected Realms.

Connection-dependent features stop for the affected Realm, including:

- Chat Relay
- Realm Console
- World broadcast and execute
- Live GameTest requests
- Other live event-driven moderation or progression systems

Use [`/world join`](join.md) when the Relay Account should reconnect and persistent joining should resume.

## Related Commands

- [`/world join`](join.md)
- [Relay Account and GameTest Dependencies](<../../Realm Modules/relay-account-and-gametest.md>)
- [Command Troubleshooting](../troubleshooting.md)
