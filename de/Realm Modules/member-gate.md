---
label: Member Gate
description: Kicke oder banne beitretende Spieler automatisch basierend auf Xbox-Profilsignalen - wie Geräteplattform, Gamerscore und sozialen Metriken - um strenge Zugangsstandards durchzusetzen.
order: 60
image: /images/custom/membergate.png
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

### Was ist Member Gate?

Member Gate ist ein **automatisiertes Zugangsmoderierungssystem**, das Spieler beim Beitritt zu deinem Realm bewertet und eine Aktion anwendet - typischerweise **Kick** oder **Bann** - basierend auf von dir definierten Regeln. Es ist für Realm-Besitzer konzipiert, die eine strengere Zugangskontrolle benötigen, als Einladungscodes allein bieten können, insbesondere für öffentliche oder halböffentliche Realms.

Member Gate ist besonders effektiv für Realms, die das Gameplay auf bestimmte Spielertypen beschränken möchten (zum Beispiel ein **Konsolen-exklusiver PvP-Realm**) oder für Communities, die eine grundlegende automatisierte Filterung für verdächtige Beitrittsmuster benötigen.

### Wie Member Gate funktioniert

Member Gate arbeitet mit regelbasierter Logik:

- Du erstellst eine oder mehrere **Moderationsregeln** im Dashboard.
- Jede Regel enthält:
  - Eine **Moderationsaktion** (Kick oder Bann)
  - Eine oder mehrere **Bedingungen**
- Wenn ein Spieler beitritt, überprüft Member Gate jede Regel.
- Wenn ein Spieler die Bedingungen der Regel erfüllt, wird die konfigurierte Aktion ausgeführt.

> **Wichtig:** Member Gate erfordert, dass das **Relay Account** **im Spiel** ist, um Kicks/Banns auszuführen. Wenn das Relay Account nicht im Realm online ist, kann Member Gate keine Regeln durchsetzen.

### Bedingungen, die du verwenden kannst

Member Gate unterstützt mehrere Bedingungstypen, die eine flexible Regelkonstruktion ermöglichen. Regeln können **jede Kombination** unterstützter Bedingungen enthalten und sind dazu gedacht, basierend auf den Anforderungen deines Realms konfiguriert zu werden.

Häufige Bedingungskategorien umfassen:

- **Geräteplattform**
  - Gerät einschließen
  - Gerät ausschließen

- **Gamerscore-Schwellenwerte**
  - Gamerscore größer als
  - Gamerscore kleiner als

- **Soziale Metriken**
  - Follower größer als / kleiner als
  - Following größer als / kleiner als

> **Regellogik:** Innerhalb einer einzelnen Regel müssen **alle Bedingungen erfüllt sein**, damit die Aktion ausgeführt wird. Wenn eine Bedingung nicht erfüllt ist, wird die Regel nicht ausgelöst.

### Unterstützte Geräteplattformen

Gerätebasierte Regeln können verwendet werden, um plattformspezifische Realms durchzusetzen. Unterstützte Plattformen umfassen:

- Android
- iOS
- Windows
- Xbox
- PlayStation
- Nintendo

Dies macht Member Gate geeignet für Anwendungsfälle wie:
- Konsolen-exklusives PvP
- Nur-Mobilgerät-Casual-Realms
- Einschränkung von Windows-Beitritten während gezielter Missbrauchsperioden

### Voraussetzungen

Um Member Gate effektiv zu nutzen, stelle sicher, dass Folgendes vorhanden ist:

- Der Realm ist über den autorisierten Verknüpfungsablauf mit Realm Bot verbunden
- Das **Relay Account ist aktiv im Spiel**
- Ein Discord-Kanal ist ausgewählt, um Durchsetzungsprotokolle zu empfangen (empfohlen)

### Einrichtung

1.  Öffne das **Member Gate**-Modul im Realm Bot Dashboard.<br/>
    ![Member Gate Konfiguration](/images/member-gate.png)
2.  Aktiviere **Member Gate** mit dem Hauptschalter.
3.  Lege den **Discord-Zielkanal** fest.
    - Kick- und Bann-Aktionen werden zur Überprüfung und Fehlerbehebung in diesem Kanal protokolliert.
4.  Erstelle unter **Moderationsregeln** eine Regel:
    - Gib einen kurzen, klaren Regelnamen an (zum Beispiel: `Console Only` oder `Block Low Gamerscore`).
    - Wähle die **Moderationsaktion**: **Kick** oder **Bann**.
    - Füge eine oder mehrere **Bedingungen** hinzu und konfiguriere deren Werte.
5.  Bestätige, dass dein Relay Account **im Realm online** ist, und teste dann, indem du mit einem erlaubten Konto und (wenn möglich) einem nicht erlaubten Konto beitrittst.

### Empfohlener Konfigurationsansatz

Um Störungen zu reduzieren und versehentliche Überregulierung zu vermeiden:

- Beginne mit **Kick** statt Bann, während du die Bedingungen abstimmst.
- Füge Regeln schrittweise hinzu und überwache die Ergebnisse über deine Discord-Zielkanal-Protokolle.
- Bevorzuge Geräteregeln für "harte" Einschränkungen (z.B. Konsolen-exklusiv) und Schwellenwertregeln für "weiche" Filterung (z.B. verdächtige Profile).

### Beispiel-Regelmuster

**Konsolen-exklusiver Realm**
- Aktion: **Kick**
- Bedingungen:
  - Gerät ausschließen: Android, iOS, Windows

**Konten mit niedrigem Signal filtern**
- Aktion: **Kick**
- Bedingungen:
  - Gamerscore kleiner als: *dein gewählter Schwellenwert*
  - Follower kleiner als: *dein gewählter Schwellenwert*

**Hochvertrauens-Zugang**
- Aktion: **Kick** oder **Bann** (mit Vorsicht verwenden)
- Bedingungen:
  - Gamerscore größer als: *Schwellenwert*
  - Follower größer als: *Schwellenwert*

> **Hinweis:** Soziale und Gamerscore-Schwellenwerte können je nach Community-Demografie falsch-positive Ergebnisse liefern (neue Spieler, alternative Konten, Datenschutzeinstellungen usw.). Verwende konservative Schwellenwerte und iteriere.

### Empfohlene Vorgehensweise

- Beschränke, wer Member Gate-Einstellungen in deiner Staff-Struktur ändern kann.
- Verwende einen dedizierten Discord-Protokollkanal wie `#automod-logs`.
- Veröffentliche klare Zugangserwartungen für Spieler, wenn du strenge Plattform- oder Profilanforderungen durchsetzt.
- Halte einen einfachen Einspruchsweg bereit, falls ein legitimer Spieler durch die Automatisierung entfernt wird.

### Häufige Probleme

**Member Gate ist aktiviert, aber es werden keine Aktionen ausgeführt**
- Bestätige, dass das **Relay Account im Spiel** ist.
- Überprüfe, ob der richtige Realm im Dashboard ausgewählt ist.
- Stelle sicher, dass Regeln erstellt und gespeichert sind (und nicht leer sind).
- Überprüfe den Discord-Zielkanal auf Durchsetzungsnachrichten.

**Legitime Spieler werden entfernt**
- Senke die Strenge der Gamerscore-/Follower-Schwellenwerte.
- Wechsle von **Bann** zu **Kick** während der Abstimmung.
- Bevorzuge reine Gerätebeschränkungen, wenn dein Ziel die Plattformtrennung ist, anstatt Profilfilterung.
