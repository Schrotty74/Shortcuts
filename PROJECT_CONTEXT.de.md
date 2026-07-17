# Projektkontext: Shortcuts

Stand: 2026-07-17

Repository:
`https://github.com/Schrotty74/Shortcuts`

English: [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md)

## Projektziel und Zweck

Dieses Repository stellt öffentliche Apple-Kurzbefehle bereit. Es ist als
Sammlung angelegt: Jeder Kurzbefehl lebt vollständig in einem eigenen Ordner
unter `shortcuts/`.

Der erste veröffentlichte Kurzbefehl ist `Weather for City` in Version `1.2.1`.

## Architektur und technische Entscheidungen

- Root-Dateien beschreiben nur die Sammlung.
- Jeder Shortcut hat einen eigenen Ordner mit Version, README-Dateien,
  Changelog, Release Notes, Datenschutzberichten, Prüfsummen, Assets und ZIP.
- Englisch ist die Hauptsprache des Repositorys. Deutsche Dokumentation liegt
  als `.de.md` vor und ist gegenseitig verlinkt.
- Changelog und Release Notes bleiben immer Englisch.
- Jeder öffentliche Shortcut soll ein kompaktes Vorschaubild im eigenen
  Shortcut-Ordner enthalten und dieses Bild auf der Repository-Startseite
  anzeigen.
- Aktueller Shortcut-Ordner: `shortcuts/weather-for-city/`
- Das ZIP für `Weather for City` liegt unter:
  `shortcuts/weather-for-city/dist/weather-for-city-1.2.1.zip`
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
|-- NEXT_STEPS.de.md
|-- PROJECT_CONTEXT.md
|-- PROJECT_CONTEXT.de.md
|-- README.md
|-- README.de.md
`-- shortcuts/
    `-- weather-for-city/
        |-- CHANGELOG.md
        |-- CHECKSUMS.txt
        |-- PORTFOLIO_UPDATE.md
        |-- PORTFOLIO_UPDATE.de.md
        |-- PRIVACY_REPORT.md
        |-- PRIVACY_REPORT.de.md
        |-- README.md
        |-- README.de.md
        |-- RELEASE_NOTES.md
        |-- VERSION
        |-- Weather for City.shortcut
        |-- Weather_for_City.xml
        |-- assets/
        |   |-- html-preview.svg
        |   `-- social-preview.svg
        `-- dist/
            |-- weather-for-city-1.2.1.zip
            `-- weather-for-city-1.2.1.zip.sha256
```

## Umgesetzte Funktionen

- Öffentliches Repository für Shortcuts eingerichtet.
- Sammlungsstruktur eingeführt: jeder Shortcut in eigenem Unterordner.
- `Weather for City` Version `1.2.1` bereitgestellt.
- Signierte `.shortcut`-Datei und XML-Quelle veröffentlicht.
- Wetter-spezifische Version, Changelog, Release Notes, Portfolio-Update,
  Datenschutzbericht, Assets und ZIP in `shortcuts/weather-for-city/`
  einsortiert.
- Kompaktes HTML-Vorschaubild ergänzt unter
  `shortcuts/weather-for-city/assets/html-preview.svg`.
- Die Repository-Startseite zeigt das kompakte Vorschaubild direkt neben dem
  Shortcut-Eintrag, damit Besucher sofort sehen, wie der Shortcut aussieht.
- Version `1.1` behebt die Temperatureinheit, indem Celsius oder Fahrenheit
  aus dem Länder-Code der gefundenen Stadt ausgewählt wird.
- Version `1.2.1` ergänzt ein Startmenü und eine GitHub-Latest-Release-
  Update-Prüfung.
- Version `1.2.1` wurde innerhalb derselben Version neu gebaut, damit der große
  Temperaturwert und die Einheit in der HTML-Wetteransicht einzeilig bleiben.
- Die signierte `.shortcut`-Datei wird zusätzlich zum ZIP als direktes
  Release-Asset veröffentlicht.
- GitHub Actions Release-Status-Automatik eingerichtet.
- GitHub Release `v1.2.1` mit ZIP, direktem Shortcut-Asset und SHA-256-Datei
  erstellt.

## Wichtige Designentscheidungen

- Keine Shortcut-spezifischen Release-Dateien im Repository-Root.
- Root bleibt für Sammlung, Lizenz, Projektkontext und nächste Schritte.
- Datenschutzbericht ist pro Shortcut Pflichtbestandteil.
- Nicht veröffentlicht werden lokale Arbeitsarchive, Screenshots, `.DS_Store`
  oder private lokale Projektdateien aus dem ursprünglichen Arbeitsordner.
- Der öffentliche Shortcut-Name bleibt immer Englisch: `Weather for City`.
- Shortcut-Einträge auf der Startseite enthalten ein kleines Vorschaubild,
  nicht nur Text.
- Update-Prüfungen können den neuesten GitHub Release öffnen, aber Apple
  verlangt weiterhin eine Nutzerbestätigung beim Importieren oder Ersetzen.

## Bekannte Einschränkungen oder Probleme

- Die Release-Status-Automatik ist eine statische Prüfung und ersetzt kein
  manuelles Datenschutzreview.
- Der Wetter-Kurzbefehl sendet den eingegebenen Stadtnamen und Koordinaten an
  Open-Meteo, wie im Datenschutzbericht beschrieben.
- GitHub Release `v1.2.1` bleibt ein Release für den Wetter-Kurzbefehl, auch wenn
  das Repository künftig weitere Shortcuts enthält.

## Pflegehinweis

Bei größeren Änderungen, neuen Shortcuts, neuen Releases oder wichtigen
Entscheidungen müssen `PROJECT_CONTEXT.md` und `NEXT_STEPS.md` aktualisiert
werden.
