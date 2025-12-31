---
label: "/player lookup"
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
---

# `/player lookup`

Look up live data about a player on the Realm. This includes their inventory, location, and health.

- **Permissions**: Authorized Users Only (Premium)
- **Usage**: `/player lookup <realm> <user>`

**Arguments**:
- `realm` (Required): The realm to check.
- `user` (Required): The player to lookup.

**Response**:
- Health & Gamemode.
- Position (X, Y, Z) & Dimension.
- Spawn Point.
- Tags.
- **Inventory**: Renders an image of their current inventory.
