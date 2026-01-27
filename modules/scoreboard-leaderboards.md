---
label: Scoreboard Leaderboards
description: Publish live in-game scoreboard rankings to Discord, allowing players to track progress and compete through automated leaderboard embeds.
order: 25
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

### What are Scoreboard Leaderboards?

Scoreboard Leaderboards allow you to display a live leaderboard for an in-game **Minecraft scoreboard objective** directly inside a Discord channel. This enables communities to track progress, promote competition, and keep key statistics visible without requiring players to join the Realm to view rankings.

Leaderboards are rendered as Discord embeds and can be configured per scoreboard, per channel.

### How it Works

Scoreboard Leaderboards operate by reading a selected scoreboard objective from your Realm and publishing the results to Discord.

In practice:
- You select a **Discord channel** where the leaderboard will be posted.
- You choose the **Minecraft scoreboard** (objective) you want to display.
- Realm Bot periodically retrieves scoreboard values through the connected Realm environment and updates the embed.

> **Important:** This feature is dependent on the Realm runtime environment. If the required in-game components are not active, leaderboards cannot update.

### Requirements

Scoreboard Leaderboards require:

- The **Relay Account** to be actively **in-game**.
- The **Realm Bot Gametest Pack** installed and enabled in the Realm.
- At least one valid in-game **scoreboard objective** to display.

If any requirement is missing (Relay Account offline, pack disabled, or scoreboard not present), leaderboard updates may fail or show no data.

### How to Set Up

1.  Open the **Scoreboard Leaderboards** module in the Realm Bot Dashboard and enable it.<br/>
    ![Scoreboard Leaderboards Main Page](/images/scoreboard.png)
2.  Select **Create Leaderboard**.
3.  Configure the leaderboard using the creation menu.<br/>
    ![Create Scoreboard Leaderboard Menu](/images/scoreboard-definitions.png)
4.  Set the following:
    - **Select channel** - the Discord channel where the leaderboard should be displayed.
    - **Minecraft Scoreboard** - the scoreboard objective to publish.
5.  (Optional) Customise the embed appearance:
    - **Embed Title** - the label shown at the top of the embed.
    - **Embed Color** - the accent color used for the embed.
6.  Save the leaderboard configuration.

Once created, the leaderboard will begin updating in the selected channel when the Relay Account is online and the Gametest Pack is active.

### Recommended Usage

Scoreboard Leaderboards are ideal for:
- Factions / prisons progression metrics
- Kills, deaths, K/D tracking (where implemented via scoreboards)
- Event wins, captures, or objective scoring
- Currency or point systems tracked via scoreboard objectives

Operational recommendations:
- Use a dedicated channel such as `#leaderboards`, `#stats`, or `#rankings`.
- Keep one leaderboard per channel unless you have a structured layout (multiple leaderboards in one channel can become difficult to read).
- Use clear embed titles aligned with your scoreboard objective name (for example: “Top Kills”, “Top Balance”, “Top Wins”).

### Common Issues

**The leaderboard shows no entries**
- Confirm the selected scoreboard objective exists in-game and contains values.
- Ensure the Relay Account is online in the Realm.
- Verify the Realm Bot Gametest Pack is installed and enabled.

**The leaderboard is not posting to Discord**
- Confirm the bot has permission to **View Channel**, **Send Messages**, and **Embed Links** in the selected channel.
- Verify the correct channel was selected during setup.

**The scoreboard name is not appearing in the dropdown**
- The scoreboard objective may not be created in-game yet, or the environment may not be detectable if the required pack/account is offline.
- Create or validate the scoreboard in-game, then refresh the dashboard and try again.

### Best Practices

- Treat leaderboard channels as read-only where possible to keep output clean.
- Standardise scoreboard objective naming in-game to reduce confusion in the dashboard.
- If you are using leaderboards competitively, ensure your scoreboard values cannot be trivially manipulated by players.

