---
label: Skin Filtering
description: Erkenne und entferne automatisch Spieler mit ungewöhnlichen Skins (kleine, unsichtbare/transparente oder 4D/Horion-Skins), um Fairness zu verbessern und Exploit-Missbrauch zu reduzieren.
order: 30
image: /images/custom/skinfiltering.png
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Skin Filtering

Skin Filtering ist eine Moderationsfunktion, die Realm-Besitzern hilft, Exploit-orientierte Kosmetik zu unterbinden, indem **ungewöhnliche Spieler-Skins** erkannt und entsprechend gehandelt wird. Dies umfasst Muster, die häufig mit unfairer Sichtbarkeit, täuschenden Hitboxen oder Client-Exploit-Verhalten in Verbindung gebracht werden.

Skin Filtering ist derzeit eine **Beta**-Funktion. Abhängig vom Skin-Typ und Plattformverhalten können einige Fehlerkennungen auftreten.

![Skin Filtering Konfiguration](/images/skin-filtering.png)

---

## Was Skin Filtering bewirkt

Wenn aktiviert, überwacht Skin Filtering beitretende Spieler (und/oder aktive Spieler, je nach deiner Konfiguration) und identifiziert Skins, die einer der konfigurierten "ungewöhnlichen" Kategorien entsprechen. Wenn ein Skin gegen deine ausgewählten Regeln verstößt, kann der Spieler basierend auf dem Durchsetzungsverhalten des Systems aus dem Realm entfernt werden.

Dies ist dafür gedacht:
- Fairness in PvP und wettbewerbsorientiertem Gameplay zu verbessern
- Sichtbarkeitsmissbrauch und Täuschungstaktiken zu reduzieren
- Kosmetikregeln für deine Community zu standardisieren

---

## Voraussetzungen

Skin Filtering erfordert:

- Der Realm Bot **Relay Account** muss **im Spiel** sein
- Skin Filtering muss im Modulbereich des Realms aktiviert sein

Wenn der Relay Account nicht im Spiel ist, kann das System Filteraktionen nicht zuverlässig durchsetzen.

---

## Filtereinstellungen

Du kannst die Filterung pro Kategorie aktivieren. Diese Kategorien sind darauf ausgelegt, gängige Exploit-orientierte Skin-Muster zu erkennen.

### Kleine Skins

Filtert kleinere oder "halbgroße" Skin-Darstellungen, die verwendet werden können, um das visuelle Profil zu verkleinern oder das Spieleraussehen falsch darzustellen.

Empfohlen für:
- PvP-Realms
- Wettbewerbsorientierte Minigames
- Server mit strengen kosmetischen Standards

### Unsichtbare Skins

Filtert Skins, die unsichtbare oder transparente Texturen verwenden, um die Sichtbarkeit zu verringern oder unfaire Vorteile zu schaffen.

Empfohlen für:
- Jeden Realm, in dem PvP, Tarnung oder Wettbewerbsvorteile eine Rolle spielen
- Öffentliche Realms, in denen Exploit-Kosmetik verbreitet ist

### Horion Skins (4D Skins)

Filtert "4D"- oder Horion-Skins, die häufig mit Exploit-Clients und kosmetischer Manipulation in Verbindung gebracht werden.

Empfohlen für:
- Realms, die Horion-bezogenen Missbrauch erlebt haben
- Realms mit öffentlichem Code
- Wettbewerbsumgebungen

> **Hinweis:** Diese Bezeichnungen spiegeln gängige Community-Terminologie wider. Der Filter basiert auf beobachteten Mustern ungewöhnlichen Skin-Verhaltens.

---

## Wie die Durchsetzung aussieht

Wenn ein Spieler mit einem nicht erlaubten Skin-Typ erkannt wird, kann Realm Bot eine automatisierte Aktion ausführen und das Ergebnis protokollieren. In Discord erscheint dies typischerweise als automatisierter Moderationseintrag, der den Spielerverbindungskontext und den Grund der Entfernung anzeigt.

![Skin Filtering Beispiel (Discord-Ausgabe)](/images/skin-filtering-example.png)

Dies bietet Mitarbeitern:
- eine klare Angabe, welcher Benutzer betroffen war
- die Grundkategorie (z. B. **Unfairer Skin**)
- grundlegenden Kontext für die Überprüfung, falls ein Spieler Einspruch einlegt

---

## Beispielkontext: Kleiner Skin im Einsatz

Kleine Skins verringern die scheinbare Größe und Sichtbarkeit des Spielers, was einen Vorteil im PvP oder bei schneller Bewegung schaffen kann. Das folgende Beispiel zeigt, wie ein kleiner Skin im Spiel aussehen kann.

![Kleiner Skin Beispiel (In-Game-Kontext)](/images/skin-filtering-example-context.png)

---

## Wann Skin Filtering aktiviert werden sollte

Skin Filtering ist am nützlichsten bei:

- Öffentlichen Einladungs-/Hochverkehrs-Realms
- PvP-Realms, bei denen Sichtbarkeit und Fairness entscheidend sind
- Realms, die häufig von Exploit-Nutzern angegriffen werden
- Communities mit etablierten Kosmetikregeln

Für private Realms mit Einladungen ist Skin Filtering möglicherweise unnötig, es sei denn, du begegnest regelmäßig Exploit-Kosmetik.

---

## Empfohlene Vorgehensweise

- Beginne mit den eindeutigsten Filtern zuerst (typischerweise **Unsichtbare Skins** und **Horion/4D Skins**).
- Beobachte in den ersten Tagen der Nutzung auf Fehlerkennungen.
- Veröffentliche eine kurze Regelaussage für Spieler (z. B. "Unsichtbare/4D-Skins sind nicht erlaubt.").
- Pflege ein Mitarbeiterverfahren für Einsprüche, falls ein legitimer Spieler fälschlicherweise entfernt wird.

---

## Beta-Hinweise und Fehlerkennungen

Da sich Skin Filtering in der Beta befindet:
- können einige legitime Skins in Randfällen fälschlicherweise markiert werden
- können Plattformunterschiede und Skin-Format-Eigenheiten zu inkonsistenter Erkennung führen

Wenn du Fehlerkennungen beobachtest:
- deaktiviere zuerst die Kategorie, die am wahrscheinlichsten Fehlerkennungen verursacht
- aktiviere jeweils nur einen Filter, um die Ursache einzugrenzen
- protokolliere betroffene Gamertags und Zeitstempel für die Support-Überprüfung

---

## Fehlerbehebung

### Filterung ist aktiviert, aber nichts passiert

- Bestätige, dass der Relay Account **im Spiel** ist
- Bestätige, dass Skin Filtering für den richtigen Realm aktiviert ist
- Stelle sicher, dass mindestens eine Filterkategorie aktiviert ist

### Legitime Spieler werden entfernt

- Deaktiviere zuerst die aggressivste Kategorie (häufig 4D/Horion)
- Teste erneut mit einem kleineren Umfang (aktiviere jeweils nur einen Filter)
- Behandle frühe Beta-Durchsetzung als überprüfbar, bis sich die Erkennung stabilisiert

---
