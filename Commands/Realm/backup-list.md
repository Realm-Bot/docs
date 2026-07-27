---
label: "/realm backup-list"
description: List, save, and restore automatic or manual backups for a selected Realm.
order: 79
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/realm backup-list`

Opens an interactive backup manager for one Realm. It lists automatic and saved backups, displays storage information where available, and provides save and restore actions.

## Syntax

`/realm backup-list <realm>`

The required `realm` argument selects the Realm whose backups will be managed.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with access to the Realm.
- The member must have `command.realm.backup-list`, the legacy `command.realm.backup`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Backup Manager

- Select automatic or saved/manual backups.
- View up to **five backups per page**.
- Review backup storage information where the service provides it.
- Save an automatic backup under a custom name of up to **20 characters**.
- Restore a displayed backup to the Realm.

## Restore Safety

> **Warning:** Restore immediately rolls the selected Realm back to the selected backup. Current world progress after that backup can be lost, and there is no separate confirmation prompt.

Before selecting **Restore**:

1. Confirm the correct Realm is shown.
2. Confirm the backup type, date, and name.
3. Notify active players and stop important activity.
4. Allow the restore time to finish before attempting another operation.

The restore process may take time. Verify the resulting world directly in the Realm, and do not repeat the action merely because Discord status appears delayed.

## Common Issues

### No backups are shown

The Realm may not have available backups, or the official backup service may be temporarily unavailable. Retry later before assuming no recovery point exists.

### Saving or restoring fails

Confirm the backup still exists, the custom name is no longer than 20 characters, and the connected account retains Realm access.

## Related Commands

- [`/realm backup-create`](backup-create.md)
- [`/realm slot`](slot.md)
- [Command Troubleshooting](../troubleshooting.md)
