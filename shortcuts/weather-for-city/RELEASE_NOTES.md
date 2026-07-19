# Release Notes

## Weather for City 1.2.3

Bugfix release of the Apple Shortcut `Weather for City`.

Fixed:

- saves the selected Open-Meteo location locally after city lookup
- lets repeated `Get Weather` runs skip city input and ambiguous location
  selection after the first confirmed run
- adds a separate `Change City` menu item for replacing the saved location
- improves city-name contrast in the HTML card for phone displays
- keeps the existing UTF-8 HTML card, weather lookup, DACH/LI language handling,
  unit selection, and update-check behavior

Privacy:

- no API keys
- no passwords
- no personal tokens
- no local work archives
- no screenshots
- GitHub update check reads only the public latest-release metadata
- the saved location file stays local to the user's Shortcuts file area and is
  not included in the release
- iOS/macOS may ask for Apple Shortcuts permissions on the first and sometimes
  second run, depending on the selected menu item: Open-Meteo for weather,
  GitHub for update checks, notifications, HTML preview, and local Shortcuts
  file access for the saved location

Release files:

- `Weather for City.shortcut`
- `dist/weather-for-city-1.2.3.zip`
- `dist/weather-for-city-1.2.3.zip.sha256`

Installation:

- [Official iCloud shortcut link](https://www.icloud.com/shortcuts/98b0d52ec71448068d4d4494e28c1336)
