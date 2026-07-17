# Changelog

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
