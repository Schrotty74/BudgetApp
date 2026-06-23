# 💶 BudgetApo

**Monatliche Einnahmen & Ausgaben auf einen Blick**

Eine Progressive Web App (PWA) zur einfachen Verwaltung deines Haushaltsbudgets — direkt im Browser, ohne Installation, läuft auch offline.

🇬🇧 [English version](README.md)

---

## ✨ Features

- 📊 **Übersicht** — Monatliches Polster, Einnahmen & Ausgaben auf einen Blick
- 🍩 **Donut-Chart** — Visuelle Aufschlüsselung der Ausgaben-Kategorien
- 📥 **Excel-Import** — `.xlsx` Dateien direkt einlesen (Einnahmen & Ausgaben werden automatisch erkannt)
- ✏️ **Bearbeiten** — Einträge hinzufügen, bearbeiten und löschen
- 💾 **Lokale Speicherung** — Alle Daten bleiben ausschließlich auf deinem Gerät
- 📴 **Offline-fähig** — Service Worker cached die App für die Nutzung ohne Internet
- 📱 **Installierbar** — Als App auf dem iPhone/iPad Home-Bildschirm oder am Desktop speichern

---

## 🔒 Datenschutz

**Keine Daten verlassen dein Gerät.** Der Quellcode enthält keinerlei persönliche Finanzdaten. Alle Einträge werden ausschließlich im lokalen Browser-Speicher (localStorage) gespeichert und sind nur auf deinem Gerät sichtbar.

---

## 📱 Als App installieren

**iPhone / iPad (Safari):**
1. `schrotty74.github.io/BudgetApo` in Safari öffnen
2. Teilen-Symbol antippen
3. „Zum Home-Bildschirm" wählen
4. „Hinzufügen" tippen

**Mac / Windows (Chrome oder Edge):**
1. Die Seite öffnen
2. In der Adressleiste das Install-Symbol antippen
3. „Installieren" bestätigen

---

## 📥 Excel-Import

Die App erkennt `.xlsx` Dateien automatisch, solange sie Abschnitte mit den Bezeichnungen **Einnahmen** und **Ausgaben** enthalten. Beispielformat:



Unterstützte Häufigkeiten: `Monatlich` · `Alle 2 Monate` · `Quartalsweise` · `Jährlich` · `Variabel`

---

## 🛠 Technologie

- Reines HTML / CSS / JavaScript — keine Frameworks, kein Build-Schritt
- [SheetJS](https://sheetjs.com) für den Excel-Import
- Service Worker für Offline-Unterstützung
- localStorage für lokale Datenpersistenz

---

## 📄 Lizenz

GPL-3.0 — siehe [LICENSE](LICENSE)
