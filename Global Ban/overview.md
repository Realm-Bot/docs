---
label: Overview
description: Understand the Realm Hub Global Ban Database, its public features, source boundaries, and moderation lifecycle.
order: 100
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Global Ban Overview

The **Realm Hub Global Ban Database** is Realm Bot's shared moderation system for Minecraft Bedrock Realms. It lets players submit evidence-backed reports, publishes reviewed moderation records, allows eligible account-owned appeals, and lets Realm owners enforce selected record categories.

## Quick Links

| Feature | Site path |
|---|---|
| Browse public records | `/global-bans` |
| Report a player | `/ban-list/report` |
| View your reports | `/ban-list/reports` |
| Reporting help | `/help/database-reports` |
| View your appeals | `/appeal` |
| Manage Realm protection | Dashboard -> Server -> Realm -> Tools -> Banlist |

These paths refer to Realm Bot's main website or dashboard, not this documentation site.

## Different Lists and Sources

| System | Purpose |
|---|---|
| Realm Hub Database | Shared moderation records maintained through Realm Hub reporting and review |
| Realm banlist | Players currently banned from one specific Realm, including local and applied Global Ban entries |
| ARAS / Realms+ | An independent public provider whose records Realm Hub cannot change |
| Custom GitHub lists | Third-party lists that can be previewed in the Ban List Explorer but are not automatically enforced |

Reports submitted through Realm Bot affect only the Realm Hub Database. They do not modify ARAS / Realms+, custom GitHub lists, or another external database.

## Moderation Lifecycle

1. A player submits a report through the website or `/db report`.
2. Realm Bot creates a pending case after the reporter confirms the submission.
3. Authorised reviewers assess the report and its private evidence.
4. An approved report can create a public Realm Hub record.
5. Connected Realms with matching protection categories enabled are updated asynchronously.
6. The affected player can appeal an eligible record through the linked Xbox account that owns it.
7. An accepted appeal revokes the Realm Hub record and triggers asynchronous Realm reconciliation.

A report is not a ban. A pending, denied, or expired report does not create a Global Ban record.

## Public Records

Realm Hub records may publish:

- Case number.
- Player profile and gamertag.
- 16-digit XUID.
- Public moderation reason.
- Ban type.
- Effective date and duration.
- Current status.
- Evidence specifically approved for public display.

Evidence submitted with a report begins as private material. It appears publicly only when explicitly approved for publication.

## Essential Points

- Global Ban protection is enabled by default for newly connected Realms that have no saved custom setting.
- Realm owners can choose exactly which categories their Realm enforces.
- Reports are reviewed before any database record is created.
- Website reporters need Discord sign-in but do not need to link their own Xbox account.
- Appeals require the linked Xbox account that matches the affected Realm Hub record.
- Submitting an appeal does not pause enforcement.
- External databases remain independent from Realm Hub.
- Disabling protection does not remove bans already present in a Realm's native banlist.

## Next Steps

- Configure [Realm Protection](realm-protection.md).
- Browse the [Ban List Explorer](ban-list-explorer.md).
- Learn how to [Report a Player and Track the Case](reporting-players.md).
- Review the [Appeals](appeals.md) process.
- Prepare a [Custom Ban List](custom-ban-list-format.md).
