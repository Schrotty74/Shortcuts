# Weather for City

Version: `1.2.2`

Deutsch: [README.de.md](README.de.md)

`Weather for City` is an Apple Shortcut for Mac and iPhone.

The shortcut asks for a city, resolves the matching location through
Open-Meteo, fetches current weather data, and shows it as a notification, a
result view, and an animated HTML weather card.

![Weather for City HTML preview](assets/html-preview.svg)

## Installation

1. Open the [official iCloud shortcut link](https://www.icloud.com/shortcuts/9558234c76a84628ab4838677433dbcc).
2. Import it into Apple Shortcuts.
3. Run the shortcut and enter a city.

## Included Files

- `Weather_for_City.xml` - readable XML source
- `PRIVACY_REPORT.md` - privacy report
- `CHECKSUMS.txt` - SHA-256 checksums
- `assets/html-preview.svg` - compact preview image of the HTML weather card

## Features

- free city input
- location picker for ambiguous city names such as `Columbia`
- current temperature in Celsius or Fahrenheit, selected from the found city's country code
- WMO weather code converted to a readable description
- animated weather card
- weather scene based on the weather code
- dynamic temperature color from `-15 °C` to `+50 °C`
- Fahrenheit display for US, Bahamas, Cayman Islands, Liberia, and Myanmar
- built-in update check against the latest GitHub release
- responsive layouts for Mac and iPhone
- German visible shortcut texts and HTML output for `de-AT`, `de-DE`, `de-CH`, `de-LI`
- English fallback for all other device languages and regions
- official iCloud installation link for iPhone and Mac
- privacy report, signed shortcut file, release ZIP, and SHA-256 checksums

## Data Sources

The shortcut uses public Open-Meteo endpoints:

- `https://geocoding-api.open-meteo.com/v1/search`
- `https://api.open-meteo.com/v1/forecast`

No API key is required.
