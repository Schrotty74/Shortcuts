# Weather for City

Version: `1.0`

English: [README.md](README.md)

`Weather for City` ist ein Apple-Kurzbefehl für Mac und iPhone.

Der Kurzbefehl fragt nach einer Stadt, sucht den passenden Ort über Open-Meteo,
ruft aktuelle Wetterdaten ab und zeigt sie als Mitteilung, Ergebnisansicht und
animierte HTML-Wetterkarte.

## Installation

1. Datei `Weather for City.shortcut` öffnen.
2. In Apple Kurzbefehle importieren.
3. Den Kurzbefehl starten und eine Stadt eingeben.

## Enthaltene Dateien

- `Weather for City.shortcut` - signierte, importierbare Shortcut-Datei
- `Weather_for_City.xml` - lesbare XML-Quelle
- `PRIVACY_REPORT.de.md` - Datenschutzbericht
- `CHECKSUMS.txt` - SHA-256-Prüfsummen

## Funktionen

- freie Stadteingabe
- aktuelle Temperatur in Grad Celsius
- WMO-Wettercode als lesbare Beschreibung
- animierte Wetterkarte
- Wetterbild passend zum Wettercode
- dynamische Temperaturfarbe von `-15 °C` bis `+50 °C`
- responsive Layouts für Mac und iPhone
- deutsche HTML-Ausgabe für `de-AT`, `de-DE`, `de-CH`, `de-LI`
- englischer Fallback für andere Gerätesprachen

## Datenquellen

Der Kurzbefehl nutzt öffentliche Open-Meteo-Endpunkte:

- `https://geocoding-api.open-meteo.com/v1/search`
- `https://api.open-meteo.com/v1/forecast`

Es ist kein API-Schlüssel erforderlich.
