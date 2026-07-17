# Projektkontext: Shortcuts

Stand: 2026-07-17

Repository:
`https://github.com/Schrotty74/Shortcuts`

## Projektziel und Zweck

Dieses Repository stellt öffentliche Apple-Kurzbefehle bereit. Es ist als
Sammlung angelegt: Jeder Kurzbefehl lebt vollständig in einem eigenen Ordner
unter `shortcuts/`.

Der erste veröffentlichte Kurzbefehl ist `Wetter für Stadt` in Version `1.0`.

## Architektur und technische Entscheidungen

- Root-Dateien beschreiben nur die Sammlung.
- Jeder Shortcut hat einen eigenen Ordner mit Version, README, Changelog,
  Release Notes, Datenschutzbericht, Prüfsummen, Assets und ZIP.
- Aktueller Shortcut-Ordner:
  `shortcuts/wetter-fuer-stadt/`
- Das ZIP für `Wetter für Stadt` liegt unter:
  `shortcuts/wetter-fuer-stadt/dist/wetter-fuer-stadt-1.0.zip`
- GitHub Actions prüft die erwartete Ordnerstruktur, Prüfsummen und einfache
  Datenschutzindikatoren.
- Der Wetter-Kurzbefehl nutzt öffentliche Open-Meteo-APIs und benötigt keinen
  API-Schlüssel.

## Dateistruktur

```text
Shortcuts/
|-- .github/workflows/release-status.yml
|-- LICENSE
|-- NEXT_STEPS.md
|-- PROJECT_CONTEXT.md
|-- README.md
`-- shortcuts/
    `-- wetter-fuer-stadt/
        |-- CHANGELOG.md
        |-- CHECKSUMS.txt
        |-- PORTFOLIO_UPDATE.md
        |-- PRIVACY_REPORT.md
        |-- README.md
        |-- RELEASE_NOTES.md
        |-- VERSION
        |-- Wetter für Stadt.shortcut
        |-- Wetter_fuer_Stadt.xml
        |-- assets/
        |   `-- social-preview.svg
        `-- dist/
            |-- wetter-fuer-stadt-1.0.zip
            `-- wetter-fuer-stadt-1.0.zip.sha256
```

## Umgesetzte Funktionen

- Öffentliches Repository für Shortcuts eingerichtet.
- Sammlung-Struktur eingeführt: jeder Shortcut in eigenem Unterordner.
- `Wetter für Stadt` Version `1.0` bereitgestellt.
- Signierte `.shortcut`-Datei und XML-Quelle veröffentlicht.
- Wetter-spezifische Version, Changelog, Release Notes, Portfolio-Update,
  Datenschutzbericht, Assets und ZIP in `shortcuts/wetter-fuer-stadt/`
  einsortiert.
- GitHub Actions Release-Status-Automatik eingerichtet.
- GitHub Release `v1.0` mit ZIP und SHA-256-Datei erstellt.

## Wichtige Designentscheidungen

- Keine Shortcut-spezifischen Release-Dateien im Repository-Root.
- Root bleibt für Sammlung, Lizenz, Projektkontext und nächste Schritte.
- Datenschutzbericht ist pro Shortcut Pflichtbestandteil.
- Nicht veröffentlicht werden lokale Arbeitsarchive, Screenshots, `.DS_Store`
  oder private lokale Projektdateien aus dem ursprünglichen Arbeitsordner.

## Bekannte Einschränkungen oder Probleme

- Die Release-Status-Automatik ist eine statische Prüfung und ersetzt kein
  manuelles Datenschutzreview.
- Der Wetter-Kurzbefehl sendet den eingegebenen Stadtnamen und Koordinaten an
  Open-Meteo, wie im Datenschutzbericht beschrieben.
- GitHub Release `v1.0` bleibt ein Release für den Wetter-Kurzbefehl, auch wenn
  das Repository künftig weitere Shortcuts enthält.

## Pflegehinweis

Bei größeren Änderungen, neuen Shortcuts, neuen Releases oder wichtigen
Entscheidungen müssen `PROJECT_CONTEXT.md` und `NEXT_STEPS.md` aktualisiert
werden.
