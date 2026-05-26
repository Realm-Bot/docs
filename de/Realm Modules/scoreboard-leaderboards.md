---
label: Scoreboard Leaderboards
description: Veröffentliche Live-Scoreboard-Ranglisten aus dem Spiel auf Discord, damit Spieler ihren Fortschritt verfolgen und durch automatisierte Leaderboard-Embeds gegeneinander antreten können.
order: 50
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

### Was sind Scoreboard Leaderboards?

Scoreboard Leaderboards ermöglichen es dir, eine Live-Rangliste für ein In-Game **Minecraft Scoreboard-Ziel** direkt in einem Discord-Kanal anzuzeigen. Dies ermöglicht Communities, Fortschritte zu verfolgen, Wettbewerb zu fördern und wichtige Statistiken sichtbar zu halten, ohne dass Spieler dem Realm beitreten müssen, um Ranglisten einzusehen.

Leaderboards werden als Discord-Embeds dargestellt und können pro Scoreboard und pro Kanal konfiguriert werden.

### Wie es funktioniert

Scoreboard Leaderboards funktionieren, indem ein ausgewähltes Scoreboard-Ziel aus deinem Realm ausgelesen und die Ergebnisse auf Discord veröffentlicht werden.

In der Praxis:
- Du wählst einen **Discord-Kanal**, in dem das Leaderboard gepostet wird.
- Du wählst das **Minecraft Scoreboard** (Ziel), das du anzeigen möchtest.
- Realm Bot ruft regelmäßig Scoreboard-Werte über die verbundene Realm-Umgebung ab und aktualisiert das Embed.

> **Wichtig:** Diese Funktion ist von der Realm-Laufzeitumgebung abhängig. Wenn die erforderlichen In-Game-Komponenten nicht aktiv sind, können Leaderboards nicht aktualisiert werden.

### Voraussetzungen

Scoreboard Leaderboards erfordern:

- Der **Relay Account** muss aktiv **im Spiel** sein.
- Das **Realm Bot Gametest Pack** muss im Realm installiert und aktiviert sein.
- Mindestens ein gültiges In-Game **Scoreboard-Ziel** muss vorhanden sein.

Wenn eine Voraussetzung fehlt (Relay Account offline, Pack deaktiviert oder Scoreboard nicht vorhanden), können Leaderboard-Aktualisierungen fehlschlagen oder keine Daten anzeigen.

### Einrichtung

1.  Öffne das **Scoreboard Leaderboards**-Modul im Realm Bot Dashboard und aktiviere es.<br/>
    ![Scoreboard Leaderboards Hauptseite](/images/scoreboard.png)
2.  Wähle **Leaderboard erstellen**.
3.  Konfiguriere das Leaderboard über das Erstellungsmenü.<br/>
    ![Scoreboard Leaderboard Erstellungsmenü](/images/scoreboard-definitions.png)
4.  Lege Folgendes fest:
    - **Kanal auswählen** - der Discord-Kanal, in dem das Leaderboard angezeigt werden soll.
    - **Minecraft Scoreboard** - das Scoreboard-Ziel, das veröffentlicht werden soll.
5.  (Optional) Passe das Embed-Erscheinungsbild an:
    - **Embed-Titel** - die Bezeichnung, die oben im Embed angezeigt wird.
    - **Embed-Farbe** - die Akzentfarbe, die für das Embed verwendet wird.
6.  Speichere die Leaderboard-Konfiguration.

Sobald erstellt, beginnt das Leaderboard mit der Aktualisierung im ausgewählten Kanal, wenn der Relay Account online und das Gametest Pack aktiv ist.

### Empfohlene Nutzung

Scoreboard Leaderboards sind ideal für:
- Fraktions-/Gefängnis-Fortschrittsmetriken
- Kills, Tode, K/D-Tracking (wo über Scoreboards implementiert)
- Event-Siege, Eroberungen oder Zielpunkte
- Währungs- oder Punktesysteme, die über Scoreboard-Ziele verfolgt werden

Betriebsempfehlungen:
- Verwende einen dedizierten Kanal wie `#leaderboards`, `#stats` oder `#rankings`.
- Halte ein Leaderboard pro Kanal, es sei denn, du hast ein strukturiertes Layout (mehrere Leaderboards in einem Kanal können schwer lesbar werden).
- Verwende klare Embed-Titel, die mit deinem Scoreboard-Zielnamen übereinstimmen (zum Beispiel: "Top Kills", "Top Guthaben", "Top Siege").

### Häufige Probleme

**Das Leaderboard zeigt keine Einträge**
- Bestätige, dass das ausgewählte Scoreboard-Ziel im Spiel existiert und Werte enthält.
- Stelle sicher, dass der Relay Account online im Realm ist.
- Überprüfe, ob das Realm Bot Gametest Pack installiert und aktiviert ist.

**Das Leaderboard wird nicht auf Discord gepostet**
- Bestätige, dass der Bot die Berechtigungen **Kanal anzeigen**, **Nachrichten senden** und **Links einbetten** im ausgewählten Kanal hat.
- Überprüfe, ob der richtige Kanal bei der Einrichtung ausgewählt wurde.

**Der Scoreboard-Name erscheint nicht im Dropdown-Menü**
- Das Scoreboard-Ziel wurde möglicherweise noch nicht im Spiel erstellt, oder die Umgebung ist nicht erkennbar, wenn das erforderliche Pack/Konto offline ist.
- Erstelle oder überprüfe das Scoreboard im Spiel, aktualisiere dann das Dashboard und versuche es erneut.

### Empfohlene Vorgehensweise

- Behandle Leaderboard-Kanäle nach Möglichkeit als schreibgeschützt, um die Ausgabe sauber zu halten.
- Standardisiere die Benennung von Scoreboard-Zielen im Spiel, um Verwirrung im Dashboard zu reduzieren.
- Wenn du Leaderboards für Wettbewerbe verwendest, stelle sicher, dass deine Scoreboard-Werte nicht trivial von Spielern manipuliert werden können.
