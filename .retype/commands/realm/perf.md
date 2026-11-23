# `/realm perf`

Sends a PNG graph of recent Realm performance and a **Visit Dashboard** button. The posted graph is a snapshot; it does not update in Discord.

## Syntax

`/realm perf realm:<realm> [metrics:<combination>]`

| Argument | Required | Description |
|---|---:|---|
| `realm` | Yes | Select the Realm from autocomplete. |
| `metrics` | No | Choose a combination of CPU, Memory, Tick time and Players. Omit to show all four. |

## Requirements

- The Discord member needs the **Realm Performance** command permission or Discord **Administrator**.
- The server's linked Xbox account must have game-settings access to the selected **Minecraft Realms Pro** Realm.

## Troubleshooting

If the Realm is missing or access is denied, check the selected Realm, its Minecraft subscription and both sets of permissions. If there is no usable performance history, check [Server Performance](<../../Realm Page/server-performance.md>) again later. Recent historical samples can take up to ten minutes to appear.
