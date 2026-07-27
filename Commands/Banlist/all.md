---
label: "/banlist all"
description: List players on a selected Minecraft Realm's official blocklist.
order: 97
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/banlist all`

Displays the official Minecraft blocklist for one connected Realm. It does not query Realm Bot's separate Global Ban system.

## Syntax

`/banlist all <realm>`

The required `realm` argument selects the Realm whose blocklist will be read.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with access to the Realm.
- The member must have `command.banlist.all`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Output

Realm Bot resolves available Xbox profiles and displays up to **15 blocked players per page**.

> **Current limitation:** Some pagination controls may not behave as expected. If the required page cannot be reached, run the command again and verify the blocklist through the official Realm interface.

## Common Issues

### No blocked players are shown

The Realm may have an empty blocklist, but an Xbox or Realm API failure can also produce an empty result. Verify the official blocklist before treating the result as complete.

## Related Commands

- [`/banlist lookup`](lookup.md)
- [`/realm ban`](../Realm/ban.md)
- [`/realm unban`](../Realm/unban.md)
- [Command Troubleshooting](../troubleshooting.md)
