---
label: Erste Schritte
description: Verbinde dein Minecraft Bedrock Realm in drei Schritten mit Discord. Verknüpfe dein Microsoft-Konto, führe den Verbindungsbefehl aus und konfiguriere dann Module und Einstellungen.
icon: rocket
order: 101
authors:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Erste Schritte

Diese Anleitung führt dich durch den offiziellen Einrichtungsprozess, um dein Minecraft Bedrock Realm mit Discord über Realm Bot zu verbinden. Der Onboarding-Prozess ist darauf ausgelegt, in wenigen Minuten abgeschlossen zu werden, und ist in drei Phasen unterteilt:

1. **Microsoft-Konto verknüpfen**
2. **Discord-Befehl ausführen**
3. **Einstellungen konfigurieren**

![Übersicht Einrichtungsprozess](/images/getting-started-step-1.png)

---

## Bevor du beginnst

### 1) Lade Realm Bot auf deinen Discord-Server ein
Realm Bot muss auf deinem Discord-Server vorhanden sein, bevor du den Verbindungsbefehl ausführen kannst.

- Verwende den `/invite`-Befehl **oder** lade ein über: https://realmbot.dev/invite
- Erteile die erforderlichen Erlaubnisse. **Administrator** wird für den vollen Funktionsumfang empfohlen.

> **Wichtig:** Wenn Realm Bot keine Nachrichten senden oder Kanäle nicht lesen kann, in denen du Funktionen nutzen möchtest (Logs, Chat Relay, Bestenlisten), kann die Einrichtung zwar erfolgreich sein, aber die Module werden nicht korrekt funktionieren.

### 2) Stelle sicher, dass du den richtigen Zugang hast
Du solltest sein:
- Der Realm-Besitzer oder ein vertrauenswürdiger Administrator mit Zugriff auf die Realm-Verwaltung
- Ein Discord-Administrator (oder gleichwertig) auf dem Server, den du verbinden möchtest

---

## Schritt 1 - Microsoft-Konto verknüpfen

Realms werden über ein Microsoft/Xbox-Konto besessen und verwaltet. Realm Bot erfordert, dass du ein Microsoft-Konto verknüpfst, damit es deine verfügbaren Realms erkennen und verwalten kann.

1. Gehe zum Dashboard: https://dashboard.realmbot.dev
2. Melde dich mit Discord an.
3. Wähle **Microsoft-Konto verbinden**, um dein Microsoft/Xbox-Konto zu verknüpfen.

![Microsoft-Konto verbinden](/images/getting-started-step-1.png)

> **Sicherheitshinweis:** Verknüpfe nur ein Konto, dem du vertraust, das Realm zu administrieren. Behandle die Kontoverknüpfung als privilegierten Zugang.

---

## Schritt 2 - Discord-Verbindungsbefehl ausführen

Nachdem dein Microsoft-Konto verknüpft ist, besteht der nächste Schritt darin, dieses Konto mit dem richtigen Discord-Server zu verbinden.

1. Öffne den Discord-Server, den du verbinden möchtest.
2. Führe den folgenden Befehl in einem beliebigen Kanal aus, in dem Realm Bot antworten kann:

`/connect`

![Discord-Befehl ausführen](/images/getting-started-step-2.png)

### Was `/connect` bewirkt
- Verifiziert dein verknüpftes Microsoft-Konto
- Verknüpft den aktuellen Discord-Server mit deinem Realm-Verwaltungskontext
- Ermöglicht dem Dashboard, Realm-spezifische Einstellungen und Module zu laden und zu konfigurieren

> **Tipp:** Wenn du mehrere Server verwaltest, stelle sicher, dass du `/connect` zuerst im richtigen Server ausführst. Du kannst den Prozess bei Bedarf pro Server wiederholen.

---

## Schritt 3 - Realm-Einstellungen konfigurieren

Sobald deine Verbindung hergestellt ist, kannst du dein Realm über das Dashboard und die entsprechenden Modulseiten konfigurieren.

Empfohlene Konfigurationsreihenfolge:

1. **Wähle dein Realm** (falls aufgefordert)
2. Überprüfe die **Bot-Beitrittseinstellungen** (wie der Relay/Bot sich verbindet)
3. Konfiguriere die **Gametest-Paketverwaltung** (nur wenn von deinen Modulen benötigt)
4. Aktiviere und konfiguriere alle **Realm-Module**, die du nutzen möchtest:
   - Chat Relay
   - Realm Console
   - Bot Detection
   - Member Gate
   - Skin Filtering
   - Leveling
   - Scoreboard Leaderboards
   - (Optional) Tebex-Integration

Du kannst jederzeit die Befehlshilfe in Discord aufrufen:
- `/help`

---

## Häufige Probleme

### „Ich kann meine Realms im Dashboard nicht sehen."
- Bestätige, dass du das richtige Microsoft/Xbox-Konto verknüpft hast.
- Stelle sicher, dass das Konto tatsächlich die Realms besitzt (oder Zugriff darauf hat), die du erwartest.
- Öffne das Dashboard erneut und aktualisiere es nach der Verknüpfung.

### `/connect` macht nichts oder schlägt fehl.
Überprüfe Folgendes:
- Realm Bot ist auf dem Server eingeladen und online.
- Du führst `/connect` in einem Serverkanal aus, in dem der Bot die Erlaubnis hat zu antworten.
- Deine Rolle hat ausreichende Erlaubnisse, um Verwaltungsbefehle auszuführen (Server-Admin empfohlen).

### Xbox/Microsoft-Datenschutz blockiert die Verknüpfung oder den Zugriff.
Wenn die Verknüpfung oder der Realm-Zugriff fehlschlägt, überprüfe deine Xbox-Datenschutzeinstellungen, um sicherzustellen, dass externe Dienste korrekt funktionieren können.

> **Wichtig:** Datenschutzeinstellungen können verhindern, dass Anwendungen auf erforderliche Profil-/Realm-Daten zugreifen. Wenn die Probleme weiterhin bestehen, passe die entsprechenden Xbox-Datenschutzoptionen an und versuche die Verknüpfung erneut.

---

## Nächste Schritte

Sobald die Einrichtung abgeschlossen ist, fahre mit der **Übersichtsseite** fort, um mehr zu erfahren.
