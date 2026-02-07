---
label: Permissions
description: Control which Discord roles can use specific Realm Bot commands by assigning granular permissions per role.
order: 93
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Permissions

The **Permissions** page allows you to control exactly which **Discord roles** can use Realm Bot’s commands. Permissions are applied at the **role level**, meaning every member with that role inherits the configured access immediately.

This is the recommended way to prevent accidental misuse of high-impact commands (e.g., bans, realm code changes, world actions) while still allowing staff to perform routine moderation.

![Role Permissions Overview](/images/server-permissions-roles.png)

---

## How the Permission System Works

Realm Bot permissions are:

- **Role-based**: permissions are assigned to Discord roles, not individual users
- **Granular**: you can allow or deny access to specific command groups and actions
- **Immediate**: changes apply as soon as you save them, affecting all members with that role

> **Important:** Your Discord permissions (Administrator, Manage Server, etc.) do not automatically map to Realm Bot permissions. You must explicitly grant access here.

---

## Managing Role Permissions

### 1) Select a Role
In **Manage Role Permissions**, locate the role you want to configure. You can use the search bar if you have many roles.

Each role card shows whether it currently has Realm Bot permissions assigned.

### 2) Edit the Role
Select the edit icon on the role card to open that role’s permission configuration.

---

## Permission Categories

Permissions are grouped by feature area. When editing a role, you will see categories such as:

- **Realm** (invites, kicks/bans, realm code, open/close, slots, players, backups)
- **World** (execute, broadcast, join/leave, live actions)
- **Warn** (add/lookup/remove warnings)
- **Allowlist** (add/check/list/remove allowlist entries)
- **Player** (lookup and player-level info commands)
- **Verify** (verification/embed or onboarding utilities)
- **Banlist** (lookup or list ban records, where supported)

Each category includes a **Select All** option to quickly grant everything within that section—use this cautiously.

![Role Permission Editor](/images/server-permissions-settings.png)

---

## Recommended Role Model (Best Practice)

A clean permission structure reduces mistakes and keeps accountability clear. A typical setup looks like this:

### Owner / Head Admin
Grant full permissions, including:
- Realm code changes
- Ban/unban
- World execute
- Backups/world replacement tools (if present)
- Permission editing itself (if available)

### Senior Staff / Managers
Grant operational moderation + management, but limit high-risk actions:
- Kick/ban/unban (optional)
- Player lookup, realm players, recents
- Warnings and allowlist management
- Limited world actions if required (broadcast/live), avoid `World Execute` unless fully trusted

### Moderators
Grant routine moderation only:
- Kick (optional)
- Warn add/lookup/remove
- Player lookup
- Allowlist check/list
- View realm players

### Support / Helpers
Minimal access:
- Player lookup
- Allowlist check/list
- Verify tools (if your server uses them)
- No kick/ban and no realm management

> **Security guideline:** Treat `World Execute` and realm code management as **high-risk**. Only grant these to trusted administrators.

---

## Common Misconfiguration Pitfalls

### “Staff can’t use commands they should have”
- Confirm the correct role was edited (many servers have similarly named roles).
- Ensure the user actually has that role in Discord.
- Check that you enabled the specific permission (e.g., `Realm Kick` is separate from `Realm Ban`).

### “Too many people can run dangerous commands”
- Remove **Select All** usage for broad categories.
- Create a dedicated “Technical Admin” role for high-impact permissions.
- Split moderation (Warn/Kick) from infrastructure controls (Code Change/Execute).

---

## Operational Tips

- Keep permission sets **as small as possible** per role.
- Use roles, not individuals, to prevent “one-off exceptions” that are forgotten later.
- Review your permissions after staff changes or major server restructuring.
- If you use automated onboarding roles, ensure new members do **not** inherit staff permissions accidentally.

---
