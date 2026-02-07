---
label: Server Setup
description: Complete the recommended setup checklist for your Discord server, including logging, permissions, warn presets, and account linking.
order: 14
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Server Setup

The **Server Setup** page is a guided checklist designed to help you configure the essential server-wide settings required for Realm Bot to operate cleanly and securely. It provides a clear progress indicator and direct links into each configuration area.

![Server Setup Page](/images/server-setup.png)

---

## What Server Setup Does

Server Setup consolidates core configuration into one place so you can:

- Confirm the minimum required settings are in place
- Set up auditing and moderation foundations before enabling advanced modules
- Reduce misconfiguration (missing logs, incorrect permissions, incomplete linking)
- Revisit and review settings at any time as your staff structure evolves

---

## Setup Progress

At the top of the page you will see a **Setup Progress** bar indicating how many steps are completed (for example, **3 of 4 steps completed**). Each step is shown as a card with a brief description and an action button.

Status indicators typically appear as:
- **Completed** (checkmark) — the step has been configured
- **Incomplete** (pending icon) — the step still requires setup
- **Review** — the step is complete and can be reviewed
- **Configure** — the step requires action

---

## Setup Steps

### 1) Logging
Logging is the audit foundation of your server configuration. It ensures staff actions and automated events can be reviewed when investigating incidents.

Use this step to:
- Select appropriate log channels
- Ensure the bot can post to those channels
- Create separation between moderation logs and general activity logs (recommended)

**Best practice:** Keep log channels staff-only and non-chatty to preserve signal-to-noise.

---

### 2) Permissions
Permissions determine who can access server features and who can make high-impact changes.

Use this step to:
- Assign management access to trusted roles only
- Restrict configuration access (dashboard and sensitive modules)
- Prevent accidental misuse by general staff or members

**Best practice:** Apply least privilege. Start strict, then expand access intentionally.

---

### 3) Warn Settings
Warn Settings allow you to configure preset warning behaviour for administrators and moderators. This ensures consistent discipline actions and reduces ambiguity across staff.

Use this step to:
- Configure your default warning preset(s)
- Align warning actions with your server rules
- Ensure moderators operate under the same standards

> **Operational Note:** If you are running a public community, consistent warning policies reduce disputes and improve staff coordination.

---

### 4) Account Linking
Account Linking ties your operational identity to Realm Bot so the bot can reliably verify members and connect your server to the correct Realm access context.

Use this step to:
- Confirm linking flows are complete
- Ensure the correct Discord and Microsoft/Xbox accounts are connected
- Enable workflows that depend on verified identity and Realm access

**Best practice:** Only link trusted administrative accounts. Treat linking as privileged access.

---

## Recommended Order

Although Server Setup is flexible, the recommended order is:

1. **Logging** (audit first)
2. **Permissions** (control access)
3. **Warn Settings** (standardise moderation workflow)
4. **Account Linking** (finalise identity + Realm access flows)

This sequence ensures the server is secure and auditable before more advanced features are enabled.

---

## Troubleshooting

### A step shows as incomplete after configuration
- Re-open the step and confirm you saved changes.
- Ensure Realm Bot has the required Discord permissions for the feature (especially for logging).
- Refresh the dashboard to confirm the state updates.

### Review buttons work, but modules still fail
Server Setup covers foundational configuration. Some Realm modules additionally require:
- Realm-specific configuration (inside the Realm dashboard)
- A Relay Account to be in-game (for certain modules)
- Gametest Pack dependencies (for advanced Realm features)

---
