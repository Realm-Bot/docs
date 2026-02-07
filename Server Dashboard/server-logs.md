---
label: Log Channels
description: Configure which Discord channels receive Realm Bot moderation logs, including bans, unbans, kicks, and warnings.
order: 98
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Log Channels

The **Log Channels** page allows you to define where Realm Bot sends operational log messages in your Discord server. Logging is a core administrative feature: it improves transparency, supports staff accountability, and provides an auditable record of moderation actions.

![Log Channels Configuration](/images/server-logs.png)

---

## What Log Channels Are For

Log Channels help you:

- Maintain a reliable record of moderation actions
- Review incidents after the fact (who acted, what happened, when it happened)
- Coordinate staff work across time zones
- Reduce disputes by keeping objective evidence in one place

> **Best Practice:** Keep log channels **staff-only** and **read-only** for most roles. Avoid using public channels for moderation logs.

---

## Available Log Types

The Log Channels section provides separate destinations for different moderation events. Each log type can be routed to its own channel, or multiple log types can share one channel (recommended only for smaller servers).

### Ban Logs
**Messages sent when a user is banned** from your server or Realm Bot-managed environment (depending on your configuration).

Use this for:
- tracking removals and ban reasons (where provided)
- identifying patterns of repeated abuse

### Unban Logs
**Messages sent when a user is unbanned.**

Use this for:
- ensuring unbans are deliberate and visible to senior staff
- reviewing ban reversal decisions

### Kick Logs
**Messages sent when a user is kicked.**

Use this for:
- monitoring short-term removals
- distinguishing temporary removal behaviour from permanent bans

### Warn Logs
**Messages sent when a user receives a warning.**

Use this for:
- monitoring warning escalation
- maintaining consistency in discipline standards across staff

---

## How to Configure

1. Create (or choose) one or more staff-only Discord channels, for example:
   - `#mod-logs`
   - `#staff-commands`
   - `#audit-log`

2. In **Log Channels**, select the destination channel for each log type:
   - Ban Logs
   - Unban Logs
   - Kick Logs
   - Warn Logs

3. Ensure Realm Bot has the required permissions in each selected channel:
   - **View Channel**
   - **Send Messages**
   - **Read Message History** (recommended)

> **If logs are not posting:** the first thing to verify is channel permissions.

---

## Recommended Channel Structure

For most servers, one of the following approaches works best:

### Option A - Single Consolidated Log Channel (Simple)
Route all log types to one channel, such as `#mod-logs`.  
This is appropriate for smaller teams and lower activity.

### Option B - Split by Severity (Recommended for Staff Teams)
- `#warnings-and-kicks` → Warn Logs + Kick Logs  
- `#ban-and-unban` → Ban Logs + Unban Logs  

This improves readability and makes it easier to locate high-impact actions.

### Option C - Full Separation (High Activity)
Use separate channels for each log type.  
This is most suitable for large servers with frequent moderation activity.

---

## Operational Notes

- Logs are only useful if they remain readable. Avoid chatting in log channels.
- Ensure senior staff can review logs even if moderators cannot delete or edit messages.
- If your server is using multiple Realms, keep your log structure consistent across them to reduce staff confusion.

---
