---
label: Scheduled Restart
description: Schedule Realm restarts by local time and weekday and configure reminders for players.
order: 96
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Scheduled Restart

Scheduled Restart closes an open Realm and reopens it so players can rejoin. Realm owners and Realm Admins configure it in the [Realms Hub](realms-hub.md).

## Set a Schedule

1. In the **Realm manager**, open **Realms Hub > Settings > Scheduled Restart**.
2. Enable the schedule. Select a local time, a named time zone and at least one weekday.
3. Choose any reminders you want players to receive.
4. Select **Save schedule**.

The initial configuration is **off**, with **04:00 UTC**, every day selected and no reminders. To stop future runs, disable the schedule and save it.

## Player Reminders

Choose an advance reminder of **10, 15, 30 or 60 minutes**. The optional **five-minute final warning** is independent; it does not require an earlier reminder.

In-game reminders need a working game connection. For Discord reminders, enable [Chat Relay](<../Realm Modules/chat-relay.md>) and choose a player-chat channel where the bot can send messages. Older configurations can use the legacy relay channel. A missed reminder does not mean the restart was cancelled.

## If a Restart Is Missed

- Check the saved weekdays, time and time zone. A local time skipped when clocks move forward does not run. If the clock repeats the selected time in autumn, it runs at most once that local date.
- Closed or expired Realms are not opened for a scheduled restart. A run more than 15 minutes late is skipped.
- If the Realm closed but has not reopened, check its status before taking another action. Turning off future runs does not cancel recovery for a restart already in progress.
