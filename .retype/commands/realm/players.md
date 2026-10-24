# `/realm players`

Displays players currently reported online through the official Realm and Xbox services.

## Syntax

`/realm players [realm]`

The optional `realm` argument selects one Realm. If omitted, Realm Bot retrieves each Realm associated with the connected server account.

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.realm.players`, or be a Discord Administrator.
- Premium, the Relay Account, GameTest, and Beta APIs are not required.

## Display Modes

The server's [Command Settings](<../../Server Dashboard/server-command-settings.md>) control the output:

- **Compact** displays the gamertag and detected device.
- **Detailed** can also display the player's official Realm permission.

The runtime does not currently provide gamerscore or an Xbox Gold/Silver indicator through this command.

When several Realms are displayed, the public controls move between Realm results.

## Common Issues

If a player is missing, confirm they are currently online and wait for official Realm presence data to refresh. This view is separate from Relay/GameTest player lookup.

## Related Commands

- [`/player lookup`](../Player/lookup.md)
- [`/realm members`](members.md)
- [Command Troubleshooting](../troubleshooting.md)
