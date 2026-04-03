---
label: Live Playerlist
description: Publish an automatically updating list of online Realm players to a Discord channel, with optional playtime and device identification.
order: 10
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Live Playerlist

Live Playerlist publishes a near-real-time view of who is currently online in your Realm to a selected Discord channel. It is designed for staff awareness and community visibility, providing a consistent "who's online" reference without requiring players to be in-game to check.

This feature is located under **Realm Modules** and can be enabled per Realm.

---

## What Live Playerlist Does

When enabled, Realm Bot will:

- Post a live list of players currently online in the Realm
- Update the output automatically every **5 minutes**
- Maintain a single message that refreshes over time (where supported by your configuration), keeping the channel clean

This makes it suitable for:
- moderation coverage (knowing when activity is high)
- event coordination (confirming attendance)
- community engagement (players can see who is active)

---

## Example Output

![Live Playerlist Example](/images/live-playerlist-example.png)

Depending on your configuration, the player list can include:
- the player name (gamertag)
- optional device/platform indicators (e.g., Android, Windows)
- optional current session playtime

---

## Configuration

![Live Playerlist Configuration](/images/live-playerlist.png)

### Enable Live Playerlist

Use the primary toggle at the top of the module to enable or disable Live Playerlist for the selected Realm.

### Discord Destination

Select the Discord channel where the live playerlist will be posted and updated.

Recommended channel choices:
- `#players-online`
- `#realm-status`
- `#realm-activity`

Ensure the bot has:
- **View Channel**
- **Send Messages**
- **Embed Links** (recommended for clean formatting)

### Display Settings

You can control which information appears alongside each player entry:

#### Display Playtime

When enabled, the playerlist includes a playtime indicator showing how long the player has been active (as supported by your deployment).

Use this if you want:
- clearer staff context during incidents
- session visibility for activity monitoring

#### Device Identification

When enabled, the playerlist displays each player's device/platform indicator (where detectable), such as:
- Android
- Windows
- Console platforms (where supported)

Use this if you want:
- platform visibility for staff (especially when running device-restricted communities)
- quick indicators when investigating suspicious join patterns

---

## Update Interval

Live Playerlist updates every **5 minutes**. This interval is designed to balance:
- reasonably current visibility
- minimal spam and operational overhead
- predictable refresh timing for staff

> **Note:** The playerlist is "live" in the operational sense (regular refresh), not second-by-second.

---

## Best Practices

- Use a dedicated channel and keep it low-noise.
- Restrict who can post in the destination channel (optional) so the output remains easy to read.
- Enable **Device Identification** if you enforce platform-specific rules or run competitive modes where device context matters.
- Enable **Display Playtime** if your staff workflow benefits from session context.

---

## Troubleshooting

### The playerlist does not appear

- Confirm Live Playerlist is enabled in the module.
- Confirm a Discord Destination channel is selected.
- Verify permissions: View Channel, Send Messages (and Embed Links if required).
- Confirm the Realm is connected and functioning.

### The playerlist is not updating

- Updates occur every 5 minutes; wait for the next cycle.
- Confirm the bot remains online and has access to the destination channel.

### Device/playtime fields are missing

- Ensure the corresponding Display Settings toggles are enabled.
- Some fields may depend on what information is available from the Realm at the time of update.

---
