---
label: Reporting Players
description: Submit an evidence-backed Realm Hub Global Ban report and track its review status.
order: 97
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Reporting Players

Players can submit evidence-backed reports to the Realm Hub Global Ban review workflow through the website or the `/db report` Discord command.

A successful submission creates a **pending review**. It does not immediately ban the reported player.

## Report Through the Website

Open `/ban-list/report` and sign in with Discord. Website reporters do not need to link their own Microsoft/Xbox account.

1. Enter the player's exact Microsoft/Xbox gamertag.
2. Select **Find Player**.
3. Check the avatar, exact gamertag and 16-digit XUID before reporting the account.
4. Choose the closest category and explain what happened.
5. Attach one to three evidence images.
6. Review the player, category, explanation and evidence.
7. Complete the security check, then select **Submit Report**.

Keep the case number to track the report.

Website explanations must contain meaningful context and be between **40 and 4,000 characters**.

For additional website guidance, open `/help/database-reports`.

## Report Through Discord

In a fully connected Discord server, use:

`/db report`

| Field | Requirement |
|---|---|
| `user` | Exact Microsoft/Xbox gamertag |
| `category` | Required report category |
| `details` | Clear explanation between 40 and 1,000 characters |
| `evidence` | Required screenshot |
| `evidence_2` | Optional additional screenshot |
| `evidence_3` | Optional additional screenshot |

Realm Bot resolves the account and presents a private confirmation containing the avatar, gamertag, XUID, category, explanation, and evidence preview.

Select **Submit Report** to create the case or **Cancel** to abandon it. No case exists before **Submit Report** is selected, and the confirmation expires after ten minutes.

If the command is missing or displays outdated options, close and reopen Discord's command menu. If it remains unavailable, use the website report page.

See the full [`/db report` command reference](<../Commands/Banlist/report.md>).

## Report Categories

Reports use broad categories so reviewers can determine the exact classification from the incident:

- **Nuking or Crashing**
- **Cheating or Exploiting**
- **Harassment or Threats**
- **Ban Evasion**
- **Other**

Choose the closest category. Do not select **Other** for an incident already covered by a named option.

## Evidence Requirements

| Requirement | Limit |
|---|---|
| Supported formats | PNG, JPG, JPEG, WebP, and GIF |
| Maximum size per file | 10 MB |
| Maximum combined attachment size | 20 MB |
| Minimum attachments | 1 |
| Maximum attachments | 3 |

Videos, PDFs, archives, text files, and unsupported image formats are rejected.

Choose images that show the player, the incident and its surrounding context.

Avoid unrelated screenshots, duplicates, or edited evidence that changes the original meaning.

## Evidence Privacy

Submitted evidence begins as private review material. It appears on a public Realm Hub record only when specifically approved for public display.

Before submitting:

- Remove unrelated personal information.
- Avoid exposing private account details or access credentials.
- Include private messages only when they are necessary and appropriate for review.
- Confirm that each image relates directly to the reported incident.

## Submission Limits

To reduce spam and duplicate reports:

- At least 60 seconds must pass between successful submissions.
- One Discord account can submit up to five reports in a rolling hour.
- The same reporter cannot create another pending report for the same player.
- A pending report with no decision after seven days becomes **Expired** and creates no ban.
- Repeated spam, knowingly false reports, abuse, or targeted harassment can result in reporting restrictions.

## Track Your Reports

Open `/ban-list/reports` while signed in with the same Discord account used to submit the report.

Use the gamertag, XUID or case number to identify the report. Each entry shows its category, submission date and review status.

### Report Statuses

| Status | Meaning |
|---|---|
| Pending Review | The case was submitted and is waiting for review |
| Under Review | An authorised reviewer is assessing the report |
| Approved | The report was accepted and can produce a Realm Hub record |
| Denied | The report did not meet the Global Ban standard |
| Expired | No decision was recorded before the seven-day review window ended |

An approved report can produce an active Realm Hub record. Connected Realms enforcing the resulting category are then updated asynchronously.

A case number confirms submission, not a ban. Denied and expired reports do not create bans.

## Troubleshooting

### The player cannot be found

- Re-enter the exact Microsoft/Xbox gamertag.
- Verify spelling and recent gamertag changes.
- Confirm the resolved avatar, gamertag, and XUID before continuing.

### Evidence is rejected

- Confirm the extension and actual file format are supported.
- Keep each image at or below 10 MB.
- Keep all attachments together at or below 20 MB.
- Attach no more than three images.

### The report is blocked as a duplicate

Open [Your Reports](#track-your-reports) and wait for the existing pending report to be decided or expire.

### A recent report is missing

- Confirm the final **Submit Report** action was completed.
- Sign in with the same Discord account used for the submission.
- Check whether the confirmation expired before submission.
- Keep the original evidence if the submission may have failed.

### A report remains pending

- Confirm that fewer than seven days have passed.
- Do not submit another report for the same player.
- Wait for a decision or automatic expiry.

### A report is approved but the Realm is unchanged

- Realm protection updates are asynchronous.
- Confirm the Realm has Global Ban protection enabled.
- Confirm the approved category is enabled for that Realm.
- Use **Check Global Ban Database** and **Check Realm** on the Realm Banlist page.
- Verify the result against the Realm's native banlist.

### A report expired

An expired report did not create a ban. Review the reporting guidance before deciding whether a new, evidence-backed report is appropriate.

### The security check fails

Refresh the page, complete a new security check, and submit again.

### The Discord command is unavailable

Close and reopen Discord's command menu. If `/db report` remains unavailable, use `/ban-list/report`.

## Related Pages

- [Global Ban Overview](overview.md)
- [Realm Protection](realm-protection.md)
- [Ban List Explorer](ban-list-explorer.md)
- [`/db report` command reference](<../Commands/Banlist/report.md>)
