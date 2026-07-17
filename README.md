# Shortcuts

[![Release Status](https://github.com/Schrotty74/Shortcuts/actions/workflows/release-status.yml/badge.svg)](https://github.com/Schrotty74/Shortcuts/actions/workflows/release-status.yml)

Public Apple Shortcuts with clear releases, privacy notes, and reproducible files.

Deutsch: [README.de.md](README.de.md)

This repository is a collection. Each shortcut lives completely in its own
folder below `shortcuts/`, so future shortcuts can be released independently.

## Available Shortcuts

| Preview | Shortcut | Version | Folder | Release |
| --- | --- | --- | --- | --- |
| <img src="shortcuts/weather-for-city/assets/html-preview.svg" alt="Weather for City HTML preview" width="180"> | Weather for City | 1.2.2 | [`shortcuts/weather-for-city`](shortcuts/weather-for-city/) | [`Install`](https://www.icloud.com/shortcuts/ab7055ef07da4836bc40b12c02204e51), [`v1.2.2`](https://github.com/Schrotty74/Shortcuts/releases/tag/v1.2.2) |

## Structure

```text
shortcuts/
`-- weather-for-city/
    |-- Weather_for_City.xml
    |-- VERSION
    |-- README.md
    |-- README.de.md
    |-- CHANGELOG.md
    |-- RELEASE_NOTES.md
    |-- PRIVACY_REPORT.md
    |-- PRIVACY_REPORT.de.md
    |-- PORTFOLIO_UPDATE.md
    |-- PORTFOLIO_UPDATE.de.md
    |-- CHECKSUMS.txt
    |-- assets/
    `-- dist/
```

## Privacy

Each published shortcut includes its own privacy report in the shortcut folder.

For `Weather for City`:

[`shortcuts/weather-for-city/PRIVACY_REPORT.md`](shortcuts/weather-for-city/PRIVACY_REPORT.md)

## Release Status

The GitHub Action checks the published structure, checksums, ZIP files, and
basic privacy indicators.
