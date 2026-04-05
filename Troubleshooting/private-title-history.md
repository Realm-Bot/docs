---
label: Private Title History
description: Fix kicks caused by private Xbox title history by setting “Others can see your game and app history” to Everybody.
order: 85
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Automod kicked me for “Private Title History”

If you were removed from a Realm with the reason **“Private Title History”**, your Xbox privacy settings are preventing Realm Bot from reading the minimum public profile signals needed to confirm basic account context, most commonly **device/platform identification**.

This check is commonly used alongside automated entry and security systems, for example device-based gating. When title history is private, the system cannot validate that signal reliably, and you may be removed automatically.

## What you need to change

You must set the Xbox privacy option:

**“Others can see your game and app history”** -> **Everybody**

After updating the setting, rejoin the Realm and try again.

> Note: If you change this setting back to private later, the same kick may occur again depending on the Realm’s configuration.

---

## Fix on Xbox Console (Xbox One / Series X|S)

1. Press the **Xbox** button to open the guide.
2. Go to **Profile & system** -> **Settings**.
3. Select **Account** -> **Privacy & online safety** -> **Xbox privacy**.
4. Select **View details & customise**.
5. Open **Online status & history**.
6. Set **Others can see your game and app history** to **Everybody**.

If you do not see these options or cannot change them, your account may be a child account managed by a family organiser. In that case, a parent or organiser must update the privacy settings.

---

## Fix on Web (Nintendo / PlayStation / PC / Mobile users)

1. Sign in to Xbox privacy settings using the Microsoft account you use for Minecraft.
2. Navigate to **Privacy & online safety** -> **Xbox privacy** -> **View details & customise**.
3. Open **Online status & history**.
4. Set **Others can see your game and app history** to **Everybody**.

Practical reminders:

- Ensure you are signed into the correct Microsoft account, the one that owns your Minecraft profile.
- After saving, wait briefly and try joining again.

---

## If it still kicks you

Check the following:

- You changed the correct setting: **Others can see your game and app history** is set to **Everybody**.
- You are signed into the correct Microsoft account. Many users have more than one.
- Your account is not restricted by family controls.
- You waited long enough for the setting to apply, then rejoined.

If the issue persists after confirming the above, contact the server staff and provide:

- your gamertag
- the approximate time of the kick
- confirmation that title history is set to Everybody
