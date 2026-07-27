---
label: Command Troubleshooting
description: Resolve common Realm Bot slash-command permission, connection, Premium, Relay Account, GameTest, and input errors.
order: 0
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Command Troubleshooting

Use this page for failures shared by several Realm Bot commands. Command-specific limitations remain documented on the relevant command page.

## The Command Cannot Be Used Here

All Realm Bot commands must be used in a Discord server. If Discord reports that a command can only be used in a guild, leave the direct message and run it in a server channel where Realm Bot can respond.

Confirm Realm Bot has the required Discord channel permissions, usually **View Channel**, **Send Messages**, and **Embed Links**. Commands that post files or panels can require additional attachment or interaction permissions.

## The Server Is Not Connected

Most Realm, player, moderation, and activity commands require a connected server.

1. Confirm the intended Microsoft/Xbox account is linked in the Realm Bot Dashboard.
2. Ask a Discord Administrator to run `/connect`.
3. Confirm the expected Realms appear in the dashboard.

If the wrong account is connected, use the documented disconnect process carefully before reconnecting the correct account.

## Missing Realm Bot Command Permission

Permission-controlled commands require the exact permission listed on their command page. Assign it to an appropriate Discord role under [Server Permissions](<../Server Dashboard/server-permissions.md>).

Discord members with **Administrator** bypass the custom Realm Bot role map. Other Discord permissions, including Manage Server, do not automatically bypass it. Administrator bypass does not replace Premium or external account requirements.

## Premium Is Required

Premium commands require an active Realm Bot Premium subscription for the server account. Confirm the subscription is active and associated with the expected account. If a current subscription is not recognised, avoid repeatedly running a high-impact command and contact Realm Bot support with the server ID and approximate attempt time.

## A Realm Cannot Be Found

- Re-open the command and select the Realm from autocomplete rather than typing an old value.
- Confirm the connected Microsoft/Xbox account still owns or can access the Realm.
- Run `/connect` again only when you intend to refresh the server's Realm association.
- Check that the Realm was not moved to another Discord server configuration.

## A Player or Gamertag Cannot Be Found

- Confirm the gamertag spelling and the Microsoft/Xbox account being searched.
- Allow time for temporary Xbox profile service issues to clear.
- For Realm-member lookups, confirm the player belongs to the relevant Realm or appears in the command's expected source.

Different commands search different sources, such as Xbox profiles, Realm membership, official blocklists, stored activity, or live Relay data.

## Relay Account Is Offline

Live World commands and some player features require an active Relay Account.

- Confirm the Relay Account still has access to the selected Realm.
- Confirm persistent joining is enabled and use `/world join` for the intended Realm.
- Refresh expired Microsoft/Xbox authentication.
- Allow time for connection attempts; reconnection is not guaranteed to be immediate.

See [Relay Account and GameTest Dependencies](<../Realm Modules/relay-account-and-gametest.md>) for the shared setup.

## Operator Permission or Cheats Are Missing

Minecraft commands run with the Relay Account's in-game authority. Confirm the account has the permission required by the intended command and enable cheats only when acceptable for that Realm.

An Operator role does not grant Discord access, and a Realm Bot command permission does not grant Minecraft Operator authority.

## GameTest Data Is Unavailable

For features that use GameTest:

- Confirm the GameTest Pack is installed on the active world slot.
- Confirm the installed pack version is compatible.
- Enable **Beta APIs** when required by the installed pack.
- Allow the Relay Account to rejoin after pack or experiment changes.

GameTest is not required by every Relay feature. Check the individual command page before changing a Realm's experiments.

## Xbox or Realm Services Are Unavailable

Official Xbox and Realm services can temporarily fail or return incomplete information. Wait briefly, retry a read-only command, and verify important changes directly in Minecraft or the official Realm interface.

Do not immediately repeat a destructive action merely because Discord did not display the expected response.

## Invalid Input

### Duration

Use supported compact values such as `1h`, `1d`, or `1w`. A blank duration is meaningful only where the command page explicitly documents it.

### World slot

Use `1`, `2`, or `3`. Confirm the intended world before switching slots.

### Minecraft command

For `/world execute`, enter the Minecraft command without a leading `/`. Check the command's Bedrock syntax, selectors, operator requirements, and cheat requirements.

## No Stored Activity or Player Information

Playtime, sessions, Leveling, and offline player lookup depend on previously collected records. A player can be valid but still have no stored data if collection was not active while they played.

Restore the relevant connection or module, allow new activity to be collected, and treat old fallback information as potentially incomplete.

## The Interaction Remains Pending

An internal or external service error can occasionally prevent a deferred Discord interaction from completing.

- Check whether the action changed the Realm before retrying.
- For read-only commands, retry once after a short wait.
- For bans, backups, slot changes, link deletion, open/close, or World commands, verify the target state first.
- If the issue continues, contact support with the command, server ID, Realm name, and approximate time.

## Before Retrying a High-Impact Command

> **Important:** Discord output is not always proof that an external Realm operation completed or failed. Verify the actual Realm, membership, blocklist, backup, slot, or Relay state before repeating an action.
