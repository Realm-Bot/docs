---
label: Weltverwaltung
description: Verwalte den aktiven Welt-Slot deines Realms, lade Backups herunter, ersetze Welten und steuere Behaviour/Resource Packs (einschließlich Upload, Aktivieren/Deaktivieren und Pack-Priorität).
order: 12
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Weltverwaltung

Der Bereich **Weltverwaltung** ermöglicht es dir, die Dateien und Konfigurationen zu verwalten, die mit den Welten deines Realms verknüpft sind. Er ist in vier Abschnitte unterteilt:

1. **Welt-Slot** - wähle aus, welchen der Welt-Slots deines Realms du verwaltest  
2. **Welt** - lade ein Backup herunter und ersetze die aktive Weltdatei  
3. **Behaviour Packs** - lade Behaviour Packs für die aktive Welt hoch und verwalte sie  
4. **Resource Packs** - lade Resource Packs für die aktive Welt hoch und verwalte sie  

![Weltverwaltungs-Abschnitte](/images/world-management.png)

> **Wichtig:** Alle Aktionen in der Weltverwaltung gelten für den **aktuell ausgewählten Welt-Slot**. Stelle immer sicher, dass du den richtigen Slot bearbeitest, bevor du etwas hochlädst, ersetzt oder die Pack-Reihenfolge änderst.

---

## Welt-Slot

Realms bieten in der Regel mehrere Welt-Slots. Der **Welt-Slot**-Selektor ermöglicht es dir, zwischen Slots zu wechseln und jeden Slot unabhängig zu verwalten.

![Welt-Slot-Selektor](/images/world-slot.png)

Typische Nutzung:
- Wähle den Slot aus, den du verwalten möchtest (z. B. Slot 1, Slot 2, Slot 3).
- Bestätige den Slot-Namen und den Spielmodus (z. B. Survival, Adventure) bevor du Änderungen vornimmst.

**Empfohlene Vorgehensweise:** Behandle Welt-Slots als separate Umgebungen. Halte mindestens einen Slot für Backups/Tests reserviert, wenn es dein Workflow erlaubt.

---

## Welt

Der Abschnitt **Welt** wird für Backups und den Weltersatz auf dem aktiven Slot verwendet.

![Weltseite](/images/world-page.png)

### Welt herunterladen (Backup)
Verwende **Welt herunterladen**, um die aktuelle Welt aus dem ausgewählten Slot zu exportieren.

Dies wird dringend empfohlen, bevor du:
- die Welt ersetzt
- umfangreiche Packs installierst
- größere Gameplay-Änderungen vornimmst, die einen Rollback erfordern könnten

### Welt ersetzen
Mit Welt ersetzen kannst du eine neue Weltdatei in den aktiven Slot hochladen.

- Unterstützter Dateityp: **.mcworld**
- Maximale Dateigröße: **100MB** (wie im Uploader angezeigt)

> **Warnung:** Das Ersetzen der Welt löscht die aktuelle Welt für diesen Slot dauerhaft. Lade zuerst ein Backup herunter, um den Verlust von Fortschritten zu vermeiden.

Operative Hinweise:
- Ersetze Welten nur während Zeiten geringer Aktivität.
- Kündige Ausfallzeiten gegenüber Mitarbeitern/Spielern an, wenn das Realm während des Wechsels nicht verfügbar sein wird.
- Stelle sicher, dass der richtige Slot ausgewählt ist, bevor du etwas hochlädst.

---

## Behaviour Packs

Behaviour Packs ändern die Spiellogik und das Verhalten (Systeme, Mechaniken, Regelwerke, Entities usw.). Diese Seite ermöglicht es dir, Packs hochzuladen und zu steuern, welche auf dem aktuellen Welt-Slot aktiv sind.

![Behaviour Pack Tracker](/images/behaviour-pack-tracker.png)

### Behaviour Packs hochladen
- Unterstützte Dateitypen: **.mcpack** oder **.zip**
- Drag-and-Drop wird unterstützt, oder klicke zum Hochladen.

### Aktivierte vs. deaktivierte Packs
Behaviour Packs sind unterteilt in:
- **Aktivierte Behaviour Packs** - auf der Welt aktiv
- **Deaktivierte Behaviour Packs** - verfügbar, aber derzeit nicht aktiv

### Pack-Priorität (Reihenfolge)
Die Liste der aktivierten Packs unterstützt Neuanordnung:

- **Ziehe Packs, um sie neu zu ordnen**
- Packs **weiter oben** in der Liste haben **höhere Priorität**

Dies ist wichtig, wenn mehrere Packs überlappende Inhalte ändern.

### Verwaltungsaktionen
Abhängig von den Pack-Eintragssteuerungen kannst du typischerweise:
- ein Pack aus der aktivierten Liste entfernen/deaktivieren
- einen Pack-Eintrag löschen (sofern verfügbar)

**Empfohlene Vorgehensweise:**
- Füge Packs einzeln hinzu und teste nach jeder Änderung.
- Führe eine Aufzeichnung der in Produktion verwendeten Pack-Versionen.
- Wenn ein Pack mit einem anderen in Konflikt steht, passe zuerst die Priorität an, bevor du es entfernst.

---

## Resource Packs

Resource Packs beeinflussen die Darstellung (Texturen, Sounds, UI-Ressourcen und clientseitige Assets). Die Resource Packs-Seite folgt dem gleichen Workflow wie bei Behaviour Packs.

![Resource Pack Tracker](/images/resource-pack-tracker.png)

### Resource Packs hochladen
- Unterstützte Dateitypen: **.mcpack** oder **.zip**
- Drag-and-Drop wird unterstützt, oder klicke zum Hochladen.

### Aktivierte vs. deaktivierte Packs
Resource Packs sind unterteilt in:
- **Aktivierte Resource Packs**
- **Deaktivierte Resource Packs**

Wenn keine Packs vorhanden sind, siehst du möglicherweise eine Meldung, die dich auffordert, Packs aus dem deaktivierten Bereich zu aktivieren.

**Empfohlene Vorgehensweise:**
- Verwende Resource Packs mit Bedacht, wenn du eine konsistente visuelle Darstellung für alle Spieler benötigst.
- Wenn du benutzerdefinierte Visuals erzwingst, stelle sicher, dass deine Welt-/Servereinstellungen mit dem beabsichtigten „Texturpaket erforderlich"-Verhalten übereinstimmen.

---

## Sicherheits- und Betriebshinweise

- **Lade immer ein Backup herunter**, bevor du eine Welt ersetzt oder größere Pack-Änderungen vornimmst.
- **Bestätige den aktiven Slot**, bevor du etwas hochlädst.
- Wenn du ein öffentliches Realm betreibst, erwäge, Änderungen in ruhigen Stunden vorzunehmen und Updates im Voraus zu kommunizieren.
- Wenn nach einer Änderung etwas nicht funktioniert, setze zurück, indem du:
  - die zuletzt vorgenommenen Pack-Änderungen entfernst/deaktivierst, oder
  - ein bekanntermaßen funktionierendes Welt-Backup wiederherstellst, sofern verfügbar.
