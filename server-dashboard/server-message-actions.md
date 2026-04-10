# Message Actions

The **Message Actions** page allows you to configure the messages Realm Bot sends when moderation actions are performed. These messages help players understand what happened, why it happened, and what to do next-while keeping your enforcement consistent across staff.

![Message Actions Notice and Variables](/images/server-message-actions-explanation.png)

---

## Important Notice

Moderation messages are sent **through your Xbox account**. You are responsible for ensuring any content sent is compliant with the **Xbox Community Standards** and appropriate for your audience.

Practical implications:
- Avoid harassment, threats, slurs, or inflammatory language
- Keep messages factual, calm, and procedural
- Do not share personal data or internal staff discussion

---

## How Message Actions Work

For each moderation action, you can:

1. **Enable** the message type (per action)
2. Customise the message text
3. Insert variables so the message automatically adapts to each case

When enabled, Realm Bot will send the configured message to the affected player when the corresponding action occurs.

![Message Templates (Kick / Ban / Unban / Warn)](/images/server-message-actions-messages.png)

---

## Available Variables

You can insert variables at the cursor position to dynamically populate details:

- `{user}` - the staff member or account that performed the action
- `{target}` - the player who received the action
- `{reason}` - the reason provided (if any)
- `{length}` - the action duration (if applicable)
- `{guild}` - your Discord server name/identifier
- `{realm}` - the Realm name/context

> **Tip:** Always include `{reason}` where possible. A clear reason reduces disputes and repeat offences.

---

## Message Types

### Kick Message
Sent when a player is **kicked**.

Recommended content:
- What occurred (kick)
- Reason
- Next step (rejoin allowed unless otherwise stated)

### Ban Message
Sent when a player is **banned**.

Recommended content:
- What occurred (ban)
- Reason
- Duration (if temporary)
- Appeal path (if you support appeals)

### Unban Message
Sent when a player is **unbanned**.

Recommended content:
- Confirmation of unban
- Reminder of rules/expectations

### Warn Message
Sent when a player receives a **warning**.

Recommended content:
- Warning reason
- Behaviour expected going forward
- Escalation note (optional, avoid threats)

---

## Suggested Templates (Copy/Paste)

These templates are intentionally short, neutral, and procedural.

### Kick
`{target}, you were removed from {realm}. Reason: {reason}. You may rejoin if you follow the rules.`

### Kick 
`{target} was kicked from {realm} by {user}. Reason: {reason}.`

---

### Ban 
`{target}, you have been banned from {realm}. Reason: {reason}. Duration: {length}.`

### Ban
`{target}, you have been banned from {realm}. Reason: {reason}. If you believe this is an error, contact staff in {guild}.`

---

### Unban
`{target}, your ban has been removed in {realm}. Please review the rules before rejoining.`

---

### Warn 
`{target}, you have received a warning in {guild}. Reason: {reason}. Please stop this behaviour to avoid further action.`

### Warn
`Warning issued to {target}. Reason: {reason}.`

---

## Best Practices

- Keep messages **short and factual**. Players should understand the action within one read.
- Avoid staff-only detail (internal notes, accusations, speculation).
- Use consistent phrasing across Kick/Ban/Warn so players recognise official notices.
- If you support appeals, reference a single channel or process-do not argue in-game.
- Leave `{reason}` blank only when necessary; otherwise make it mandatory in your workflow.

---

## Troubleshooting

### Messages are not sending
- Confirm the specific message type toggle is **enabled** (Kick/Ban/Unban/Warn).
- Ensure your moderation commands include a **reason** and **duration** where applicable.
- If your implementation depends on a linked Xbox account for outbound messages, verify the correct account is linked and operational.

### Variables are showing literally (not replaced)
- Ensure variables match the supported format exactly: `{user}`, `{target}`, `{reason}`, `{length}`, `{guild}`, `{realm}`.
- Avoid extra spaces inside braces (e.g., `{ reason }`).

---
