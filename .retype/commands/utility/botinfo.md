# `/botinfo`

Displays operational information about Realm Bot and the cluster currently handling the command.

## Syntax

`/botinfo`

## Requirements

- The command must be used in a Discord server.
- The member must have `command.botinfo`, or be a Discord Administrator.
- The server does not need to be connected to a Microsoft/Xbox account.
- Premium is not required.

## Information Shown

- Global Discord server and user totals
- Current cluster ID
- Cluster Discord server and user totals
- Ping
- Uptime
- Aggregate Realm Bot statistics, including selected join, leave, relay, moderation, and membership totals

The command does not currently show a shard ID or application build/version.

## Related Commands

- [`/help`](help.md)
- [`/dashboard`](dashboard.md)
- [Command Troubleshooting](../troubleshooting.md)
