# Scoreboard Leaderboards

Scoreboard Leaderboards allow you to display a live leaderboard for an in-game **Minecraft scoreboard objective** directly inside a Discord channel. This enables communities to track progress, promote competition, and keep key statistics visible without requiring players to join the Realm to view rankings.

Leaderboards are rendered as Discord embeds and can be configured per scoreboard, per channel.

### How it Works

Scoreboard Leaderboards operate by reading a selected scoreboard objective from your Realm and publishing the results to Discord.

In practice:
- You select a **Discord channel** where the leaderboard will be posted.
- You choose the **Minecraft scoreboard** (objective) you want to display.
- Realm Bot retrieves scoreboard values approximately **once per minute** and updates the embed.
- You can configure up to **10 leaderboards**, each showing up to **10 entries**.
- Realm Bot edits the existing Discord message where possible and recreates it if that message is no longer available.

> **Important:** This feature is dependent on the Realm runtime environment. If the required in-game components are not active, leaderboards cannot update.

### Requirements

Scoreboard Leaderboards require:

- The **Relay Account** to be actively **in-game**.
- The **Realm Bot GameTest Pack** installed and current.
- **Beta APIs** enabled for the Realm.
- An active Realm Bot Premium subscription.
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

Realm Bot requires **View Channel**, **Send Messages**, **Embed Links**, and **Read Message History** in each destination channel.

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
- Verify the Realm Bot GameTest Pack is installed and current.
- Confirm Beta APIs are enabled.

**The leaderboard is not posting to Discord**
- Confirm the bot has permission to **View Channel**, **Send Messages**, **Embed Links**, and **Read Message History** in the selected channel.
- Verify the correct channel was selected during setup.

**The scoreboard name is not appearing in the dropdown**
- The scoreboard objective may not be created in-game yet, or the environment may not be detectable if the required pack/account is offline.
- Create or validate the scoreboard in-game, then refresh the dashboard and try again.
- Confirm the Relay Account joined after the GameTest Pack and Beta APIs were enabled.

### Best Practices

- Treat leaderboard channels as read-only where possible to keep output clean.
- Standardise scoreboard objective naming in-game to reduce confusion in the dashboard.
- If you are using leaderboards competitively, ensure your scoreboard values cannot be trivially manipulated by players.
