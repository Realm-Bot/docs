---
label: Chat Relay
description: Connect your Realm and Discord with a two-way chat bridge, allowing staff and players to stay aligned in real time across both platforms.
order: 20
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

### What is Chat Relay?

Chat Relay is a **two-way communication bridge** between your **Minecraft Bedrock Realm chat** and a selected **Discord channel**. It is designed to maintain continuity between in-game activity and your community’s primary coordination space, enabling faster responses, better visibility, and more consistent moderation workflow.

### What Chat Relay Relays

Chat Relay can relay multiple categories of activity from Minecraft to Discord, depending on your configuration:

- **Player Chat Messages:** Standard messages sent by players in Realm chat.
- **Tellraw Messages:** Command-generated, formatted outputs (commonly used for announcements, rewards, systems output, and scripted events).
- **Death Messages:** Player death notifications for visibility during gameplay and moderation review.

> **Note:** Chat Relay is a communications utility. It does not independently “secure” or “protect” a Realm. All messages are still governed by your Realm rules and Discord policies.

### Requirements

To use Chat Relay as intended, ensure the following are in place:

- An **active Premium subscription**, where applicable to your deployment.
- A Realm that is successfully connected to Realm Bot via the authorised account-linking flow.
- A Discord channel designated for relay output (strongly recommended).

### How to Set Up

1.  Open the **Chat Relay** module inside the Realm Bot Dashboard.<br/>
    ![Chat Relay Configuration](/images/chat-relay.png)
2.  Enable **Chat Relay** using the **Chat Relay Configuration** toggle.
3.  Set the **Discord Destination** channel (this is where Realm messages will be posted).
4.  Under **Message Types**, enable the categories you want relayed to Discord:
    - **Player Chat Messages**
    - **Tellraw Messages**
    - **Death Messages**

Once enabled, relay output should begin immediately when relevant messages occur in the Realm.

### Recommended Configuration

For a clean, professional relay channel that remains usable during peak activity:

- Use a dedicated channel such as `#realm-chat`, `#chat-relay`, or `#realm-live`.
- Enable only the message types you operationally need:
  - Public communities: **Player Chat** + (optional) **Death Messages**
  - Staff operations: **Player Chat** + **Tellraw** (common for system events)
- Consider Discord **slowmode** if you anticipate spam or high throughput.
- Treat the relay channel as an extension of in-game chat; apply the same behavioural standards.

### Discord Permissions

Realm Bot must be able to operate in the destination channel. Ensure it has:

- **View Channel**
- **Send Messages**
- **Read Message History**

If relay output does not appear, channel permissions should be the first item verified.

### Operational Notes

Chat Relay is most effective when used to support:

- **Live moderation visibility** (staff can follow incidents without joining immediately)
- **Event coordination** (Discord staff can react to in-game developments in real time)
- **Community responsiveness** (players receive timely answers without staff context-switching)

If troubleshooting is required, confirm:
- The correct Realm is selected in the dashboard
- Chat Relay is enabled
- The destination channel is correct
- The Realm connection remains valid
- The required Discord permissions are present
