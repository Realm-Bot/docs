---
label: Member Gate
description: Automatically kick or ban joining players based on Xbox profile signals - such as device platform, gamerscore, and social metrics - to enforce strict entry standards.
order: 3
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

### What is Member Gate?

Member Gate is an **automated entry moderation system** that evaluates players as they join your Realm and applies an action -typically **Kick** or **Ban** - based on rules you define. It is designed for Realm Owners who need stricter access control than invite codes alone can provide, especially for public or semi-public Realms.

Member Gate is particularly effective for Realms that want to restrict gameplay to specific player types (for example, a **Console-Only PvP Realm**), or for communities that need basic automated filtering for suspicious join patterns.

### How Member Gate Works

Member Gate operates using rule-based logic:

- You create one or more **Moderation Rules** in the dashboard.
- Each rule contains:
  - A **Moderation Action** (Kick or Ban)
  - One or more **Conditions**
- When a player joins, Member Gate checks each rule.
- If a player matches the rule’s conditions, the configured action is executed.

> **Important:** Member Gate requires the **Relay Account** to be **in-game** to execute kicks/bans. If the Relay Account is not online in the Realm, Member Gate cannot enforce rules.

### Conditions You Can Use

Member Gate supports multiple condition types, allowing flexible rule construction. Rules may include **any combination** of supported conditions, and are intended to be configured based on your Realm’s requirements.

Common condition categories include:

- **Device Platform**
  - Device includes
  - Device excludes

- **Gamerscore Thresholds**
  - Gamerscore greater than
  - Gamerscore less than

- **Social Metrics**
  - Followers greater than / less than
  - Following greater than / less than

> **Rule Logic:** Within a single rule, **all conditions must be met** for the action to be executed. If any condition is not met, the rule will not trigger.

### Supported Device Platforms

Device-based rules can be used to enforce platform-specific Realms. Supported platforms include:

- Android
- iOS
- Windows
- Xbox
- PlayStation
- Nintendo

This makes Member Gate suitable for use-cases such as:
- Console-only PvP
- Mobile-only casual Realms
- Restricting Windows joins during targeted abuse periods

### Requirements

To use Member Gate effectively, ensure the following are in place:

- The Realm is connected to Realm Bot via the authorised linking flow
- The **Relay Account is actively in-game**
- A Discord channel is selected to receive enforcement logs (recommended)

### How to Set Up

1.  Open the **Member Gate** module inside the Realm Bot Dashboard.<br/>
    ![Member Gate Configuration](/images/member-gate.png)
2.  Enable **Member Gate** using the main toggle.
3.  Set the **Discord Destination** channel.
    - Kick and ban actions will be logged to this channel for auditing and troubleshooting.
4.  Under **Moderation Rules**, create a rule:
    - Provide a short, clear rule name (for example: `Console Only` or `Block Low Gamerscore`).
    - Select the **Moderation Action**: **Kick** or **Ban**.
    - Add one or more **Conditions** and configure their values.
5.  Confirm your Relay Account is **online in the Realm**, then test by joining with a permitted account and (if possible) a non-permitted account.

### Recommended Configuration Approach

To reduce disruption and avoid accidental over-enforcement:

- Start with **Kick** rather than Ban while tuning conditions.
- Add rules gradually and monitor results through your Discord Destination logs.
- Prefer device rules for “hard” restrictions (e.g., console-only), and threshold rules for “soft” filtering (e.g., suspicious profiles).

### Example Rule Patterns

**Console-only Realm**
- Action: **Kick**
- Conditions:
  - Device excludes: Android, iOS, Windows

**Filter low-signal accounts**
- Action: **Kick**
- Conditions:
  - Gamerscore less than: *your chosen threshold*
  - Followers less than: *your chosen threshold*

**High-trust access**
- Action: **Kick** or **Ban** (use caution)
- Conditions:
  - Gamerscore greater than: *threshold*
  - Followers greater than: *threshold*

> **Note:** Social and gamerscore thresholds can produce false positives depending on your community demographics (new players, alt accounts, privacy settings, etc.). Use conservative thresholds and iterate.

### Best Practices

- Restrict who can modify Member Gate settings in your staff structure.
- Use a dedicated Discord log channel such as `#automod-logs`.
- Publish clear entry expectations to players if you enforce strict platform or profile requirements.
- Maintain a simple appeal path if a legitimate player is removed by automation.

### Common Issues

**Member Gate is enabled, but no actions occur**
- Confirm the **Relay Account is in-game**.
- Verify the correct Realm is selected in the dashboard.
- Ensure rules are created and saved (and not empty).
- Check the Discord Destination channel for enforcement messages.

**Legitimate players are being removed**
- Lower the strictness of gamerscore/follower thresholds.
- Switch from **Ban** to **Kick** while tuning.
- Prefer device-only restrictions if your goal is platform separation rather than profile filtering.
