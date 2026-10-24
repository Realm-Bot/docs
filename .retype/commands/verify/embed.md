# `/verify embed`

Posts a public Microsoft/Xbox account-linking panel in the current Discord channel.

## Syntax

`/verify embed`

## Requirements

- The Discord server must be connected to a Microsoft/Xbox account.
- The member must have `command.verify.embed`, or be a Discord Administrator.
- Realm Bot must be able to view and send messages in the current channel.
- Premium is not required.

## What Users Experience

The slash-command confirmation is private to the staff member who runs it, while the verification panel is public in the channel.

When a member selects **Verify**, Realm Bot sends a private Microsoft/Xbox linking URL by direct message. The member must allow direct messages from the server.

Depending on [Account Linking](<../../Server Dashboard/server-account-linking.md>) configuration, successful linking can:

- Assign configured Discord roles
- Update the member's Discord nickname
- Invite the linked Microsoft/Xbox account to selected Realms
- Send the result for staff review

## Channel Security

> **Important:** Place review-required linking messages in a staff-only review or log channel. Restrict **View Channel** and interaction access to trusted reviewers.

The public verification panel belongs in the intended onboarding channel. The review channel should never be visible to general members.

## Common Issues

### The panel does not appear

Confirm Realm Bot can **View Channel**, **Send Messages**, and use embeds or components in the selected channel.

### A member does not receive the linking URL

Ask them to enable direct messages from server members and select **Verify** again.

## Related Documentation

- [Account Linking](<../../Server Dashboard/server-account-linking.md>)
- [Command Troubleshooting](../troubleshooting.md)
