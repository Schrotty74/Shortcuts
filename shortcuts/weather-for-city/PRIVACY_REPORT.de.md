# Datenschutzbericht: Weather for City

Version: `1.2.3`

Stand: 2026-07-17

English: [PRIVACY_REPORT.md](PRIVACY_REPORT.md)

## Ergebnis

Die veröffentlichten Dateien enthalten keine privaten Zugangsdaten, keine
API-Schlüssel, keine Passwörter und keine persönlichen lokalen Dateien.

## Welche Daten verwendet der Kurzbefehl?

Der Kurzbefehl verarbeitet:

- die Stadt, die der Nutzer beim Start eingibt
- die zuletzt gewählte Position, lokal gespeichert als
  `Weather for City Last Location.json` im Kurzbefehle-Dateibereich
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

## Was wird lokal gespeichert?

Der Kurzbefehl kann die zuletzt gewählte Position lokal als
`Weather for City Last Location.json` im Kurzbefehle-Dateibereich speichern.
Gespeichert werden Stadtname, Länder-Code, Breitengrad und Längengrad, damit
bei wiederholten Läufen weder Stadteingabe noch mehrdeutige Ortsauswahl erneut
nötig sind. Diese gespeicherte Position ist nicht Bestandteil dieses
Repositorys oder der Release-Dateien.

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
- die lokal gespeicherte Positionsdatei des Nutzers

## Veröffentlichungskontrolle

Veröffentlicht werden nur die Dateien im öffentlichen Projektordner:

- `Weather_for_City.xml`
- Projektdokumentation
- Datenschutzbericht
- Prüfsummen

Nicht veröffentlicht werden lokale Arbeitsdateien aus `Shortcuts Playground`,
alte Archivstände, Desktop-Screenshots oder `.DS_Store`-Dateien.
