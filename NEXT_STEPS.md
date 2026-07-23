# BudgetApp Next Steps

Stand: 2026-07-23

Diese Datei beschreibt nur bekannte, realistisch offene Punkte. Sie soll bei
groesseren Aenderungen aktualisiert werden.

## Aktueller Stand

- Aktuelle dokumentierte App-Version: `v1.6`
- Architektur: statische PWA, hauptsaechlich `index.html`
- Kein Build-Schritt
- Keine Paketmanager- oder Lockfile-Abhaengigkeiten
- Datenhaltung: `localStorage`
- Oeffentliche Projektbeschreibung: `README.md` und `README_de.md`
- Versionshistorie: `CHANGELOG.md`

## Prioritaet 1

- `README.md` und `README_de.md` bei naechster Dokumentationspflege mit dem
  aktuellen Funktionsstand abgleichen. Aus dem Code und `CHANGELOG.md` ist
  JSON-Backup vorhanden; in den README-Featurelisten ist es aktuell nicht als
  eigener Punkt sichtbar.
- Vor jedem Release pruefen, ob alle Versionsstellen synchron sind:
  `index.html`, `CHANGELOG.md`, `version.json`, `sw.js` und eingebetteter
  Service-Worker-Code in `index.html`.
- Bei jeder Aenderung an sichtbaren Texten DE/EN-I18N synchron halten.

## Prioritaet 2

- Manuelle Test-Checkliste fuer die wichtigsten Workflows dokumentieren oder
  in `PROJECT_CONTEXT.md` erweitern, sobald ein wiederholbarer Ablauf feststeht.
- JSON-Backup/Restore gezielt mit alten und neuen Datenformen pruefen, bevor
  darauf eine weitere App, z.B. eine moegliche macOS-Schwester-App, aufbaut.
- PWA-/Offline-Verhalten nach Aenderungen an Service Worker, Manifest, Icons
  oder externen Ressourcen erneut testen.

## Geplante Verbesserungen

- Moegliche macOS-Schwester-App als separates SwiftUI-Projekt, nicht als Umbau
  der PWA. Das JSON-Backupformat soll dabei als Datenaustausch-Bruecke dienen.
- Bei Bedarf Import-Vorschau fuer Excel- oder JSON-Import verbessern.
- Bei Bedarf Barrierefreiheit der Icon-Buttons und Tastaturbedienung weiter
  pruefen.

## Bekannte Einschraenkungen

- Es gibt aktuell keine automatisierte Testsuite im Repository.
- Es gibt aktuell keine CI-Konfiguration im Repository.
- Vollstaendige Browser-/PWA-Kompatibilitaet ist nicht in dieser Datei
  abschliessend verifiziert.

## Nicht Offen Oder Nicht Belegt

- Keine offenen Bugs sind in der vorhandenen Markdown-Dokumentation eindeutig
  dokumentiert.
- Keine geplante Release-Version ist dokumentiert.
- Keine globale Entwicklungsabhaengigkeit ist aus diesem Projekt abzuleiten.
