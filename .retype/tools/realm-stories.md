# Realm Stories

Realm Stories shares new posts from your Minecraft Realm's **Story Feed** in a selected Discord channel. It gives community members a way to follow player posts, screenshots, and supported Realm events without joining the game.

This is a **Realm Bot Premium** feature and is currently in **Beta**. Each Realm has its own configuration under **Tools > Realm Stories** in the dashboard.

---

## What Realm Stories Shares

Player posts can include the author's name and avatar, a short text preview, a screenshot when available, a timestamp, and the Realm name. Text previews are limited to approximately **300 characters**.

Supported Realm events use descriptive notifications and relevant artwork. The available event templates cover:

| Category | Supported events |
|---|---|
| Progression | First diamond, Nether portal, End portal, powered beacon, Netherite, and enchantment |
| Exploration | Discoveries of Mushroom Fields, Badlands, mountain peaks, abandoned mineshafts, Ancient Cities, Woodland Mansions, Pillager Outposts, and Nether Fortresses |
| Combat | First and subsequent Ender Dragon or Wither defeats, and Pillager Captain defeats |
| Realm and player moments | Realm creation, new members, and naming a mob |

Notifications identify the players involved when that information is available. Major events can include a large image; other events use a thumbnail.

> **Important:** Some event notifications include **coordinates**. Choose a destination channel whose audience is permitted to see discovery locations.

Realm Stories depends on the information Minecraft supplies through the Story Feed. Support for an event template does not guarantee that every matching in-game action will generate a post.

---

## Requirements

- An active Realm Bot Premium subscription recognised for the Realm owner.
- A linked Microsoft/Xbox account with access to the Realm.
- An available, open Realm for normal feed collection.
- A Discord text or announcement channel selected as the destination.
- **View Channel**, **Send Messages**, and **Embed Links** for Realm Bot in that channel.

Realm Stories does **not** require the Relay Account to be connected in-game, the GameTest Pack, or Beta APIs. An expired Microsoft/Xbox login can still interrupt access to the Story Feed.

---

## How to Set Up

1. Select your Discord server in the Realm Bot Dashboard.
2. Expand the intended Realm and open **Tools > Realm Stories**.
3. Enable **Live Feed**.
4. Select the **Discord Destination** channel.
5. Wait for the dashboard header to confirm the changes have saved.

Changes save automatically after approximately **1.5 seconds** without further edits. The header shows pending changes, saving progress, or an error with a **Retry** option.

Use a dedicated channel such as `#realm-stories` or `#realm-milestones` to keep the feed easy to follow.

---

## Update Timing

Despite the **Live Feed** label, Realm Stories normally checks for new posts every **15 minutes**. The first check is staggered and may also take approximately one interval.

The **first scan establishes a starting point and skips existing posts**. It does not import the Realm's previous Story Feed history. To test the feature, use posts created after that initial scan and allow another checking interval for delivery.

Xbox service delays, authentication errors, or Discord delivery failures can extend the wait. Queued notifications can survive service interruptions, and delivery retries preserve their order. Expired Premium pauses both collection and delivery.

---

## Controls and Limits

- Each Realm has one enable switch and one destination channel.
- There are no settings for event filtering, custom message designs, checking frequency, or importing old history.
- Changing the destination cancels pending deliveries addressed to the previous channel.
- Disabling Live Feed stops further delivery; it does not delete messages already posted in Discord.
- Replies in Discord do not create Minecraft Story Feed posts.
- Story notifications do not automatically mention staff roles or everyone.

---

## Best Practices

- Decide whether the feed should be public or restricted before enabling it, particularly when coordinates may be included.
- Keep routine conversation in a separate channel if it makes Story posts difficult to find.
- Allow the initial scan to complete before using new posts to test delivery.
- Check the dashboard's saved state before leaving the configuration page.

---

## Troubleshooting

### No stories appear

- Confirm **Live Feed** is enabled for the correct Realm and a destination is selected.
- Check that the configuration saved successfully; use **Retry** if the header reports an error.
- Allow time for the initial scan, then test with a new Story Feed post.
- Confirm Premium is active and the linked account still has access to the open Realm.
- Verify Realm Bot can view the destination and send messages with embeds.

### Posts are delayed or missing

- Allow for the normal 15-minute checking interval and any service interruption.
- Confirm the post exists in Minecraft's Story Feed; an in-game action alone may not produce one.
- Reconnect the linked Microsoft/Xbox account if authentication has expired.
- Check whether the destination changed while notifications were pending. Deliveries for the previous channel are cancelled.

### Older posts were not imported

The first scan deliberately skips existing history. There is no historical import control; test with a post created after the initial scan.

### Coordinates appear in a public channel

Restrict access to the destination or select a more appropriate channel. There is no event-filtering or message-customisation control for removing coordinates from individual notifications. Messages already posted remain in Discord until staff remove them.

---
