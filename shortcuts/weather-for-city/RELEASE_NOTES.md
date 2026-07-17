# Release Notes

## Weather for City 1.2

Feature release of the Apple Shortcut `Weather for City`.

Added:

- start menu with `Get Weather` and `Check for Update`
- latest-release check through the public GitHub Releases API
- release-page handoff when a newer version is available
- direct signed `.shortcut` release asset, in addition to the ZIP package

Note:

- Apple Shortcuts does not allow a shortcut to silently replace itself.
  Updating still requires user confirmation during import.

Privacy:

- no API keys
- no passwords
- no personal tokens
- no local work archives
- no screenshots
- GitHub update check reads only the public latest-release metadata

Release files:

- `shortcuts/weather-for-city/Weather for City.shortcut`
- `Weather for City.shortcut`
- `dist/weather-for-city-1.2.zip`
- `dist/weather-for-city-1.2.zip.sha256`
