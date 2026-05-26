---
label: Moderations-Logs
description: Überprüfe und auditiere Moderationsmaßnahmen, die in deinen verbundenen Realms durchgeführt wurden, mit Filter- und Verlaufsansichten pro Benutzer.
order: 91
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Moderations-Logs

Die Seite **Moderations-Logs** bietet eine nachvollziehbare Aufzeichnung der Moderationsmaßnahmen, die in deinen verbundenen Realms durchgeführt wurden. Sie ist auf Transparenz, Verantwortlichkeit des Teams und schnelle Untersuchung von Wiederholungstätern ausgelegt.

![Moderations-Logs](/images/server-mod-logs.png)

---

## Was du hier tun kannst

### Maßnahmen über Realms hinweg verfolgen
Moderations-Logs fassen Maßnahmen zusammen, die über Realm Bot durchgeführt wurden, darunter:
- Banns
- Kicks
- Verwarnungen (wenn in deiner Konfiguration aktiviert)
- Entbannungen und andere Aufhebungsmaßnahmen (sofern zutreffend)

Jedes Ereignis wird mit genügend Kontext gespeichert, um zu verstehen:
- **was passiert ist**
- **wer die Maßnahme durchgeführt hat**
- **wann es passiert ist**
- **auf welches Realm sich die Maßnahme bezog**

---

## Zeitleistenansicht

Standardmäßig verwenden Moderations-Logs eine **Zeitleistenansicht**, die Maßnahmen nach Benutzer gruppiert.

- Jede Benutzerzeile zeigt:
  - Gamertag / Identität
  - einen eindeutigen Bezeichner (z. B. XUID, sofern verfügbar)
  - den Zeitstempel der letzten Aktivität
  - einen Zähler für protokollierte Maßnahmen

- Erweitere einen Benutzer, um seinen vollständigen Maßnahmenverlauf anzuzeigen, einschließlich:
  - Maßnahmentyp (z. B. Bann)
  - Datum/Uhrzeit der Maßnahme
  - verantwortlicher Moderator
  - Begründungstext (falls angegeben)
  - Realm, auf das sich die Maßnahme bezog

> **Tipp:** Die Zeitleistenansicht ist ideal, wenn du das Verhaltensmuster eines Spielers untersuchst.

---

## Suche & Filterung

### Suche
Verwende die **Suchleiste**, um einen Spieler schnell zu finden. Dies ist der schnellste Weg, um:
- einen bestimmten Benutzer zu finden
- zu bestätigen, ob bereits Maßnahmen ergriffen wurden
- frühere Gründe und Ergebnisse zu überprüfen

### Maßnahmenfilter
Verwende das Dropdown **Alle Maßnahmen**, um nach Maßnahmentyp zu filtern. Dies ist nützlich für:
- die Überprüfung von Banns, die über einen Zeitraum ausgesprochen wurden
- das Auditieren der Kick-Nutzung durch das Team
- die Isolierung von Verwarnungsaktivitäten, wenn dein Server diese intensiv nutzt

---

## Tabellenansicht

Du kannst zur **Tabellenansicht** wechseln, um ein strukturierteres, listenbasiertes Layout zu erhalten.

Die Tabellenansicht ist nützlich, wenn du:
- einen schnellen Überblick über aktuelle Maßnahmen benötigst
- eine übersichtliche Darstellung für Moderationsüberprüfungen brauchst
- schnellere Vergleiche über mehrere Benutzer/Maßnahmen hinweg durchführen möchtest

---

## Empfohlene Vorgehensweise

- **Verlange Begründungen für wichtige Maßnahmen.** Ein einheitlicher Begründungsstandard verbessert zukünftige Moderationsentscheidungen und Einsprüche.
- **Überprüfe Logs regelmäßig.** Wöchentliche Kontrollen helfen, Missbrauch oder Inkonsistenzen frühzeitig zu erkennen.
- **Nutze Logs für Eskalationen.** Ein sich wiederholendes Muster in der Zeitleiste ist oft die klarste Begründung für längere Banns oder dauerhafte Entfernung.

---

## Hinweise zu Genauigkeit und Sichtbarkeit

- Moderations-Logs spiegeln Maßnahmen wider, die über Realm Bot und zugehörige Systeme ausgeführt wurden.
- Wenn dein Team zusätzliche reine In-Game-Moderation nutzt, werden diese Maßnahmen möglicherweise nicht angezeigt, es sei denn, sie werden über Realm Bot-Arbeitsabläufe ausgeführt.

---
