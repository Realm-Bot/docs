---
label: Kontoverknüpfung
description: Konfiguriere, wie Mitglieder ihr Minecraft-Konto mit Discord verknüpfen, einschließlich automatischer Rollenzuweisung, optionaler Spitznamen-Synchronisierung, automatischer Einladungen zu ausgewählten Realms und Beitrittsprotokoll-Berichten.
order: 97
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Kontoverknüpfung

Die Kontoverknüpfung ermöglicht es Mitgliedern, ihre **Minecraft (Microsoft/Xbox)**-Identität mit ihrem **Discord**-Konto zu verknüpfen. Sobald aktiviert, kann Realm Bot häufige Onboarding-Aufgaben wie **Rollenzuweisung** und **Realm-Einladungen** automatisieren und gleichzeitig übersichtliche Prüfprotokolle für Mitarbeiter bereitstellen.

![Kontoverknüpfung Konfiguration](/images/server-account-linking.png)

---

## Wofür die Kontoverknüpfung gedacht ist

Die Kontoverknüpfung soll dir helfen:

- Zu verifizieren, dass ein Discord-Mitglied das Minecraft-Konto kontrolliert, das es beansprucht
- Automatisch Rollen zu vergeben, wenn ein Mitglied sich erfolgreich verknüpft
- Optional Discord-Spitznamen an Minecraft-Benutzernamen anzupassen
- Verknüpfte Benutzer automatisch zu einem oder mehreren verbundenen Realms einzuladen
- Verknüpfungsereignisse in einem dedizierten Kanal für Transparenz zu protokollieren

---

## Benutzereinstellungen

Diese Einstellungen steuern, ob die Verknüpfung aktiviert ist und wie sie sich für Benutzer verhält.

### Kontoverknüpfung
Wenn aktiviert, können Mitglieder ihr Minecraft-Konto über den Realm Bot-Verknüpfungsablauf mit Discord verknüpfen.

**Empfohlen:** Aktiviere dies für die meisten Communities, insbesondere für öffentliche oder halböffentliche Server, da es Verifizierung und Automatisierung unterstützt.

### Spitznamen ändern
Wenn aktiviert, aktualisiert Realm Bot den **Discord-Spitznamen** eines Benutzers, um nach der Verknüpfung dem Minecraft-Benutzernamen zu entsprechen.

**Stelle vor der Aktivierung sicher, dass:**
- Realm Bot die Berechtigung **Spitznamen verwalten** in deinem Discord-Server hat
- Die Rolle von Realm Bot **über** den Rollen der Benutzer steht, deren Spitznamen bearbeitet werden sollen (Discord-Rollenhierarchie)
- Deine Serverregeln die Automatisierung von Spitznamen erlauben (einige Communities bevorzugen, dass Mitglieder ihre Spitznamen selbst kontrollieren)

> **Hinweis:** Wenn Berechtigungen oder die Rollenhierarchie Spitznamenänderungen verhindern, kann die Verknüpfung trotzdem erfolgreich sein, aber die Spitznamen-Synchronisierung kann fehlschlagen.

---

## Server-Integration

Diese Einstellungen definieren, was *nach* einer Kontoverknüpfung passiert.

### Rollen für verknüpfte Konten
Wähle eine oder mehrere Discord-Rollen aus, die automatisch zugewiesen werden, wenn ein Mitglied sich erfolgreich verknüpft.

Häufige Anwendungen:
- Zugang zu Mitglieder-exklusiven Kanälen nach Verifizierung gewähren
- Verifizierte Spieler von nicht verifizierten Benutzern trennen
- Moderations- oder Spielrollen anwenden, die an den Kontobesitz gebunden sind

**Empfohlene Vorgehensweise:** Weise nur die minimal erforderliche(n) Rolle(n) für den Zugang zu. Halte Mitarbeiterrollen manuell.

### Automatische Einladung zu Realms
Wähle, welche verbundenen Realm(s) Benutzer automatisch einladen sollen, wenn sie ihr Konto verknüpfen.

Dies ist ideal für:
- Realms mit Whitelist
- Mitglieder-exklusive Realms
- Server, die einen "Verknüpfen → Sofort beitreten"-Onboarding-Ablauf wünschen

**Betriebliche Hinweise:**
- Die automatische Einladung sollte auf vertrauenswürdige Realms beschränkt werden (vermeide automatische Einladungen zu Test-/Admin-Realms).
- Wenn ein Realm im Dropdown fehlt, bestätige, dass er verbunden ist und unter deinem verknüpften Xbox-Kontokontext sichtbar ist.

### Beitrittsprotokoll-Kanal
Wähle einen Discord-Kanal, in dem Realm Bot Kontoverknüpfungsereignisse postet (z. B. erfolgreiche Verknüpfungen, wichtige Ergebnisse und zugehörige Systemnachrichten, sofern unterstützt).

**Empfohlene Einrichtung:**
- Verwende einen nur für Mitarbeiter zugänglichen Kanal (z. B. `#join-logs` oder `#verification-logs`)
- Stelle sicher, dass Realm Bot folgende Berechtigungen hat:
  - **Kanal anzeigen**
  - **Nachrichten senden**
  - **Nachrichtenverlauf lesen** (empfohlen)

---

## Empfohlene Konfiguration

Für die meisten Server ist dies die sauberste Konfiguration:

1. **Kontoverknüpfung** aktivieren
2. **Rollen für verknüpfte Konten** auf eine Standard-Mitgliederrolle setzen (z. B. `Member` / `Verified`)
3. **Automatische Einladung zu Realms** nur für deinen primären öffentlichen/Mitglieder-Realm aktivieren
4. Einen dedizierten **Beitrittsprotokoll-Kanal** festlegen
5. **Spitznamen ändern** nur aktivieren, wenn dein Mitarbeiterteam eine einheitliche Identitätskonsistenz wünscht

---

## Fehlerbehebung

### Rollen werden nicht zugewiesen
- Bestätige, dass die ausgewählte Rolle existiert und noch ausgewählt ist.
- Stelle sicher, dass die Rolle von Realm Bot **über** der/den Zielrolle(n) in der Discord-Rollenhierarchie steht.
- Überprüfe, ob Realm Bot die Berechtigung **Rollen verwalten** hat.

### Spitznamen werden nicht geändert
- Stelle sicher, dass **Spitznamen ändern** aktiviert ist.
- Stelle sicher, dass Realm Bot die Berechtigung **Spitznamen verwalten** hat.
- Überprüfe die Rollenhierarchie: Realm Bot muss über der höchsten Rolle des Mitglieds stehen.

### Automatische Einladung sendet keine Einladungen
- Bestätige, dass der Realm unter **Automatische Einladung zu Realms** ausgewählt ist.
- Überprüfe, ob der Realm verbunden ist und unter dem verknüpften Xbox-Kontokontext verfügbar ist.
- Wenn dein Realm strenge Mitgliederlimits hat, stelle sicher, dass Kapazität für neue Einladungen vorhanden ist.

---
