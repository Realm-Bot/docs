---
label: Bot Detection
description: Detect and remove suspected automated accounts from connected public Realms, with optional experimental checks and automatic bans.
order: 70
image: /images/custom/botdetection.png
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Bot Detection

Bot Detection is a **Beta** moderation module for Realms affected by automated joins or disruptive bot activity. It evaluates live connection activity and may remove an account when its behaviour is consistent with automation.

> **Important:** Automated detection reduces common disruption but cannot guarantee complete prevention. False positives remain possible, particularly when experimental checks are enabled.

## Current Behaviour

- Suspected bot accounts are removed from the Realm with a kick by default.
- **Auto Ban** can additionally ban accounts identified by the detector.
- **Experimental Detection** adds more aggressive checks and may increase false positives.
- Users on the Realm Bot allowlist are exempt.
- Enforcement events are recorded in the configured Automod logging channel.

The dashboard's master enable control is currently limited. Treat the available detection settings and connected Relay Account state as the practical controls, and contact support before relying on a master switch to suspend all detection.

## Requirements

Bot Detection requires:

- An active Realm Bot Premium subscription
- A Relay Account connected to and present in the correct Realm
- A healthy Realm event connection
- A configured Automod logging channel for staff visibility

The GameTest Pack is not required for Bot Detection.

## Configuration

![Bot Detection Configuration](/images/bot-detection.png)

### Experimental Detection

Enable this only when standard detection is not sufficient and staff can review appeals. It broadens the checks used against suspected automation but carries a higher false-positive risk.

### Auto Ban

When enabled, detected accounts may be banned in addition to being removed. Begin with kick-only enforcement while evaluating behaviour in your community.

## Recommended Use

- Use Bot Detection primarily for public or widely advertised Realms.
- Keep the Relay Account online during high-risk periods.
- Maintain a clear appeal process and record the player's gamertag and join time.
- Use controlled Invite Links and other access measures alongside detection.

## Troubleshooting

### Suspected bots are not removed

- Confirm the Relay Account is online in the selected Realm.
- Confirm the Realm connection is receiving live events.
- Check the configured Automod log channel for errors or enforcement records.
- Reconnect the Microsoft/Xbox account if authentication has expired.

### A legitimate player is removed

- Disable **Experimental Detection** first.
- Disable **Auto Ban** while reviewing false positives.
- Add a confirmed trusted player to the allowlist where appropriate.
- Provide support with the gamertag and approximate join time.
