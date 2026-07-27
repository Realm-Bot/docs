---
label: "/realm recents"
description: Display up to 100 recently seen Xbox club members for a selected Realm.
order: 84
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/realm recents`

Displays recently seen players from the selected Realm's Xbox club/member information.

## Syntax

`/realm recents <realm>`

The required `realm` argument selects one Realm.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with access to the Realm.
- The member must have `command.realm.recents`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Output

Realm Bot sorts the available records by most recently seen, takes up to **100 players**, and groups them into age ranges from recent minutes through older periods. Interactive controls move between the groups.

This command reads Xbox club/member data. It is not the Relay Account's local session history.

## Common Issues

Xbox privacy, club visibility, profile lookup failures, or service delays can make the list incomplete.

## Related Commands

- [`/realm lastseen`](lastseen.md)
- [`/realm sessions`](sessions.md)
- [Command Troubleshooting](../troubleshooting.md)
