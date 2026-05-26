---
label: Server-Einrichtung
description: Schließe die empfohlene Einrichtungscheckliste für deinen Discord-Server ab, einschließlich Protokollierung, Erlaubnis, Verwarnungsvoreinstellungen und Kontoverknüpfung.
order: 99
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Server-Einrichtung

Die Seite **Server-Einrichtung** ist eine geführte Checkliste, die dir hilft, die wesentlichen serverweiten Einstellungen zu konfigurieren, die für einen sauberen und sicheren Betrieb von Realm Bot erforderlich sind. Sie bietet einen klaren Fortschrittsindikator und direkte Links zu jedem Konfigurationsbereich.

![Server-Einrichtungsseite](/images/server-setup.png)

---

## Was die Server-Einrichtung bewirkt

Die Server-Einrichtung fasst die Kernkonfiguration an einem Ort zusammen, damit du:

- Bestätigen kannst, dass die minimal erforderlichen Einstellungen vorhanden sind
- Prüfungs- und Moderationsgrundlagen einrichten kannst, bevor du erweiterte Module aktivierst
- Fehlkonfigurationen reduzieren kannst (fehlende Protokolle, falsche Erlaubnis, unvollständige Verknüpfungen)
- Einstellungen jederzeit überprüfen kannst, wenn sich deine Mitarbeiterstruktur weiterentwickelt

---

## Einrichtungsfortschritt

Oben auf der Seite siehst du einen **Einrichtungsfortschritt**-Balken, der anzeigt, wie viele Schritte abgeschlossen sind (zum Beispiel **3 von 4 Schritten abgeschlossen**). Jeder Schritt wird als Karte mit einer kurzen Beschreibung und einer Aktionsschaltfläche angezeigt.

Statusanzeigen erscheinen typischerweise als:
- **Abgeschlossen** (Häkchen) - der Schritt wurde konfiguriert
- **Unvollständig** (ausstehendes Symbol) - der Schritt erfordert noch Einrichtung
- **Überprüfen** - der Schritt ist abgeschlossen und kann überprüft werden
- **Konfigurieren** - der Schritt erfordert eine Aktion

---

## Einrichtungsschritte

### 1) Protokollierung
Die Protokollierung ist das Prüfungsfundament deiner Serverkonfiguration. Sie stellt sicher, dass Mitarbeiteraktionen und automatisierte Ereignisse bei der Untersuchung von Vorfällen überprüft werden können.

Verwende diesen Schritt, um:
- Geeignete Protokollkanäle auszuwählen
- Sicherzustellen, dass der Bot in diese Kanäle posten kann
- Eine Trennung zwischen Moderationsprotokollen und allgemeinen Aktivitätsprotokollen zu schaffen (empfohlen)

**Empfohlene Vorgehensweise:** Halte Protokollkanäle nur für Mitarbeiter zugänglich und frei von unnötigem Rauschen, um das Signal-Rausch-Verhältnis zu bewahren.

---

### 2) Erlaubnis
Die Erlaubnis bestimmt, wer auf Serverfunktionen zugreifen kann und wer wirkungsvolle Änderungen vornehmen darf.

Verwende diesen Schritt, um:
- Verwaltungszugriff nur vertrauenswürdigen Rollen zuzuweisen
- Konfigurationszugriff (Dashboard und sensible Module) einzuschränken
- Versehentlichen Missbrauch durch allgemeine Mitarbeiter oder Mitglieder zu verhindern

**Empfohlene Vorgehensweise:** Wende das Prinzip der geringsten Berechtigung an. Beginne streng und erweitere den Zugriff dann gezielt.

---

### 3) Verwarnungseinstellungen
Verwarnungseinstellungen ermöglichen es dir, voreingestelltes Verwarnungsverhalten für Administratoren und Moderatoren zu konfigurieren. Dies sorgt für einheitliche Disziplinarmaßnahmen und reduziert Mehrdeutigkeiten unter den Mitarbeitern.

Verwende diesen Schritt, um:
- Deine Standard-Verwarnungsvoreinstellung(en) zu konfigurieren
- Verwarnungsmaßnahmen an deine Serverregeln anzupassen
- Sicherzustellen, dass Moderatoren nach den gleichen Standards arbeiten

> **Betrieblicher Hinweis:** Wenn du eine öffentliche Community betreibst, reduzieren einheitliche Verwarnungsrichtlinien Streitigkeiten und verbessern die Koordination der Mitarbeiter.

---

### 4) Kontoverknüpfung
Die Kontoverknüpfung verbindet deine Betriebsidentität mit Realm Bot, damit der Bot Mitglieder zuverlässig verifizieren und deinen Server mit dem richtigen Realm-Zugriffskontext verbinden kann.

Verwende diesen Schritt, um:
- Zu bestätigen, dass die Verknüpfungsprozesse abgeschlossen sind
- Sicherzustellen, dass die richtigen Discord- und Microsoft/Xbox-Konten verbunden sind
- Workflows zu aktivieren, die auf verifizierter Identität und Realm-Zugriff basieren

**Empfohlene Vorgehensweise:** Verknüpfe nur vertrauenswürdige administrative Konten. Behandle die Verknüpfung als privilegierten Zugriff.

---

## Empfohlene Reihenfolge

Obwohl die Server-Einrichtung flexibel ist, lautet die empfohlene Reihenfolge:

1. **Protokollierung** (zuerst die Prüfung)
2. **Erlaubnis** (Zugriff kontrollieren)
3. **Verwarnungseinstellungen** (Moderationsworkflow standardisieren)
4. **Kontoverknüpfung** (Identität + Realm-Zugriffsabläufe abschließen)

Diese Reihenfolge stellt sicher, dass der Server sicher und prüfbar ist, bevor erweiterte Funktionen aktiviert werden.

---

## Fehlerbehebung

### Ein Schritt wird nach der Konfiguration als unvollständig angezeigt
- Öffne den Schritt erneut und bestätige, dass du die Änderungen gespeichert hast.
- Stelle sicher, dass Realm Bot die erforderlichen Discord-Berechtigungen für die Funktion hat (insbesondere für die Protokollierung).
- Aktualisiere das Dashboard, um zu bestätigen, dass sich der Status aktualisiert.

### Überprüfungsschaltflächen funktionieren, aber Module schlagen trotzdem fehl
Die Server-Einrichtung deckt die grundlegende Konfiguration ab. Einige Realm-Module erfordern zusätzlich:
- Realm-spezifische Konfiguration (innerhalb des Realm-Dashboards)
- Ein Relay Account, das im Spiel aktiv ist (für bestimmte Module)
- Gametest Pack-Abhängigkeiten (für erweiterte Realm-Funktionen)

---
