---
label: Tebex
description: Integriere Tebex mit Realm Bot, um die Zustellung von In-Game-Belohnungen (z. B. Ränge und Vorteile) nach einem erfolgreichen Shop-Kauf zu automatisieren.
order: 97
author:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Tebex

Tebex (früher bekannt als **Buycraft**) ist eine dedizierte Webshop- und Monetarisierungsplattform, die von Minecraft-Communities genutzt wird, um **Ränge**, **Vorteile**, **Kosmetika** und andere digitale Produkte zu verkaufen. Realm Bot integriert sich mit Tebex, um **automatisierte Auslieferung** zu unterstützen, sodass berechtigte Käufe mit minimalem Mitarbeitereingriff im Spiel zugestellt werden können.

> **Wichtig:** Du bist dafür verantwortlich, sicherzustellen, dass deine Shop-Konfiguration und Produkte allen geltenden Minecraft / Microsoft Monetarisierungsanforderungen sowie deinen eigenen Serverregeln und Richtlinien entsprechen.

---

## Was diese Integration bewirkt

Wenn verbunden, kann Realm Bot Tebex-Käufe ausliefern, indem konfigurierte Belohnungen in deinem Realm zugestellt werden (zum Beispiel die Vergabe eines gekauften Rangs an den richtigen Spieler).

Dies ist dazu gedacht:
- Den manuellen Arbeitsaufwand der Mitarbeiter zu reduzieren („Ränge von Hand vergeben").
- Liefergeschwindigkeit und Konsistenz zu verbessern.
- Einen klareren Audit-Trail zu bieten, wenn es mit deinem Moderations-/Logging-Workflow kombiniert wird.

---

## Voraussetzungen

Um die Tebex-Integration zu nutzen:

- **Realm Bot Premium** muss aktiv sein.
- Du musst einen Tebex-Shop mit einem konfigurierten **Game Server** haben.
- Du musst deinen Tebex **Secret Key** (manchmal als „Secret Code" angezeigt) erhalten und privat halten.

> **Sicherheitshinweis:** Der Secret Key autorisiert den Zugriff auf deine Tebex-Server-Integration. Teile ihn nicht öffentlich, füge ihn nicht in allgemeine Kanäle ein und rotiere ihn sofort, wenn du glaubst, dass er offengelegt wurde.

---

## Einrichtung

1.  Erstelle ein Tebex-Konto und erstelle einen **Game Server** in Tebex.  
    ![Tebex Game Server Einrichtung](/images/tebex/1.png)

2.  Wähle **Minecraft** als Plattform für deinen Webshop.  
    ![Tebex Minecraft auswählen](/images/tebex/2.png)

3.  Wähle **Minecraft: Bedrock Edition**.  
    ![Tebex Minecraft auswählen](/images/tebex/3.png)

4.  Kopiere nur den **Secret Key / Secret Code**.  
    ![Tebex Secret Key](/images/tebex/4.png)

5.  Öffne das **Tebex**-Modul im Realm Bot Dashboard.  
    ![Dashboard Tebex-Modul](/images/tebex/dash-5.png)

6.  Aktiviere das Modul, füge deinen Tebex **Secret Key** ein und wähle dann **Speichern**.

7.  Bestätige, dass sowohl Realm Bot als auch Tebex den Status **Verbunden** anzeigen.  
    ![Verbindungsstatus Tebex](/images/tebex/7.png)

---

## Produkte auf Tebex erstellen

Sobald die Integration verbunden ist, erstelle Produkte auf Tebex (Ränge, Bundles, Abonnements usw.) und konfiguriere die Auslieferungsmethode, die für dein Realm Bot-Setup erforderlich ist.

Operative Empfehlungen:
- Verwende eine klare, konsistente Produktbenennung (z. B. `Rank: Knight`, `Rank: Emperor`).
- Halte „Rang"-Produkte von „Verbrauchsartikeln" (Schlüssel, Kisten, Boosts) getrennt, um den Support zu erleichtern.
- Führe eine interne Liste der Produkte und ihrer beabsichtigten In-Game-Ergebnisse als Referenz für Mitarbeiter.

Für die vollständige Tebex-Shop-Konfiguration und Produkt-Tools siehe die offizielle Tebex-Dokumentation:
https://docs.tebex.io/

---

## Fehlerbehebung

### „Nicht verbunden" / „Verbindung fehlgeschlagen"
- Überprüfe erneut, ob du den **Secret Key** kopiert hast (nicht andere Kennungen).
- Stelle sicher, dass keine zusätzlichen Leerzeichen vor/nach dem Schlüssel beim Einfügen vorhanden sind.
- Speichere die Moduleinstellungen erneut, nachdem du den Schlüssel eingefügt hast.

### Käufe werden nicht zugestellt
- Bestätige, dass das Tebex-Modul im Dashboard **aktiviert** bleibt.
- Bestätige, dass der Kauf in Tebex als **Abgeschlossen** markiert ist.
- Überprüfe, ob das Produkt korrekt konfiguriert ist und dem beabsichtigten In-Game-Belohnungsablauf zugeordnet ist.
- Wenn deine Realm Bot-Umgebung einen In-Game-Zustellungspfad erfordert (abhängig von deiner Konfiguration), bestätige, dass die erforderlichen Komponenten online und betriebsbereit sind.

### Falscher Spieler hat die Belohnung erhalten
- Stelle sicher, dass die Shop-Anweisungen den Käufern klar mitteilen, welche Identität (Benutzername / Gamertag) beim Checkout angegeben werden muss.
- Vermeide mehrdeutige Namenskonventionen und stelle sicher, dass Mitarbeiter einen konsistenten Prozess zur Lösung von Fehlzuordnungen haben.

Wenn du Unterstützung benötigst, gib Folgendes an:
- Deinen Tebex-Shop-/Servernamen
- Einen Screenshot des Modul-Verbindungsstatus
- Die Bestell-ID (oder Transaktionsreferenz) von Tebex
- Das erwartete Ergebnis im Vergleich zum beobachteten Ergebnis
