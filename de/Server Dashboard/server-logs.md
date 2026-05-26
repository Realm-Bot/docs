---
label: Log-Kanäle
description: Konfiguriere, welche Discord-Kanäle die Moderations-Logs von Realm Bot erhalten, einschließlich Banns, Entbannungen, Kicks und Verwarnungen.
order: 98
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Log-Kanäle

Die Seite **Log-Kanäle** ermöglicht es dir festzulegen, wohin Realm Bot operative Log-Nachrichten in deinem Discord-Server sendet. Logging ist eine zentrale Verwaltungsfunktion: Es verbessert die Transparenz, unterstützt die Verantwortlichkeit des Teams und bietet eine nachvollziehbare Aufzeichnung von Moderationsmaßnahmen.

![Log-Kanäle Konfiguration](/images/server-logs.png)

---

## Wofür Log-Kanäle gedacht sind

Log-Kanäle helfen dir:

- Eine zuverlässige Aufzeichnung von Moderationsmaßnahmen zu führen
- Vorfälle im Nachhinein zu überprüfen (wer hat gehandelt, was ist passiert, wann ist es passiert)
- Die Arbeit des Teams über Zeitzonen hinweg zu koordinieren
- Streitigkeiten zu reduzieren, indem objektive Nachweise an einem Ort gesammelt werden

> **Empfohlene Vorgehensweise:** Halte Log-Kanäle **nur für das Team** und **schreibgeschützt** für die meisten Rollen. Vermeide es, öffentliche Kanäle für Moderations-Logs zu verwenden.

---

## Verfügbare Log-Typen

Der Bereich Log-Kanäle bietet separate Ziele für verschiedene Moderationsereignisse. Jeder Log-Typ kann in einen eigenen Kanal geleitet werden, oder mehrere Log-Typen können einen Kanal teilen (nur für kleinere Server empfohlen).

### Bann-Logs
**Nachrichten, die gesendet werden, wenn ein Benutzer gebannt wird** – aus deinem Server oder der von Realm Bot verwalteten Umgebung (je nach Konfiguration).

Verwende dies für:
- Die Nachverfolgung von Entfernungen und Banngründen (sofern angegeben)
- Das Erkennen von Mustern wiederholten Missbrauchs

### Entbannungs-Logs
**Nachrichten, die gesendet werden, wenn ein Benutzer entbannt wird.**

Verwende dies für:
- Die Sicherstellung, dass Entbannungen beabsichtigt und für leitende Teammitglieder sichtbar sind
- Die Überprüfung von Entscheidungen zur Aufhebung von Banns

### Kick-Logs
**Nachrichten, die gesendet werden, wenn ein Benutzer gekickt wird.**

Verwende dies für:
- Die Überwachung kurzfristiger Entfernungen
- Die Unterscheidung zwischen vorübergehenden Entfernungen und permanenten Banns

### Verwarnungs-Logs
**Nachrichten, die gesendet werden, wenn ein Benutzer eine Verwarnung erhält.**

Verwende dies für:
- Die Überwachung der Eskalation von Verwarnungen
- Die Aufrechterhaltung einheitlicher Disziplinarstandards im Team

---

## Konfiguration

1. Erstelle (oder wähle) einen oder mehrere Nur-Team-Discord-Kanäle, zum Beispiel:
   - `#mod-logs`
   - `#staff-commands`
   - `#audit-log`

2. Wähle in **Log-Kanäle** den Zielkanal für jeden Log-Typ aus:
   - Bann-Logs
   - Entbannungs-Logs
   - Kick-Logs
   - Verwarnungs-Logs

3. Stelle sicher, dass Realm Bot die erforderlichen Berechtigungen in jedem ausgewählten Kanal hat:
   - **View Channel**
   - **Send Messages**
   - **Read Message History** (empfohlen)

> **Falls Logs nicht gesendet werden:** Überprüfe zuerst die Kanalberechtigungen.

---

## Empfohlene Kanalstruktur

Für die meisten Server funktioniert einer der folgenden Ansätze am besten:

### Option A – Einzelner konsolidierter Log-Kanal (Einfach)
Leite alle Log-Typen in einen Kanal, z. B. `#mod-logs`.  
Dies eignet sich für kleinere Teams und geringere Aktivität.

### Option B – Aufgeteilt nach Schweregrad (Empfohlen für Teams)
- `#warnings-and-kicks` → Verwarnungs-Logs + Kick-Logs  
- `#ban-and-unban` → Bann-Logs + Entbannungs-Logs  

Dies verbessert die Lesbarkeit und erleichtert das Auffinden schwerwiegender Maßnahmen.

### Option C – Vollständige Trennung (Hohe Aktivität)
Verwende separate Kanäle für jeden Log-Typ.  
Dies eignet sich am besten für große Server mit häufiger Moderationsaktivität.

---

## Operative Hinweise

- Logs sind nur nützlich, wenn sie lesbar bleiben. Vermeide es, in Log-Kanälen zu chatten.
- Stelle sicher, dass leitende Teammitglieder Logs einsehen können, auch wenn Moderatoren Nachrichten nicht löschen oder bearbeiten können.
- Wenn dein Server mehrere Realms nutzt, halte deine Log-Struktur über alle Realms hinweg konsistent, um Verwirrung im Team zu vermeiden.

---
