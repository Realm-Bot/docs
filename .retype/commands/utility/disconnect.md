# `/disconnect`

Disconnects the current Discord server from its linked Microsoft/Xbox account. An optional mode removes the server's primary stored Guild record.

## Syntax

`/disconnect [guild]`

The optional Boolean `guild` argument defaults to `false`.

## Requirements

- The server must currently be connected.
- The invoking Discord member's linked Xbox identity must match the account connected to the server.
- The member must have `command.disconnect`, or be a Discord Administrator.
- Premium is not required.

## Modes

- `guild:false` or omission clears the Guild's connected-account association.
- `guild:true` removes the primary stored Guild record.

> **Warning:** There is no confirmation prompt. Record or export important settings before disconnecting.

Do not use `guild:true` as a data-erasure request. Contact Realm Bot support if you need all data associated with a server removed.

## Example

`/disconnect guild:false`

Use the default mode when the goal is to unlink the account without requesting removal of the primary Guild record.

## Related Commands

- [`/connect`](connect.md)
- [`/dashboard`](dashboard.md)
- [Command Troubleshooting](../troubleshooting.md)
