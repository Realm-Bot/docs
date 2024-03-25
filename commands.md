---
label: Command List
order: 100
icon: cpu
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
---

## Global Commands

{.compact}
| Command | Description | Usage |
| :--------------------------------- | :---------- | :---------------- |
| [/help](/command/help) | Displays the help embed and a invite to the support server | `/help` |
| [/connect](/command/connect) | Allows you to connect your xbox account the guild, enabling the realm commands | `/connect` |
| [/dashboard](/command/dashboard) | Sends you a link to the guilds web dashboard | `/dashboard` |
| [/invite](/command/invite) | Displays the invite Url to invite Realm Bot to your guild | `/invite` |
| [/disconnect](/command/disconnect) | Disconnects the current xbox account from the guild | `/disconnect` |
| [/rank](/command/rank) | Displays the rank of the user | `/rank` |
| [/leaderboard](/command/leaderboard) | Displays the leaderboard of the guild | `/leaderboard` |
| [/premium](/command/premium) | Displays the premium information | `/premium` |
| [/shard](/command/shard) | Displays the shard information | `/shard` |

## Realm Management Commands

{.compact}
| Command | Description | Usage |
| :--------------------------------- | :---------- | :---------------- |
| [/realm backup](/command/realm-backup) | Backups the realm | `/realm backup` |
| [/realm ban](/command/realm-ban) | Bans a player from the realm | `/realm ban <player> [realm] [reason] [duration] [attachment] [silent]` |
| [/realm close](/command/realm-close) | Closes the realm | `/realm close <realm>` |
| [/realm code-change](/command/realm-code-change) | Changes the realm code | `/realm code-change <realm>` |
| [/realm code](/command/realm-code) | Displays the realm code | `/realm code <realm>` |
| [/realm invite](/command/realm-invite) | Invites a player to the realm | `/realm invite <player> [realm]` |
| [/realm kick](/command/realm-kick) | Kicks a player from the realm | `/realm kick <player> [realm] [reason]` |
| [/realm lastseen](/command/realm-lastseen) | Displays the last seen date of a player on all realms | `/realm lastseen <player>` |
| [/realm nickname](/command/realm-nickname) | Changes the display name of the realm on realm bot | `/realm nickname <realm> <nickname>` |
| [/realm open](/command/realm-open) | Opens the realm | `/realm open <realm>` |
| [/realm permission](/command/realm-permission) | Changes the permission of a player on the realm | `/realm permission <player> <permission> [realm]` |
| [/realm players](/command/realm-players) | Displays the players on the realm | `/realm players <realm>` |
| [/realm recents](/command/realm-recents) | Displays the recent players on the realm | `/realm recents <realm>` |
| [/realm slot](/command/realm-slot) | Changes the realm slots | `/realm slot <realm> <slots>` |
| [/realm unban](/command/realm-unban) | Unbans a player from the realm | `/realm unban <player> [realm] [reason] [attachment] [silent]` |

## Allowlist commands

{.compact}
| Command | Description | Usage |
| :--------------------------------- | :---------- | :---------------- |
| [/allowlist add](/command/allowlist-add) | Adds a player to the realm allowlist | `/realm allowlist add <player>` |
| [/allowlist remove](/command/allowlist-remove) | Removes a player from the realm allowlist | `/realm allowlist remove <player>` |
| [/allowlist list](/command/allowlist-list) | Lists the players on the realm allowlist | `/realm allowlist list` |
| [/allowlist check](/command/allowlist-check) | Checks if a player is on the realm allowlist | `/realm allowlist check <player>` |

## Banlist commands

{.compact}
| Command | Description | Usage |
| :--------------------------------- | :---------- | :---------------- |
| [/banlist all](/command/banlist-all) | Lists all the players on the realm banlist | `/realm banlist all` |
| [/banlist lookup](/command/banlist-lookup) | Looks up a player on the realm banlist | `/realm banlist lookup <player>` |

## Verify commands

{.compact}
| Command | Description | Usage |
| :--------------------------------- | :---------- | :---------------- |
| [/verify embed](/command/verify-embed) | Displays the verify embed | `/verify embed` |


## World commands

{.compact}
| Command | Description | Usage |
| :--------------------------------- | :---------- | :---------------- |
| [/world broadcast](/command/world-broadcast) [!badge variant="warning" text="Premium"] | Broadcasts a message to the realm | `/world broadcast <realm> <message>` |
| [/world execute](/command/world-execute) [!badge variant="warning" text="Premium"] | Executes a command on the realm | `/world execute <realm> <command>` |
| [/world join](/command/world-join) [!badge variant="warning" text="Premium"] | Joins the realm | `/world join <realm>` |
| [/world leave](/command/world-leave) [!badge variant="warning" text="Premium"] | Leaves the realm | `/world leave <realm>` |

## Player commands

{.compact}
| Command | Description | Usage |
| :--------------------------------- | :---------- | :---------------- |
| [/player lookup](/command/player-lookup) [!badge variant="warning" text="Premium"] | Displays the player inventory, location etc. | `/player lookup <realm> <player>` |
