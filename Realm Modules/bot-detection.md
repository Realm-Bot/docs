---
label: Bot Detection
description: Mitigate malicious bot accounts joining public Realms by automatically detecting and removing suspicious connections. Includes an Experimental mode for advanced detection.
order: 70
image: /images/custom/botdetection.png
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

### What is Bot Detection?

Bot Detection is a protective feature designed to mitigate malicious **bot accounts** that join Realms to cause **latency**, **performance degradation**, or **gameplay disruption**. It is primarily intended for Realms that use **public invite codes**, where automated join attempts are more likely to occur.

> **Important:** Bot Detection reduces risk and disruption, but it cannot guarantee absolute prevention. Minecraft Realms are subject to platform constraints, and detection is based on observable behaviour at join-time.

### When Bot Detection is Recommended

Bot Detection is best suited to:
- **Public-code Realms** (open access, frequently shared codes)
- Realms experiencing repeated **join floods**, **lag spikes**, or **suspicious new accounts**
- Communities that require better stability during peak activity or events

For private invite-only Realms, Bot Detection may be unnecessary unless you are actively experiencing suspicious join patterns.

### How Bot Detection Works

When enabled, Bot Detection observes join activity and applies automated mitigation to accounts that appear to be malicious or automated. This is intended to keep your Realm stable by reducing disruptive join behaviour commonly associated with bot activity.

Bot Detection requires a **Relay Account to be in-game** to function. If the Relay Account is not online in the Realm, Bot Detection cannot execute its mitigation actions.

### Detection Modes

Bot Detection currently includes two detection modes:

- **Regular Bot Detection**  
  The standard detection mode. This is the recommended default and is generally sufficient for most public Realms.

- **Experimental Bot Detection (Beta)**  
  A more aggressive detection mode intended to identify more sophisticated bot behaviour.  
  **This mode may occasionally flag legitimate player accounts.** Enable with caution and only when necessary.

> **Caution:** If you enable Experimental Bot Detection, ensure staff are prepared to respond quickly to reports of legitimate players being affected.

### Requirements

To use Bot Detection, you must have:

- A configured **Relay Account** that is actively **in-game**.
- Bot Detection enabled within the Realm Bot Dashboard.

### How to Set Up

1.  Open the **Bot Detection** module in the Realm Bot Dashboard.<br/>
    ![Bot Detection Configuration](/images/bot-detection.png)
2.  Enable **Bot Detection** using the main toggle.
3.  Under **Detection Settings**, choose one of the following:
    - By default, **Regular Bot Detection** is enabled
    - Optionally enable **Experimental Bot Detection (Beta)** if your Realm continues to experience bot activity
4.  Confirm your Relay Account is **online in the Realm**, as Bot Detection requires an in-game executor to operate.

### Recommended Configuration

For most public Realms:
- Enable **Regular Bot Detection**
- Leave **Experimental Bot Detection** disabled unless bot activity persists

Enable **Experimental Bot Detection** only when:
- Regular mode is insufficient against repeated bot activity
- You can tolerate the risk of occasional false positives
- Staff are available to handle disputes quickly and professionally

### Best Practices

- Restrict access to public codes where possible (rotate codes if abuse is ongoing).
- Keep the Relay Account reliably online during high-risk periods (peak times, events, after a code is shared publicly).
- Treat Experimental detection as an escalation tool, not a default setting.
- Maintain a clear staff procedure for handling reports of false positives (collect the player name, time of join, and what they observed).

### Common Issues

**Bot Detection is enabled, but nothing happens**
- Confirm the Relay Account is **in-game**.
- Verify the correct Realm is selected in the dashboard.
- Ensure the module toggles are saved and remain enabled.

**Legitimate players are being flagged**
- Disable **Experimental Bot Detection** immediately.
- Continue using **Regular Bot Detection** while monitoring join behaviour.
- If false positives persist, keep the feature in Regular mode and consider additional access controls (e.g., limiting code distribution).

