---
label: Account Linking
description: Configure how members link their Minecraft account to Discord, including automatic role assignment, optional nickname syncing, auto-invites to selected Realms, and join log reporting.
order: 97
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Account Linking

Account Linking allows members to associate their **Minecraft (Microsoft/Xbox)** identity with their **Discord** account. Once enabled, Realm Bot can automate common onboarding tasks such as **role assignment** and **Realm invitations**, while providing clear audit logs for staff.

![Account Linking Configuration](/images/server-account-linking.png)

---

## What Account Linking is for

Account Linking is designed to help you:

- Verify that a Discord member controls the Minecraft account they claim
- Automatically grant roles when a member successfully links
- Optionally sync Discord nicknames to match Minecraft usernames
- Automatically invite linked users to one or more connected Realms
- Log linking events to a dedicated channel for transparency

---

## User Settings

These settings control whether linking is enabled and how it behaves for users.

### Account Linking
When enabled, members can link their Minecraft account to Discord using the Realm Bot linking flow.

**Recommended:** Enable this for most communities, especially public or semi-public servers, as it supports verification and automation.

### Change Nickname
When enabled, Realm Bot will update a user’s **Discord nickname** to match their Minecraft username after linking.

**Before enabling, ensure:**
- Realm Bot has **Manage Nicknames** permission in your Discord server
- Realm Bot’s role is **above** the roles of users whose nicknames it needs to edit (Discord role hierarchy)
- Your server rules allow nickname automation (some communities prefer members to control nicknames themselves)

> **Note:** If permissions or role hierarchy prevent nickname changes, linking can still succeed, but nickname syncing may fail.

---

## Server Integration

These settings define what happens *after* an account is linked.

### Linked Account Roles
Select one or more Discord roles to automatically assign when a member successfully links.

Common uses:
- Grant access to member-only channels after verification
- Separate verified players from unverified users
- Apply moderation or gameplay roles tied to account ownership

**Best practice:** Assign only the minimum role(s) needed for access. Keep staff roles manual.

### Auto-invite to Realms
Choose which connected Realm(s) should automatically invite users when they link their account.

This is ideal for:
- Whitelisted Realms
- Member-only Realms
- Servers that want a “link → join instantly” onboarding flow

**Operational notes:**
- Auto-invite should be limited to trusted Realms (avoid auto-inviting to testing/admin Realms).
- If a Realm is missing from the dropdown, confirm it is connected and visible under your linked Xbox account context.

### Join Logs Channel
Select a Discord channel where Realm Bot will post account linking events (e.g., successful links, key outcomes, and related system messages as supported).

**Recommended setup:**
- Use a staff-only channel (e.g., `#join-logs` or `#verification-logs`)
- Ensure Realm Bot has:
  - **View Channel**
  - **Send Messages**
  - **Read Message History** (recommended)

---

## Recommended Configuration

For most servers, this is the cleanest configuration:

1. Enable **Account Linking**
2. Set **Linked Account Roles** to a standard member role (e.g., `Member` / `Verified`)
3. Enable **Auto-invite to Realms** only for your primary public/member Realm
4. Set a dedicated **Join Logs Channel**
5. Enable **Change Nickname** only if your staff team wants enforced identity consistency

---

## Troubleshooting

### Roles are not being assigned
- Confirm the selected role exists and is still selected.
- Ensure Realm Bot’s role is **above** the target role(s) in Discord role hierarchy.
- Verify Realm Bot has **Manage Roles** permission.

### Nicknames are not changing
- Ensure **Change Nickname** is enabled.
- Ensure Realm Bot has **Manage Nicknames** permission.
- Check role hierarchy: Realm Bot must be above the member’s highest role.

### Auto-invite is not sending invites
- Confirm the Realm is selected under **Auto-invite to Realms**.
- Verify the Realm is connected and available under the linked Xbox account context.
- If your Realm has strict membership limits, ensure you have capacity for new invites.

---
