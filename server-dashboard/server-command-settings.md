# Command Settings

The **Command Settings** page controls how information is displayed in selected Realm Bot commands. This is primarily used to adjust the level of detail shown when viewing player information in Discord.

![Command Settings](/images/server-command-settings.png)

---

## Player Information Display

This setting changes the output format used in commands such as:

- `/realm players`

You can choose between two display modes depending on how your staff team moderates and how much information you want exposed in-command.

### Compact Display
A minimal output designed for quick checks.

Typically includes:
- Player username
- Device type

**Recommended for:** fast moderation workflows, smaller servers, or servers where you want to minimise visible player metadata.

### Detailed Display
A richer output designed for investigation and verification.

Typically includes:
- Player username
- Device type
- Gamerscore
- Xbox Live status

**Recommended for:** larger teams, higher-risk public servers, or environments where staff routinely verify player legitimacy and activity patterns.

---

## Recommended Configuration

- Use **Compact Display** for day-to-day staff work where speed and readability matter most.
- Switch to **Detailed Display** if your moderation depends on additional identity/context signals (for example, platform patterns or account indicators).

> **Note:** This setting changes how information is presented in Discord outputs; it does not change what actions the bot can perform.

---
