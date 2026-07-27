# `/db report`

Submits a player for internal Realm Bot **Global Ban** review. A report creates a review request for authorised Realm Bot staff; it does not directly ban the player.

## Syntax

`/db report <user> <reason> <evidence>`

## Arguments

| Argument | Required | Description |
|---|---:|---|
| `user` | Yes | The Minecraft player's Xbox gamertag. |
| `reason` | Yes | A concise explanation of the reported behaviour. |
| `evidence` | Yes | An attachment that supports the report. |

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.db.report`, or be a Discord Administrator.
- Premium is not required.
- A user can submit approximately one report every 60 seconds.

## What Happens Next

Realm Bot resolves the player, sends the report and attachment to its internal review workflow, and confirms submission. Authorised Realm Bot staff decide whether the evidence meets the Global Ban standard.

> **Privacy:** Submit only relevant evidence. Remove unrelated personal information, private messages, account details, or content that staff do not need to assess the report.

## Common Issues

### The report is rejected before submission

Confirm the gamertag can be resolved, a reason is present, and an evidence attachment is included. If the cooldown is active, wait for the displayed period before retrying.

### Submission fails

Keep the original evidence and retry later. Do not assume that a failed or pending interaction created a review.

## Related Commands

- [`/banlist lookup`](lookup.md)
- [`/realm ban`](../Realm/ban.md)
- [Command Troubleshooting](../troubleshooting.md)
