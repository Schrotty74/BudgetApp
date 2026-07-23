# New Codex Chat Template

Nutze diese Vorlage fuer einen neuen Codex-Chat zu BudgetApp.

```text
Arbeite im BudgetApp-Projekt.

Lies zuerst:
1. PROJECT_CONTEXT.md
2. NEXT_STEPS.md
3. CHANGELOG.md
4. README.md und README_de.md, wenn die Aenderung oeffentliche Doku betrifft
5. PORTFOLIO_UPDATE.md vor einer oeffentlichen Veroeffentlichung

Wichtige Regeln:
- Single-File-Architektur erhalten, solange keine Aufteilung verlangt wird.
- Kein Framework und keine neue externe Abhaengigkeit ohne klare Begruendung.
- Keine globale Installation von Projektabhaengigkeiten.
- Neue sichtbare Texte immer in Deutsch und Englisch pflegen.
- localStorage-Daten rueckwaertskompatibel behandeln.
- Offline-first und GitHub-Pages-Kompatibilitaet erhalten.
- Version nur anheben, wenn ein Release ausdruecklich verlangt wird.
- Bei Release alle Versionsstellen synchronisieren:
  index.html, CHANGELOG.md, version.json, sw.js und eingebetteter Service Worker.
- Keine lokalen Pfade, Zugangsdaten, Tokens, privaten Backups oder echten
  Finanzdaten dokumentieren oder veroeffentlichen.
- Oeffentliche Namen nur als Schrotty74 verwenden.
- Keine Commits, Tags oder Pushes ohne ausdrueckliche Anweisung.
- Bei wichtigen Aenderungen PROJECT_CONTEXT.md und NEXT_STEPS.md aktualisieren.

Wenn Bash-spezifische Befehle noetig sind, nutze:
/opt/homebrew/bin/bash
```
