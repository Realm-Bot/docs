---
label: Relay Account and GameTest
description: Check Relay Account access, install the GameTest bridge, and diagnose connection-dependent Realm Bot features.
order: 5
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Relay Account and GameTest Dependencies

Many Realm Bot features depend on a live account inside the Realm. A smaller set also depends on the Realm Bot GameTest Pack for scripted requests that are not available through the standard Realm connection.

## Relay Account

The **Relay Account** is the Microsoft/Xbox account Realm Bot uses to join the selected Realm and exchange live events or commands.

- The Realm owner account can be used as the Relay Account.
- An alternative account can be selected when that account has access to the Realm.
- The account must remain connected for live modules to operate.
- Commands that require elevated in-game access need sufficient operator permissions and, where applicable, cheats enabled.
- An active Realm Bot Premium subscription is required for the connected Relay Account workflow.

Realm maintenance, session disconnects or expired Microsoft/Xbox authentication can temporarily stop connection-dependent features.

**Compatibility note:** Realm Bot's world-joining support was updated for Minecraft 26.60 in version 5.3.0.

## GameTest Pack

The **Realm Bot GameTest Pack** provides an in-game bridge for features such as scoreboard retrieval and emote events. The v3 bridge version check starts at **3.0.0**. An installed pack is not proof that the bridge is responding; check the installed version and the Realm connection separately.

## Feature Dependency Matrix

| Feature                                    | GameTest required | Connected Relay Account required            |
| ------------------------------------------ | ----------------- | ------------------------------------------- |
| Chat Relay player chat                     | No                | Yes                                         |
| Chat Relay emotes                          | No                | Yes                                         |
| Scoreboard Leaderboards                    | Yes               | Yes                                         |
| Player Lookup enriched live data           | Conditional       | Yes for live data                           |
| Tebex empty-slot conditions                | Conditional       | Yes                                         |
| Live Playerlist, Leveling System           | No                | Yes                                         |
| Bot Detection, Member Gate, Skin Filtering | No                | Yes                                         |
| Realm Console                              | No                | Yes                                         |
| Realm Stories                              | No                | No; linked account access is still required |

**Conditional** means the feature can use GameTest for a specific data source or condition but may retain more limited behaviour without it.

[Realm Security](realm-security.md) requires a connected Relay Account for Lockdown kicks and Watchlist join detection. [Realm Stories](../Tools/realm-stories.md) collects posts through the Story Feed without an in-game connection.

## Install the GameTest Pack

1. Select the Discord server and Realm, then open **Overview > Gametest Pack Management**.
2. Review **Status**, **Pack version**, **Latest build** and **Last installed**. Check for updates.
3. Select **Install Pack** or **Update Pack** as appropriate. The installer places the bridge first among behaviour packs and preserves the other packs. An equal or newer bridge already in first position need not be reinstalled.
4. Check the displayed version after installation. To test a live feature, connect the Relay Account and check that the feature receives a response.

The dashboard uploads the pack using server access and the associated Realm; the Relay Account does not need to be in-game for the upload.

## Updates and Removal

- **Check For Updates** compares the installed and current pack versions.
- **Update Pack** installs the latest available managed version.
- **Auto Update Gametest Pack** is off by default. When enabled, it checks for an update when Realm Bot joins, not continuously.
- **Manual Download** provides the current pack for a manual installation workflow.
- **Remove Pack** removes the managed dependency.

Removing the pack stops GameTest-dependent features until it is installed again.

## Troubleshooting

### Relay Account is offline

- Confirm bot joining is enabled on the Realm Overview.
- Confirm the correct Realm and active slot are selected.
- Verify the owner or alternative account still has Realm access.
- Reconnect the Microsoft/Xbox account if authentication has expired.
- Confirm an active Premium subscription is available.

### GameTest requests fail or data is unavailable

- Check **Pack version** and **Latest build**. If no latest build appears, check that a bridge release is available.
- Verify the pack is active in the world you are using and that the Relay Account is connected.
- Check for a pack update and allow the Relay Account to rejoin.
- Verify the feature is listed as GameTest-dependent in the matrix above.

### Commands fail

- Confirm the Relay Account has sufficient operator permissions.
- Confirm cheats are enabled for commands that require them.
- Use explicit targets so executor-based commands do not affect the Relay Account unexpectedly.

### A module is enabled but produces no output

- Confirm the module is enabled for the correct Realm.
- Confirm its Discord destination and channel permissions.
- If the feature requires an in-game connection, confirm the Relay Account is online. Realm Stories instead requires valid linked-account access to the Story Feed.
- If the feature uses GameTest, confirm that its bridge is current and responding.
