---
label: Übersicht
description: Verstehe die Übersicht des Server Dashboard, einschließlich Premium-Status, verknüpfter Kontoinformationen, verbundener Realms und wo du serverweite Einstellungen konfigurierst.
order: 100
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Server Dashboard

Das **Server Dashboard** ist die zentrale Steuerungsoberfläche für deinen Discord-Server innerhalb von Realm Bot. Es bietet:

- Einen allgemeinen Überblick über den aktuellen Status deines Servers (einschließlich Premium-Status)
- Bestätigung, welche Discord- und Xbox-Konten verknüpft sind
- Eine Liste verbundener Realms mit schnellem "Ansehen"-Zugriff
- Eine strukturierte Navigationsleiste für alle serverweiten Konfigurationsseiten

![Server Dashboard Übersicht](/images/server-dashboard-overview.png)

---

## Wofür das Server Dashboard gedacht ist

Nutze das Server Dashboard, um:

- Zu bestätigen, dass der Server verbunden und korrekt konfiguriert ist
- Zu überprüfen, ob die **richtigen verknüpften Konten** für die Verwaltung und den Realm-Zugang verwendet werden
- Zu **serverweiten Einstellungen** zu navigieren (Protokollierung, Erlaubnis, Befehlskonfiguration)
- Über die Liste der verbundenen Realms in **Realm-spezifische Dashboards** zu wechseln

Diese Seite dient als **Betriebsübersicht auf einen Blick**, während die Seitenleiste die detaillierten Konfigurationsseiten enthält.

---

## Premium-Status

Der obere Bereich zeigt deine Serveridentität und den Premium-Indikator (falls zutreffend), zusammen mit einem **Premium-Status**-Fortschrittsbalken und der verbleibenden Zeit.

Typische Anwendungen:
- Bestätigen, dass Premium aktiv ist, bevor du Premium-exklusive Module konfigurierst
- Verbleibende Abonnementzeit für die Betriebsplanung prüfen

> **Hinweis:** Einige Funktionen und Module funktionieren möglicherweise nur, wenn Premium für den Server aktiv ist.

---

## Verknüpfte Benutzerinformationen

Der Abschnitt **Verknüpfte Benutzerinformationen** bestätigt die Identitäten, die mit dieser Serverkonfiguration verbunden sind.

Er enthält typischerweise:

### Discord-Konto
- Das Discord-Profil, das aktuell mit dem Server Dashboard-Kontext verknüpft ist
- Benutzername und Handle (wie auf Discord angezeigt)

### Xbox-Konto
- Der Xbox-Gamertag, der aktuell für den Realm-Zugang verknüpft ist
- Eine Kennung wie **XUID** (Xbox User ID), sofern angezeigt

Dieser Abschnitt ist wichtig für die Fehlerbehebung:
- Fehlende Realms deuten oft darauf hin, dass das **falsche Microsoft/Xbox-Konto** verknüpft ist.
- Unerwartete Erlaubnis- oder Zugriffsprobleme können durch die Verknüpfung eines Nicht-Besitzer-Kontos verursacht werden.

---

## Verbundene Realms

Das Panel **Verbundene Realms** zeigt alle Realms an, die unter deinem/deinen verknüpften Xbox-Konto(en) erkannt/verbunden wurden. Jede Realm-Karte enthält typischerweise:

- Realm-Name und Unterbezeichnung (falls zutreffend)
- Eine **Ansehen**-Schaltfläche, um die Dashboard-Seiten dieses Realms zu öffnen

Dies ist der schnellste Weg, zwischen Realms zu wechseln, ohne durch Menüs suchen zu müssen.

Betriebliche Hinweise:
- Halte die Realm-Benennung einheitlich, damit Mitarbeiter den richtigen Realm schnell identifizieren können.
- Wenn ein Realm fehlt, überprüfe zuerst die Kontoverknüpfung und die Erlaubnis.

---

## Navigationsleiste

Die linke Seitenleiste ist der Einstiegspunkt zu allen Server Dashboard-Seiten und ist in übersichtliche Abschnitte unterteilt.

![Server Dashboard Navigationsliste](/images/server-dashboard-list.png)

### Übersicht
- **Übersicht** - die Seite, die du gerade anschaust
- **Server-Einrichtung** - geführte oder zusammengefasste Einrichtungswerkzeuge (sofern verfügbar)

### Verwalten
Serverweite Konfigurationsseiten für den täglichen Betrieb:

- **Protokollkanäle** - wähle, wo Betriebsprotokolle veröffentlicht werden
- **Kontoverknüpfung** - verwalte den Discord/Microsoft-Verknüpfungsstatus und zugehörige Abläufe
- **Nachrichtenaktionen** - konfiguriere automatisierte Nachrichtenverhalten (sofern unterstützt)
- **Verwarnungseinstellungen** - konfiguriere Verwarnungs-/Disziplinarverhalten und Schwellenwerte (sofern unterstützt)
- **Befehlseinstellungen** - steuere, wie Befehle Informationen anzeigen
- **Erlaubnis** - lege fest, wer auf Serverfunktionen und Dashboards zugreifen kann
- **Allowlist** - beschränke den Zugang auf genehmigte Benutzer/Rollen (sofern zutreffend)
- **Protokolle** - zeige aufgezeichnete Ereignisse und administrative Aktivitäten an (sofern verfügbar)

### Realms
Eine Liste aller verbundenen Realms wird unten angezeigt. Die Auswahl eines Realms erweitert dessen verfügbare Realm-Seiten und Konfigurationsbereiche.

> **Empfohlene Vorgehensweise:** Behandle serverweite Einstellungen (Erlaubnis, Allowlist, Befehlssteuerung) als dein Sicherheitsfundament, bevor du wirkungsvolle Module auf einzelnen Realms aktivierst.

---

## Empfohlene Einrichtungsreihenfolge

Für eine saubere und sichere Bereitstellung:

1. Premium-Status bestätigen (falls zutreffend)
2. **Verknüpfte Benutzerinformationen** überprüfen (korrektes Discord- + Xbox-Konto)
3. Bestätigen, dass deine Realms unter **Verbundene Realms** erscheinen
4. **Erlaubnis / Allowlist** konfigurieren, bevor du Mitarbeiterwerkzeuge aktivierst
5. **Protokollkanäle** konfigurieren, damit Aktionen nachvollziehbar sind
6. In Realm-spezifische Seiten für Module und Weltkonfiguration wechseln

---

## Häufige Probleme

### "Meine Realms werden nicht angezeigt."
- Stelle sicher, dass das richtige Microsoft/Xbox-Konto verknüpft ist.
- Führe den Verknüpfungsvorgang unter **Kontoverknüpfung** erneut durch, falls nötig.
- Bestätige, dass das Konto tatsächlich die erwarteten Realms besitzt oder Zugriff darauf hat.

### "Mitarbeiter können Dinge sehen, die sie nicht sehen sollten."
- Überprüfe zuerst **Erlaubnis** und **Allowlist**.
- Beschränke wirkungsvolle Bereiche auf vertrauenswürdige Administratorrollen.

### "Ich kann eine Seite in der Seitenleiste nicht aufrufen."
- Bestätige, dass deine Rolle die Erlaubnis für diesen Bereich hat.
- Stelle sicher, dass der Bot die erforderlichen Discord-Berechtigungen im Server hat.

---
