---
label: Erlaubnis
description: Steuere, welche Discord-Rollen bestimmte Realm Bot-Befehle verwenden können, indem du detaillierte Erlaubnis pro Rolle zuweist.
order: 93
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Erlaubnis

Die Seite **Erlaubnis** ermöglicht es dir, genau zu steuern, welche **Discord-Rollen** die Befehle von Realm Bot verwenden können. Erlaubnis wird auf **Rollenebene** vergeben, d. h. jedes Mitglied mit dieser Rolle erhält den konfigurierten Zugang sofort.

Dies ist die empfohlene Methode, um die versehentliche Nutzung von Befehlen mit großer Auswirkung (z. B. Banns, Realm-Code-Änderungen, Welt-Aktionen) zu verhindern und gleichzeitig dem Team die Durchführung routinemäßiger Moderation zu ermöglichen.

![Rollen-Erlaubnis Übersicht](/images/server-permissions-roles.png)

---

## Wie das Erlaubnis-System funktioniert

Realm Bot-Erlaubnis ist:

- **Rollenbasiert**: Erlaubnis wird Discord-Rollen zugewiesen, nicht einzelnen Benutzern
- **Detailliert**: Du kannst den Zugang zu bestimmten Befehlsgruppen und Aktionen erlauben oder verweigern
- **Sofort wirksam**: Änderungen gelten, sobald du sie speicherst, und betreffen alle Mitglieder mit dieser Rolle

> **Wichtig:** Deine Discord-Berechtigungen (Administrator, Server verwalten usw.) werden nicht automatisch auf Realm Bot-Erlaubnis übertragen. Du musst den Zugang hier explizit gewähren.

---

## Rollen-Erlaubnis verwalten

### 1) Eine Rolle auswählen
Suche in **Rollen-Erlaubnis verwalten** die Rolle, die du konfigurieren möchtest. Du kannst die Suchleiste verwenden, wenn du viele Rollen hast.

Jede Rollenkarte zeigt an, ob derzeit Realm Bot-Erlaubnis zugewiesen ist.

### 2) Die Rolle bearbeiten
Wähle das Bearbeiten-Symbol auf der Rollenkarte, um die Erlaubnis-Konfiguration dieser Rolle zu öffnen.

---

## Erlaubnis-Kategorien

Erlaubnis ist nach Funktionsbereichen gruppiert. Beim Bearbeiten einer Rolle siehst du Kategorien wie:

- **Realm** (Einladungen, Kicks/Banns, Realm-Code, Öffnen/Schließen, Slots, Spieler, Backups)
- **World** (Ausführen, Broadcast, Beitreten/Verlassen, Live-Aktionen)
- **Warn** (Verwarnungen hinzufügen/nachschlagen/entfernen)
- **Allowlist** (Allowlist-Einträge hinzufügen/prüfen/auflisten/entfernen)
- **Player** (Nachschlagen und Spieler-Infobefehle)
- **Verify** (Verifizierungs-/Embed- oder Onboarding-Dienstprogramme)
- **Banlist** (Banneinträge nachschlagen oder auflisten, sofern unterstützt)

Jede Kategorie enthält eine **Alle auswählen**-Option, um schnell alle Berechtigungen in diesem Abschnitt zu gewähren – verwende dies mit Vorsicht.

![Rollen-Erlaubnis Editor](/images/server-permissions-settings.png)

---

## Empfohlenes Rollenmodell (Empfohlene Vorgehensweise)

Eine saubere Erlaubnis-Struktur reduziert Fehler und sorgt für klare Verantwortlichkeiten. Ein typisches Setup sieht so aus:

### Besitzer / Hauptadministrator
Vergib volle Erlaubnis, einschließlich:
- Realm-Code-Änderungen
- Bann/Entbannung
- World Execute
- Backup-/Weltersetzungs-Tools (falls vorhanden)
- Erlaubnis-Bearbeitung selbst (falls verfügbar)

### Leitende Mitarbeiter / Manager
Vergib operative Moderation + Verwaltung, aber beschränke Aktionen mit hohem Risiko:
- Kick/Bann/Entbannung (optional)
- Spieler-Nachschlagen, Realm-Spieler, Letzte Aktivitäten
- Verwarnungs- und Allowlist-Verwaltung
- Eingeschränkte Welt-Aktionen bei Bedarf (Broadcast/Live), vermeide `World Execute`, sofern nicht voll vertrauenswürdig

### Moderatoren
Vergib nur routinemäßige Moderation:
- Kick (optional)
- Verwarnung hinzufügen/nachschlagen/entfernen
- Spieler-Nachschlagen
- Allowlist prüfen/auflisten
- Realm-Spieler anzeigen

### Support / Helfer
Minimaler Zugang:
- Spieler-Nachschlagen
- Allowlist prüfen/auflisten
- Verify-Tools (falls dein Server sie nutzt)
- Kein Kick/Bann und keine Realm-Verwaltung

> **Sicherheitsrichtlinie:** Behandle `World Execute` und Realm-Code-Verwaltung als **hohes Risiko**. Vergib diese nur an vertrauenswürdige Administratoren.

---

## Häufige Fehlkonfigurationen

### „Teammitglieder können Befehle nicht verwenden, die sie haben sollten"
- Bestätige, dass die richtige Rolle bearbeitet wurde (viele Server haben ähnlich benannte Rollen).
- Stelle sicher, dass der Benutzer diese Rolle tatsächlich in Discord hat.
- Überprüfe, ob du die spezifische Erlaubnis aktiviert hast (z. B. `Realm Kick` ist getrennt von `Realm Ban`).

### „Zu viele Personen können gefährliche Befehle ausführen"
- Entferne die Nutzung von **Alle auswählen** für breite Kategorien.
- Erstelle eine dedizierte „Technischer Admin"-Rolle für Erlaubnis mit großer Auswirkung.
- Trenne Moderation (Verwarnung/Kick) von Infrastruktursteuerung (Code-Änderung/Ausführen).

---

## Operative Tipps

- Halte die Erlaubnis-Sätze **so klein wie möglich** pro Rolle.
- Verwende Rollen statt Einzelpersonen, um „Einmal-Ausnahmen" zu vermeiden, die später vergessen werden.
- Überprüfe deine Erlaubnis nach Personaländerungen oder größeren Server-Umstrukturierungen.
- Wenn du automatisierte Onboarding-Rollen verwendest, stelle sicher, dass neue Mitglieder **nicht** versehentlich Team-Erlaubnis erben.

---
