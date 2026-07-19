# Weather for City

Version: `1.2.3`

Deutsch: [README.de.md](README.de.md)

`Weather for City` is an Apple Shortcut for Mac and iPhone.

The shortcut asks for a city, resolves the matching location through
Open-Meteo, fetches current weather data, and shows it as a notification, a
result view, and an animated HTML weather card.

![Weather for City HTML preview](assets/html-preview.svg)

## Installation

1. Open the [official iCloud shortcut link](https://www.icloud.com/shortcuts/98b0d52ec71448068d4d4494e28c1336).
2. Import it into Apple Shortcuts.
3. Run the shortcut and enter a city.

## Included Files

- `Weather_for_City.xml` - readable XML source
- `PRIVACY_REPORT.md` - privacy report
- `CHECKSUMS.txt` - SHA-256 checksums
- `assets/html-preview.svg` - compact preview image of the HTML weather card

## Features

- free city input
- remembers the last selected location locally so `Get Weather` can run without
  asking for the city or location choice again
- separate `Change City` menu item for replacing the saved location
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

## First Run And Permissions

On the first run, iOS/macOS may ask for permission to access Open-Meteo,
GitHub, the local Shortcuts file area, notifications, or the HTML preview.
These prompts come from Apple Shortcuts and cannot be fully disabled by the
shortcut. After the first confirmed run, `Get Weather` can reuse the saved
selected location without asking again. Use `Change City` when you want to
replace it.

## Data Sources

The shortcut uses public Open-Meteo endpoints:

- `https://geocoding-api.open-meteo.com/v1/search`
- `https://api.open-meteo.com/v1/forecast`

No API key is required.
