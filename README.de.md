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
| <img src="shortcuts/weather-for-city/assets/html-preview.svg" alt="Weather for City HTML-Vorschau" width="180"> | Weather for City | 1.2.3 | [`shortcuts/weather-for-city`](shortcuts/weather-for-city/) | [`Installieren`](https://www.icloud.com/shortcuts/98b0d52ec71448068d4d4494e28c1336), [`v1.2.3`](https://github.com/Schrotty74/Shortcuts/releases/tag/v1.2.3) |

## Aktuelle Highlights

- zweisprachige öffentliche Shortcut-Dokumentation auf Englisch und Deutsch
- kompaktes Vorschaubild für jeden veröffentlichten Shortcut-Eintrag
- Datenschutzbericht, Prüfsummen, signierte Shortcut-Dateien und ZIP-Downloads
  pro Shortcut
- releasefähige Struktur für mehrere unabhängige Kurzbefehle

Für `Weather for City`:

- animierte Wetterkarte mit responsivem Layout für Mac und iPhone
- gespeicherte gewählte Position, damit `Wetter abrufen` nicht jedes Mal neu
  nach Stadt oder Ort fragt
- klarer Hinweis zu Erstlauf-Berechtigungen von Apple Kurzbefehle für
  Open-Meteo, GitHub, Mitteilungen, HTML-Vorschau und lokalen Zugriff auf die
  gespeicherte Position
- eigener Menüpunkt `Stadt ändern`, um die gespeicherte Position zu ersetzen
- Ortssuche mit Auswahl bei mehrdeutigen Treffern
- aktuelle Wetterdaten über öffentliche Open-Meteo-APIs, ohne API-Schlüssel
- Celsius oder Fahrenheit abhängig vom Land des gefundenen Orts
- deutsche Oberfläche für `de-AT`, `de-DE`, `de-CH`, `de-LI`; sonst Englisch
- eingebaute Update-Prüfung gegen den neuesten GitHub Release

## Datenschutz

Jeder veröffentlichte Kurzbefehl enthält einen eigenen Datenschutzbericht im
jeweiligen Shortcut-Ordner.

Für `Weather for City`:

[`shortcuts/weather-for-city/PRIVACY_REPORT.de.md`](shortcuts/weather-for-city/PRIVACY_REPORT.de.md)

## Release-Status

Die GitHub Action prüft die veröffentlichte Struktur, Prüfsummen, ZIP-Dateien
und einfache Datenschutzindikatoren.
