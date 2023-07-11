---
label: Chat relay
order: 1
---

# Chat Relay
Chat relay is a feature which allows people in Discord to talk with people in your realm and vice versa 

Chat relay requires you to be a premium user and needs the bot to be in the Realm

---

## How it Works 
  Chat relay works by the Realmbot instantly sending messages sent in the realm to a dedicated channel in your discord and messages sent in that channel are sent to the realm instantly 
  
  The bot does this by joining the realm on the realm owner's account or its own account *if you have alt account joining enabled* 
  
  There are two ways how the bot sends messages from the realm to the discord. One as a normal message and as an embed (*also called tellraw relay*)

  ![Example of normal relay message](/images/relay.png)  
  
  ![Example of tellraw relay](images/tr_relay.png)
  
---

## Configuring chat relay 
  Chat relay can be configured via the [dashboard](https://realmbot.dev/)
  
  For the commands related to chat relay see [Chat Relay](world.md) 
  
  If you want the bot to rejoin automatically every time, go to the world joining tab in your server dashboard and turn on `Joins World Automatically` option 
  
  By default, the bot joins the realm with the owner's account

  If you want the bot to join with its own account instead of owner's account, turn on `Use Alternative account` option in the world joining tab in your server dashboard 
  
  ![world joining tab](/images/wrld_join.png)
  
  To turn on chat relay head over to the Chat Relay tab in your server dashboard and turn on `Chat Relay` option and set the channel you want the messages to be relayed in the `Relay Channel` box
  
  If you want the relayed messages to be sent as an embed turn on `Tellraw Relay` option 
  
  ![Chat Relay tab](/images/chat_relay_tab.png) 
