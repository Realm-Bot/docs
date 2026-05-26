---
label: Bot Detection
description: Schütze öffentliche Realms vor schadhaften Bot-Konten, indem verdächtige Verbindungen automatisch erkannt und entfernt werden. Enthält einen experimentellen Modus für erweiterte Erkennung.
order: 70
image: /images/custom/botdetection.png
author:
  name: Frazer
  avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

### Was ist Bot Detection?

Bot Detection ist eine Schutzfunktion, die dazu dient, schadhafte **Bot-Konten** abzuwehren, die Realms beitreten, um **Latenzen**, **Leistungseinbußen** oder **Spielstörungen** zu verursachen. Sie ist in erster Linie für Realms gedacht, die **öffentliche Einladungscodes** verwenden, bei denen automatisierte Beitrittsversuche häufiger vorkommen.

> **Wichtig:** Bot Detection reduziert Risiken und Störungen, kann aber keine absolute Sicherheit garantieren. Minecraft Realms unterliegen Plattformbeschränkungen, und die Erkennung basiert auf beobachtbarem Verhalten beim Beitritt.

### Wann Bot Detection empfohlen wird

Bot Detection eignet sich am besten für:
- **Realms mit öffentlichem Code** (offener Zugang, häufig geteilte Codes)
- Realms, die wiederholt **Beitrittswellen**, **Lag-Spitzen** oder **verdächtige neue Konten** erleben
- Communities, die bessere Stabilität während Stoßzeiten oder Events benötigen

Für private Realms mit Einladungen ist Bot Detection möglicherweise unnötig, es sei denn, du erlebst aktiv verdächtige Beitrittsmuster.

### Wie Bot Detection funktioniert

Wenn aktiviert, beobachtet Bot Detection die Beitrittsaktivität und wendet automatisierte Gegenmaßnahmen auf Konten an, die bösartig oder automatisiert erscheinen. Dies soll dein Realm stabil halten, indem störendes Beitrittsverhalten, das häufig mit Bot-Aktivität verbunden ist, reduziert wird.

Bot Detection erfordert, dass ein **Relay Account im Spiel ist**, um zu funktionieren. Wenn der Relay Account nicht online im Realm ist, kann Bot Detection seine Gegenmaßnahmen nicht ausführen.

### Erkennungsmodi

Bot Detection umfasst derzeit zwei Erkennungsmodi:

- **Reguläre Bot Detection**  
  Der Standard-Erkennungsmodus. Dies ist die empfohlene Standardeinstellung und ist für die meisten öffentlichen Realms in der Regel ausreichend.

- **Experimentelle Bot Detection (Beta)**  
  Ein aggressiverer Erkennungsmodus, der darauf ausgelegt ist, raffinierteres Bot-Verhalten zu identifizieren.  
  **Dieser Modus kann gelegentlich legitime Spielerkonten markieren.** Aktiviere ihn mit Vorsicht und nur wenn nötig.

> **Vorsicht:** Wenn du die experimentelle Bot Detection aktivierst, stelle sicher, dass Mitarbeiter bereit sind, schnell auf Meldungen von betroffenen legitimen Spielern zu reagieren.

### Voraussetzungen

Um Bot Detection zu verwenden, benötigst du:

- Einen konfigurierten **Relay Account**, der aktiv **im Spiel** ist.
- Bot Detection muss im Realm Bot Dashboard aktiviert sein.

### Einrichtung

1.  Öffne das **Bot Detection**-Modul im Realm Bot Dashboard.<br/>
    ![Bot Detection Konfiguration](/images/bot-detection.png)
2.  Aktiviere **Bot Detection** mit dem Hauptschalter.
3.  Wähle unter **Erkennungseinstellungen** eine der folgenden Optionen:
    - Standardmäßig ist **Reguläre Bot Detection** aktiviert
    - Aktiviere optional **Experimentelle Bot Detection (Beta)**, wenn dein Realm weiterhin Bot-Aktivität erlebt
4.  Bestätige, dass dein Relay Account **online im Realm** ist, da Bot Detection einen In-Game-Ausführer benötigt, um zu funktionieren.

### Empfohlene Konfiguration

Für die meisten öffentlichen Realms:
- Aktiviere **Reguläre Bot Detection**
- Lasse **Experimentelle Bot Detection** deaktiviert, es sei denn, Bot-Aktivität hält an

Aktiviere **Experimentelle Bot Detection** nur wenn:
- Der reguläre Modus bei wiederholter Bot-Aktivität nicht ausreicht
- Du das Risiko gelegentlicher Fehlerkennungen tolerieren kannst
- Mitarbeiter verfügbar sind, um Streitfälle schnell und professionell zu bearbeiten

### Empfohlene Vorgehensweise

- Beschränke den Zugang zu öffentlichen Codes, wo möglich (rotiere Codes, wenn Missbrauch andauert).
- Halte den Relay Account zuverlässig online während Hochrisikozeiten (Stoßzeiten, Events, nachdem ein Code öffentlich geteilt wurde).
- Behandle die experimentelle Erkennung als Eskalationswerkzeug, nicht als Standardeinstellung.
- Pflege ein klares Verfahren für Mitarbeiter zur Bearbeitung von Fehlerkennungsmeldungen (erfasse den Spielernamen, die Beitrittszeit und was beobachtet wurde).

### Häufige Probleme

**Bot Detection ist aktiviert, aber nichts passiert**
- Bestätige, dass der Relay Account **im Spiel** ist.
- Überprüfe, ob der richtige Realm im Dashboard ausgewählt ist.
- Stelle sicher, dass die Modulschalter gespeichert sind und aktiviert bleiben.

**Legitime Spieler werden markiert**
- Deaktiviere **Experimentelle Bot Detection** sofort.
- Verwende weiterhin **Reguläre Bot Detection** und beobachte das Beitrittsverhalten.
- Wenn Fehlerkennungen anhalten, belasse die Funktion im regulären Modus und erwäge zusätzliche Zugangskontrollen (z. B. Einschränkung der Code-Verteilung).
