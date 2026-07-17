# Datenschutzbericht: Weather for City

Version: `1.2.1`

Stand: 2026-07-17

English: [PRIVACY_REPORT.md](PRIVACY_REPORT.md)

## Ergebnis

Die veröffentlichten Dateien enthalten keine privaten Zugangsdaten, keine
API-Schlüssel, keine Passwörter und keine persönlichen lokalen Dateien.

## Welche Daten verwendet der Kurzbefehl?

Der Kurzbefehl verarbeitet:

- die Stadt, die der Nutzer beim Start eingibt
- die daraus ermittelten öffentlichen Geocoding-Daten
- aktuelle Wetterdaten von Open-Meteo
- den Länder-Code der gefundenen Stadt, um Celsius oder Fahrenheit auszuwählen
- die Sprache/Locale der HTML-Webansicht, um Deutsch oder Englisch anzuzeigen
- öffentliche GitHub-Latest-Release-Metadaten, wenn der Nutzer `Check for Update` auswählt

## Welche Daten werden an externe Dienste gesendet?

An Open-Meteo wird die eingegebene Stadt beziehungsweise daraus abgeleitete
Koordinaten gesendet:

- Geocoding: Stadtname
- Forecast: Breitengrad und Längengrad des gefundenen Orts

## Welche externen Dienste werden verwendet?

- Open-Meteo Geocoding API
- Open-Meteo Forecast API
- GitHub Releases API für Update-Prüfungen

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

- `Weather for City.shortcut`
- `Weather_for_City.xml`
- Projektdokumentation
- Datenschutzbericht
- Prüfsummen
- Release-ZIP

Nicht veröffentlicht werden lokale Arbeitsdateien aus `Shortcuts Playground`,
alte Archivstände, Desktop-Screenshots oder `.DS_Store`-Dateien.
