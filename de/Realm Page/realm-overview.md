---
label: Realm-Übersicht
description: Sieh dir den aktuellen Realm-Status, Plätze, Einstellungen und die letzten Aktivitäten auf einer einzigen Dashboard-Seite an, mit schnellem Zugriff auf die offizielle Realm-Verwaltung.
order: 100
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Realm-Übersicht

Die **Realm-Übersicht** bietet eine zusammengefasste Darstellung deines ausgewählten Minecraft Bedrock Realms. Sie wurde entwickelt, um Realm-Besitzern und Mitarbeitern einen schnellen, zuverlässigen Überblick zu geben über:

- Aktuellen Realm-Status und Mitgliedschaft
- Verfügbarkeit der Welt-Slots und die aktive Welt
- Grundlegende Welt- und Servereinstellungen (sofern verfügbar)
- Aktuelle Aktivitätsindikatoren für den operativen Überblick
- Einen direkten Link zur Verwaltung des Realms über die offiziellen Minecraft-Dienste

![Realm-Übersichtsseite](/images/realm-overview.png)

---

## Wofür diese Seite gedacht ist

Nutze diese Seite, um schnell zu überprüfen, dass:

- Du das **richtige Realm** verwaltest
- Das Realm derzeit **geöffnet/online** ist (Status wird in der Zusammenfassung angezeigt)
- Deine **Mitgliederzahl**, **Welt-Slots** und der **aktive Slot** wie erwartet aussehen
- Wichtige Einstellungen wie **Spielmodus**, **Schwierigkeitsgrad** und **PvP** mit deiner beabsichtigten Konfiguration übereinstimmen

Diese Seite ist als **operatives Übersichtspanel** gedacht, nicht als Ersatz für die tiefergehende Modulkonfiguration.

---

## Realm-Zusammenfassungskarte

Am oberen Rand der Seite zeigt die Realm-Zusammenfassungskarte übergeordnete Kennungen und Metadaten an, typischerweise einschließlich:

- **Realm-Name** (und interne Kennung, falls zutreffend)
- **Realm-Beschreibung** (falls gesetzt)
- **Mitgliederzahl** (Gesamtanzahl der dem Realm zugeordneten Mitglieder)
- **Verbleibende Zeit** des Abonnementzeitraums (falls verfügbar)
- **Erstellungsdatum** (Zeitstempel der Realm-Erstellung)

### Auf Minecraft verwalten
Die Schaltfläche **Manage on Minecraft.Net** leitet dich zum offiziellen Realm-Verwaltungsportal weiter. Dies ist nützlich für Änderungen, die über die offizielle Oberfläche vorgenommen werden müssen (zum Beispiel Abonnement- oder plattformseitige Verwaltungsaufgaben).

> **Hinweis:** Einige Realm-Einstellungen können nur über die offiziellen Minecraft-Verwaltungstools bearbeitet werden. Realm Bot zeigt Informationen an, aber nicht alle Änderungen können über das Dashboard vorgenommen werden.

---

## Schnellstatus-Karten

Direkt unter der Zusammenfassungskarte findest du Schnellstatus-Kacheln. Diese sind für eine schnelle Überprüfung während des Betriebs gedacht:

- **Realm-Status**  
  Zeigt an, ob das Realm derzeit geöffnet/verfügbar ist.

- **Gesamtmitglieder**  
  Zeigt die aktuelle Anzahl der dem Realm zugeordneten Mitglieder an.

- **Welt-Slots**  
  Zeigt an, wie viele Welt-Slots für das Realm verfügbar sind (Realms unterstützen in der Regel mehrere Slots).

- **Aktiver Slot**  
  Gibt an, welcher Welt-Slot derzeit aktiv ist (die Welt, die momentan vom Realm genutzt wird).

---

## Aktive Welt-Informationen

Der Abschnitt **Aktive Welt-Informationen** bietet eine strukturierte Übersicht der Einstellungen für die aktuell aktive Welt. Typische Felder umfassen:

### Welt-Einstellungen
- **Weltname**
- **Spielmodus** (zum Beispiel Survival oder Kreativ)
- **Schwierigkeitsgrad** (zum Beispiel Einfach / Normal / Schwer)
- **PvP**-Status (Aktiviert/Deaktiviert)

### Server-Einstellungen
- **Cheats**-Status (Erlaubt/Nicht erlaubt)
- **Texturpaket erforderlich** (Erzwungen/Nicht erzwungen), falls konfiguriert

> **Wichtig:** Die hier angezeigten Werte beziehen sich nur auf den **aktiven Slot**. Wenn du den aktiven Welt-Slot wechselst, können sich die angezeigten Werte entsprechend ändern.

---

## Letzte Aktivität

Das Panel **Letzte Aktivität** hebt aktuelle Teilnahmesignale hervor, damit Mitarbeiter schnell einschätzen können, ob das Realm aktiv war. Dies kann beinhalten:

- Kontoname (zum Beispiel ein Relay Account oder Dienstkonto)
- Gespielte Zeit oder Sitzungsdauer (sofern verfügbar)
- Aktualitätsindikator (z. B. „vor 2 Std.")

Dies dient in erster Linie dem operativen Kontext -- besonders bei der Koordination der Mitarbeiterabdeckung, der Untersuchung von Vorfällen oder der Bestätigung, dass dein Relay Account kürzlich online war.

---

## Fehlerbehebung und Hinweise

### Die Seite zeigt fehlende Daten oder sieht unvollständig aus
- Stelle sicher, dass das Realm korrekt verbunden und im Dashboard ausgewählt ist.
- Aktualisiere die Seite und überprüfe, ob die Kontoverknüpfung noch gültig ist.
- Einige Werte hängen davon ab, was die Plattform zum Zeitpunkt des Abrufs bereitstellt.

### Der Realm-Status sieht falsch aus
- Der Realm-Status kann leicht hinter Echtzeitänderungen hinterherhinken.
- Überprüfe den Status mit offiziellen Tools, wenn du einen aktiven Ausfall untersuchst.

### Werte stimmen nicht mit dem überein, was im Spiel erwartet wird
- Stelle sicher, dass du den **aktiven Welt-Slot** anschaust, den du überprüfen möchtest.
- Wenn du kürzlich Einstellungen geändert hast, warte, bis die Änderungen übernommen wurden, und aktualisiere die Seite.

---

## Verwandte Seiten

Wenn du deine Realm-Konfiguration einrichtest oder erweiterst, sind die folgenden Seiten typischerweise die nächsten Schritte:

- **Erste Schritte** (initiale Kontoverknüpfung und Verbindung)
- **Bot-Beitrittseinstellungen** (wie der Relay Account beitritt)
- **Gametest-Paketverwaltung** (erforderlich für bestimmte erweiterte Funktionen)
- **Realm-Module** (Chat Relay, Realm Console, Bot Detection, Member Gate, Skin Filtering, Leveling, Scoreboards, Live Playerlist, Vanity URL)
