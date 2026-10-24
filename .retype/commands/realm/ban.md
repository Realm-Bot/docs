# `/realm ban`

Adds a resolved Minecraft player to the official blocklist for one or more connected Realms.

## Syntax

`/realm ban <user> [realm] [reason] [duration] [attachment] [silent]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's Xbox gamertag. |
| `realm` | No | One Realm to target. If omitted, every connected Realm is targeted. |
| `reason` | No | The moderation reason recorded with the action. |
| `duration` | No | A value such as `1h`, `1d`, or `1w`. If blank, the ban is permanent. |
| `attachment` | No | Supporting evidence for the moderation record. |
| `silent` | No | Suppresses the configured Discord moderation-log message when enabled. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with permission to manage the target Realm.
- The member must have `command.realm.ban`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Example

`/realm ban user:ExamplePlayer realm:<selected Realm> reason:Rule violation duration:1d`

Realm Bot attempts the official blocklist action, records moderation context, and can send the configured player message. `silent:true` affects the configured Discord log output only; it does not suppress the blocklist action, audit record, or player message.

## Safety and Duration

> **Warning:** If `realm` is omitted, the player is targeted across every connected Realm. Select one Realm explicitly unless server-wide scope is intentional.

Invalid duration text returns an error.

> **Current limitation:** Automatic expiry of timed bans could not be confirmed. Treat a temporary ban as requiring later verification and use [`/realm unban`](unban.md) manually if the player remains blocked after the intended duration.

Verify the player's official blocklist status after the action, especially when the Realm service reports a partial or delayed result.

## Related Commands

- [`/realm unban`](unban.md)
- [`/banlist lookup`](../Banlist/lookup.md)
- [`/realm kick`](kick.md)
- [Command Troubleshooting](../troubleshooting.md)
