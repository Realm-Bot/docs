# `/connect`

Connects the current Discord server to the invoking member's linked Microsoft/Xbox account and refreshes the Realms available through that account.

## Syntax

`/connect`

## Requirements

- The invoking Discord member must first link their Microsoft/Xbox account in the Realm Bot Dashboard.
- The member must have `command.connect`, or be a Discord Administrator.
- The linked account must own or have usable access to at least one Realm.
- Premium is not required for the connection command itself.

On a new server, a Discord Administrator is normally the practical first caller because no Realm Bot role permissions have been configured yet.

## What the Command Does

Realm Bot:

1. Refreshes the Realms available through the linked Microsoft/Xbox account.
2. Associates the Discord server with that account.
3. Registers the server's Realm Bot slash commands.
4. Reports the connected Realms.

Ensure each Realm has usable access or invite information, commonly a permanent official code where the configured workflow requires one.

## Migration Warning

> **Warning:** Connecting a Realm that is already associated with another Discord server can move that Realm's stored association to the new server and reset its Realm Module configuration. There is no separate migration confirmation.

Before running `/connect`:

- Confirm the intended Discord server and Microsoft/Xbox account.
- Record important module destinations and settings.
- Check whether the same Realms are already managed from another server.

Command registration can take a short time after the connection response.

## Related Commands

- [`/disconnect`](disconnect.md)
- [`/dashboard`](dashboard.md)
- [Getting Started](../../setup.md)
- [Command Troubleshooting](../troubleshooting.md)
