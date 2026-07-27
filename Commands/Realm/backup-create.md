---
label: "/realm backup-create"
description: Start a named backup request for a selected Minecraft Bedrock Realm.
order: 80
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/realm backup-create`

Starts a backup request for one selected Realm. The command reports when creation has started; it does not guarantee that asynchronous processing has fully completed.

## Syntax

`/realm backup-create <realm> [name]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `realm` | Yes | The Realm to back up. |
| `name` | No | A custom backup name. If omitted, Realm Bot generates a name. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with access to the Realm.
- The member must have `command.realm.backup-create`, the legacy `command.realm.backup`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Example

`/realm backup-create realm:<selected Realm> name:Before event`

Realm Bot submits the backup request and reports that creation has started.

## Verify the Backup

Use [`/realm backup-list`](backup-list.md) to confirm that the backup appears and to review its details. Do not treat the initial response as proof that processing is complete.

## Related Commands

- [`/realm backup-list`](backup-list.md)
- [Command Troubleshooting](../troubleshooting.md)
