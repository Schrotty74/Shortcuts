# Release Notes

## Weather for City 1.2.2

Bugfix release of the Apple Shortcut `Weather for City`.

Fixed:

- adds an explicit UTF-8 character declaration to the generated HTML card
- fixes malformed German special characters and `°C` on iPhone
- repairs ambiguous city lookup by loading multiple Open-Meteo geocoding
  results and letting the user choose the correct location
- normalizes city inputs such as `Columbia SC` and `Columbia, SC`
- keeps the existing weather lookup and update-check behavior

Privacy:

- no API keys
- no passwords
- no personal tokens
- no local work archives
- no screenshots
- GitHub update check reads only the public latest-release metadata

Release files:

- `Weather for City.shortcut`
- `dist/weather-for-city-1.2.2.zip`
- `dist/weather-for-city-1.2.2.zip.sha256`

Installation:

- [Official iCloud shortcut link](https://www.icloud.com/shortcuts/d5eed8a950494a799b8a3ec0d268ac4c)
