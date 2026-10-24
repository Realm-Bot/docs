---
label: Realm Security
description: Configure temporary Realm lockdowns and staff alerts for watched players using the Lockdown and Watchlist controls.
order: 55
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Realm Security

Realm Security provides two **Realm Bot Premium** features: **Lockdown**, which restricts who can remain in a Realm, and **Watchlist**, which alerts staff when selected players join.

Open **Automod > Security** for the selected Realm in the dashboard. Lockdown and Watchlist have separate tabs and enable switches, and their settings apply only to that Realm.

---

## Requirements

- An active Realm Bot Premium subscription.
- A connected Microsoft/Xbox account with access to the selected Realm.
- The **Relay Account** connected in-game to perform Lockdown kicks and receive Watchlist join events.
- Sufficient in-game command privileges for Lockdown kicks.
- A configured Discord destination for Watchlist alerts.

Realm Bot needs **View Channel**, **Send Messages**, and **Embed Links** in the Watchlist destination. If you select a **Ping Role**, Discord must also permit Realm Bot to mention that role.

Changes on both dashboard tabs save automatically after approximately **1.5 seconds** without further edits. Check the header for pending changes, saving progress, or an error with a **Retry** option.

For shared connection guidance, see [Relay Account and GameTest Dependencies](relay-account-and-gametest.md).

---

## Lockdown

Lockdown temporarily removes players outside an allowed group while the Realm continues running. It checks players already online when activated and checks subsequent joins while enforcement remains active.

Lockdown kicks do **not** create permanent bans or close the Realm.

### Configure Lockdown

1. Open **Automod > Security** and select the **Lockdown** tab.
2. Enable **Lockdown Configuration**.
3. Choose whether to **Allow Operators**.
4. Add any approved players to the **Lockdown Exempt List** using their gamertag or XUID.
5. Confirm the dashboard has saved the settings before activating lockdown.

An **XUID** is a player's Xbox account identifier. The exempt list shows each player, who added them, and the date added. It supports searching and removal, with ten entries displayed per page.

> **Important:** Enabling **Lockdown Configuration** prepares the feature for use. Activate the lockdown separately with `/realm lockdown` in Discord.

### Who Can Remain

| Player group | Allowed during lockdown |
|---|---|
| Realm owner | Yes |
| Account used by the bot | Yes |
| Players on the Lockdown Exempt List | Yes |
| Minecraft Realm operators | Only when **Allow Operators** is enabled |
| Other players | No |

**Allow Operators** is enabled by default. Turning it off leaves access to the Realm owner, the bot account, and explicitly exempted players.

A Discord staff role does not automatically make someone a Minecraft operator or exempt them from Lockdown. Exemptions apply only to this check: players still need normal Realm access and remain subject to other moderation rules.

### Activate or End Lockdown

Run these commands in Discord, selecting the intended Realm:

| Command | Purpose |
|---|---|
| `/realm lockdown realm:<selected Realm>` | Activate lockdown and check players already online |
| `/realm unlock realm:<selected Realm>` | End the active lockdown |

Omitting `realm` applies the action across the account's Realms available through the command. Select one Realm explicitly when you intend to affect only that Realm.

Activation attempts to kick players outside the allowed group. If the command reports that some players could not be checked or removed, the lockdown can still be active. Restore the bot's connection and retry the check; do not assume a partial failure cancelled the restriction.

### Changing an Active Lockdown

Use **`/realm unlock`** to end an active lockdown.

Turning off **Lockdown Configuration** pauses enforcement but preserves the saved configuration and active-lockdown state. Turning it back on can therefore resume restrictions.

Changing exemptions or **Allow Operators** does not automatically check everyone already online again. Run `/realm lockdown` again for the selected Realm when you need another check.

---

## Watchlist

Watchlist sends a Discord alert when Realm Bot detects a watched player joining the configured Realm. It reports the player's name, an avatar when available, the Realm, and a timestamp. An optional staff role can be mentioned.

Watchlist is an alerting feature. Adding a player does not ban or remove them, and does not exempt them from Lockdown. Alerts operate independently of Chat Relay's ordinary join/leave messages.

### Configure Watchlist

1. Open **Automod > Security** and select the **Watchlist** tab.
2. Enable **Watchlist Configuration**.
3. Select the **Discord Destination** for alerts.
4. Optionally select a **Ping Role**.
5. Add players under **Watched Players** using their gamertag or XUID.
6. Confirm the dashboard has saved the settings.

Entries are matched using Xbox account identity. The list shows names and XUIDs, supports searching and removal, and displays ten players per page.

### Manage Players from Discord

| Command | Purpose |
|---|---|
| `/watchlist add user:<gamertag-or-XUID> realm:<selected Realm>` | Add a player to the selected Realm's watchlist |
| `/watchlist remove user:<gamertag-or-XUID> realm:<selected Realm>` | Remove a watched player |
| `/watchlist list realm:<selected Realm>` | Show the watched players |

Adding a player through a command does not enable Watchlist notifications or choose a destination. Configure those settings in the dashboard. Discord lists include navigation buttons when there are more than ten entries.

Watchlist reports only joins detected in the configured Realm. It does not track a player's activity across other Realms or all of Minecraft.

---

## Staff Permissions

Discord Administrators pass Realm Bot's command-permission check automatically. Other staff need the relevant permission assigned to one of their roles through [Server Permissions](<../Server Dashboard/server-permissions.md>).

| Action | Required Realm Bot permission |
|---|---|
| Activate or end Lockdown | **Manage Lockdown System** |
| Add a watched player | **Watchlist Add** |
| View watched players | **Watchlist List** |
| Remove a watched player | **Watchlist Remove** |

These commands also require the relevant account connection and Premium access. Permission to manage Lockdown does not itself exempt a staff member's Minecraft account from enforcement.

---

## Best Practices

- Prepare staff exemptions before activating Lockdown.
- Select a Realm explicitly when running access-changing commands.
- Use a staff channel for Watchlist alerts and verify that the selected role can receive mentions.
- Keep a record of when Lockdown was activated and confirm `/realm unlock` has succeeded when restrictions are no longer needed.
- Treat Watchlist alerts as context for staff review; the feature does not take a moderation action by itself.

---

## Troubleshooting

### Lockdown is configured, but players are not removed

- Activate it with `/realm lockdown`; enabling the dashboard configuration alone does not activate it.
- Confirm the correct Realm is selected and the Relay Account is connected in-game.
- Check Premium, account access, and the Relay Account's command privileges.
- Check whether the player is the owner, bot account, explicitly exempt, or an allowed operator.

### Lockdown is active, but some players remain online

- Review the command result for failures to check or remove players.
- Restore the bot's connection, then run lockdown again for the selected Realm.
- If exemptions or operator access changed, run lockdown again to check players already online.

### Restrictions return after re-enabling the configuration

Disabling the dashboard configuration preserves the active-lockdown state. Run `/realm unlock realm:<selected Realm>` to end that state, rather than relying on the configuration switch alone.

### Watchlist alerts do not appear

- Confirm Watchlist is enabled, the destination is selected, and the settings saved successfully.
- Check that the watched entry matches the player's Xbox account and the correct Realm.
- Confirm the Relay Account was connected when the player joined.
- Verify Premium and the destination channel permissions.
- If the player was added through a command, confirm notification settings were also configured in the dashboard.

### The alert appears, but the role is not notified

- Confirm the correct **Ping Role** is selected.
- Check that Discord permits Realm Bot to mention that role.

---
