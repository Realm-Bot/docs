---
label: Allowlist
description: Maintain an allowlist of trusted users who can bypass automated enforcement systems such as Member Gate and Bot Detection.
order: 92
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Allowlist

The **Allowlist** is a safety control that marks specific users as trusted. Users added to the allowlist can **bypass automated enforcement**, ensuring that legitimate players (staff, creators, testers, known community members) are not incorrectly removed by security systems.

![Allowlist](/images/server-allowlist.png)

---

## What the Allowlist Does

When a user is on the allowlist:

- They can bypass **Member Gate**
- They can bypass **Bot Detection**

This is particularly useful if you:
- run strict Member Gate rules (device locks, gamerscore thresholds, etc.)
- enable Experimental Bot Detection and want protection against false positives
- have trusted alt accounts, testers, or staff joining frequently

> **Important:** The allowlist is designed for exceptions. Adding too many users reduces the effectiveness of your automated protections.

---

## Adding Users

Use the **Search or Add** field to find a player and add them to your allowlist.

Recommended use cases:
- Realm staff accounts
- Verified community members
- Long-term players with known identities
- Test accounts used during development or maintenance

---

## Removing Users

Each allowlisted entry can be removed using the delete icon on the right-hand side of the row.

**Best practice:** Remove access when:
- a staff member steps down
- a trusted account changes hands
- you no longer need exceptions for a temporary tester

---

## Security Guidance

### Treat Allowlisting as Privileged Access
Allowlisted users are exempt from key protections. Only allowlist users you genuinely trust.

### Keep an Audit Habit
Periodically review the list (weekly or monthly for large servers), especially if your realm uses public codes or sees frequent traffic.

### Prefer Fixing the Rule Before Allowlisting Everyone
If many legitimate players are being blocked, consider:
- loosening Member Gate conditions
- disabling Experimental Bot Detection
- adjusting thresholds (e.g., gamerscore criteria)
- using allowlist only for edge cases

---

## Common Questions

### “Does allowlisting bypass bans?”
No. The allowlist is intended to bypass automated gatekeeping systems such as Member Gate and Bot Detection. It does not override manual bans or realm-level enforcement actions.

### “Should we allowlist all staff?”
Only staff who need reliable access should be allowlisted. For larger teams, consider allowlisting senior roles only, and rely on correct Member Gate rules for everyone else.

---
