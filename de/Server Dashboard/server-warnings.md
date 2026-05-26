---
label: Verwarnungseinstellungen
description: Konfiguriere Verwarnungstypen mit benutzerdefinierten Gründen und Schwellenwerten, um eine konsistente Moderation und automatische Eskalation basierend auf der Anzahl ausgesprochener Verwarnungen zu ermöglichen.
order: 95
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Verwarnungseinstellungen

Die Seite **Verwarnungseinstellungen** ermöglicht es dir, strukturierte **Verwarnungstypen** für deinen Server zu definieren. Jeder Verwarnungstyp hat:

- Einen **Grund** (wofür die Verwarnung steht)
- Einen **Verwarnungen bis zum Bann**-Schwellenwert (wie oft dieser Verwarnungstyp ausgesprochen werden kann, bevor ein automatischer Bann erfolgt)

Dies stellt sicher, dass die Moderation im gesamten Team konsistent ist und ermöglicht eine vorhersehbare Eskalation bei wiederholtem Fehlverhalten.

![Verwarnungssystem Konfiguration](/images/server-warnings.png)

---

## Wie das Verwarnungssystem funktioniert

Verwarnungen sind nach **Typ** organisiert. Wenn ein Teammitglied eine Verwarnung eines bestimmten Typs ausspricht (z. B. *Spamming*), zeichnet Realm Bot diese gegen den Benutzer auf.

Der konfigurierte **Verwarnungen bis zum Bann**-Wert bestimmt den automatischen Eskalationspunkt:

- Wenn **Verwarnungen bis zum Bann = 3**, wird der Benutzer nach dem Erhalt von **drei Verwarnungen dieses Typs** gebannt
- Wenn **Verwarnungen bis zum Bann = 1**, löst eine einzelne Verwarnung dieses Typs einen sofortigen Bann aus (sparsam verwenden)

> **Operativer Hinweis:** Verwarnungsschwellenwerte gelten pro Verwarnungstyp. So kannst du verschiedene Verhaltensweisen mit unterschiedlicher Schwere behandeln (z. B. Spamming vs. Cheating).

---

## Einen Verwarnungstyp erstellen

Im Bereich **Verwarnungstyp erstellen** konfigurierst du:

### Verwarnungsgrund
Eine kurze Bezeichnung für das verwarnte Verhalten (die maximale Länge kann in der Benutzeroberfläche vorgegeben sein).

Beispiele:
- `Spamming`
- `Harassment`
- `Staff Disrespect`
- `Cheating`
- `Inappropriate Language`

**Empfohlene Vorgehensweise:** Halte Gründe kurz, klar und im Einklang mit deinen Serverregeln.

### Verwarnungen bis zum Bann
Die Anzahl der Verwarnungen dieses Typs, die erforderlich sind, bevor ein automatischer Bann angewendet wird.

Empfohlene Schwellenwerte:
- **1** – Schweres Fehlverhalten (z. B. Cheating, Doxxing-Drohungen, extreme Belästigung)
- **3** – Mittleres Fehlverhalten (z. B. Spamming, wiederholte geringfügige Störung)
- **5** – Geringfügiges Fehlverhalten (z. B. leichter Respektmangel, niedrigschwellige Belästigung)

Wenn du bereit bist, wähle **Verwarnungstyp hinzufügen**, um ihn zu erstellen.

---

## Verwarnungstypen verwalten

Der Bereich **Verwarnungstypen** listet alle konfigurierten Verwarnungstypen und ihre Schwellenwerte auf.

Jeder Eintrag zeigt:
- Den Verwarnungsgrund/-namen
- Den Bann-Schwellenwert (z. B. „Bann nach 3 Verwarnungen")

Du kannst jeden Verwarnungstyp über die Aktionsschaltflächen verwalten (sofern verfügbar):
- **Bearbeiten** (Stiftsymbol) – Grund oder Schwellenwert ändern
- **Löschen** (Papierkorbsymbol) – den Verwarnungstyp entfernen

> **Wichtig:** Wenn du einen Verwarnungstyp löschst, stelle sicher, dass dein Moderationsablauf und die Anleitung für dein Team aktualisiert werden. Konsistenz ist wichtiger als Komplexität.

---

## Empfohlenes Moderationsdesign

### Halte die Liste klein und aussagekräftig
Strebe Verwarnungstypen an, die direkt deinen Regelkategorien entsprechen. Zu viele Typen verlangsamen das Team und machen die Durchsetzung inkonsistent.

Ein praktischer Ausgangspunkt für die meisten Server:
- Spamming (3)
- Harassment (2–3)
- Staff Disrespect (5)
- Cheating (1)
- Inappropriate Content (1–2)

### Schwellenwerte an die Schwere der Regel anpassen
Setze Schwellenwerte basierend auf dem Schadensniveau:
- Sofortiger Bann für „Null-Toleranz"-Regeln
- Mehrfachverwarnungen für Verhalten, das korrigiert werden kann

### Leitfaden für das Team erstellen
Dein Verwarnungssystem ist nur dann effektiv, wenn das Team es konsequent nutzt. Erwäge, Folgendes zu dokumentieren:
- Welche Verwarnungstypen für häufige Situationen zu verwenden sind
- Welche Beweise für schwerwiegende Typen erforderlich sind (z. B. Cheating)

---

## Fehlerbehebung

### Automatische Banns fühlen sich zu aggressiv an
- Erhöhe **Verwarnungen bis zum Bann** für den betreffenden Verwarnungstyp
- Teile zu breite Verwarnungstypen in „geringfügig" vs. „schwerwiegend" auf (nur wenn nötig)

### Teammitglieder vergeben inkonsistente Verwarnungsgründe
- Reduziere die Anzahl der Verwarnungstypen
- Benenne Verwarnungsgründe so um, dass sie exakt deinen Regeln entsprechen
- Stelle dem Team Beispiele zur Verfügung, welcher Typ in welchem Szenario zu verwenden ist

---
