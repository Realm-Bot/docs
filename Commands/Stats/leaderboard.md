---
label: "/leaderboard"
description: Open the Discord server's public Realm Bot web leaderboard.
order: 96
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/leaderboard`

Provides a button linking to the current Discord server's public Realm Bot web leaderboard.

## Syntax

`/leaderboard`

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- No Realm Bot custom command-role permission is required.
- Premium is not required.

## Output

The command links to:

`https://dashboard.realmbot.dev/leaderboard/<server_id>/`

It does not render leaderboard entries directly in Discord.

This is the Leveling/playtime web leaderboard. It is separate from the [Scoreboard Leaderboards](<../../Realm Modules/scoreboard-leaderboards.md>) Realm Module, which publishes Minecraft scoreboard values to Discord.

## Related Commands

- [`/rank`](rank.md)
- [`/realm playtime`](../Realm/playtime.md)
- [Command Troubleshooting](../troubleshooting.md)
