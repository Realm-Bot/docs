---
label: Übersicht
description: Ein zentraler Knotenpunkt zur Verwaltung deiner Realm-Verbindung, des Bot-Beitrittsverhaltens, der Gametest-Paketabhängigkeiten und aller verfügbaren Realm-Module.
order: 100
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Übersicht

Diese Seite dient als zentraler Verwaltungsknotenpunkt für deinen verbundenen Realm. Von hier aus kannst du auf die Kernkonfiguration deines Realms zugreifen, steuern, wie Realm Bot deiner Welt beitritt, Gametest-Paketabhängigkeiten verwalten (wo erforderlich) und alle aktivierten Premium-Module konfigurieren.

---

## Deinen Realm verwalten

Oben auf der Seite siehst du die Karte deines ausgewählten Realms. Dies ist der primäre Einstiegspunkt zur Verwaltung Realm-spezifischer Konfigurationen und zur schnellen Bestätigung, dass du am richtigen Realm arbeitest.

![Realm-Karte (Realm verwalten)](/images/overview-realm.png)

Verwende die Schaltfläche **Verwalten**, um die Verwaltungsansicht des Realms zu öffnen und auf die unten gezeigten Einstellungen zuzugreifen.

---

## Bot-Beitrittseinstellungen

Die Bot-Beitrittseinstellungen bestimmen, wie Realm Bot sich mit deinem Realm verbindet. Diese Optionen sind betriebliche Steuerungen und sollten mit Blick auf Zuverlässigkeit und Sicherheit konfiguriert werden.

![Bot-Beitrittseinstellungen](/images/overview-bot.png)

Wichtige Optionen umfassen:

- **Bot erlauben, dem Spiel beizutreten**  
  Erlaubt Realm Bot (über das Relay Account), deinem Realm beizutreten, wenn dies von Funktionen benötigt wird, die einen In-Game-Executor erfordern.

- **Beta-Beitritt verwenden**  
  Verwendet eine experimentelle Beitrittsmethode (deaktiviert die Standard-Beitrittsmethode). Dies sollte nur aktiviert werden, wenn du dazu aufgefordert wirst oder wenn der Standard-Beitritt in deiner Umgebung nicht zuverlässig funktioniert.

- **Bot erlauben, als alternatives Konto beizutreten**  
  Erlaubt Realm Bot, mit einem alternativen Konto beizutreten. Dies wird häufig verwendet, wenn dein primäres Relay Account für bestimmte Arbeitsabläufe reserviert bleiben muss oder wenn Redundanz erforderlich ist.

> **Wichtig:** Viele Module (zum Beispiel Chat Relay, Realm Console, Bot Detection, Member Gate und Skin Filtering) benötigen ein In-Game Relay Account, um Aktionen auszuführen. Wenn der Bot nicht im Spiel ist, funktionieren diese Module möglicherweise nicht.

---

## Gametest-Paketverwaltung

Die Gametest-Paketverwaltung steuert das Abhängigkeitspaket, das für erweiterte Realm-Funktionen verwendet wird, die In-Game-Skripting-Fähigkeiten erfordern. Wenn ein Modul auf das Gametest-Paket angewiesen ist, muss es installiert und aktiv sein.

![Gametest-Paketverwaltung](/images/overview-gametest.png)

Dieser Abschnitt umfasst:

- **Beta-API-Anforderung**  
  Einige Gametest-Funktionalitäten erfordern, dass **Beta-APIs** in deinen Realm-Einstellungen aktiviert sind. Wenn du dazu aufgefordert wirst, aktiviere **Beta-APIs verwenden** unter den experimentellen Funktionen deines Realms.

- **Gametest-Paket automatisch aktualisieren**  
  Aktualisiert das Paket automatisch, wenn neue Versionen verfügbar sind (empfohlen, wenn du minimalen Wartungsaufwand bevorzugst).

- **Paket-Aktionen**
  - **Paket installieren** - installiert das Abhängigkeitspaket im Realm
  - **Manueller Download** - bietet eine Download-Option für manuelle Bereitstellungsabläufe
  - **Nach Updates suchen** - prüft, ob eine neuere Paketversion verfügbar ist

> **Hinweis:** Wenn ein Modul nicht wie erwartet funktioniert und es von Gametest abhängt, überprüfe zuerst, ob das Paket installiert, aktiviert und aktuell ist.

---

## Realm-Module

Der Abschnitt Realm-Module enthält alle konfigurierbaren Funktionsmodule, die für deinen Realm verfügbar sind. Premium-Module sind deutlich gekennzeichnet und können direkt über **Konfigurieren** geöffnet werden.

![Realm-Module](/images/overview-realm-modules.png)

Von hier aus kannst du alle derzeit für deinen Realm verfügbaren Realm-Module konfigurieren:

- **Bot Detection** - Maßnahmen gegen bösartige Bot-Konten, einschließlich eines experimentellen Modus für strengere Erkennung
- **Chat Relay** - eine bidirektionale Chat-Brücke zwischen deinem Realm und Discord
- **Leveling System** - spielzeitbasierter XP-Fortschritt mit konfigurierbaren Stufenaufstiegs-Ankündigungen
- **Live Playerlist** - automatisches Veröffentlichen und Aktualisieren einer Discord-Ansicht, welche Spieler online sind
- **Member Gate** - regelbasierte automatische Moderation für Beitrittsbeschränkungen basierend auf Gerät, Gamerscore und sozialen Metriken
- **Realm Console** - Minecraft-Befehle über einen gesicherten Discord-Konsolenkanal ausführen
- **Scoreboard Leaderboards** - In-Game-Scoreboard-Ranglisten auf Discord veröffentlichen
- **Skin Filtering** - Spieler mit unregelmäßigen oder Exploit-orientierten Skins erkennen und entfernen
- **Vanity URL** - einen gebrandeten, stabilen Einladungslink für deinen Realm erstellen

Wenn du auch Monetarisierungstools verwendest, siehe die separate **Tebex**-Integrationsseite für die Store-Fulfillment-Einrichtung.

> **Betriebshinweis:** Beschränke den Zugriff auf Module mit hoher Auswirkung (wie Realm Console, Member Gate und Skin Filtering) auf vertrauenswürdige Administratoren. Diese Funktionen können direkt das Gameplay, den Spielerzugang und die Serverstabilität beeinflussen.

---

## Empfohlene Einrichtungsreihenfolge

Für beste Ergebnisse konfiguriere deinen Realm in der folgenden Reihenfolge:

1. Bestätige, dass du den richtigen Realm verwaltest (obere Karte).
2. Konfiguriere die **Bot-Beitrittseinstellungen**, um eine zuverlässige In-Game-Konnektivität sicherzustellen.
3. Falls erforderlich, installiere und überprüfe das **Gametest-Paket** (und aktiviere Beta-APIs, wo du dazu aufgefordert wirst).
4. Aktiviere und konfiguriere die Module, die du verwenden möchtest.

Diese Struktur stellt sicher, dass alle Abhängigkeiten vorhanden sind, bevor du dich operativ auf ein Modul verlässt.
