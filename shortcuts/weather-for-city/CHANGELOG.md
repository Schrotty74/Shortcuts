# Changelog

## 1.2.3 - 2026-07-19

Bugfix release.

- Saves the selected Open-Meteo location locally, including city name, country
  code, latitude, and longitude.
- Lets repeated `Get Weather` runs skip both city input and ambiguous location
  selection after the first confirmed run.
- Adds a separate `Change City` menu item for replacing the saved location.
- Updates the published iCloud installation link.

## 1.2.2 - 2026-07-17

Bugfix release.

- Fixes UTF-8 decoding of the generated HTML weather card on iPhone.
- German special characters and the Celsius symbol now render correctly.
- Rebuilt in place to repair ambiguous Open-Meteo city lookup.
- Loads multiple geocoding results and asks the user to choose the correct
  location when needed.
- Normalizes city inputs such as `Columbia SC` and `Columbia, SC` before
  searching, so they resolve to the expected Columbia results.
- Keeps the HTML weather card UTF-8 declaration and DACH/LI language handling.

## 1.2.1 - 2026-07-17

Bugfix release.

- Replaces the imported multi-condition temperature-unit branch with a more compatible Match Text + Count + If flow.
- Fixes a runtime prompt that asked the user to choose values for missing action parameters after entering a city.
- Keeps the 1.2 update-check feature intact.

## 1.2 - 2026-07-17

Feature release.

- Adds a start menu with `Get Weather` and `Check for Update`.
- Checks the latest public GitHub release through the GitHub Releases API.
- Opens the latest release page when a newer version is available.
- Documents that Apple Shortcuts still requires user confirmation to import or
  replace a shortcut.
- Publishes the signed `.shortcut` file as a direct release asset in addition to
  the ZIP package.

## 1.1 - 2026-07-17

Bugfix release.

- Selects Celsius or Fahrenheit from the found city's country code.
- Uses Fahrenheit for US, Bahamas, Cayman Islands, Liberia, and Myanmar.
- Keeps Celsius for all other countries.
- Updates notification, result view, and HTML weather card to show the matching unit.
- Keeps the HTML temperature color scale normalized to Celsius.

## 1.0 - 2026-07-17

Initial public release.

- Adds the `Weather for City` shortcut.
- Asks for a city and fetches current weather data through Open-Meteo.
- Shows a notification, result view, and animated HTML weather card.
- Supports German HTML output for DACH/LI device languages and English fallback
  for all other locales.
- Includes dynamic temperature color, weather-code scenes, and responsive Mac
  and iPhone layouts.
- Includes privacy report and checksums.
