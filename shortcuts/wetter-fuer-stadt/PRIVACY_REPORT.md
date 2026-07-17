# Datenschutzbericht: Wetter für Stadt

Version: `1.0`

Stand: 2026-07-17

## Ergebnis

Die veröffentlichten Dateien enthalten keine privaten Zugangsdaten, keine
API-Schlüssel, keine Passwörter und keine persönlichen lokalen Dateien.

## Welche Daten verwendet der Kurzbefehl?

Der Kurzbefehl verarbeitet:

- die Stadt, die der Nutzer beim Start eingibt
- die daraus ermittelten öffentlichen Geocoding-Daten
- aktuelle Wetterdaten von Open-Meteo
- die Sprache/Locale der HTML-Webansicht, um Deutsch oder Englisch anzuzeigen

## Welche Daten werden an externe Dienste gesendet?

An Open-Meteo wird die eingegebene Stadt beziehungsweise daraus abgeleitete
Koordinaten gesendet:

- Geocoding: Stadtname
- Forecast: Breitengrad und Längengrad des gefundenen Orts

## Welche externen Dienste werden verwendet?

- Open-Meteo Geocoding API
- Open-Meteo Forecast API

## Was ist nicht enthalten?

Nicht enthalten sind:

- API-Schlüssel
- Passwörter
- persönliche Tokens
- Account-Daten
- private Dateien
- lokale Backup-Archive
- Screenshots
- alte Entwicklungsarchive

## Veröffentlichungskontrolle

Veröffentlicht werden nur die Dateien im öffentlichen Projektordner:

- `Wetter für Stadt.shortcut`
- `Wetter_fuer_Stadt.xml`
- Projektdokumentation
- Datenschutzbericht
- Prüfsummen
- Release-ZIP

Nicht veröffentlicht werden lokale Arbeitsdateien aus `Shortcuts Playground`,
alte Archivstände, Desktop-Screenshots oder `.DS_Store`-Dateien.
