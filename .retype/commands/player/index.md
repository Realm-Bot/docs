# Player Commands

Player commands provide staff with detailed information about a selected player. Live enriched information depends on the Relay Account and GameTest path; stored fallback information can be older or incomplete.

The current player lookup requires a connected server, Premium, and the `command.player.lookup` Realm Bot permission.

## Commands

- [`/player lookup`](lookup.md) - retrieve live or stored player details and, where available, an inventory link.

Player information can include sensitive operational data such as location, tags, and inventory. Restrict this command to trusted staff and use it in an appropriate channel.

For a lighter official online-player view, use [`/realm players`](../Realm/players.md). For shared failures, see [Command Troubleshooting](../troubleshooting.md).
