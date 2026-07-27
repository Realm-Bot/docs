---
label: Embed Panel
description: Create a persistent Discord embed with up to five link or Realm-action buttons.
order: 100
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Embed Panel

Embed Panel creates a persistent Discord embed for Realm information, links, and carefully selected Realm actions. The dashboard provides a live preview before the panel is sent.

This feature is presented as part of Realm Bot Premium.

## Capabilities

- Configure the embed title, description, colour, and presentation.
- Send the panel to a selected Discord channel.
- Save the panel configuration for later editing.
- Update or replace the previously sent panel.
- Delete the active panel.
- Add up to **five buttons**.
- Use link buttons for trusted external destinations.
- Use action buttons to execute a configured command through the connected Realm.

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
2. Configure the embed content and review the live preview.
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
