---
label: Befehlseinstellungen
description: Steuere, wie Realm Bot Spielerinformationen in Befehlen anzeigt, einschließlich einer kompakten Ansicht oder einer detaillierteren Ausgabe für Moderation und Prüfung.
order: 94
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Befehlseinstellungen

Die Seite **Befehlseinstellungen** steuert, wie Informationen in ausgewählten Realm Bot-Befehlen angezeigt werden. Dies wird hauptsächlich verwendet, um den Detailgrad anzupassen, der bei der Anzeige von Spielerinformationen in Discord gezeigt wird.

![Befehlseinstellungen](/images/server-command-settings.png)

---

## Anzeige von Spielerinformationen

Diese Einstellung ändert das Ausgabeformat, das in Befehlen wie:

- `/realm players`

verwendet wird.

Du kannst zwischen zwei Anzeigemodi wählen, je nachdem, wie dein Mitarbeiterteam moderiert und wie viel Information du im Befehl anzeigen möchtest.

### Kompakte Anzeige
Eine minimale Ausgabe für schnelle Überprüfungen.

Enthält typischerweise:
- Spieler-Benutzername
- Gerätetyp

**Empfohlen für:** schnelle Moderationsworkflows, kleinere Server oder Server, bei denen du sichtbare Spielermetadaten minimieren möchtest.

### Detaillierte Anzeige
Eine umfangreichere Ausgabe für Untersuchung und Verifizierung.

Enthält typischerweise:
- Spieler-Benutzername
- Gerätetyp
- Gamerscore
- Xbox Live-Status

**Empfohlen für:** größere Teams, öffentliche Server mit höherem Risiko oder Umgebungen, in denen Mitarbeiter routinemäßig die Legitimität und Aktivitätsmuster von Spielern überprüfen.

---

## Empfohlene Konfiguration

- Verwende die **kompakte Anzeige** für die tägliche Mitarbeiterarbeit, bei der Geschwindigkeit und Lesbarkeit am wichtigsten sind.
- Wechsle zur **detaillierten Anzeige**, wenn deine Moderation von zusätzlichen Identitäts-/Kontextsignalen abhängt (zum Beispiel Plattformmuster oder Kontoindikatoren).

> **Hinweis:** Diese Einstellung ändert, wie Informationen in Discord-Ausgaben dargestellt werden; sie ändert nicht, welche Aktionen der Bot ausführen kann.

---
