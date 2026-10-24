# `/realm playtime`

Calculates a player's total from the recorded activity intervals returned for one selected Realm.

## Syntax

`/realm playtime <user> <realm>`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `realm` | Yes | The Realm whose recorded activity will be totalled. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.realm.playtime`, or be a Discord Administrator.
- Activity must have been collected for the player.
- Premium and a currently active Relay Account are not required to read existing data.

## Data Range

Realm Bot adds the available recorded session intervals and displays one total duration.

The activity service defines the returned date range. Do not assume a fixed one-month window unless the current dashboard or service explicitly confirms it.

## Common Issues

`No activity found` means Realm Bot received no usable intervals for the player and Realm. It does not prove the player has never joined.

## Related Commands

- [`/realm sessions`](sessions.md)
- [`/leaderboard`](../Stats/leaderboard.md)
- [Command Troubleshooting](../troubleshooting.md)
