# Commands

Realm Bot commands are Discord slash commands. Run them in a Discord server channel where Realm Bot can respond; commands cannot be used in direct messages.

## Command Access

Realm Bot commands use several access models:

- **Public commands** do not require a Realm Bot role permission, although they must still be used in a Discord server.
- **Connected-server commands** require the Discord server to be connected to a Microsoft/Xbox account through `/connect`.
- **Premium commands** require an active Realm Bot Premium subscription.
- **Permission-controlled commands** require the named Realm Bot command permission assigned to one of the member's Discord roles.

Discord members with the **Administrator** permission bypass Realm Bot's custom command permission map. This does not bypass Premium, account-linking, Realm access, Relay Account, GameTest, or Minecraft permission requirements.

## Separate Permission Systems

These permissions are independent:

- **Discord channel permissions** control where members and Realm Bot can read, post, and use interactions.
- **Realm Bot command permissions** control which roles can run supported slash commands.
- **Minecraft Realm permissions** control whether a player is a Visitor, Member, or Operator.
- **Minecraft operator permission and cheats** control what the in-game Relay Account can execute.

Review [Server Permissions](<../Server Dashboard/server-permissions.md>) before granting high-impact commands to staff.

## Syntax

- `<required>` means the argument must be supplied.
- `[optional]` means the argument can be omitted.

Discord displays command arguments as named fields. Examples such as `realm:<selected Realm>` mean choosing a Realm from the command interface.

> **Important:** For commands with an optional `realm` argument, omitting it can target every Realm connected through the server account. Read the command page and select one Realm explicitly when the action changes access, membership, permissions, or world state.

## Command Categories

- [Allowlist](Allowlist/index.md) - manage Realm Bot's server-level automation exemptions.
- [Banlist](Banlist/index.md) - inspect official Realm blocklists and submit Global Ban reports.
- [Player](Player/index.md) - retrieve live or stored player information.
- [Realm](Realm/index.md) - manage membership, moderation, settings, activity, and backups.
- [Invites](Invites/index.md) - create and manage Realm Bot web invite links.
- [Stats](Stats/index.md) - open the web leaderboard or generate a Leveling rank card.
- [Utility](Utility/index.md) - connect Realm Bot and open common service links.
- [Verify](Verify/index.md) - publish the Microsoft/Xbox account-linking panel.
- [Warn](Warn/index.md) - create and review player warning records.
- [World](World/index.md) - connect the Relay Account and perform live in-game actions.

For shared error guidance, see [Command Troubleshooting](troubleshooting.md).
