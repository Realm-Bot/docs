# Warn Commands

Warn commands manage Realm Bot moderation records for Minecraft players. Warning reasons can use dashboard presets, and a configured count threshold can attempt an official Realm ban.

These commands require a connected server and their named Realm Bot command permission. They do not manage Discord warnings or Realm Bot Global Ban entries.

## Commands

- [`/warn add`](add.md) - record a warning and evaluate its threshold.
- [`/warn lookup`](lookup.md) - review warning and removal history.
- [`/warn remove`](remove.md) - record a warning-removal event.

When a threshold action is expected, verify the player's official Realm blocklist status. See [Warning Configuration](<../../Server Dashboard/server-warnings.md>) and [Command Troubleshooting](../troubleshooting.md).
