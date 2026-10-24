# Leveling System

The Leveling System records persistent player progression for a Realm. Eligible in-game chat activity and time spent online can award XP, which contributes to levels, rankings, and the Realm leaderboard.

## How XP Is Awarded

When the module is enabled and the Relay Account connection is operational:

- **Chat activity:** an eligible in-game message awards a random **15-25 XP**, at most once per player per minute.
- **Online activity:** online players receive a random **15-25 XP** during a progression check approximately every **5 minutes**.
- **Relay Account:** messages and activity from the Realm Bot Relay Account do not receive XP.

These awards recognise normal participation. Repeated messages are not a reliable progression method, and Chat Relay Anti-Spam controls and Realm moderation rules still apply.

## Levels, Ranks, and Leaderboards

Each level requires more XP than the previous level. XP and levels are stored for the Realm and used by:

- Player rank displays
- The Leveling leaderboard
- Level-up announcements

Players with a higher level are ranked first; XP determines ordering between players at the same level.

## Level-Up Announcements

When a player levels up, Realm Bot can optionally announce this:

- **In-game** through Minecraft chat
- **In Discord** through a selected announcement channel

Both destinations are configurable.

## Custom Level-Up Message

The level-up message supports these placeholders:

- `{user}` - the player's current username
- `{level}` - the player's new level
- `{rank}` - the player's ranking relative to others

Example:

`Congratulations {user} for reaching level {level}! You are now ranked #{rank}.`

> **Note:** Use placeholders exactly as shown. Incorrect formatting may prevent a value from being replaced.

## Requirements

To use the Leveling System:

- An active Realm Bot Premium subscription is required.
- The module must be enabled for the correct Realm.
- The Relay Account must be connected and receiving live Realm events.
- Players must be online for online-activity awards or send an eligible in-game message for chat awards.

The GameTest Pack is not required for Leveling progression.

## How to Set Up

1. Open the **Leveling System** module inside the Realm Bot Dashboard.
   ![Leveling System Configuration](/images/leveling-system.png)
2. Enable the **Leveling System** toggle.
3. Optionally select a **Discord Destination** for level-up announcements.
4. Choose whether to **Send In-Game Messages** for level-ups.
5. Customise the message using `{user}`, `{level}`, and `{rank}` where appropriate.

## Recommended Configuration

- Use a dedicated Discord channel such as `#level-ups` if announcements would clutter general chat.
- Keep the level-up message concise during busy periods.
- Apply normal moderation rules to chat; XP should reward participation rather than message volume.

## Data Actions and Safety

The dashboard provides an action to **reset all user levels** for the selected Realm.

> **Warning:** Resetting levels is irreversible. Confirm the selected Realm and communicate the change before proceeding.

## Troubleshooting

### XP is not updating

- Confirm Leveling is enabled for the correct Realm.
- Confirm the Relay Account is online and the Realm connection is healthy.
- For chat XP, wait at least one minute between eligible awards.
- For online XP, allow at least five minutes for the next progression check.
- Confirm the player is not the Relay Account.

### Announcements do not appear

- Confirm a Discord destination is selected for Discord announcements.
- Verify Realm Bot can **View Channel**, **Send Messages**, and **Embed Links**.
- Confirm **Send In-Game Messages** is enabled if an in-game announcement is expected.
