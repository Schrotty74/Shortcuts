# Shortcuts

[![Release Status](https://github.com/Schrotty74/Shortcuts/actions/workflows/release-status.yml/badge.svg)](https://github.com/Schrotty74/Shortcuts/actions/workflows/release-status.yml)

English: [README.md](README.md)

Öffentliche Apple-Kurzbefehle mit klaren Releases, Datenschutzberichten und
nachvollziehbaren Dateien.

Dieses Repository ist als Sammlung gedacht. Jeder Kurzbefehl liegt vollständig
in einem eigenen Unterordner unter `shortcuts/`, damit spätere Kurzbefehle
sauber getrennt veröffentlicht werden können.

## Verfügbare Kurzbefehle

| Vorschau | Kurzbefehl | Version | Ordner | Release |
| --- | --- | --- | --- | --- |
| <img src="shortcuts/weather-for-city/assets/html-preview.svg" alt="Weather for City HTML-Vorschau" width="180"> | Weather for City | 1.2.2 | [`shortcuts/weather-for-city`](shortcuts/weather-for-city/) | [`Installieren`](https://www.icloud.com/shortcuts/ab7055ef07da4836bc40b12c02204e51), [`v1.2.2`](https://github.com/Schrotty74/Shortcuts/releases/tag/v1.2.2) |

## Struktur

```text
shortcuts/
`-- weather-for-city/
    |-- Weather_for_City.xml
    |-- VERSION
    |-- README.md
    |-- README.de.md
    |-- CHANGELOG.md
    |-- RELEASE_NOTES.md
    |-- PRIVACY_REPORT.md
    |-- PRIVACY_REPORT.de.md
    |-- PORTFOLIO_UPDATE.md
    |-- PORTFOLIO_UPDATE.de.md
    |-- CHECKSUMS.txt
    |-- assets/
    `-- dist/
```

## Datenschutz

Jeder veröffentlichte Kurzbefehl enthält einen eigenen Datenschutzbericht im
jeweiligen Shortcut-Ordner.

Für `Weather for City`:

[`shortcuts/weather-for-city/PRIVACY_REPORT.de.md`](shortcuts/weather-for-city/PRIVACY_REPORT.de.md)

## Release-Status

Die GitHub Action prüft die veröffentlichte Struktur, Prüfsummen, ZIP-Dateien
und einfache Datenschutzindikatoren.
