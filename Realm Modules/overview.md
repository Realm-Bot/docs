---
label: Overview
description: A central hub for managing your Realm connection, bot join behaviour, Gametest pack dependencies, and all available Realm Modules.
order: 100
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Overview

This page serves as the central management hub for your connected Realm. From here, you can access your Realm’s core configuration, control how Realm Bot joins your world, manage Gametest pack dependencies (where required), and configure any Premium modules you have enabled.

---

## Manage Your Realm

At the top of the page you will see your selected Realm card. This is the primary entry point for managing Realm-specific configuration and quickly confirming you are working on the correct Realm.

![Realm Card (Manage Realm)](/images/overview-realm.png)

Use the **Manage** button to open the Realm’s management view and access the settings shown below.

---

## Bot Join Settings

Bot Join Settings determine how Realm Bot connects to your Realm. These options are operational controls and should be configured with reliability and safety in mind.

![Bot Join Settings](/images/overview-bot.png)

Key options include:

- **Enable Bot to Join Game**  
  Allows Realm Bot (via the Relay Account) to join your Realm when required by features that depend on an in-game executor.

- **Use Beta Joining**  
  Uses an experimental joining method (disables the standard joining method). This should only be enabled if instructed or if standard joining is not functioning reliably in your environment.

- **Enable Bot to Join as Alt Account**  
  Allows Realm Bot to join using an alternative account. This is commonly used when your primary Relay Account must remain reserved for specific workflows or when redundancy is required.

> **Important:** Many modules (for example, Chat Relay, Realm Console, Bot Detection, Member Gate, and Skin Filtering) require an in-game Relay Account to perform actions. If the bot is not in-game, these modules may not function.

An active Realm Bot Premium subscription is required for the connected Relay Account workflow. Connection-dependent features may pause during Realm disconnections or Microsoft/Xbox authentication failures.

---

## GameTest Pack Management

Gametest Pack Management controls the dependency pack used for advanced Realm features that require in-game scripting capabilities. Where a module relies on the Gametest pack, it must be installed and active.

![Gametest Pack Management](/images/overview-gametest.png)

This section includes:

- **Beta API Requirement**  
  Some Gametest functionality requires **Beta APIs** to be enabled in your Realm settings. If prompted, enable **Use Beta APIs** under your Realm’s experimental features.

- **Auto Update GameTest Pack**
  Installs an available update when Realm Bot next joins the Realm. This is not a continuous background update.

- **Pack Actions**
  - **Install Pack** - installs the dependency pack into the Realm
  - **Update Pack** - installs the latest available version
  - **Remove Pack** - removes the managed pack
  - **Manual Download** - provides a download option for manual deployment workflows
  - **Check For Updates** - checks whether a newer pack version is available

> **Note:** If a module is not behaving as expected and it depends on Gametest, first confirm the pack is installed, enabled, and current.

See [Relay Account and GameTest Dependencies](relay-account-and-gametest.md) for installation requirements and the feature dependency matrix.

---

## Realm Modules

The Realm Modules section contains all configurable feature modules available for your Realm. Premium modules are clearly marked and can be opened directly via **Configure**.

![Realm Modules](/images/overview-realm-modules.png)

From here you can configure all Realm Modules currently available for your Realm:

- **Bot Detection** - mitigation for malicious bot accounts, including an Experimental mode for stricter detection
- **Chat Relay** - a two-way chat bridge with category-specific channels, custom messages, Fun Mode, and Anti-Spam
- **Leveling System** - chat and online-activity XP with persistent rankings and configurable announcements
- **Live Playerlist** - automatically publish and refresh a Discord view of which players are online
- **Member Gate** - rule-based entry moderation using device, gamerscore, social metrics, and private-title-history checks
- **Realm Console** - run Minecraft commands through a secured Discord console channel
- **Scoreboard Leaderboards** - publish in-game scoreboard rankings to Discord
- **Skin Filtering** - detect and remove players using irregular or exploit-oriented skins
- **Vanity URL** - create a branded, stable invite entry point for your Realm

Also see:

- [Relay Account and GameTest Dependencies](relay-account-and-gametest.md) for shared operational requirements
- [Tebex](../Integrations/tebex.md) for store fulfilment
- [Embed Panel](../Tools/embed-panel.md) for persistent Discord panels with link or Realm-action buttons

> **Operational Guidance:** Restrict access to high-impact modules (such as Realm Console, Member Gate, and Skin Filtering) to trusted administrators. These features can directly affect gameplay, player access, and server stability.

---

## Recommended Setup Order

For best results, configure your Realm in the following sequence:

1. Confirm you are managing the correct Realm (top card).
2. Configure **Bot Join Settings** to ensure reliable in-game connectivity.
3. If required, install and validate the **Gametest Pack** (and enable Beta APIs where prompted).
4. Enable and configure the modules you intend to use.

This structure ensures that all dependencies are in place before you rely on any module operationally.
