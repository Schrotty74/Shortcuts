# Project Context: Shortcuts

Updated: 2026-07-17

Repository:
`https://github.com/Schrotty74/Shortcuts`

Deutsch: [PROJECT_CONTEXT.de.md](PROJECT_CONTEXT.de.md)

## Goal And Purpose

This repository publishes public Apple Shortcuts. It is structured as a
collection: each shortcut lives fully inside its own folder below `shortcuts/`.

The first published shortcut is `Weather for City` version `1.1`.

## Architecture And Technical Decisions

- Root files describe the collection only.
- Each shortcut has its own folder with version, README files, changelog,
  release notes, privacy reports, checksums, assets, and ZIP files.
- English is the primary repository language. German documentation is provided
  as `.de.md` files and cross-linked from the English files.
- Changelog and release notes are always written in English.
- Every public shortcut should include a compact visual preview in its shortcut
  folder and show that preview on the repository start page.
- Current shortcut folder: `shortcuts/weather-for-city/`
- The ZIP for `Weather for City` lives at:
  `shortcuts/weather-for-city/dist/weather-for-city-1.1.zip`
- GitHub Actions checks the expected folder structure, checksums, and basic
  privacy indicators.
- The weather shortcut uses public Open-Meteo APIs and requires no API key.

## File Structure

```text
Shortcuts/
|-- .github/workflows/release-status.yml
|-- LICENSE
|-- NEXT_STEPS.md
|-- NEXT_STEPS.de.md
|-- PROJECT_CONTEXT.md
|-- PROJECT_CONTEXT.de.md
|-- README.md
|-- README.de.md
`-- shortcuts/
    `-- weather-for-city/
        |-- CHANGELOG.md
        |-- CHECKSUMS.txt
        |-- PORTFOLIO_UPDATE.md
        |-- PORTFOLIO_UPDATE.de.md
        |-- PRIVACY_REPORT.md
        |-- PRIVACY_REPORT.de.md
        |-- README.md
        |-- README.de.md
        |-- RELEASE_NOTES.md
        |-- VERSION
        |-- Weather for City.shortcut
        |-- Weather_for_City.xml
        |-- assets/
        |   |-- html-preview.svg
        |   `-- social-preview.svg
        `-- dist/
            |-- weather-for-city-1.1.zip
            `-- weather-for-city-1.1.zip.sha256
```

## Implemented Features

- Public Shortcuts repository created.
- Collection structure introduced: each shortcut lives in its own folder.
- `Weather for City` version `1.1` published.
- Signed `.shortcut` file and XML source published.
- Shortcut-specific version file, changelog, release notes, portfolio update,
  privacy report, assets, and ZIP are stored in `shortcuts/weather-for-city/`.
- Compact HTML preview image added at
  `shortcuts/weather-for-city/assets/html-preview.svg`.
- The repository start page shows the compact preview next to the shortcut
  entry so visitors immediately see what the shortcut looks like.
- Version `1.1` fixes temperature units by selecting Celsius or Fahrenheit from
  the found city's country code.
- GitHub Actions release status automation configured.
- GitHub Release `v1.1` created with ZIP and SHA-256 file.

## Important Design Decisions

- No shortcut-specific release files in the repository root.
- The root stays reserved for the collection, license, project context, and
  next steps.
- Each shortcut must include its own privacy report.
- Local work archives, screenshots, `.DS_Store`, and private local files are
  not published.
- The shortcut name is always English in public files: `Weather for City`.
- Start-page shortcut entries include a small preview image, not just text.

## Known Limitations Or Problems

- The release status automation is a static check and does not replace a manual
  privacy review.
- The weather shortcut sends the entered city name and derived coordinates to
  Open-Meteo, as described in the privacy report.
- GitHub Release `v1.1` remains the weather shortcut release even when the
  repository contains more shortcuts later.

## Maintenance Note

For larger changes, new shortcuts, new releases, or important decisions,
update `PROJECT_CONTEXT.md` and `NEXT_STEPS.md` before considering the task
complete.
