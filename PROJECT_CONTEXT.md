# Project Context: Shortcuts

Updated: 2026-07-19

Repository:
`https://github.com/Schrotty74/Shortcuts`

Deutsch: [PROJECT_CONTEXT.de.md](PROJECT_CONTEXT.de.md)

## Goal And Purpose

This repository publishes public Apple Shortcuts. It is structured as a
collection: each shortcut lives fully inside its own folder below `shortcuts/`.

The first published shortcut is `Weather for City` version `1.2.3`.

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
  `shortcuts/weather-for-city/dist/weather-for-city-1.2.3.zip`
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
        |-- REDDIT_POST.md
        |-- README.md
        |-- README.de.md
        |-- RELEASE_NOTES.md
        |-- VERSION
        |-- Weather for City.shortcut
        |-- Weather_for_City.xml
        |-- assets/
        |   |-- html-preview.svg
        |   |-- reddit/
        |   |   |-- weather-for-city-html-preview.png
        |   |   `-- weather-for-city-reddit-card.png
        |   `-- social-preview.svg
        `-- dist/
            |-- weather-for-city-1.2.3.zip
            `-- weather-for-city-1.2.3.zip.sha256
```

## Implemented Features

- Public Shortcuts repository created.
- Collection structure introduced: each shortcut lives in its own folder.
- `Weather for City` version `1.2.3` published.
- Signed `.shortcut` file and XML source published.
- Shortcut-specific version file, changelog, release notes, portfolio update,
  privacy report, assets, and ZIP are stored in `shortcuts/weather-for-city/`.
- Compact HTML preview image added at
  `shortcuts/weather-for-city/assets/html-preview.svg`.
- Reddit-ready PNG preview images added at
  `shortcuts/weather-for-city/assets/reddit/`.
- Reddit post draft added at `shortcuts/weather-for-city/REDDIT_POST.md`.
- The repository start page shows the compact preview next to the shortcut
  entry so visitors immediately see what the shortcut looks like.
- Version `1.1` fixes temperature units by selecting Celsius or Fahrenheit from
  the found city's country code.
- Version `1.2.1` adds a start menu and a GitHub latest-release update check.
- Version `1.2.1` was rebuilt in place to keep the large temperature value and
  unit on one line in the HTML weather view.
- Version `1.2.2` fixes UTF-8 rendering in the HTML card and was rebuilt in
  place to repair ambiguous Open-Meteo city lookup with a location picker.
- Version `1.2.3` reuses the last selected Open-Meteo location through a local
  Shortcuts file named `Weather for City Last Location.json`; `Get Weather`
  uses it directly, and `Change City` replaces it.
- GitHub documentation and the Reddit post draft explain that Apple Shortcuts
  may ask for permissions on the first and sometimes second run, depending on
  whether the user chooses `Get Weather`, `Change City`, or `Check for Update`.
- The signed `.shortcut` is published as a direct release asset in addition to
  the ZIP package.
- GitHub Actions release status automation configured.
- GitHub Release `v1.2.3` created with ZIP, direct shortcut asset, and SHA-256
  file.
- GitHub profile repository `Schrotty74/Schrotty74` must stay in sync with a
  neutral link to the public Shortcuts collection, but must not show a specific
  shortcut release version.

## Important Design Decisions

- No shortcut-specific release files in the repository root.
- The root stays reserved for the collection, license, project context, and
  next steps.
- Publication workflow: build and verify changes locally first, then wait for
  Martin's explicit approval before pushing to GitHub or replacing release
  assets.
- Each shortcut must include its own privacy report.
- Local work archives, screenshots, `.DS_Store`, and private local files are
  not published.
- The shortcut name is always English in public files: `Weather for City`.
- Start-page shortcut entries include a small preview image, not just text.
- Update checks can open the latest GitHub release, but Apple still requires
  user confirmation to import or replace a shortcut.
- For every public shortcut release/update, also check the GitHub profile page
  and keep its neutral Shortcuts collection entry accurate. Do not add
  per-shortcut release links there, because the repository can contain multiple
  shortcuts.

## Known Limitations Or Problems

- The release status automation is a static check and does not replace a manual
  privacy review.
- The weather shortcut sends the entered city name and derived coordinates to
  Open-Meteo, as described in the privacy report.
- The weather shortcut can store the last selected location locally in the
  Shortcuts file area. This is user-local state and must not be included in release
  archives or screenshots.
- GitHub Release `v1.2.3` remains the weather shortcut release even when the
  repository contains more shortcuts later.

## Maintenance Note

For larger changes, new shortcuts, new releases, or important decisions,
update `PROJECT_CONTEXT.md` and `NEXT_STEPS.md` before considering the task
complete.
