# `/realm slot`

Requests that a selected Realm switch its active world to slot `1`, `2`, or `3`.

## Syntax

`/realm slot <realm> <slot>`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `realm` | Yes | The Realm whose active world will change. |
| `slot` | Yes | The target world slot: `1`, `2`, or `3`. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account with permission to manage the Realm.
- The member must have `command.realm.slot`, or be a Discord Administrator.
- Premium and an active Relay Account are not required.

## Safety

> **Warning:** Switching slots changes the active Realm world and has no confirmation prompt. Players may be disconnected and Realm availability can be interrupted.

Use this command during a maintenance window. Confirm the intended Realm and slot, create or verify an appropriate backup, and notify players first.

> **Current limitation:** The Discord success response can appear before the Realm service confirms completion. Verify the active slot in the official Realm interface before continuing.

## Related Commands

- [`/realm backup-create`](backup-create.md)
- [`/realm backup-list`](backup-list.md)
- [Command Troubleshooting](../troubleshooting.md)
