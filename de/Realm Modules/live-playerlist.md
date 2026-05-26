---
label: Live Playerlist
description: Veröffentliche eine automatisch aktualisierende Liste der online Realm-Spieler in einem Discord-Kanal, mit optionaler Spielzeit- und Geräteidentifikation.
order: 10
image: /images/custom/liveplayerlist.png
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Live Playerlist

Live Playerlist veröffentlicht eine nahezu in Echtzeit aktualisierte Ansicht, wer derzeit in deinem Realm online ist, in einem ausgewählten Discord-Kanal. Es ist für Staff-Bewusstsein und Community-Sichtbarkeit konzipiert und bietet eine konsistente "Wer ist online"-Referenz, ohne dass Spieler im Spiel sein müssen, um nachzuschauen.

Diese Funktion befindet sich unter **Realm-Module** und kann pro Realm aktiviert werden.

---

## Was Live Playerlist macht

Wenn aktiviert, wird Realm Bot:

- Eine Live-Liste der derzeit im Realm online befindlichen Spieler posten
- Die Ausgabe automatisch alle **5 Minuten** aktualisieren
- Eine einzelne Nachricht pflegen, die sich über die Zeit aktualisiert (wo von deiner Konfiguration unterstützt), um den Kanal sauber zu halten

Dies macht es geeignet für:
- Moderationsabdeckung (wissen, wann die Aktivität hoch ist)
- Event-Koordination (Anwesenheit bestätigen)
- Community-Engagement (Spieler können sehen, wer aktiv ist)

---

## Beispielausgabe

![Live Playerlist Beispiel](/images/live-playerlist-example.png)

Je nach Konfiguration kann die Spielerliste Folgendes enthalten:
- den Spielernamen (Gamertag)
- optionale Geräte-/Plattformindikatoren (z.B. Android, Windows)
- optionale aktuelle Sitzungsspielzeit

---

## Konfiguration

![Live Playerlist Konfiguration](/images/live-playerlist.png)

### Live Playerlist aktivieren

Verwende den Hauptschalter oben im Modul, um Live Playerlist für den ausgewählten Realm zu aktivieren oder zu deaktivieren.

### Discord-Zielkanal

Wähle den Discord-Kanal aus, in dem die Live Playerlist gepostet und aktualisiert wird.

Empfohlene Kanaloptionen:
- `#players-online`
- `#realm-status`
- `#realm-activity`

Stelle sicher, dass der Bot hat:
- **View Channel**
- **Send Messages**
- **Embed Links** (empfohlen für saubere Formatierung)

### Anzeigeeinstellungen

Du kannst steuern, welche Informationen neben jedem Spielereintrag angezeigt werden:

#### Spielzeit anzeigen

Wenn aktiviert, enthält die Spielerliste einen Spielzeitindikator, der anzeigt, wie lange der Spieler aktiv war (soweit von deiner Bereitstellung unterstützt).

Verwende dies, wenn du möchtest:
- klareren Staff-Kontext bei Vorfällen
- Sitzungssichtbarkeit für Aktivitätsüberwachung

#### Geräteidentifikation

Wenn aktiviert, zeigt die Spielerliste den Geräte-/Plattformindikator jedes Spielers an (wo erkennbar), wie z.B.:
- Android
- Windows
- Konsolenplattformen (wo unterstützt)

Verwende dies, wenn du möchtest:
- Plattformsichtbarkeit für Staff (besonders bei gerätebeschränkten Communities)
- schnelle Indikatoren bei der Untersuchung verdächtiger Beitrittsmuster

---

## Aktualisierungsintervall

Live Playerlist aktualisiert sich alle **5 Minuten**. Dieses Intervall ist darauf ausgelegt, ein Gleichgewicht zu finden zwischen:
- angemessen aktueller Sichtbarkeit
- minimalem Spam und betrieblichem Overhead
- vorhersehbarem Aktualisierungstiming für Staff

> **Hinweis:** Die Spielerliste ist "live" im betrieblichen Sinne (regelmäßige Aktualisierung), nicht sekundengenau.

---

## Empfohlene Vorgehensweise

- Verwende einen dedizierten Kanal und halte ihn rauscharm.
- Beschränke, wer im Zielkanal posten kann (optional), damit die Ausgabe leicht lesbar bleibt.
- Aktiviere **Geräteidentifikation**, wenn du plattformspezifische Regeln durchsetzt oder Wettbewerbsmodi betreibst, bei denen der Gerätekontext wichtig ist.
- Aktiviere **Spielzeit anzeigen**, wenn dein Staff-Workflow vom Sitzungskontext profitiert.

---

## Fehlerbehebung

### Die Spielerliste erscheint nicht

- Bestätige, dass Live Playerlist im Modul aktiviert ist.
- Bestätige, dass ein Discord-Zielkanal ausgewählt ist.
- Überprüfe die Berechtigungen: View Channel, Send Messages (und Embed Links falls erforderlich).
- Bestätige, dass der Realm verbunden ist und funktioniert.

### Die Spielerliste aktualisiert sich nicht

- Aktualisierungen erfolgen alle 5 Minuten; warte auf den nächsten Zyklus.
- Bestätige, dass der Bot online bleibt und Zugriff auf den Zielkanal hat.

### Geräte-/Spielzeitfelder fehlen

- Stelle sicher, dass die entsprechenden Anzeigeeinstellungs-Schalter aktiviert sind.
- Einige Felder können davon abhängen, welche Informationen zum Zeitpunkt der Aktualisierung vom Realm verfügbar sind.

---
