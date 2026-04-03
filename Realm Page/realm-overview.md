---
label: Realm Overview
description: View essential Realm status, slots, settings, and recent activity from a single dashboard page, with quick access to official Realm management.
order: 100
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Realm Overview

The **Realm Overview** page provides a consolidated summary of your selected Minecraft Bedrock Realm. It is designed to give Realm Owners and staff a fast, reliable view of:

- Current Realm status and membership
- World slot availability and the active world
- Core world and server settings (where available)
- Recent activity indicators for operational awareness
- A direct link to manage the Realm through the official Minecraft services

![Realm Overview Page](/images/realm-overview.png)

---

## What This Page Is For

Use this page to quickly confirm that:

- You are managing the **correct Realm**
- The Realm is currently **open/online** (status shown in the summary)
- Your **member count**, **world slots**, and **active slot** look as expected
- Key settings such as **game mode**, **difficulty**, and **PvP** align with your intended configuration

This page is intended as an **at-a-glance operational panel**, not a replacement for deeper module configuration.

---

## Realm Summary Card

At the top of the page, the Realm summary card shows high-level identifiers and metadata, typically including:

- **Realm Name** (and internal identifier, where applicable)
- **Realm description** (if set)
- **Member count** (total members associated with the Realm)
- **Time remaining** on the subscription period (if available)
- **Creation date** (Realm creation timestamp)

### Manage on Minecraft
The **Manage on Minecraft.Net** button redirects you to the official Realm management portal. This is useful for changes that must be performed through the official interface (for example, subscription or platform-side management tasks).

> **Note:** Some Realm settings are only editable through official Minecraft management tools. Realm Bot surfaces information, but not all changes can be applied through the dashboard.

---

## Quick Status Cards

Directly beneath the summary card, you will see quick status tiles. These are designed for rapid verification during operations:

- **Realm Status**  
  Indicates whether the Realm is currently open/available.

- **Total Members**  
  Displays the current number of members associated with the Realm.

- **World Slots**  
  Shows how many world slots are available for the Realm (Realms commonly support multiple slots).

- **Active Slot**  
  Identifies which world slot is currently active (the world presently being used by the Realm).

---

## Active World Information

The **Active World Information** section provides a structured readout of settings for the currently active world. Typical fields include:

### World Settings
- **World Name**
- **Game Mode** (for example, Survival or Creative)
- **Difficulty** (for example, Easy / Normal / Hard)
- **PvP** status (Enabled/Disabled)

### Server Settings
- **Cheats** status (Allowed/Disallowed)
- **Texture pack required** (Forced/Not forced), if configured

> **Important:** Values shown here reflect the **active slot only**. If you switch the active world slot, the displayed values may change accordingly.

---

## Recent Activity

The **Recent Activity** panel highlights recent participation signals to help staff quickly assess whether the Realm has been active. This can include:

- Account name (for example, a relay or service account)
- Time played or session duration (where available)
- Recency indicator (e.g., “2h ago”)

This is primarily intended for operational context—especially when coordinating staff coverage, investigating incidents, or confirming that your relay account has been online recently.

---

## Troubleshooting and Notes

### The page is missing data or looks incomplete
- Confirm the Realm is correctly connected and selected in the dashboard.
- Refresh the page and verify the account linking is still valid.
- Some values are dependent on what the platform exposes at the time of retrieval.

### The Realm status looks wrong
- Realm status can lag slightly behind real-time changes.
- Verify status using official tools if you are troubleshooting an active outage.

### Values do not match what is expected in-game
- Ensure you are viewing the **active world slot** you intend to check.
- If you recently changed settings, allow time for changes to propagate and refresh the page.

---

## Related Pages

If you are setting up or extending your Realm configuration, the following pages are typically the next steps:

- **Getting Started** (initial account linking and connection)
- **Bot Join Settings** (how the Relay Account joins)
- **Gametest Pack Management** (required for certain advanced features)
- **Realm Modules** (Chat Relay, Realm Console, Bot Detection, Member Gate, Skin Filtering, Leveling, Scoreboards, Live Playerlist, Vanity URL)
