# Weather for City

Version: `1.2.3`

English: [README.md](README.md)

`Weather for City` ist ein Apple-Kurzbefehl für Mac und iPhone.

Der Kurzbefehl fragt nach einer Stadt, sucht den passenden Ort über Open-Meteo,
ruft aktuelle Wetterdaten ab und zeigt sie als Mitteilung, Ergebnisansicht und
animierte HTML-Wetterkarte.

![Weather for City HTML-Vorschau](assets/html-preview.svg)

## Installation

1. Den [offiziellen iCloud-Kurzbefehl-Link](https://www.icloud.com/shortcuts/98b0d52ec71448068d4d4494e28c1336) öffnen.
2. In Apple Kurzbefehle importieren.
3. Den Kurzbefehl starten und eine Stadt eingeben.

## Enthaltene Dateien

- `Weather_for_City.xml` - lesbare XML-Quelle
- `PRIVACY_REPORT.de.md` - Datenschutzbericht
- `CHECKSUMS.txt` - SHA-256-Prüfsummen
- `assets/html-preview.svg` - kompaktes Vorschaubild der HTML-Wetterkarte

## Funktionen

- freie Stadteingabe
- merkt sich die zuletzt gewählte Position lokal, damit `Wetter abrufen` nicht
  erneut nach Stadt oder Ort fragen muss
- eigener Menüpunkt `Stadt ändern`, um die gespeicherte Position zu ersetzen
- Ortsauswahl bei mehrdeutigen Städten wie `Columbia`
- aktuelle Temperatur in Celsius oder Fahrenheit, abhängig vom Länder-Code der gefundenen Stadt
- WMO-Wettercode als lesbare Beschreibung
- animierte Wetterkarte
- Wetterbild passend zum Wettercode
- dynamische Temperaturfarbe von `-15 °C` bis `+50 °C`
- Fahrenheit-Anzeige für USA, Bahamas, Cayman Islands, Liberia und Myanmar
- eingebaute Update-Prüfung gegen den neuesten GitHub Release
- responsive Layouts für Mac und iPhone
- deutsche sichtbare Shortcut-Texte und HTML-Ausgabe für `de-AT`, `de-DE`, `de-CH`, `de-LI`
- englischer Fallback für andere Gerätesprachen und Regionen
- Datenschutzbericht, signierte Shortcut-Datei, Release-ZIP und SHA-256-Prüfsummen

## Erster Start und Berechtigungen

Beim ersten Lauf kann iOS/macOS um Erlaubnis für Open-Meteo, GitHub, den
lokalen Kurzbefehle-Dateibereich, Mitteilungen oder die HTML-Vorschau fragen.
Diese Dialoge kommen von Apple Kurzbefehle und können vom Kurzbefehl nicht
vollständig deaktiviert werden. Nach dem ersten bestätigten Lauf kann
`Wetter abrufen` die gespeicherte gewählte Position ohne erneute Stadt- oder
Ortsabfrage verwenden. Mit `Stadt ändern` kann sie ersetzt werden.

## Datenquellen

Der Kurzbefehl nutzt öffentliche Open-Meteo-Endpunkte:

- `https://geocoding-api.open-meteo.com/v1/search`
- `https://api.open-meteo.com/v1/forecast`

Es ist kein API-Schlüssel erforderlich.
