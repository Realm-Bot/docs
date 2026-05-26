---
label: Realm Console
description: Führe Minecraft-Befehle direkt aus einem gesicherten Discord-Kanal aus, wobei dein Relay Account im Spiel als Befehlsausführer dient.
order: 80
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

### Was ist die Realm Console?

Die Realm Console ist ein dedizierter Discord-Kanal, der autorisierten Benutzern ermöglicht, **Minecraft Bedrock-Befehle** direkt in einen verbundenen Realm auszuführen. Nachrichten, die im konfigurierten Konsolenkanal gesendet werden, werden als Befehle interpretiert und über den **Chat Relay Account** im Spiel ausgeführt.

Dieses Modul ist für die operative Verwaltung, schnelle Moderationsmaßnahmen und optimiertes Management konzipiert - ohne dass Mitarbeiter aktiv im Spiel auf einem Client sein müssen.

### Wie es funktioniert

Die Realm Console funktioniert, indem dein Relay Account als In-Game-Befehlsausführer verwendet wird:

- Ein Benutzer sendet eine Nachricht im festgelegten **Realm Console** Discord-Kanal.
- Realm Bot leitet die Nachricht über den **Chat Relay Account** an den Realm weiter.
- Der Relay Account führt die Nachricht als Befehl im Realm-Chat aus.

Da der Befehl vom Relay Account ausgeführt wird, folgt das gesamte Befehlsverhalten (Berechtigungen, Ziele und Nebeneffekte) denselben Regeln, als ob der Relay Account den Befehl manuell im Spiel eingegeben hätte.

![Realm Console](/images/realm-console.png)

### Befehlsbeispiel

Wenn ein Benutzer Folgendes in den Realm Console-Kanal eingibt:

`gamemode c @a`

Wird der Realm versuchen auszuführen:

- `gamemode c @a`  
  (Alle Spieler in den Kreativmodus setzen)

### Relay Account-Verhalten und Zielauswahl

Befehle werden **als der Relay Account** ausgeführt. Dies ist wichtig bei der Verwendung von Selektoren oder spielerspezifischen Befehlen.

Zum Beispiel:
- Wenn der Relay Account Realm Bot ist und ein Befehl ausgeführt wird, der auf den Ausführenden abzielt (z. B. ein Befehl, der implizit den Absender betrifft), kann der Relay Account betroffen sein.

Dies ist besonders relevant bei:
- Verwendung von `@s`
- Befehlen, die davon ausgehen, dass der Ausführende ein Spieler ist
- Befehlen ohne explizite Ziele

> **Wichtig:** Wenn du spielerspezifische Befehle ausführst, gib immer explizite Ziele an (zum Beispiel `@a`, `@p`, einen Benutzernamen oder eine markierte Gruppe), um unbeabsichtigte Auswirkungen auf den Relay Account zu vermeiden.

### Voraussetzungen

Um die Realm Console zu verwenden, benötigst du:

- Einen konfigurierten und funktionierenden **Chat Relay Account**, der mit dem Realm verbunden ist.
- Der Relay Account muss aktiv im Realm präsent sein (im Spiel).
- Einen festgelegten Discord-Kanal, der als Realm Console ausgewählt wurde.

Wenn der Relay Account nicht im Spiel ist, können keine Befehle ausgeführt werden.

### Zugriffskontrolle und Sicherheit

Die Realm Console ist konstruktionsbedingt hochprivilegiert. Jeder Benutzer, der Nachrichten im Konsolenkanal senden kann, kann versuchen, Befehle im Realm auszuführen.

Aus diesem Grund solltest du:

- Den Kanal einschränken, sodass nur **vertrauenswürdige In-Game-Administratoren** Zugriff haben.
- Allgemeine Mitglieder daran hindern, den Konsolenkanal zu sehen oder darin zu posten.
- Die Konsolenausgabe als operative Infrastruktur behandeln, nicht als Community-Chat.

Mangelnde Absicherung dieses Kanals kann zu Folgendem führen:
- Missbrauch von Befehlen
- Griefing-Aktionen
- Nicht autorisierte administrative Änderungen
- Versehentliche Störungen durch Fehlbedienung

### Syntaxfehler und sichere Nutzung

Wenn eine Nachricht kein gültiger Befehl ist oder falsche Syntax enthält, gibt Minecraft einen **Syntaxfehler** zurück.

Dies ist erwartetes Verhalten.

Um unnötige Störungen zu vermeiden:
- Stelle sicher, dass dein Befehl korrekt ist, bevor du ihn sendest.
- Vermeide Unterhaltungsnachrichten im Konsolenkanal.
- Verwende ein striktes Format und erwäge, Nutzungshinweise oben im Kanal anzupinnen.

### Empfohlene Betriebspraktiken

Um die Realm Console zuverlässig und sicher zu halten:

- Verwende einen dedizierten Kanal wie `#realm-console` oder `#console`.
- Beschränke den Zugriff auf eine kleine Gruppe vertrauenswürdiger Mitarbeiter.
- Ermutige Mitarbeiter, komplexe Befehle in einer kontrollierten Umgebung zu testen, bevor sie sie in Produktion ausführen.
- Bevorzuge gezielte Befehle (`@a`, Tags, Benutzernamen) gegenüber mehrdeutigen oder ausführerabhängigen Befehlen.

Wenn du Hilfe bei der Konfiguration der Realm Console für deinen Realm benötigst, eröffne ein Support-Ticket und gib Folgendes an:
- Den Realm-Namen
- Den Namen des Konsolenkanals
- Bestätigung, dass der Relay Account im Spiel ist
- Einen Beispielbefehl, der fehlschlägt, und die resultierende Fehlerausgabe (falls vorhanden)
