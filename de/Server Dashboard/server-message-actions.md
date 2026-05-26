---
label: Nachrichtenaktionen
description: Konfiguriere die automatisierten Moderationsnachrichten, die an Spieler gesendet werden, wenn Maßnahmen ergriffen werden, und verwende Variablen, um Nachrichten konsistent, informativ und regelkonform zu halten.
order: 96
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Nachrichtenaktionen

Die Seite **Nachrichtenaktionen** ermöglicht es dir, die Nachrichten zu konfigurieren, die Realm Bot bei Moderationsmaßnahmen sendet. Diese Nachrichten helfen Spielern zu verstehen, was passiert ist, warum es passiert ist und was als Nächstes zu tun ist – und halten gleichzeitig deine Durchsetzung im gesamten Team konsistent.

![Nachrichtenaktionen Hinweis und Variablen](/images/server-message-actions-explanation.png)

---

## Wichtiger Hinweis

Moderationsnachrichten werden **über dein Xbox-Konto** gesendet. Du bist dafür verantwortlich sicherzustellen, dass alle gesendeten Inhalte den **Xbox Community Standards** entsprechen und für dein Publikum angemessen sind.

Praktische Auswirkungen:
- Vermeide Belästigung, Drohungen, Beleidigungen oder provokante Sprache
- Halte Nachrichten sachlich, ruhig und verfahrensorientiert
- Teile keine persönlichen Daten oder internen Teamdiskussionen

---

## Wie Nachrichtenaktionen funktionieren

Für jede Moderationsmaßnahme kannst du:

1. Den Nachrichtentyp **aktivieren** (pro Maßnahme)
2. Den Nachrichtentext anpassen
3. Variablen einfügen, damit sich die Nachricht automatisch an jeden Fall anpasst

Wenn aktiviert, sendet Realm Bot die konfigurierte Nachricht an den betroffenen Spieler, sobald die entsprechende Maßnahme ausgeführt wird.

![Nachrichtenvorlagen (Kick / Bann / Entbannung / Verwarnung)](/images/server-message-actions-messages.png)

---

## Verfügbare Variablen

Du kannst Variablen an der Cursorposition einfügen, um Details dynamisch einzufügen:

- `{user}` – das Teammitglied oder Konto, das die Maßnahme durchgeführt hat
- `{target}` – der Spieler, der die Maßnahme erhalten hat
- `{reason}` – der angegebene Grund (falls vorhanden)
- `{length}` – die Dauer der Maßnahme (falls zutreffend)
- `{guild}` – der Name/Bezeichner deines Discord-Servers
- `{realm}` – der Realm-Name/Kontext

> **Tipp:** Füge `{reason}` nach Möglichkeit immer ein. Ein klarer Grund reduziert Streitigkeiten und Wiederholungsverstöße.

---

## Nachrichtentypen

### Kick-Nachricht
Wird gesendet, wenn ein Spieler **gekickt** wird.

Empfohlener Inhalt:
- Was passiert ist (Kick)
- Grund
- Nächster Schritt (erneutes Beitreten erlaubt, sofern nicht anders angegeben)

### Bann-Nachricht
Wird gesendet, wenn ein Spieler **gebannt** wird.

Empfohlener Inhalt:
- Was passiert ist (Bann)
- Grund
- Dauer (falls temporär)
- Einspruchsmöglichkeit (falls du Einsprüche unterstützt)

### Entbannungs-Nachricht
Wird gesendet, wenn ein Spieler **entbannt** wird.

Empfohlener Inhalt:
- Bestätigung der Entbannung
- Erinnerung an Regeln/Erwartungen

### Verwarnungs-Nachricht
Wird gesendet, wenn ein Spieler eine **Verwarnung** erhält.

Empfohlener Inhalt:
- Verwarnungsgrund
- Erwartetes Verhalten in Zukunft
- Eskalationshinweis (optional, vermeide Drohungen)

---

## Vorgeschlagene Vorlagen (Kopieren/Einfügen)

Diese Vorlagen sind bewusst kurz, neutral und verfahrensorientiert gehalten.

### Kick
`{target}, du wurdest aus {realm} entfernt. Grund: {reason}. Du kannst wieder beitreten, wenn du dich an die Regeln hältst.`

### Kick 
`{target} wurde von {user} aus {realm} gekickt. Grund: {reason}.`

---

### Bann 
`{target}, du wurdest aus {realm} gebannt. Grund: {reason}. Dauer: {length}.`

### Bann
`{target}, du wurdest aus {realm} gebannt. Grund: {reason}. Wenn du glaubst, dass dies ein Fehler ist, kontaktiere das Team in {guild}.`

---

### Entbannung
`{target}, dein Bann in {realm} wurde aufgehoben. Bitte lies dir die Regeln durch, bevor du wieder beitrittst.`

---

### Verwarnung 
`{target}, du hast eine Verwarnung in {guild} erhalten. Grund: {reason}. Bitte unterlasse dieses Verhalten, um weitere Maßnahmen zu vermeiden.`

### Verwarnung
`Verwarnung ausgesprochen an {target}. Grund: {reason}.`

---

## Empfohlene Vorgehensweise

- Halte Nachrichten **kurz und sachlich**. Spieler sollten die Maßnahme beim ersten Lesen verstehen.
- Vermeide teaminternes Detail (interne Notizen, Anschuldigungen, Spekulationen).
- Verwende eine einheitliche Formulierung bei Kick/Bann/Verwarnung, damit Spieler offizielle Mitteilungen erkennen.
- Wenn du Einsprüche unterstützt, verweise auf einen einzelnen Kanal oder Prozess – argumentiere nicht im Spiel.
- Lass `{reason}` nur leer, wenn es nötig ist; mache es ansonsten in deinem Arbeitsablauf verpflichtend.

---

## Fehlerbehebung

### Nachrichten werden nicht gesendet
- Bestätige, dass der jeweilige Nachrichtentyp-Schalter **aktiviert** ist (Kick/Bann/Entbannung/Verwarnung).
- Stelle sicher, dass deine Moderationsbefehle einen **Grund** und eine **Dauer** enthalten, wo zutreffend.
- Wenn deine Implementierung auf ein verknüpftes Xbox-Konto für ausgehende Nachrichten angewiesen ist, überprüfe, ob das richtige Konto verknüpft und funktionsfähig ist.

### Variablen werden wörtlich angezeigt (nicht ersetzt)
- Stelle sicher, dass die Variablen exakt dem unterstützten Format entsprechen: `{user}`, `{target}`, `{reason}`, `{length}`, `{guild}`, `{realm}`.
- Vermeide zusätzliche Leerzeichen innerhalb der geschweiften Klammern (z. B. `{ reason }`).

---
