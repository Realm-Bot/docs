---
label: "/player lookup"
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Seif (Übersetzer)
    avatar: https://avatars.githubusercontent.com/u/126988925?s=96&v=4
---

# `/player lookup`

Zeigt Live-Daten über einen Spieler auf dem Realm an. Das beinhaltet sein Inventar, seinen Standort und sein Leben.

- **Erlaubnis**: Nur autorisierte Benutzer (Premium)
- **Nutzung**: `/player lookup <realm> <user>`

**Argumente**:
- `realm` (Erforderlich): Der Realm zum Überprüfen.
- `user` (Erforderlich): Der Spieler zum Nachschlagen.

**Antwort**:
- Leben & Spielmodus.
- Position (X, Y, Z) & Dimension.
- Spawnpunkt.
- Tags.
- **Inventar**: Rendert ein Bild des aktuellen Inventars.
