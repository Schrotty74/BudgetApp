# BudgetApp Project Context

Stand: 2026-07-23

Diese Datei ist die Haupt-Wissensquelle fuer neue Codex-Chats und fuer die
Fortsetzung nach einer Mac-Neuinstallation.

## Zuerst Lesen

1. `PROJECT_CONTEXT.md` fuer Architektur, Regeln und aktuellen Projektkontext
2. `NEXT_STEPS.md` fuer offene Aufgaben und Prioritaeten
3. `CHANGELOG.md` fuer Versionshistorie
4. `README.md` und `README_de.md` fuer oeffentliche Projektbeschreibung
5. `PORTFOLIO_UPDATE.md` vor jeder oeffentlichen Veroeffentlichung

Bei wichtigen Projektentscheidungen, groesseren Funktionsaenderungen oder neuen
bekannten Problemen muessen `PROJECT_CONTEXT.md` und `NEXT_STEPS.md`
aktualisiert werden.

## Projektziel

BudgetApp ist eine einfache Progressive Web App zur lokalen Verwaltung eines
Haushaltsbudgets. Nutzer koennen monatliche Einnahmen und Ausgaben erfassen,
bearbeiten, importieren, exportieren und offline verwenden.

Die App ist bewusst klein gehalten:

- kein Backend
- kein Login
- kein Tracking
- keine Server-Speicherung
- lokale Datenhaltung im Browser

## Architektur

Die App ist eine Single-File-Web-App mit wenigen statischen Begleitdateien.

Wichtige Dateien:

- `index.html`: komplette App-Logik, UI, CSS und Vanilla-JavaScript
- `sw.js`: Service Worker fuer Offline-Cache und Benachrichtigungen
- `manifest.json`: PWA-Manifest
- `version.json`: Versionssignal fuer den Update-Hinweis
- `CHANGELOG.md`: Versionshistorie
- `README.md`: englische oeffentliche Projektbeschreibung
- `README_de.md`: deutsche oeffentliche Projektbeschreibung
- `PORTFOLIO_UPDATE.md`: Regel fuer Portfolio-/Profil-Aktualisierungen
- `demo.xlsx`: Demo-Excel-Datei
- `icons/`: PWA-Icons
- `screenshots/`: oeffentliche Demo-Screenshots

Es gibt keinen Framework-, Paketmanager- oder Build-Schritt.

## Externe Abhaengigkeiten

Die App nutzt externe Ressourcen direkt im Browser:

- SheetJS ueber CDN fuer Excel-Import und Excel-Export
- Google Fonts ueber CSS-Import

Nach der Abhaengigkeits-Checkliste gilt:

- Diese Abhaengigkeiten sind projektgebunden und im App-Code referenziert.
- Sie sollen nicht global installiert und nicht automatisch in eine allgemeine
  Entwicklungsumgebung aufgenommen werden.
- Es gibt aktuell keine allgemeine, wiederkehrende Entwicklungsabhaengigkeit,
  die aus diesem Projekt heraus zur globalen Installation vorgeschlagen werden
  muss.

Lokale Pruefung kann mit einem einfachen statischen HTTP-Server erfolgen, zum
Beispiel:

```bash
python3 -m http.server 8087
```

Dann die App im Browser unter `http://127.0.0.1:8087/` oeffnen.

Wenn Bash-spezifische Skripte oder Inline-Befehle noetig sind, die moderne
Bash-Funktionen verwenden, soll die Homebrew-Bash genutzt werden:

```bash
/opt/homebrew/bin/bash scriptname.sh
/opt/homebrew/bin/bash -lc '...'
```

Die normale Login-Shell bleibt `zsh`.

## Datenformate und Speicherung

Primaere App-Daten liegen in `localStorage`.

Bekannte Schluessel:

- `budgetData`: Einnahmen und Ausgaben
- `budgetLang`: Spracheinstellung (`de` oder `en`)
- `budgetTheme`: Theme (`dark` oder `light`)
- `sectionState`: Zustand eingeklappter Sektionen
- `updateCheck`: Zeitstempel und zuletzt erkannte Online-Version
- `reminderEnabled`: aktivierte/deaktivierte Erinnerung
- `reminderTime`: Uhrzeit der taeglichen Erinnerung
- `reminderLastSent`: letzter Erinnerungstag

Interne Ausgaben-Frequenzen werden deutsch gespeichert:

- `Monatlich`
- `Alle 2 Monate`
- `Quartalsweise`
- `Jährlich`
- `Variabel`

Die UI uebersetzt diese Werte fuer Deutsch und Englisch.

JSON-Backups enthalten Budgetdaten plus App-Einstellungen. Dieses Format ist
die bevorzugte Bruecke fuer eine moegliche spaetere macOS-Schwester-App.

## Umgesetzte Funktionen

Aus vorhandener Doku und Code ersichtlich:

- Dashboard mit monatlichem Polster, Einnahmen und Ausgaben
- Donut-Chart fuer Ausgaben
- Excel-Import fuer `.xlsx` / `.xls`
- Excel-Export
- PDF-Export
- PNG-Bildexport
- JSON-Backup exportieren und wiederherstellen
- Import-/Export-Dropdown
- Inline-Hinzufuegen, Bearbeiten und Loeschen
- Swipe-to-delete auf Mobilgeraeten
- Anzeige echter Zahlungsbetraege bei nicht-monatlichen Ausgaben
- einklappbare Einnahmen- und Ausgaben-Sektionen
- Dark-/Light-Mode
- Sprachwechsel Deutsch/Englisch
- PWA-Manifest und Installierbarkeit
- Service Worker fuer Offline-Nutzung
- taegliche Erinnerung per Notification API
- Update-Hinweis ueber `version.json`
- Discord- und GitHub-Buttons im Header
- lokale Speicherung ohne Server

## Build-, Test- und Release-Workflow

Build:

- Kein Build-Schritt vorhanden.
- Keine Paketinstallation erforderlich.

Lokaler Lauf:

```bash
python3 -m http.server 8087
```

Manuelle Mindestpruefung nach Aenderungen:

- App lokal oeffnen
- Browser-Konsole auf Fehler pruefen
- Import-/Export-Menue oeffnen
- betroffene Funktion ausfuehren
- Sprachwechsel DE/EN pruefen, wenn sichtbare Texte geaendert wurden
- Dark-/Light-Mode pruefen, wenn UI/CSS geaendert wurde
- Offline-/Service-Worker-Verhalten pruefen, wenn `sw.js`, Cache-Version,
  Icons oder PWA-Dateien geaendert wurden

Versions-/Release-Regeln:

- Version nicht anheben, ausser ein Release wird ausdruecklich verlangt.
- Bei einem Release mindestens aktualisieren:
  - Footer in `index.html` fuer Deutsch und Englisch
  - `CHANGELOG.md`
  - `version.json`
  - Service-Worker-Cache-Version in `sw.js`
  - eingebettete Service-Worker-Cache-Version in `index.html`, solange dieser
    Blob-Service-Worker existiert
- Vor oeffentlicher Veroeffentlichung `PORTFOLIO_UPDATE.md` lesen.
- Keine Tags, Commits oder Pushes ohne ausdrueckliche Anweisung.

## Feste Regeln

- Single-File-Architektur erhalten, ausser eine Aufteilung wird ausdruecklich
  verlangt.
- Keine Frameworks einfuehren.
- Keine neuen externen Abhaengigkeiten ohne klare Notwendigkeit.
- Neue sichtbare Texte immer in beiden Sprachen in der I18N-Struktur pflegen.
- Bestehende localStorage-Daten rueckwaertskompatibel behandeln.
- Offline-first-Verhalten erhalten.
- GitHub-Pages-Kompatibilitaet erhalten.
- Oeffentliche Namen nur als `Schrotty74` dokumentieren.
- Keine lokalen Pfade, Tokens, Zugangsdaten, Backups oder echten privaten
  Finanzdaten dokumentieren oder veroeffentlichen.
- Oeffentliche Screenshots und Demo-Daten muessen synthetisch sein.

## Bekannte Probleme und Einschraenkungen

- Die App nutzt externe CDN-/Font-Ressourcen; deren Offline-Verhalten haengt vom
  Service-Worker-Cache und Browser-Verhalten ab.
- Notification-Funktionen sind browser- und installationsabhaengig; auf iOS/iPadOS
  ist die installierte PWA relevant.
- Automatisierte Tests sind im Repository nicht vorhanden.
- Ein vollstaendiger CI-Workflow ist im Repository nicht vorhanden.
- Weitere offene Punkte stehen in `NEXT_STEPS.md`.

## Datenschutz und Veroeffentlichung

Budgetdaten bleiben lokal im Browser. Es gibt keinen Server, kein Konto und kein
Tracking.

Nicht veroeffentlichen:

- echte Finanzdaten
- private JSON-/Excel-Backups
- lokale Pfade
- Logs mit privaten Daten
- Tokens, Keys, Zertifikate oder Accounts
- Screenshots mit realen Nutzerdaten

Bei Portfolio- oder README-Aktualisierungen nur Demo-Daten verwenden.
