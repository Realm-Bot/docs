# Relay Account and GameTest Dependencies

Many Realm Bot features depend on a live account inside the Realm. A smaller set also depends on the Realm Bot GameTest Pack for scripted requests that are not available through the standard Realm connection.

## Relay Account

The **Relay Account** is the Microsoft/Xbox account Realm Bot uses to join the selected Realm and exchange live events or commands.

- The Realm owner account can be used as the Relay Account.
- An alternative account can be selected when that account has access to the Realm.
- The account must remain connected for live modules to operate.
- Commands that require elevated in-game access need sufficient operator permissions and, where applicable, cheats enabled.
- An active Realm Bot Premium subscription is required for the connected Relay Account workflow.

Do not promise uninterrupted operation. Realm maintenance, session disconnects, or expired Microsoft/Xbox authentication can temporarily stop connection-dependent features.

## GameTest Pack

The **Realm Bot GameTest Pack** provides an in-game request channel for features such as scoreboard retrieval and emote events. It requires **Beta APIs** to be enabled in the Realm's experimental settings.

The pack version must remain compatible with the version expected by Realm Bot. A pack that is installed but outdated can behave like a missing pack.

## Feature Dependency Matrix

| Feature | GameTest Required | Beta APIs Required | Relay Account Required |
|---|---:|---:|---:|
| Chat Relay player chat | No | No | Yes |
| Chat Relay emotes | Yes | Yes | Yes |
| Scoreboard Leaderboards | Yes | Yes | Yes |
| Player Lookup enriched live data | Conditional | Conditional | Yes for live data |
| Tebex empty-slot conditions | Conditional | Conditional | Yes |
| Live Playerlist | No | No | Yes |
| Leveling System | No | No | Yes |
| Bot Detection | No | No | Yes |
| Member Gate | No | No | Yes |
| Skin Filtering | No | No | Yes |
| Realm Console | No | No | Yes |

**Conditional** means the feature can use GameTest for a specific data source or condition but may retain more limited behaviour without it.

## Install the GameTest Pack

1. Open the selected Realm's **Overview** page.
2. Confirm the correct world slot is active.
3. Enable **Beta APIs** in the Realm settings.
4. Under **GameTest Pack Management**, select **Install Pack**.
5. Allow Realm Bot to join the Realm and confirm the installed version is current.

An active Realm slot and a healthy Relay Account connection are required for managed installation.

## Updates and Removal

- **Check For Updates** compares the installed and current pack versions.
- **Update Pack** installs the latest available managed version.
- **Auto Update GameTest Pack** applies an available update when Realm Bot next joins; it is not a continuous background scheduler.
- **Manual Download** provides the current pack for a manual installation workflow.
- **Remove Pack** removes the managed dependency from the selected Realm slot.

Removing the pack stops GameTest-dependent features until it is installed again.

## Troubleshooting

### Relay Account is offline

- Confirm bot joining is enabled on the Realm Overview.
- Confirm the correct Realm and active slot are selected.
- Verify the owner or alternative account still has Realm access.
- Reconnect the Microsoft/Xbox account if authentication has expired.
- Confirm an active Premium subscription is available.

### GameTest requests fail or data is unavailable

- Confirm the pack is installed on the active slot.
- Confirm **Beta APIs** are enabled.
- Check for a pack update and allow the Relay Account to rejoin.
- Verify the feature is listed as GameTest-dependent in the matrix above.

### Commands fail

- Confirm the Relay Account has sufficient operator permissions.
- Confirm cheats are enabled for commands that require them.
- Use explicit targets so executor-based commands do not affect the Relay Account unexpectedly.

### A module is enabled but produces no output

- Confirm the module is enabled for the correct Realm.
- Confirm its Discord destination and channel permissions.
- Confirm the Relay Account is online.
- If the feature uses GameTest, confirm the pack, Beta APIs, and version first.
