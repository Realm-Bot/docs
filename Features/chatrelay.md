---
label: relay
order: 1
---

# Chat Relay
Chat relay is a feature which allows people in discord to talk with people in your realm and vice versa 

Chat relay requires you to be a premium user 

---

## How it Works 
  Chat realy works by the bot instantly sending messages sent in the realm to a dedicated channel in your discord and messages sent in that channel being sent to the realm instantly 
  
  The bot does this by joining the realm on the realm owners account or its own account *if you have alt account joining enabled* 
  
  There are two ways how the bot sends messages from realm to the discord. One as a normal message and as a embed (*also called tellraw relay*)

  ![Example of normal relay message](/images/relay.png)  
  
  ![Example of tellraw relay](images/tr_relay.png)
  
---

## Configuring chat relay 
  Chat relay can be configured via the [dashboard](https://realmbot.dev/)
  
  For the commands related to chat relay see [Chat Relay](world.md) 
  
  If you want the bot to rejoin automatically everytime, go to world joining tab in your server dashboard and turn on `Joins World Automatically` option 
  
  By default the bot joins the realm with the owners account

  If you want the bot to join with its own account insted of owners account, turn on `Use Altertive account` option in world joining tab in your server    dashboard 
  
  ![world joining tab](/images/wrld_join.png)
  
  To turn on chat relay  head over to Chat Relay tab in your server dashboard and turn on `Chat Relay` option and set the channel you want the messages to be relayed in the `Relay Channel` box
  
  If you want the relayed messages to be sent as a embed turn on `Tellraw Relay` option 
  
  ![Chat Relay tab](/images/chat_relay_tab.png) 
