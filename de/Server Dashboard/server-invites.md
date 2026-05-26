---
label: Einladungslinks
description: Erstelle sichere, teilbare Einladungslinks (realmbot.link/...), die es Spielern ermöglichen, deinen Minecraft Bedrock Realms über einen kontrollierten, nachvollziehbaren Ablauf mit optionaler VPN/Tor-Blockierung beizutreten.
order: 90
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Einladungslinks

Einladungslinks ermöglichen es dir, **kurze, teilbare URLs** zu generieren (zum Beispiel `realmbot.link/my-realm`), die Spieler zu einem ausgewählten **Minecraft Bedrock Realm** einladen, der mit deinem Discord-Server verknüpft ist. Dieses System bietet eine sicherere Alternative zur öffentlichen Verteilung offizieller Realm-Einladungscodes und reduziert wiederholten Missbrauch durch bösartige Bot-Konten.

> **Plattform-Hinweis:** Einladungslinks sind für **Minecraft Bedrock Realms** vorgesehen.

![Realm-Einladungsverwaltung](/images/realm-invites-management.png)

---

## Wofür Einladungslinks gedacht sind

Einladungslinks helfen Realm-Besitzern:

- Eine Realm-Einladung über einen **kontrollierten Beitrittsablauf** zu teilen, anstatt einen rohen Realm-Code offenzulegen
- **Grundlegende Sicherheitsprüfungen** durchzusetzen (wie VPN/Hosting/Tor-Blockierung, sofern aktiviert)
- Die Nutzung mit **maximaler Verwendungsanzahl** und **Ablaufdaten** einzuschränken
- Links schnell zu deaktivieren oder zu rotieren, wenn ein Link geleakt oder angegriffen wird

Diese Funktion ist besonders wertvoll für öffentliche Communities, die ihren Realm regelmäßig bewerben und eher Ziel von störenden Beitrittsversuchen werden.

---

## Wie der Beitritt funktioniert (Spielererfahrung)

Wenn ein Benutzer einen Einladungslink in seinem Browser öffnet, wird er zu einer dedizierten Einladungsseite für den Realm weitergeleitet.

![Einladungsannahme-Seite](/images/realm-invite-accept.png)

Um die Einladung anzunehmen, wird der Benutzer gebeten, sich sicher mit seinem **Microsoft-Konto** anzumelden. Nach der Annahme:

- wird die Realm-Einladung auf sein Microsoft-Konto angewendet
- erscheint der Realm in seiner **Minecraft-Realm-Liste** im Spiel
- kann er dem Realm normal über Minecraft beitreten

> **Sicherheitshinweis:** Benutzer authentifizieren sich über den standardmäßigen Microsoft-Anmeldeablauf. Spieler sollten sich nur auf Seiten anmelden, denen sie vertrauen, und die Domain vor dem Fortfahren überprüfen.

---

## Sicherheitseinstellungen

Einladungslinks enthalten Sicherheitsoptionen, die häufige Missbrauchsmuster abmildern sollen.

### VPN/Hosting/Tor blockieren
Wenn aktiviert, können Spieler, die versuchen, Einladungslinks über VPNs, Hosting-Anbieter oder Tor zu nutzen, am Abschluss des Einladungsablaufs gehindert werden.

Dies wird empfohlen für:
- Öffentliche Einladungswerbung
- Realms, die häufig Ziel von Bann-Umgehung sind
- Communities, die wiederholt "Wegwerfkonto"-Beitrittsverhalten erleben

---

## Einen neuen Einladungslink erstellen

Verwende die Schaltfläche **Link erstellen**, um einen neuen Einladungslink zu generieren.

![Link erstellen Modal](/images/realm-invites-create-link.png)

### Link-Details

Beim Erstellen eines Links kannst du konfigurieren:

- **Realm**  
  Wähle, für welchen verbundenen Realm die Einladung gelten soll.

- **Maximale Verwendungen** (optional)  
  Begrenze, wie viele erfolgreiche Beitritte der Link ermöglicht.  
  Leer lassen für unbegrenzt.

- **Ablaufdatum** (optional)  
  Lege ein Datum/eine Uhrzeit fest, zu der der Link automatisch aufhört zu funktionieren.  
  Leer lassen für kein Ablaufdatum.

Betriebliche Empfehlungen:
- Verwende **Maximale Verwendungen** für kurzfristige Werbeaktionen, Events oder kontrolliertes Onboarding.
- Verwende ein **Ablaufdatum** für öffentliche Werbung, damit Links sich im Laufe der Zeit natürlich rotieren.
- Erstelle separate Links für verschiedene Kampagnen (TikTok, Discord, Partnerserver), damit du eine Quelle deaktivieren kannst, ohne andere zu stören.

---

## Bestehende Links verwalten

Sobald erstellt, erscheinen Links in der Einladungslinks-Tabelle.

![Einladungslinks-Tabelle](/images/realm-invites-table.png)

Jeder Eintrag zeigt typischerweise:

- **Realm** - welcher Realm vom Link angesprochen wird  
- **Slug / URL** - der Kurzlink, den Spieler öffnen  
- **Verwendungen** - aktuelle Verwendungen vs. Limit (oder unbegrenzt)  
- **Läuft ab in** - Zeit bis zum Ablauf (oder "Nie")  
- **Status** - Schalter zum schnellen Aktivieren/Deaktivieren des Links  
- **Aktionen** - häufige Aktionen umfassen das Kopieren und Löschen des Links

### Empfohlener Workflow
- Wenn ein Link missbraucht wird, **deaktiviere ihn sofort** über den Status-Schalter.
- Wenn du einen Link dauerhaft außer Betrieb nehmen möchtest, **lösche** ihn und erstelle einen Ersatz.
- Behalte ältere Links als deaktiviert statt gelöscht, wenn du eine Aufzeichnung darüber haben möchtest, was wo geteilt wurde.

---

## Empfohlene Vorgehensweisen

- Behandle Einladungslinks als **öffentliche Einstiegspunkte**. Teile nur, was du brauchst, wo du es brauchst.
- Bevorzuge **kurze Ablaufzeiten** für öffentlich gepostete Links und rotiere dann regelmäßig.
- Aktiviere **VPN/Hosting/Tor-Blockierung**, wenn du einen Realm mit öffentlichem Code betreibst oder wiederholten Missbrauch erlebst.
- Verwende verschiedene Links für verschiedene Plattformen, damit du die Quelle von Aktivitätsspitzen identifizieren kannst.
- Behalte mindestens einen "Nur-Mitarbeiter"-Link, der nie öffentlich geteilt wird, für vertrauenswürdiges Onboarding.

---

## Fehlerbehebung

### Der Link öffnet sich, aber der Spieler kann die Einladung nicht annehmen
- Bestätige, dass der Link **aktiviert** ist.
- Überprüfe, ob der Link **abgelaufen** ist oder die **maximale Verwendungsanzahl** erreicht hat.
- Wenn VPN-Blockierung aktiviert ist, stelle sicher, dass der Spieler kein VPN/Proxy/Tor verwendet.

### Der Spieler hat angenommen, aber der Realm erscheint nicht in Minecraft
- Bitte den Spieler zu bestätigen, dass er sich mit dem **richtigen Microsoft-Konto** angemeldet hat.
- Lass ihn Minecraft neustarten und die Realm-Liste aktualisieren.
- Wenn er die Einladung mit einem anderen Microsoft-Konto angenommen hat, muss er den Vorgang mit dem beabsichtigten Konto wiederholen.

### Ein Link wird angegriffen
- Deaktiviere den Link sofort über den Status-Schalter.
- Erstelle einen neuen Link mit engerer **maximaler Verwendungsanzahl** und einem **Ablaufdatum**.
- Erwäge die Aktivierung von VPN/Hosting/Tor-Blockierung, falls noch nicht aktiviert.

---
