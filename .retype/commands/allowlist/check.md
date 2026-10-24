# `/allowlist check`

Checks whether a resolved Minecraft player is currently on Realm Bot's allowlist for the Discord server.

## Syntax

`/allowlist check <user>`

The required `user` argument is the player's Xbox gamertag.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- Realm Bot Premium must be active.
- No Realm Bot custom command-role permission is required.

The result is posted publicly in the channel where the command is used.

## Example

`/allowlist check user:ExamplePlayer`

Realm Bot reports whether the player is in the allowlist. This is a read-only check and does not change membership or exemptions.

## Common Issues

### The player cannot be found

Confirm the gamertag and the connected Microsoft/Xbox account. See [Command Troubleshooting](../troubleshooting.md) if profile lookups continue to fail.

## Related Commands

- [`/allowlist add`](add.md)
- [`/allowlist list`](list.md)
- [`/allowlist remove`](remove.md)
