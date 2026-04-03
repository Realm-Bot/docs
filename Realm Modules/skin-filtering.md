---
label: Skin Filtering
description: Automatically detect and remove players using irregular skins (small, invisible/transparent, or 4D/Horion-style skins) to improve fairness and reduce exploit abuse.
order: 30
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Skin Filtering

Skin Filtering is a moderation feature that helps Realm Owners discourage exploit-oriented cosmetics by detecting and acting on **irregular player skins**. This includes patterns commonly associated with unfair visibility, deceptive hitboxes, or client exploit behaviour.

Skin Filtering is currently a **Beta** feature. Some false positives may occur depending on the skin type and platform behaviour.

![Skin Filtering Configuration](/images/skin-filtering.png)

---

## What Skin Filtering Does

When enabled, Skin Filtering monitors joining players (and/or active players, depending on your deployment) and identifies skins that match one of the configured "irregular" categories. If a skin violates your selected rules, the player can be removed from the Realm based on the system's enforcement behaviour.

This is intended to:
- improve fairness in PvP and competitive gameplay
- reduce visibility abuse and deception tactics
- standardise cosmetic rules for your community

---

## Requirements

Skin Filtering requires:

- The Realm Bot **Relay Account** to be **in-game**
- Skin Filtering enabled within the Realm's modules section

If the Relay Account is not in-game, the system cannot reliably enforce filtering actions.

---

## Filter Settings

You can enable filtering per category. These categories are designed to target common exploit-oriented skin patterns.

### Small Skins

Filters smaller or "half-sized" skin presentations that can be used to reduce visual profile or misrepresent player appearance.

Recommended for:
- PvP Realms
- competitive minigames
- servers with strict cosmetic standards

### Invisible Skins

Filters skins that use invisible or transparent textures to reduce visibility or create unfair advantages.

Recommended for:
- any Realm where PvP, stealth, or competitive advantage matters
- public Realms where exploit cosmetics are common

### Horion Skins (4D Skins)

Filters "4D" or Horion-style skins commonly associated with exploit clients and cosmetic manipulation.

Recommended for:
- Realms that have experienced Horion-related abuse
- public-code Realms
- competitive environments

> **Note:** These labels reflect common community terminology. The filter is designed around observed irregular skin behaviour patterns.

---

## What Enforcement Looks Like

When a player is detected using a disallowed skin type, Realm Bot can take an automated action and record the outcome. In Discord, this typically appears as an automated moderation entry showing the player connection context and the reason for removal.

![Skin Filtering Example (Discord Output)](/images/skin-filtering-example.png)

This provides staff with:
- a clear indication of which user was affected
- the reason category (e.g., **Unfair Skin**)
- basic context for review if a player appeals

---

## Example Context: Small Skin in Use

Small skins reduce the player's apparent size and visibility, which can create an advantage in PvP or during fast movement. The example below demonstrates what a small skin can look like in-game.

![Small Skin Example (In-Game Context)](/images/skin-filtering-example-context.png)

---

## When to Enable Skin Filtering

Skin Filtering is most useful in:

- public invite / high-traffic Realms
- PvP Realms where visibility and fairness are critical
- Realms frequently targeted by exploit users
- communities with established cosmetic rules

For private invite-only Realms, Skin Filtering may be unnecessary unless you regularly encounter exploit cosmetics.

---

## Best Practices

- Start with the most clear-cut filters first (typically **Invisible Skins** and **Horion/4D Skins**).
- Monitor for false positives during the first few days of use.
- Publish a short rule statement to players (e.g., "Invisible/4D skins are not allowed.").
- Maintain a staff process for appeals if a legitimate player is incorrectly removed.

---

## Beta Notes and False Positives

Because Skin Filtering is in Beta:
- some legitimate skins may be flagged incorrectly in edge cases
- platform differences and skin format quirks can cause inconsistent detection

If you observe false positives:
- disable the category most likely to be causing false positives first
- enable one filter at a time to isolate the cause
- log affected gamertags and timestamps for support review

---

## Troubleshooting

### Filtering is enabled, but nothing happens

- Confirm the Relay Account is **in-game**
- Confirm Skin Filtering is enabled for the correct Realm
- Ensure at least one filter category is toggled on

### Legitimate players are being removed

- Disable the most aggressive category first (commonly 4D/Horion)
- Re-test with a smaller scope (enable one filter at a time)
- Treat early Beta enforcement as reviewable until detection stabilises

---
