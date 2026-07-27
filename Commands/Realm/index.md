# Realm Commands

Realm commands use the connected Microsoft/Xbox account to manage official Minecraft Bedrock Realm data and Realm Bot's stored records. They require a connected server and the named Realm Bot command permission.

> **Important:** Several commands accept an optional Realm. When omitted, the action targets every Realm associated with the connected server account. Select one Realm explicitly for high-impact changes.

## Player Moderation and Membership

- [`/realm ban`](ban.md)
- [`/realm unban`](unban.md)
- [`/realm kick`](kick.md)
- [`/realm invite`](invite.md)
- [`/realm permission`](permission.md)

## Realm Administration

- [`/realm open`](open.md)
- [`/realm close`](close.md)
- [`/realm rename`](rename.md)
- [`/realm nickname`](nickname.md)
- [`/realm slot`](slot.md)
- [`/realm code-manage`](code-manage.md)

## Players and Activity

- [`/realm players`](players.md)
- [`/realm members`](members.md)
- [`/realm recents`](recents.md)
- [`/realm lastseen`](lastseen.md)
- [`/realm playtime`](playtime.md)
- [`/realm sessions`](sessions.md)

## Backups and Recovery

- [`/realm backup-create`](backup-create.md)
- [`/realm backup-list`](backup-list.md)

Realm API responses can be delayed or incomplete. Verify access, blocklist, slot, backup, and availability changes directly before repeating an action. For shared failures, see [Command Troubleshooting](../troubleshooting.md).
