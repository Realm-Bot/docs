# Global Ban

The **Realm Hub Global Ban Database** is Realm Bot's shared moderation system for Minecraft Bedrock Realms. It combines evidence-backed reporting, reviewed public records, optional Realm protection, and eligible account-owned appeals.

## Documentation

- [Overview](overview.md) - understand the database, public routes, source boundaries, and moderation lifecycle.
- [Realm Protection](realm-protection.md) - configure which reviewed Global Ban categories a connected Realm enforces.
- [Ban List Explorer](ban-list-explorer.md) - search and filter public Realm Hub and supported provider records.
- [Reporting Players](reporting-players.md) - submit evidence-backed reports and track their review status.
- [Appeals](appeals.md) - appeal an eligible Realm Hub record owned by a linked Xbox account.
- [Custom Ban List Format](custom-ban-list-format.md) - prepare a public GitHub JSON source for Explorer preview.
- [`/db report`](<../Commands/Banlist/report.md>) - view the Discord command reference.

## Important Boundary

A Realm's official banlist and the Realm Hub Database are related but separate:

- The **Realm Hub Database** stores shared records created through Realm Hub reporting and review.
- A **Realm banlist** controls access to one specific Minecraft Realm.
- **External providers** own and maintain their independent records.
- **Custom GitHub lists** are preview sources and are not automatically enforced.

Reports and appeals submitted through Realm Bot affect only Realm Hub records. They do not modify ARAS / Realms+, custom GitHub lists, or another provider's database.

Use [Banlist Commands](<../Commands/Banlist/index.md>) to inspect official Realm blocklists. Use [`/realm ban`](<../Commands/Realm/ban.md>) and [`/realm unban`](<../Commands/Realm/unban.md>) to change a Realm's official blocklist.
