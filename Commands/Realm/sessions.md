---
label: "/realm sessions"
description: Display a player's recorded Realm activity intervals grouped by day.
order: 81
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/realm sessions`

Displays recorded activity intervals for one player and Realm, grouped by day.

## Syntax

`/realm sessions <user> <realm>`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `realm` | Yes | The Realm whose activity will be displayed. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.realm.sessions`, or be a Discord Administrator.
- Activity must have been collected for the player.
- Premium and a currently active Relay Account are not required to read existing data.

## Output

Each day can include session start, end, duration, and a daily total. Interactive pages display up to **five days per page**.

The upstream activity service defines the available date range. Stored sessions can be incomplete if collection was unavailable while the player was active.

## Related Commands

- [`/realm playtime`](playtime.md)
- [`/realm recents`](recents.md)
- [Command Troubleshooting](../troubleshooting.md)
