---
label: "/allowlist list"
description: Display Realm Bot's server-level allowlist using interactive pages of ten players.
order: 95
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/allowlist list`

Displays the current Realm Bot allowlist for the Discord server.

## Syntax

`/allowlist list`

This command has no arguments.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- Realm Bot Premium must be active.
- The member must have `command.allowlist.list`, or be a Discord Administrator.

## Output

Realm Bot resolves stored players and displays up to **ten entries per page**. Use the interactive controls to move between pages.

The response and its controls are public. Run the command in an appropriate staff channel if the allowlist should not be visible to general members.

## Common Issues

### A name cannot be resolved

Temporary Xbox profile failures can prevent a stored XUID from displaying as expected. Retry later before changing the entry.

### Pagination does not respond

The controls expire after a short period. Run the command again to create a new list view.

## Related Commands

- [`/allowlist add`](add.md)
- [`/allowlist check`](check.md)
- [`/allowlist remove`](remove.md)
- [Command Troubleshooting](../troubleshooting.md)
