---
label: Getting Started
description: Connect your Minecraft Bedrock Realm to Discord in three steps. Link your Microsoft account, run the connect command, then configure modules and settings.
icon: rocket
order: 101
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Getting Started

This guide walks you through the official setup flow to connect your Minecraft Bedrock Realm to Discord using Realm Bot. The onboarding process is designed to be completed in a few minutes and is separated into three stages:

1. **Link Microsoft Account**
2. **Run Discord Command**
3. **Configure Settings**

![Setup Flow Overview](/images/getting-started-step-1.png)

---

## Before You Begin

### 1) Invite Realm Bot to Your Discord Server
Realm Bot must be present in your Discord server before you can run the connection command.

- Use the `/invite` command **or** invite via: https://realmbot.dev/invite
- Grant the required permissions. **Administrator** is recommended for full functionality.

> **Important:** If Realm Bot cannot post messages or cannot read channels where you plan to use features (logs, chat relay, leaderboards), setup may succeed but modules will not operate correctly.

### 2) Ensure You Have the Correct Access
You should be:
- The Realm Owner, or a trusted administrator with access to manage the Realm
- A Discord administrator (or equivalent) in the server you are connecting

---

## Step 1 - Link Your Microsoft Account

Realms are owned and managed through a Microsoft/Xbox account. Realm Bot requires you to link a Microsoft account so it can detect and manage your available Realms.

1. Go to the dashboard: https://dashboard.realmbot.dev
2. Sign in with Discord.
3. Select **Connect Microsoft Account** to link your Microsoft/Xbox account.

![Connect Microsoft Account](/images/getting-started-step-1.png)

> **Security Note:** Only link an account you trust to administrate the Realm. Treat account linking as privileged access.

---

## Step 2 - Run the Discord Connection Command

After your Microsoft account is linked, the next step is to connect that account to the correct Discord server.

1. Open the Discord server you want to connect.
2. Run the following command in any channel where Realm Bot can respond:

`/connect`

![Run Discord Command](/images/getting-started-step-2.png)

### What `/connect` Does
- Verifies your linked Microsoft account
- Associates the current Discord server with your Realm management context
- Enables the dashboard to load and configure Realm-specific settings and modules

> **Tip:** If you manage multiple servers, ensure you run `/connect` in the correct server first. You can repeat the process per server if needed.

---

## Step 3 - Configure Your Realm Settings

Once your connection is established, you can configure your Realm using the dashboard and the relevant module pages.

Recommended configuration sequence:

1. **Choose your Realm** (if prompted)
2. Review **Bot Join Settings** (how the relay/bot connects)
3. Configure **Gametest Pack Management** (only if required by your modules)
4. Enable and configure any **Realm Modules** you plan to use:
   - Chat Relay
   - Realm Console
   - Bot Detection
   - Member Gate
   - Leveling
   - Scoreboard Leaderboards
   - (Optional) Tebex Integration

You can also view command help in Discord at any time:
- `/help`

---

## Common Issues

### “I can’t see my Realms in the dashboard.”
- Confirm you linked the correct Microsoft/Xbox account.
- Ensure the account actually owns (or has access to) the Realms you expect.
- Re-open the dashboard and refresh after linking.

### `/connect` does nothing or fails.
Check the following:
- Realm Bot is invited to the server and is online.
- You are running `/connect` in a server channel where the bot has permission to respond.
- Your role has sufficient permissions to run management commands (server admin recommended).

### Xbox/Microsoft privacy blocks linking or access.
If linking or Realm access fails, review your Xbox privacy settings to ensure external services can function correctly.

> **Important:** Privacy settings can prevent applications from accessing required profile/realm data. If issues persist, adjust the relevant Xbox privacy options and retry linking.

---

## Next Steps

Once setup is complete, proceed to the **Overview** page to learn
