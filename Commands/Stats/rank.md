---
label: "/rank"
description: Generate a rank-card image from a player's stored Leveling System XP and level.
order: 97
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/rank`

Generates a rank-card image from the selected Realm's stored [Leveling System](<../../Realm Modules/leveling-system.md>) data.

## Syntax

`/rank <realm> [user]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `realm` | Yes | The Realm whose Leveling data will be used. |
| `user` | No | The target gamertag. If omitted, Realm Bot looks up the invoking Discord member. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- No Realm Bot custom command-role permission is required.
- Premium is not required.
- Self lookup requires the Discord member to have a linked Microsoft/Xbox identity.
- The Leveling System must have recorded XP for a meaningful rank.

## Output

Realm Bot reads the player's stored XP and level, calculates their position relative to other players in that Realm, and attaches a `rank.png` card.

If the player has no recorded XP or level, Realm Bot prompts them to play before a rank can be shown.

## Common Issues

Xbox profile retrieval, colour preference retrieval, or image rendering can prevent the card from being generated. Retry later and confirm Leveling data exists.

## Related Commands

- [`/leaderboard`](leaderboard.md)
- [Leveling System](<../../Realm Modules/leveling-system.md>)
- [Command Troubleshooting](../troubleshooting.md)
