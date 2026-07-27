---
label: "/world join"
description: Enable persistent Relay joining and request a live connection to one or all connected Realms.
order: 97
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/world join`

Enables persistent joining for the selected Realm rows and requests that the configured Relay Account connect in-game.

## Syntax

`/world join [realm]`

The optional `realm` argument selects one Realm. If omitted, every Realm associated with the connected server account is targeted.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- Realm Bot Premium must be active.
- The member must have `command.world.join`, or be a Discord Administrator.
- The Realm owner or configured alternative Relay Account must have valid Microsoft/Xbox authentication and Realm access.
- Alternative Relay Accounts may require an active official Realm code.

## Connection Behaviour

Realm Bot uses the owner account or a configured alternative Relay Account. An alternative account can be invited, unblocked, and granted Operator where the configured join flow requires it.

If GameTest automatic updates are enabled, Realm Bot can update the managed pack before joining. A cheats-disabled warning does not necessarily prevent the Relay Account from connecting, but commands that require cheats will still fail.

> **Current limitation:** Reconnection is periodic and may take several minutes. Experimental or Beta joining should not be treated as automatically reliable, and uninterrupted connection is not guaranteed.

## Example

`/world join realm:<selected Realm>`

Select one Realm when restoring a specific service. Omission requests joining across all connected Realms.

## Common Issues

Expired authentication, missing Realm access, invalid codes, service rate limits, active-slot changes, or Relay service failures can prevent joining. Use the returned reason and verify the account in the dashboard.

## Related Commands

- [`/world leave`](leave.md)
- [`/world broadcast`](broadcast.md)
- [`/world execute`](execute.md)
- [Relay Account and GameTest Dependencies](<../../Realm Modules/relay-account-and-gametest.md>)
- [Command Troubleshooting](../troubleshooting.md)
