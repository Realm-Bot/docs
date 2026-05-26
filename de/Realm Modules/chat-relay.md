---
label: Chat Relay
description: Verbinde deinen Realm und Discord mit einer bidirektionalen Chat-Brücke, einschließlich konfigurierbarer Nachrichtentypen, Emote-Weiterleitung und integrierter Anti-Spam-Steuerungen.
order: 86
image: /images/custom/chat-relay.png
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Chat Relay

Chat Relay ist eine **bidirektionale Kommunikationsbrücke** zwischen deinem **Minecraft Bedrock Realm-Chat** und einem ausgewählten **Discord-Kanal**. Es ist darauf ausgelegt, Staff und Community-Mitglieder in Echtzeit abzustimmen, den Plattformwechsel zu reduzieren, die Reaktionszeit zu verbessern und bessere Sichtbarkeit während Vorfällen und Events zu bieten.

---

## Was Chat Relay weiterleitet

Chat Relay kann je nach Konfiguration mehrere Kategorien von Aktivitäten von Minecraft an Discord weiterleiten:

- **Spieler-Chatnachrichten** - Standardnachrichten, die von Spielern im Realm-Chat gesendet werden
- **Tellraw-Nachrichten** - befehlsgenerierte formatierte Ausgaben (Ankündigungen, geskriptete Events, Systemausgaben)
- **Todesnachrichten** - Spieler-Todesbenachrichtigungen für Gameplay-Sichtbarkeit und Moderationsüberprüfung
- **Spieler-Emotes** - von Spielern im Spiel ausgeführte Emotes (nützlich für soziale Sichtbarkeit und Aktivitätskontext)

> **Hinweis:** Chat Relay ist ein Kommunikationswerkzeug. Es "sichert" oder "schützt" einen Realm nicht eigenständig. Alle weitergeleiteten Inhalte unterliegen weiterhin deinen Realm-Regeln und Discord-Richtlinien.

---

## Voraussetzungen

Um Chat Relay zuverlässig zu nutzen, stelle sicher, dass Folgendes vorhanden ist:

- Ein Realm, der über den autorisierten Kontoverknüpfungsablauf mit Realm Bot verbunden ist
- Ein Discord-Kanal, der für die Relay-Ausgabe vorgesehen ist (dringend empfohlen)
- Alle erforderlichen In-Game-Ausführungskomponenten für deine Bereitstellung (zum Beispiel, wenn deine Konfiguration eine In-Game-Relay-Präsenz erfordert)

---

## Einrichtung

1. Öffne das **Chat Relay**-Modul im Realm Bot Dashboard.  
   ![Chat Relay Konfiguration](/images/chat-relay.png)

2. Aktiviere **Chat Relay** mit dem Hauptschalter.

3. Lege den **Discord-Zielkanal** fest (hierhin werden Realm-Nachrichten gepostet).

4. Aktiviere unter **Nachrichtentypen** die Kategorien, die du weiterleiten möchtest:
   - Spieler-Chatnachrichten
   - Tellraw-Nachrichten
   - Todesnachrichten
   - Spieler-Emotes

Sobald aktiviert, beginnt die Relay-Ausgabe, wenn relevante Events im Realm auftreten.

---

## Anti-Spam-Konfiguration

Chat Relay enthält ein **Anti-Spam**-System, das darauf ausgelegt ist, Discord-seitigen Spam zu reduzieren und zu verhindern, dass der Relay-Kanal bei hoher Aktivität oder Missbrauchsversuchen überflutet wird.

Die Anti-Spam-Steuerungen wenden eine einfache Schwellenwertregel an:

- **Nachrichtenschwellenwert** - die maximale Anzahl von Nachrichten, die erlaubt sind, bevor das System auslöst
- **Zeitfenster (Sekunden)** - das Zeitfenster, das zur Zählung der Nachrichten verwendet wird

Beispiellogik:
- Wenn **Schwellenwert = 10** und **Zeitfenster = 10 Sekunden**, dann lösen mehr als 10 Relay-Events innerhalb von 10 Sekunden das Anti-Spam-Verhalten für dieses Zeitfenster aus.

Betriebshinweise:
- Beginne konservativ für öffentliche Communities (z.B. 10-15 Nachrichten in 10-15 Sekunden)
- Erhöhe die Schwellenwerte für Server mit hohem Aufkommen, bei denen Relay-Spam während Events erwartet wird
- Kombiniere Anti-Spam mit Discord-Slowmode, wenn dein Relay-Kanal öffentlich zugänglich ist

> **Wichtig:** Wenn Schwellenwert/Zeitfenster auf extrem niedrige Werte gesetzt werden, kann dies legitime Aktivität unterdrücken. Passe dies schrittweise basierend auf realem Traffic an.

---

## Spieler-Emotes

Wenn **Spieler-Emotes** aktiviert sind, leitet Chat Relay von Spielern im Spiel ausgeführte Emotes an den Discord-Zielkanal weiter.

Dies ist nützlich für:
- dem Staff ein klareres Bild der In-Game-Interaktion zu geben (insbesondere in sozialen Bereichen)
- die Community-"Präsenz" in Discord zu verbessern, ohne dem Spiel beizutreten
- das Aktivitätsbewusstsein während Events zu verstärken

Empfehlungen:
- Aktiviere Emotes nur, wenn dein Relay-Kanal community-orientiert ist oder wenn das Staff ausdrücklich Verhaltenskontext wünscht
- Deaktiviere Emotes in reinen Staff-Betriebskanälen, in denen das Signal-Rausch-Verhältnis entscheidend ist

---

## Empfohlene Konfiguration

Für einen sauberen, professionellen Relay-Kanal, der auch bei Spitzenaktivität nutzbar bleibt:

- Verwende einen dedizierten Kanal wie `#realm-chat`, `#chat-relay` oder `#realm-live`.
- Aktiviere nur die Nachrichtentypen, die du tatsächlich benötigst:
  - Öffentliche Communities: **Spieler-Chat** + (optional) **Todesnachrichten** + (optional) **Emotes**
  - Staff-Betrieb: **Spieler-Chat** + **Tellraw** (Systeme/Events), normalerweise ohne Emotes
- Aktiviere **Anti-Spam**, wenn dein Realm Aktivitätsspitzen oder wiederholte Störungsversuche erlebt.
- Behandle den Relay-Kanal als Erweiterung des In-Game-Chats; setze die gleichen Regeln durch.

---

## Discord-Berechtigungen

Realm Bot muss im Zielkanal diese Berechtigungen haben:

- **View Channel**
- **Send Messages**
- **Read Message History**

Empfohlen (je nach Formatierung/Ausgabe):
- **Embed Links** (wenn das Relay in deiner Bereitstellung Embed-Ausgabe verwendet)

Wenn keine Relay-Ausgabe erscheint, sollten die Kanalberechtigungen als Erstes überprüft werden.

---

## Fehlerbehebung

### Nichts wird weitergeleitet

Überprüfe Folgendes der Reihe nach:
- Chat Relay ist für den richtigen Realm aktiviert
- Der richtige Discord-Zielkanal ist ausgewählt
- Realm Bot hat View Channel + Send Messages Berechtigung
- Alle erforderlichen In-Game-Abhängigkeiten für deine Konfiguration sind online/verbunden

### Relay ist zu laut

- Deaktiviere **Emotes**
- Aktiviere **Anti-Spam** mit einem moderaten Schwellenwert/Zeitfenster
- Erwäge Discord-Slowmode
- Beschränke, wer im Relay-Kanal sprechen kann (wenn Discord -> Realm-Weiterleitung in deinem Setup aktiviert ist)

### Nachrichten erscheinen verzögert oder inkonsistent

- Bestätige, dass der Realm stabil ist und das Relay-Konto/die Sitzung sich nicht ständig trennt
- Stelle sicher, dass der Anti-Spam-Schwellenwert bei normalem Gebrauch keine legitime Ausgabe unterdrückt

---
