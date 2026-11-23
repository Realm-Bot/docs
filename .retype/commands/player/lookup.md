# `/player lookup`

Retrieves detailed information about a player associated with a selected Realm. Realm Bot attempts live enriched retrieval first and can use its most recent stored player record when the live path is unavailable.

## Syntax

`/player lookup <realm> <user>`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `realm` | Yes | The connected Realm to search. |
| `user` | Yes | The player's Xbox gamertag. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- Realm Bot Premium must be active.
- The member must have `command.player.lookup`, or be a Discord Administrator.
- Live enriched data requires the Relay Account to be online with a compatible GameTest Pack.
- **Beta APIs** must be enabled where required by the installed GameTest Pack.

See [Relay Account and GameTest Dependencies](<../../Realm Modules/relay-account-and-gametest.md>) for the live setup.

## Information Returned

Where available, the response can include:

- Health and gamemode
- Coordinates and dimension
- Spawn coordinates and dimension
- Player tags
- Last recorded observation
- A **View Inventory** web link

The Discord command does not attach an inventory image. Inventory is opened through the Realm Bot web interface when suitable data is available.

## Live and Stored Results

If the player is online and the Relay/GameTest request succeeds, the result can contain current enriched information. Otherwise, Realm Bot can fall back to a stored player record.

> **Current limitation:** Stored data may be older, incomplete, or shaped differently from a live result. Do not treat an offline location or inventory as current.

## Privacy

Location, tags, and inventory can be sensitive moderation data. Grant `command.player.lookup` only to trusted staff and run the command in a restricted channel where appropriate.

## Common Issues

### Live data cannot be retrieved

Confirm the player is online, the Relay Account is connected, the GameTest Pack is compatible, and required Beta APIs are enabled.

### No stored player is found

The player may not have been observed while data collection was operational. Allow the player and Relay Account to be online before retrying.

## Related Commands

- [`/realm players`](../Realm/players.md)
- [Relay Account and GameTest Dependencies](<../../Realm Modules/relay-account-and-gametest.md>)
- [Command Troubleshooting](../troubleshooting.md)
