---
label: Chat Relay
order: 100
---

!!!primary Premium Only
This feature only works with **Realm Bot Premium**
!!!

# Chat Relay

Chat relay is a feature which allows people in Discord to talk with people in your realm and vice versa

Chat relay requires you to be a premium user and needs the bot to be in the Realm.

---

## How it Works

Chat relay is a premium feature which works by relaying your in-game messages to discord in the dedicated channel of your choice. Realm Bot will also work the other way around; relaying your discord messages in the channel of your choice right back into the realm. 
The bot does this by joining the realm on the realm owner's account or its own account _if you have alt account joining enabled_

The bot sends messages from the realm to the discord in two ways. One as a normal message and as an embed (_also called tellraw relay_).

![Example of normal relay message](/images/relay.png)

![Example of tellraw relay](/images/tr_relay.png)

---

## Configuring chat relay

Chat relay can be configured via the [dashboard](https://realmbot.dev/).

For the commands related to chat relay see [Chat Relay](/Commands/world-commands.md).

If you wish to enable chat relay you will need to head go to your [guild dashboard](https://realmbot.dev/guilds) and locate your realm name from the tabs on the left of the page.

![](/images/realms_tab.png)

Under **Modules** locate Chat Relay and press `settings` in the Chat Relay box. This will take you to the Chat Relay page and in there enable the button next to `Chat Relay`.

![](/images/chat_replaySetting.png)

![](/images/turnRelayON.png)

From there you can set the channel you want to use for chat relay by selecting the desired channel from the `Relay Channel` box.

You can also select what type of messages the bot Relays by turning on the respective buttons.

If you use chat ranks please ensure that you enable tellraw relay so that all your messages will relay from in-game into your discord server properly.
