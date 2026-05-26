---
label: Leveling System
description: Vergebe progressiv XP basierend auf Spielzeit, mit automatisch steigendem Schwierigkeitsgrad auf höheren Stufen und konfigurierbaren In-Game- und Discord-Stufenaufstiegs-Ankündigungen.
order: 20
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

### Was ist das Leveling System?

Das Leveling System ist ein Fortschrittsmodul, das Spielern **XP über die Zeit** basierend auf ihrer **In-Game-Spielzeit** verleiht. Wenn Spieler XP sammeln, steigen sie durch eine Kurve auf, die auf höheren Stufen natürlich anspruchsvoller wird. Dies stellt sicher, dass sich der frühe Fortschritt lohnend anfühlt, während der langfristige Fortschritt für engagierte Spieler bedeutsam bleibt.

### Wie XP und Stufen funktionieren

XP wird progressiv verliehen, solange Spieler im Spiel aktiv bleiben. Das System verwendet eine **Fortschrittskurve**, was bedeutet:

- Niedrigere Stufen werden schneller erreicht, um das Onboarding und frühes Engagement zu unterstützen.
- Höhere Stufen erfordern mehr XP, was schnellen Endgame-Fortschritt verhindert und den langfristigen Fortschritt wettbewerbsfähig hält.

Dies macht das Leveling System geeignet für:
- Langlebige Survival-Realms
- Wettbewerbsorientierte Communities, die einen konsistenten Grind suchen
- Staff-verwaltete Events, bei denen aktivitätsbasierte Belohnungen wichtig sind

### Stufenaufstiegs-Ankündigungen

Wenn ein Spieler aufsteigt, kann Realm Bot dies optional ankündigen:

- **Im Spiel** (Minecraft-Chat)
- **In Discord** (ein dedizierter Ankündigungskanal)

Beide Ankündigungsziele sind konfigurierbar, sodass du Stufenaufstiegsnachrichten sichtbar halten kannst, ohne das Gameplay oder den Staff-Betrieb zu stören.

### Benutzerdefinierte Stufenaufstiegs-Nachricht

Du kannst die Nachricht für Stufenaufstiegs-Ankündigungen anpassen. Die Nachricht unterstützt variable Platzhalter, die zur Laufzeit dynamisch ersetzt werden:

- `{user}` - der aktuelle Benutzername des Spielers
- `{level}` - die neue Stufe des Spielers
- `{rank}` - die Platzierung des Spielers im Vergleich zu anderen

Beispiel:

`Herzlichen Glückwunsch {user} zum Erreichen von Stufe {level}! Du bist jetzt auf Rang #{rank}.`

> **Hinweis:** Verwende Platzhalter genau wie gezeigt. Falsche Formatierung kann dazu führen, dass Variablen nicht wie erwartet ersetzt werden.

### Voraussetzungen

Um das Leveling System zu verwenden:
- Das Modul muss im Realm Bot Dashboard aktiviert sein.
- Spieler müssen aktiv im Realm spielen, um spielzeitbasiertes XP zu sammeln.

### Einrichtung

1.  Öffne das **Leveling System**-Modul im Realm Bot Dashboard.<br/>
    ![Leveling System Konfiguration](/images/leveling-system.png)
2.  Aktiviere den **Leveling System**-Schalter.
3.  (Optional) Wähle einen **Discord-Zielkanal** für Stufenaufstiegs-Ankündigungen.
4.  Wähle unter **Ankündigungseinstellungen**, ob **In-Game-Nachrichten senden** für Stufenaufstiege aktiviert werden soll.
5.  Bearbeite die **Benutzerdefinierte Stufenaufstiegs-Nachricht** passend zum Stil deiner Community, unter Verwendung von `{user}`, `{level}` und `{rank}` wo angemessen.

### Empfohlene Konfiguration

Für Community-Realms:
- Aktiviere **In-Game-Ankündigungen**, wenn Stufenaufstiege ein zentraler Bestandteil des Spielererlebnisses sind.
- Verwende einen dedizierten Discord-Kanal wie `#level-ups`, um die Sichtbarkeit zu erhalten, ohne den allgemeinen Chat zu überladen.

Für wettbewerbsorientierte oder Staff-intensive Realms:
- Erwäge, In-Game-Ankündigungen zu deaktivieren und nur Discord zu verwenden.
- Halte deine Nachricht kurz und konsistent, um Spam während Spitzenaktivität zu vermeiden.

### Betriebshinweise

- Das Leveling System ist darauf ausgelegt, nachhaltiges Engagement zu belohnen, anstatt kurze Spielphasen.
- Die Fortschrittskurve soll den langfristigen Wert aufrechterhalten; höhere Stufen sollten eine Errungenschaft bleiben.
- Wenn du von älteren Leveling-Daten migrierst, nutze die Dashboard-Migrationsoption, wo verfügbar, und vermeide es, Stufen zurückzusetzen, es sei denn, du beabsichtigst, den Fortschritt für den Realm vollständig neu zu starten.

### Datenaktionen und Sicherheit

Das Modul kann administrative Aktionen bereitstellen wie:
- **Daten migrieren** von einem früheren Leveling-System
- **Alle Benutzerstufen zurücksetzen** für den Realm

> **Warnung:** Zurücksetzungsaktionen sind in der Regel dauerhaft. Verwende Zurücksetzungen nur, wenn du deine Absicht bestätigt und die Änderung deiner Community im Voraus mitgeteilt hast.
