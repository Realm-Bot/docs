# `/connect`

Connects the current Discord server to the invoking member's linked Microsoft/Xbox account and refreshes the Realms available through that account.

> **Warning:** Check the Discord server and linked Xbox account first. If a returned Realm is associated with another server, connecting moves its association, disables its Realm Bot modules and clears their configurations. It does not copy the settings or transfer Minecraft ownership.

## Syntax

`/connect [referral_code]`

If you were referred, enter the code from your referrer. The code is optional; see [Referrals](../../Tools/referrals.md) for eligibility.

**Dashboard alternative:** In onboarding, select **Connect Realms** after linking Microsoft, or use **Server Overview > Connect Realms** on a server with no connected Realms. The same migration warning applies.

## Requirements

- The invoking Discord member must first link their Microsoft/Xbox account in the Realm Bot Dashboard.
- The member must have `command.connect`, or be a Discord Administrator.
- The linked account must own or have usable access to at least one Realm.
- Premium is not required for the connection command itself.

On a new server, a Discord Administrator is normally the practical first caller because no Realm Bot role permissions have been configured yet.

## What the Command Does

Realm Bot:

1. Refreshes the Realms available through the linked Microsoft/Xbox account.
2. Associates the Discord server with that account.
3. Registers the server's Realm Bot slash commands.
4. Reports the connected Realms.

Ensure each Realm has usable access or invite information, commonly a permanent official code where the configured workflow requires one.

Command registration can take a short time after the response. If the Realm list cannot be refreshed, check the linked Xbox account, the Bedrock Realm and its permanent invite code. Relink the account if the refresh continues to fail.

## Related Commands

- [`/disconnect`](disconnect.md)
- [`/dashboard`](dashboard.md)
- [Getting Started](../../setup.md)
- [Command Troubleshooting](../troubleshooting.md)
