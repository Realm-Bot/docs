### What is the Leveling System?

The Leveling System is a progression module that awards players **XP over time** based on their **in-game playtime**. As players accumulate XP, they level up through a curve that naturally becomes more demanding at higher levels. This ensures early progression feels rewarding while long-term progression remains meaningful for committed players.

### How XP and Levels Work

XP is awarded progressively as players remain active in-game. The system uses a **progression curve**, meaning:

- Lower levels are reached more quickly to support onboarding and early engagement.
- Higher levels require more XP, preventing rapid endgame progression and keeping long-term progression competitive.

This makes the Leveling System suitable for:
- Long-running survival Realms
- Competitive communities seeking a consistent grind
- Staff-managed events where activity-based rewards matter

### Level-Up Announcements

When a player levels up, Realm Bot can optionally announce this:

- **In-Game** (Minecraft chat)
- **In Discord** (a dedicated announcement channel)

Both announcement destinations are configurable, allowing you to keep level-up messages visible without disrupting gameplay or staff operations.

### Custom Level-Up Message

You may customise the message used for level-up announcements. The message supports variable placeholders that are replaced dynamically at runtime:

- `{user}` - the player’s current username
- `{level}` - the player’s new level
- `{rank}` - the player’s ranking relative to others

Example:

`Congratulations {user} for reaching level {level}! You are now ranked #{rank}.`

> **Note:** Use placeholders exactly as shown. Incorrect formatting may result in variables not being replaced as expected.

### Requirements

To use the Leveling System:
- The module must be enabled in the Realm Bot Dashboard.
- Players must be actively playing in the Realm to accrue playtime-based XP.

### How to Set Up

1.  Open the **Leveling System** module inside the Realm Bot Dashboard.<br/>
    ![Leveling System Configuration](/images/leveling-system.png)
2.  Enable the **Leveling System** toggle.
3.  (Optional) Select a **Discord Destination** channel for level-up announcements.
4.  Under **Announcement Settings**, choose whether to **Send In-Game Messages** for level-ups.
5.  Edit the **Custom Level Up Message** to match your community’s style, using `{user}`, `{level}`, and `{rank}` where appropriate.

### Recommended Configuration

For community Realms:
- Enable **in-game announcements** if level-ups are a core part of the player experience.
- Use a dedicated Discord channel such as `#level-ups` to preserve visibility without cluttering general chat.

For competitive or staff-heavy Realms:
- Consider disabling in-game announcements and using Discord only.
- Keep your message concise and consistent to avoid spam during peak activity.

### Operational Notes

- The Leveling System is designed to reward sustained engagement rather than short bursts of play.
- The progression curve is intended to maintain long-term value; higher levels should remain an achievement.
- If you are migrating from older leveling data, use the dashboard migration option where available, and avoid resetting levels unless you intend to fully restart progression for the Realm.

### Data Actions and Safety

The module may provide administrative actions such as:
- **Migrating data** from a prior leveling system
- **Resetting all user levels** for the Realm

> **Warning:** Reset actions are typically permanent. Use resets only when you have confirmed your intent and communicated the change to your community in advance.
