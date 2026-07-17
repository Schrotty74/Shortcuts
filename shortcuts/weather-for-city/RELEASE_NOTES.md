# Release Notes

## Weather for City 1.2.1

Bugfix release of the Apple Shortcut `Weather for City`.

Fixed:

- replaces the fragile multi-condition temperature-unit branch with a more compatible Match Text + Count + If flow
- fixes the runtime prompt that could appear after entering a city: `Choose a value for each parameter in this action`
- keeps the `Check for Update` feature from 1.2 intact
- keeps direct signed `.shortcut` release asset publishing

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
- `dist/weather-for-city-1.2.1.zip`
- `dist/weather-for-city-1.2.1.zip.sha256`
