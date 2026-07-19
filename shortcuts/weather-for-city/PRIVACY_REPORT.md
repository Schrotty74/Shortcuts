# Privacy Report: Weather for City

Version: `1.2.3`

Updated: 2026-07-19

Deutsch: [PRIVACY_REPORT.de.md](PRIVACY_REPORT.de.md)

## Result

The published files contain no private credentials, no API keys, no passwords,
and no personal local files.

## What Data Does The Shortcut Use?

The shortcut processes:

- the city entered by the user when the shortcut starts
- the last selected location saved locally as
  `Weather for City Last Location.json` in the Shortcuts file area
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

## Apple Shortcuts Permission Prompts

iOS/macOS may ask for permissions on the first and sometimes also the second
run. The exact prompts depend on the selected menu item:

- `Get Weather`: Open-Meteo network access, notifications, HTML preview, and
  local Shortcuts file access for the saved location.
- `Change City`: local Shortcuts file access again because the saved location is
  replaced.
- `Check for Update`: GitHub network access and opening the release page.

These prompts are controlled by Apple Shortcuts. They are not hidden tracking or
private data collection.

## What Is Stored Locally?

The shortcut can save the last selected location locally as
`Weather for City Last Location.json` in the Shortcuts file area. It stores the
city name, country code, latitude, and longitude so repeated runs do not need
the city input or ambiguous-location picker again. The saved location is not
included in this repository or in release files.

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
- the user's locally saved location file

## Publication Control

Only files inside the public project folder are published:

- `Weather_for_City.xml`
- project documentation
- privacy report
- checksums

Local work files from `Shortcuts Playground`, old archive states, desktop
screenshots, and `.DS_Store` files are not published.
