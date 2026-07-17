# Shortcuts

[![Release Status](https://github.com/Schrotty74/Shortcuts/actions/workflows/release-status.yml/badge.svg)](https://github.com/Schrotty74/Shortcuts/actions/workflows/release-status.yml)

Öffentliche Apple-Kurzbefehle, gebaut mit Liebe und sauberer Dokumentation.

## Verfügbare Kurzbefehle

### Wetter für Stadt

Version: `1.0`

`Wetter für Stadt` fragt nach einer Stadt, ruft aktuelle Wetterdaten über die
öffentlichen Open-Meteo-APIs ab und zeigt eine animierte Wetterkarte an.

Highlights:

- keine Anmeldung
- kein API-Schlüssel
- Deutsch für DACH/LI-Gerätesprachen, sonst Englisch in der HTML-Wetterkarte
- dynamische Temperaturfarbe von `-15 °C` bis `+50 °C`
- Wetterbild und Hintergrund passend zum Wettercode
- responsive Darstellung für Mac und iPhone

Installierbare Datei:

- [Wetter für Stadt.shortcut](shortcuts/wetter-fuer-stadt/Wetter%20für%20Stadt.shortcut)

Release-ZIP:

- [wetter-fuer-stadt-1.0.zip](dist/wetter-fuer-stadt-1.0.zip)
- [wetter-fuer-stadt-1.0.zip.sha256](dist/wetter-fuer-stadt-1.0.zip.sha256)

Dokumentation:

- [Shortcut-README](shortcuts/wetter-fuer-stadt/README.md)
- [Datenschutzbericht](shortcuts/wetter-fuer-stadt/PRIVACY_REPORT.md)
- [Prüfsummen](shortcuts/wetter-fuer-stadt/CHECKSUMS.txt)
- [Release Notes](RELEASE_NOTES.md)

## Datenschutz

Dieses Repository enthält keine privaten Zugangsdaten, keine API-Schlüssel und
keine lokalen persönlichen Pfade in den veröffentlichten Release-Dateien.

Der Kurzbefehl verwendet nur die vom Nutzer eingegebene Stadt und öffentliche
Open-Meteo-Endpunkte. Details stehen im
[Datenschutzbericht](shortcuts/wetter-fuer-stadt/PRIVACY_REPORT.md).

## Releases

Die Release-Status-Automatik prüft bei Änderungen, ob die wichtigen Dateien
vorhanden sind, die Version konsistent ist, Prüfsummen passen und keine
offensichtlichen lokalen privaten Pfade veröffentlicht werden.
