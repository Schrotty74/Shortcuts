# Projektkontext: Shortcuts

Stand: 2026-07-17

Repository:
`https://github.com/Schrotty74/Shortcuts`

## Projektziel und Zweck

Dieses Repository stellt öffentliche Apple-Kurzbefehle bereit. Der erste
veröffentlichte Kurzbefehl ist `Wetter für Stadt` in Version `1.0`.

Ziel ist eine saubere öffentliche Veröffentlichung inklusive ZIP-Paket,
Versionsangabe, Datenschutzbericht, Prüfsummen, Release-Status-Automatik und
Portfolio-Hinweisen.

## Architektur und technische Entscheidungen

- Release-Version wird zentral in `VERSION` geführt.
- Release-Dateien liegen unter `shortcuts/wetter-fuer-stadt`.
- Das öffentliche ZIP liegt unter `dist/wetter-fuer-stadt-1.0.zip`.
- Prüfsummen werden mit SHA-256 bereitgestellt.
- GitHub Actions prüft Release-Dateien, Version, Prüfsummen und einfache
  Datenschutzindikatoren.
- Der Kurzbefehl selbst nutzt öffentliche Open-Meteo-APIs und benötigt keinen
  API-Schlüssel.

## Dateistruktur

```text
Shortcuts/
|-- .github/workflows/release-status.yml
|-- CHANGELOG.md
|-- LICENSE
|-- NEXT_STEPS.md
|-- PORTFOLIO_UPDATE.md
|-- PROJECT_CONTEXT.md
|-- README.md
|-- RELEASE_NOTES.md
|-- VERSION
|-- dist/
|   |-- wetter-fuer-stadt-1.0.zip
|   `-- wetter-fuer-stadt-1.0.zip.sha256
`-- shortcuts/
    `-- wetter-fuer-stadt/
        |-- CHECKSUMS.txt
        |-- PRIVACY_REPORT.md
        |-- README.md
        |-- Wetter für Stadt.shortcut
        `-- Wetter_fuer_Stadt.xml
```

## Umgesetzte Funktionen

- Öffentliches Repository für Shortcuts eingerichtet.
- `Wetter für Stadt` Version `1.0` bereitgestellt.
- Signierte `.shortcut`-Datei veröffentlicht.
- XML-Quelle veröffentlicht.
- Release-ZIP und ZIP-Prüfsumme erstellt.
- Datenschutzbericht erstellt.
- Prüfsummen für Shortcut und XML erstellt.
- GitHub Actions Release-Status-Automatik eingerichtet.
- `PORTFOLIO_UPDATE.md` mit Texten für Portfolio und GitHub-Profil angelegt.
- GitHub Release `v1.0` mit ZIP und SHA-256-Datei erstellt.

## Wichtige Designentscheidungen

- Veröffentlicht werden nur notwendige Release-Dateien.
- Nicht veröffentlicht werden lokale Arbeitsarchive, Screenshots, `.DS_Store`
  oder private lokale Projektdateien aus dem ursprünglichen Arbeitsordner.
- Datenschutzbericht ist Teil des Release-Pakets.
- Release-Status-Prüfung soll früh erkennen, wenn wichtige Dateien fehlen oder
  offensichtliche private Datenmuster auftauchen.

## Bekannte Einschränkungen oder Probleme

- Die Release-Status-Automatik ist eine statische Prüfung und ersetzt kein
  manuelles Datenschutzreview.
- Der Kurzbefehl sendet den eingegebenen Stadtnamen und Koordinaten an
  Open-Meteo, wie im Datenschutzbericht beschrieben.
- Native Kurzbefehle-Mitteilungen können optisch und sprachlich weniger stark
  angepasst werden als die HTML-Wetterkarte.

## Pflegehinweis

Bei größeren Änderungen, neuen Shortcuts, neuen Releases oder wichtigen
Entscheidungen müssen `PROJECT_CONTEXT.md` und `NEXT_STEPS.md` aktualisiert
werden.
