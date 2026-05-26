---
label: Allowlist
description: Pflege eine Allowlist vertrauenswürdiger Benutzer, die automatisierte Durchsetzungssysteme wie Member Gate, Bot Detection und Skin Filtering umgehen können.
order: 92
authors:
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Allowlist

Die **Allowlist** ist eine Sicherheitskontrolle, die bestimmte Benutzer als vertrauenswürdig kennzeichnet. Benutzer, die zur Allowlist hinzugefügt werden, können **automatisierte Durchsetzungssysteme umgehen**, sodass sichergestellt wird, dass legitime Spieler (Mitarbeiter, Ersteller, Tester, bekannte Community-Mitglieder) nicht fälschlicherweise von Sicherheitssystemen entfernt werden.

![Allowlist](/images/server-allowlist.png)

---

## Was die Allowlist bewirkt

Wenn ein Benutzer auf der Allowlist steht:

- Kann er **Member Gate** umgehen
- Kann er **Bot Detection** umgehen
- Kann er **Skin Filtering** umgehen

Dies ist besonders nützlich, wenn du:
- Strenge Member Gate-Regeln betreibst (Gerätesperren, Gamerscore-Schwellenwerte usw.)
- Experimentelle Bot Detection aktivierst und Schutz vor Fehlalarmen wünschst
- Skin Filtering verwendest und vertrauenswürdige Spieler vor Beta-Fehlalarmen schützen möchtest
- Vertrauenswürdige Zweitkonten, Tester oder Mitarbeiter hast, die häufig beitreten

> **Wichtig:** Die Allowlist ist für Ausnahmen gedacht. Das Hinzufügen zu vieler Benutzer verringert die Wirksamkeit deiner automatisierten Schutzmaßnahmen.

---

## Benutzer hinzufügen

Verwende das Feld **Suchen oder Hinzufügen**, um einen Spieler zu finden und ihn zu deiner Allowlist hinzuzufügen.

Empfohlene Anwendungsfälle:
- Realm-Mitarbeiterkonten
- Verifizierte Community-Mitglieder
- Langjährige Spieler mit bekannten Identitäten
- Testkonten, die während der Entwicklung oder Wartung verwendet werden

---

## Benutzer entfernen

Jeder Allowlist-Eintrag kann über das Löschsymbol auf der rechten Seite der Zeile entfernt werden.

**Empfohlene Vorgehensweise:** Entferne den Zugang, wenn:
- Ein Mitarbeiter zurücktritt
- Ein vertrauenswürdiges Konto den Besitzer wechselt
- Du keine Ausnahmen mehr für einen temporären Tester benötigst

---

## Sicherheitshinweise

### Behandle die Allowlist als privilegierten Zugang
Benutzer auf der Allowlist sind von wichtigen Schutzmaßnahmen ausgenommen. Setze nur Benutzer auf die Allowlist, denen du wirklich vertraust.

### Pflege eine Prüfungsgewohnheit
Überprüfe die Liste regelmäßig (wöchentlich oder monatlich für große Server), besonders wenn dein Realm öffentliche Codes verwendet oder häufigen Verkehr hat.

### Bevorzuge das Anpassen der Regel statt alle auf die Allowlist zu setzen
Wenn viele legitime Spieler blockiert werden, erwäge:
- Member Gate-Bedingungen zu lockern
- Experimentelle Bot Detection zu deaktivieren
- Schwellenwerte anzupassen (z. B. Gamerscore-Kriterien)
- Die Allowlist nur für Grenzfälle zu verwenden

---

## Häufige Fragen

### "Umgeht die Allowlist Banns?"
Nein. Die Allowlist ist dafür gedacht, automatisierte Zugangskontrollsysteme wie Member Gate, Bot Detection und Skin Filtering zu umgehen. Sie überschreibt keine manuellen Banns oder Durchsetzungsmaßnahmen auf Realm-Ebene.

### "Sollten wir alle Mitarbeiter auf die Allowlist setzen?"
Nur Mitarbeiter, die zuverlässigen Zugang benötigen, sollten auf die Allowlist gesetzt werden. Bei größeren Teams erwäge, nur leitende Rollen auf die Allowlist zu setzen und dich für alle anderen auf korrekte Member Gate-Regeln zu verlassen.

---
