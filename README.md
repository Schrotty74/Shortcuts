# Shortcuts

[![Release Status](https://github.com/Schrotty74/Shortcuts/actions/workflows/release-status.yml/badge.svg)](https://github.com/Schrotty74/Shortcuts/actions/workflows/release-status.yml)

Öffentliche Apple-Kurzbefehle, gebaut mit Liebe und sauberer Dokumentation.

Dieses Repository ist als Sammlung gedacht: Jeder Kurzbefehl liegt vollständig
in einem eigenen Unterordner unter `shortcuts/`.

## Verfügbare Kurzbefehle

| Kurzbefehl | Version | Ordner | Release |
| --- | --- | --- | --- |
| Wetter für Stadt | 1.0 | [`shortcuts/wetter-fuer-stadt`](shortcuts/wetter-fuer-stadt/) | [`v1.0`](https://github.com/Schrotty74/Shortcuts/releases/tag/v1.0), [`ZIP`](shortcuts/wetter-fuer-stadt/dist/wetter-fuer-stadt-1.0.zip) |

## Struktur

```text
shortcuts/
`-- wetter-fuer-stadt/
    |-- Wetter für Stadt.shortcut
    |-- Wetter_fuer_Stadt.xml
    |-- VERSION
    |-- README.md
    |-- CHANGELOG.md
    |-- RELEASE_NOTES.md
    |-- PRIVACY_REPORT.md
    |-- PORTFOLIO_UPDATE.md
    |-- CHECKSUMS.txt
    |-- assets/
    `-- dist/
```

## Datenschutz

Jeder veröffentlichte Kurzbefehl soll einen eigenen Datenschutzbericht im
jeweiligen Shortcut-Ordner enthalten.

Für `Wetter für Stadt` liegt er hier:

[`shortcuts/wetter-fuer-stadt/PRIVACY_REPORT.md`](shortcuts/wetter-fuer-stadt/PRIVACY_REPORT.md)

## Release-Status

Die GitHub-Action prüft die aktuell veröffentlichte Struktur, Prüfsummen,
ZIP-Dateien und einfache Datenschutzindikatoren.
