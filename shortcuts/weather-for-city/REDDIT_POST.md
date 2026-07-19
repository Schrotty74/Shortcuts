# Reddit Post Draft

Title:

```text
[Update] Weather for City 1.2.3 - animated weather card with saved location
```

Post:

```text
Hi r/shortcuts,

I updated my public Apple Shortcut "Weather for City".

iCloud link:
https://www.icloud.com/shortcuts/98b0d52ec71448068d4d4494e28c1336

GitHub:
https://github.com/Schrotty74/Shortcuts/tree/main/shortcuts/weather-for-city

What it does:
- asks for a city on the first setup
- resolves ambiguous city names with Open-Meteo
- saves the selected location locally, so "Get Weather" can run without asking for the same city again
- shows current weather as a notification, result view, and animated HTML card
- supports Celsius/Fahrenheit depending on the selected location
- uses German only for DACH/LI device settings, English everywhere else
- includes a GitHub update check

Important permission note:
On the first run, and sometimes also on the second run, iOS/macOS may ask for permissions. The exact prompts depend on what you choose in the shortcut menu:

- Get Weather: Open-Meteo network access, notifications, HTML preview, and local Shortcuts file access for the saved location
- Change City: local Shortcuts file access again because it replaces the saved location
- Check for Update: GitHub network access and opening the release page

These permission prompts are normal Apple Shortcuts prompts. They are not hidden tracking. The shortcut uses public Open-Meteo APIs and does not require an API key.

Preview image:
https://github.com/Schrotty74/Shortcuts/blob/main/shortcuts/weather-for-city/assets/reddit/weather-for-city-reddit-card.png
```
