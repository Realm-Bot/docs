---
label: Realm Console
description: Execute Minecraft commands directly from a secured Discord channel, using your in-game Relay Account as the command runner.
order: 80
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

### What is the Realm Console?

The Realm Console is a dedicated Discord channel that allows authorised users to execute **Minecraft Bedrock commands** directly into a connected Realm. Messages sent in the configured console channel are interpreted as commands and executed in-game through the **Chat Relay Account**.

This module is designed for operational administration, rapid moderation actions, and streamlined management - without requiring staff to be actively in-game on a client.

### How it Works

The Realm Console functions by using your Relay Account as the in-game command runner:

- A user sends a message in the designated **Realm Console** Discord channel.
- Realm Bot forwards the message to the Realm via the **Chat Relay Account**.
- The Relay Account executes the message as a command in Realm chat.

Because the command is executed by the Relay Account, all command behaviour (permissions, targets, and side effects) follow the same rules as if the Relay Account typed the command manually in-game.

![Realm Console](/images/realm-console.png)

### Command Example

If a user types the following into the Realm Console channel:

`gamemode c @a`

The Realm will attempt to run:

- `gamemode c @a`  
  (Set all players to Creative Mode)

### Relay Account Behaviour and Targeting

Commands are executed **as the Relay Account**. This is important when using selectors or player-specific commands.

For example:
- If the Relay Account is Realm Bot and a command is run that targets the executor (such as a command that implicitly affects the sender), the Relay Account may be affected.

This is most relevant when:
- Using `@s`
- Running commands that assume the executor is a player
- Running commands without explicit targets

> **Important:** When running player-specific commands, always specify explicit targets (for example `@a`, `@p`, a username, or a tagged group) to avoid unintended effects on the Relay Account.

### Requirements

To use the Realm Console, you must have:

- A configured and functioning **Chat Relay Account** connected to the Realm.
- The Relay Account actively present in the Realm (in-game).
- A designated Discord channel selected as the Realm Console.

If the Relay Account is not in-game, commands cannot be executed.

### Access Control and Security

The Realm Console is highly privileged by design. Any user who can send messages in the console channel can attempt to run commands in the Realm.

For this reason, you should:

- Restrict the channel so only **trusted in-game Administrators** can access it.
- Prevent general members from viewing or posting in the console channel.
- Treat console output as operational infrastructure, not community chat.

Failure to secure this channel may result in:
- Abuse of commands
- Griefing actions
- Unauthorised administrative changes
- Accidental disruption through misuse

### Syntax Errors and Safe Usage

If a message is not a valid command, or contains incorrect syntax, Minecraft will return a **syntax error**.

This is expected behaviour.

To avoid unnecessary disruption:
- Ensure your command is correct before sending it.
- Avoid conversational messages in the console channel.
- Use a strict format and consider pinning usage guidance at the top of the channel.

### Recommended Operational Practices

To keep the Realm Console reliable and safe:

- Use a dedicated channel such as `#realm-console` or `#console`.
- Limit access to a small set of trusted staff.
- Encourage staff to test complex commands in a controlled environment before running them in production.
- Prefer targeted commands (`@a`, tags, usernames) over ambiguous or executor-dependent commands.

If you require assistance configuring the Realm Console for your Realm, open a support ticket and include:
- The Realm name
- The console channel name
- Confirmation that the Relay Account is in-game
- A sample command that is failing and the resulting error output (if any)
