---
label: World Management
description: Manage your Realm’s active world slot, download backups, replace worlds, and control Behaviour/Resource packs (including upload, enable/disable, and pack priority).
order: 12
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# World Management

The **World Management** area lets you manage the files and configuration tied to your Realm’s worlds. It is divided into four sections:

1. **World Slot** - choose which of your Realm’s world slots you are managing  
2. **World** - download a backup and replace the active world file  
3. **Behaviour Packs** - upload and manage behaviour packs for the active world  
4. **Resource Packs** - upload and manage resource packs for the active world  

![World Management Sections](/images/world-management.png)

> **Important:** All actions in World Management apply to the **currently selected World Slot**. Always confirm you are modifying the correct slot before uploading, replacing, or changing pack order.

---

## World Slot

Realms typically provide multiple world slots. The **World Slot** selector allows you to switch between slots and manage each slot independently.

![World Slot Selector](/images/world-slot.png)

Typical usage:
- Select the slot you want to manage (e.g., Slot 1, Slot 2, Slot 3).
- Confirm the slot name and game mode (e.g., Survival, Adventure) before making changes.

Realm slots are numbered **1 through 3**. Every upload, replacement, and pack action is scoped to the currently active slot.

**Best practice:** Treat world slots as separate environments. Keep at least one slot reserved for backups/testing if your workflow allows it.

---

## World

The **World** section is used for backups and world replacement on the active slot.

![World Page](/images/world-page.png)

### Download World (Backup)
Use **Download World** to export the current world from the selected slot.

This is strongly recommended before you:
- replace the world
- install significant packs
- make major gameplay changes that could require rollback

### Replace World
Replace World allows you to upload a new world file to the active slot.

- Supported file type: **.mcworld**
- Maximum file size: **100MB** (as displayed in the uploader)

> **Warning:** Replacing the world will permanently delete the current world for that slot. Download a backup first to avoid losing progress.

Operational guidance:
- Only replace worlds during low-activity windows.
- Announce downtime to staff/players if the Realm will be unavailable during the swap.
- Verify the correct slot is selected before upload.

---

## Behaviour Packs

Behaviour Packs change gameplay logic and behaviour (systems, mechanics, rulesets, entities, etc.). This page lets you upload packs and control which are active on the current world slot.

![Behaviour Pack Tracker](/images/behaviour-pack-tracker.png)

### Uploading Behaviour Packs
- Supported file types: **.mcpack** or **.zip**
- Maximum upload size: **25 MB** on Free plans or **50 MB** with Premium
- Drag-and-drop is supported, or click to upload.

### Enabled vs Disabled Packs
Behaviour Packs are organised into:
- **Enabled Behaviour Packs** - active on the world
- **Disabled Behaviour Packs** - available but not currently active

### Pack Priority (Order)
The Enabled list supports reordering:

- **Drag packs to reorder**
- Packs **higher** in the list have **higher priority**

This matters when multiple packs modify overlapping content.

### Management Actions
Depending on the pack entry controls, you can typically:
- remove/disable a pack from the enabled list
- delete a pack entry (where provided)

**Best practice:**
- Introduce packs one at a time and test after each change.
- Keep a record of pack versions used in production.
- If a pack conflicts with another, adjust priority first before removing.

---

## Resource Packs

Resource Packs affect presentation (textures, sounds, UI resources, and client-side assets). The Resource Packs page mirrors the Behaviour Packs workflow.

![Resource Pack Tracker](/images/resource-pack-tracker.png)

### Uploading Resource Packs
- Supported file types: **.mcpack** or **.zip**
- Maximum upload size: **25 MB** on Free plans or **50 MB** with Premium
- Drag-and-drop is supported, or click to upload.

### Enabled vs Disabled Packs
Resource Packs are organised into:
- **Enabled Resource Packs**
- **Disabled Resource Packs**

If no packs exist, you may see empty state messaging prompting you to enable packs from the disabled section.

**Best practice:**
- Use resource packs cautiously if you require consistent visual parity across players.
- If you enforce custom visuals, ensure your world/server settings align with your intended “texture pack required” behaviour.

---

## Safety and Operational Notes

- **Always download a backup** before replacing a world or making major pack changes.
- **Confirm the active slot** before uploading anything.
- If you run a public Realm, consider applying changes during quiet hours and communicating updates in advance.
- If something breaks after a change, revert by:
  - removing/disabling the most recent pack changes, or
  - restoring a known-good world backup where available.
