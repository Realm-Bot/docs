---
label: "/db report"
description: Submit an evidence-backed Minecraft player report for Realm Hub Global Ban review.
order: 95
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# `/db report`

Submits a Minecraft player and supporting evidence for Realm Hub **Global Ban** review. A confirmed report creates a pending case for authorised reviewers; it does not immediately ban the player.

## Syntax

`/db report <user> <category> <details> <evidence> [evidence_2] [evidence_3]`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The player's exact Microsoft/Xbox gamertag. |
| `category` | Yes | The broad report category that best matches the incident. |
| `details` | Yes | A meaningful explanation between 40 and 1,000 characters. |
| `evidence` | Yes | The first supporting screenshot. |
| `evidence_2` | No | A second supporting screenshot. |
| `evidence_3` | No | A third supporting screenshot. |

## Report Categories

- **Nuking or Crashing**
- **Cheating or Exploiting**
- **Harassment or Threats**
- **Ban Evasion**
- **Other**

Choose the closest category rather than **Other** when a named category already covers the incident.

## Requirements

- The Discord server must be fully connected to a Microsoft/Xbox account.
- The member must have `command.db.report`, or be a Discord Administrator.
- Premium is not required.
- The reported gamertag must resolve to an Xbox profile.
- At least one supported evidence image is required.

## Evidence

| Requirement | Limit |
|---|---|
| Supported formats | PNG, JPG, JPEG, WebP, and GIF |
| Maximum size per file | 10 MB |
| Maximum combined attachment size | 20 MB |
| Maximum attachments | 3 |

Videos, PDFs, archives, text files, and unsupported image formats are rejected.

Evidence should clearly show the relevant player, incident, and surrounding context. Avoid duplicate screenshots or edits that change the original meaning.

## Confirmation

Realm Bot resolves the account and displays a private confirmation containing:

- Player avatar.
- Exact gamertag.
- 16-digit XUID.
- Selected category.
- Report explanation.
- Evidence preview.

Select **Submit Report** to create the case or **Cancel** to abandon it. No case exists before **Submit Report** is selected.

The confirmation expires after **ten minutes**. If it expires, run the command again and review the resolved account before submitting.

## Submission Limits

- At least 60 seconds must pass between successful submissions.
- One Discord account can submit up to five reports during a rolling hour.
- The same reporter cannot create another pending report for the same player.
- Pending reports have a seven-day review window.
- A report with no decision after seven days becomes **Expired** and creates no ban.
- Reporting spam, knowingly false reports, abuse, or targeted harassment can result in reporting restrictions.

## What Happens Next

A successful submission displays a case number and creates a pending review. Authorised Realm Hub reviewers assess the report and its private evidence.

An approved report can create an active Realm Hub record. A denied or expired report creates no ban. Track the outcome through [Your Reports](<../../Global Ban/reporting-players.md#track-your-reports>).

> **Privacy:** Evidence begins as private review material and becomes public only when specifically approved for display. Submit only relevant evidence and remove unrelated personal information, credentials, or content reviewers do not need.

## Common Issues

### The command shows outdated options

Close Discord's command menu and reopen it. If the refreshed command remains unavailable, use the website report route at `/ban-list/report`.

### The player cannot be found

Re-enter the exact Microsoft/Xbox gamertag and verify its spelling. Confirm the avatar, gamertag, and XUID in the private confirmation.

### Evidence is rejected

Confirm the file format, extension, individual size, combined size, and attachment count meet the documented limits.

### The report is blocked as a duplicate

Open [Your Reports](<../../Global Ban/reporting-players.md#track-your-reports>) and wait for the existing pending case to be decided or expire.

### The confirmation expired

Run `/db report` again. Nothing was submitted unless **Submit Report** completed and a case number was shown.

### Submission fails

Keep the original evidence and retry later. Do not assume that a failed or pending interaction created a case.

## Related Pages

- [Reporting Players](<../../Global Ban/reporting-players.md>)
- [Global Ban Overview](<../../Global Ban/overview.md>)
- [`/banlist lookup`](lookup.md)
- [`/realm ban`](../Realm/ban.md)
- [Command Troubleshooting](../troubleshooting.md)
