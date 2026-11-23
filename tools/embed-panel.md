# Embed Panel

Use **Embed Panel** to publish a Discord message with Realm information, links or in-game action buttons. Preview the message in the dashboard before posting it.

## Security Model

Realm-action buttons execute through the privileged Relay Account. Any Discord user who can view and click a button may trigger its configured action.

> **Important:** Realm Bot's slash-command role permissions do not automatically protect panel buttons. Place panels with administrative actions in a restricted channel. For public panels, use link buttons or only commands that are safe for every viewer.

Do not use a public button for destructive world, member, or access-control actions.

## Requirements

- An active Realm Bot Premium subscription
- A selected Discord destination channel
- **View Channel**, **Send Messages**, **Embed Links**, and **Read Message History** for Realm Bot
- A connected Relay Account for Realm-action buttons
- Sufficient in-game command privileges for each configured action

Link-only panels do not require an active in-game command path after the message has been sent.

## Create a Panel

1. Open **Tools** and select **Embed Panel** for the intended Realm.
2. Set the embed title, description and colour, then check the preview.
3. Add no more than five buttons.
4. For each button, choose either a trusted URL or a safe Realm command.
5. Select the Discord destination.
6. Send the panel and test each button using an account with the same channel access as the intended audience.

## Editing and Deletion

Return to the Embed Panel page to update the saved configuration and resend the panel. Realm Bot replaces the prior managed message where possible. Use the delete action to remove the active panel when it is no longer needed.

## Troubleshooting

### The panel does not appear

- Confirm a destination channel is selected.
- Verify Realm Bot can View Channel, Send Messages, Embed Links, and Read Message History.
- Confirm the panel content passes the dashboard validation.

### A Realm-action button does not work

- Confirm the Relay Account is online in the correct Realm.
- Confirm the command is supported and has valid Minecraft syntax.
- Confirm the Relay Account has sufficient operator permissions.
- Check the Realm Console or operational logs for command feedback where available.

### The wrong audience can use an action

- Restrict **View Channel** access immediately.
- Remove or replace the action button.
- Use a staff-only channel for privileged actions.
