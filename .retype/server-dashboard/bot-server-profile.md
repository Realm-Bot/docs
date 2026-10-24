# Bot Server Profile

Bot Server Profile lets you give Realm Bot a **custom avatar and nickname** in one Discord server. Use it to match your community's branding while keeping the bot's appearance in other servers independent.

This is a **Realm Bot Premium** feature. It is configured from the server's **Overview** page and applies to the Discord server as a whole, rather than an individual Minecraft Realm.

---

## Requirements

- Dashboard access to manage the selected Discord server.
- Realm Bot present in that server.
- Active Premium recognised through the server's linked account.
- The bot's **Change Nickname** permission when changing its nickname.

Without active Premium, the card shows an upgrade notice and disables customisation. Saving changes and resetting the profile both require Premium.

---

## Open the Profile Settings

1. Select your Discord server in the Realm Bot Dashboard.
2. Open **Overview**.
3. Find **Bot Server Profile**, below the server information and above **Linked User Information**.

The card shows the current profile and a preview of pending edits. If the initial profile load fails, use **Retry**.

---

## Change the Avatar

1. Select **Change Avatar**.
2. Choose a supported image and review the avatar preview.
3. Select **Save Changes** to apply it.

Supported formats are **PNG**, **JPEG/JPG**, and **WebP**, with a maximum file size of **10 MB**. GIF uploads are rejected; animated GIF avatars are not supported by this control.

Selecting a file prepares the change but does not apply it to Discord. Check the success message after saving.

---

## Change the Nickname

Enter the desired name in **Server Nickname**, then select **Save Changes**. The field supports up to **32 characters** and includes a character counter.

Clearing the field and saving restores the default bot name. The avatar and nickname can be changed together or independently.

**Cancel** discards pending edits. Unlike Realm Stories and Security settings, this card requires an explicit **Save Changes** action; it does not save edits automatically.

---

## Reset the Profile

| Control | Effect | How to apply it |
|---|---|---|
| **Reset** beside the avatar | Prepare a return to the default avatar | Select **Save Changes** |
| Clear **Server Nickname** | Prepare a return to the default bot name | Select **Save Changes** |
| **Reset to Default** in the card header | Reset both the avatar and nickname | Select **Confirm Reset** in the confirmation dialog |

**Confirm Reset** submits the full reset directly. It does not require a second save action. Successful changes display a confirmation message.

---

## Scope and Limits

The feature changes Realm Bot's member avatar and nickname in the selected Discord server. It does not change:

- The bot's application identity or slash-command names.
- Its Minecraft account or in-game appearance.
- Your own Discord profile or the Discord server's icon.
- Its profile in other Discord servers.

There are no banner, biography, or other profile-customisation controls. Images explicitly included in individual embeds can retain their existing branding.

Do not rely on Premium expiry to restore the default profile. Active Premium is required to make further changes or reset the profile through this feature.

---

## Best Practices

- Use an image that remains recognisable at a small size.
- Choose a nickname that makes the bot easy for members and staff to identify.
- Review the preview and confirm the selected server before saving.
- Use the reset controls while Premium is active if you want to restore the default profile.

---

## Troubleshooting

### The Bot Server Profile card is missing

- Open the Discord server's **Overview**, rather than an individual Realm page.
- Confirm your dashboard version includes **Bot Server Profile**. If the card is still absent, contact support to check availability for your deployment.

### Customisation controls are disabled

- Confirm active Premium is recognised through the server's linked account.
- Confirm you have dashboard access to manage the selected server and that Realm Bot is still present.

### An image is rejected

- Use PNG, JPEG/JPG, or WebP.
- Keep the file within the 10 MB limit.
- Do not upload a GIF; use a supported static image instead.

### Changes are visible in the preview but not in Discord

- Select **Save Changes** and check for a success message or error.
- Confirm you are viewing the bot's member profile in the same Discord server.
- For nickname changes, verify the bot has **Change Nickname** permission.
- If Discord reports a rate limit, wait before retrying.

### Resetting the avatar did not restore the nickname

The avatar's **Reset** control affects only the avatar. Use **Reset to Default**, then **Confirm Reset**, to restore both fields, or clear the nickname and save it separately.

---
