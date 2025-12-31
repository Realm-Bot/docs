---
label: "/realm ban"
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
---

# `/realm ban`

Bans a user from the Realm.

- **Permissions**: Authorized Users Only
- **Usage**: `/realm ban <user> [realm] [reason] [duration] [attachment] [silent]`

**Arguments**:
- `user` (Required): The player to ban. Supports name or XUID.
- `realm` (Optional): The realm to ban on. Defaults to all.
- `reason` (Optional): The reason for the ban.
- `duration` (Optional): Duration of the ban (e.g., "1d", "1h"). Defaults to Permanent.
- `attachment` (Optional): Proof for the ban (image/video).
- `silent` (Optional): If True, the ban will not be logged in the log channel.
