# World Commands

World commands operate through the live Relay Account. All require a connected server, Realm Bot Premium, and their named Realm Bot command permission.

Broadcast and execute require an active Relay connection. Their Minecraft operations run with the Relay Account's in-game authority, so operator permission and cheats may also be required.

## Commands

- [`/world join`](join.md) - enable persistent joining and request a Relay connection.
- [`/world leave`](leave.md) - disable persistent joining and stop the connection.
- [`/world broadcast`](broadcast.md) - send a formatted in-game announcement.
- [`/world execute`](execute.md) - execute a Minecraft command with the Relay Account's authority.

> **Important:** Omitted Realm arguments target all connected Realms. Restrict World permissions to trusted technical administrators and select one Realm explicitly whenever possible.

See [Relay Account and GameTest Dependencies](<../../Realm Modules/relay-account-and-gametest.md>) and [Command Troubleshooting](../troubleshooting.md).
