# Privacy Report: Weather for City

Version: `1.2.1`

Updated: 2026-07-17

Deutsch: [PRIVACY_REPORT.de.md](PRIVACY_REPORT.de.md)

## Result

The published files contain no private credentials, no API keys, no passwords,
and no personal local files.

## What Data Does The Shortcut Use?

The shortcut processes:

- the city entered by the user when the shortcut starts
- public geocoding data derived from that city
- current weather data from Open-Meteo
- the country code of the found city to select Celsius or Fahrenheit
- the language/locale of the HTML web view to display German or English
- public GitHub latest-release metadata when the user chooses `Check for Update`

## What Data Is Sent To External Services?

Open-Meteo receives the entered city or coordinates derived from it:

- Geocoding: city name
- Forecast: latitude and longitude of the found location

## Which External Services Are Used?

- Open-Meteo Geocoding API
- Open-Meteo Forecast API
- GitHub Releases API for update checks

## What Is Not Included?

The release does not include:

- API keys
- passwords
- personal tokens
- account data
- private files
- local backup archives
- screenshots
- old development archives

## Publication Control

Only files inside the public project folder are published:

- `Weather for City.shortcut`
- `Weather_for_City.xml`
- project documentation
- privacy report
- checksums
- release ZIP

Local work files from `Shortcuts Playground`, old archive states, desktop
screenshots, and `.DS_Store` files are not published.
