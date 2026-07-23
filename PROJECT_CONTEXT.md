# Project Context: Shortcuts

Updated: 2026-07-23

Repository:
`https://github.com/Schrotty74/Shortcuts`

Deutsch: [PROJECT_CONTEXT.de.md](PROJECT_CONTEXT.de.md)

## Start Here In A New Chat

Read these files in this order before changing the project:

1. this file for the durable project model and non-negotiable rules
2. [NEXT_STEPS.md](NEXT_STEPS.md) for the currently open work
3. [CHAT_TEMPLATE.md](CHAT_TEMPLATE.md) when starting a new Codex chat
4. the relevant shortcut folder's README, privacy report, changelog, and
   release notes
5. `.github/workflows/release-status.yml` before changing release files or CI

Use the German companion files when German documentation is needed. Do not
treat old release files or ignored local work files as the current source of
truth.

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

## Data Formats And Workflows

- `Weather_for_City.xml` is the readable Shortcut plist source.
- `Weather for City.shortcut` is the signed, importable Shortcut file.
- `VERSION` is the shortcut's plain-text release version.
- `CHECKSUMS.txt` and the `.zip.sha256` file contain SHA-256 integrity checks.
- `dist/` contains release ZIP packages; `assets/` contains public SVG and PNG
  previews only.
- The workflow plist contains the visible Shortcut text, Open-Meteo requests,
  saved-location handling, and the embedded HTML weather card.
- Timestamped work copies and `.DS_Store` are ignored by Git and are not
  release input.

## Build, Test, And Release Workflow

1. Check `git status --short` and stay on `main`. Preserve unexpected local
   changes; do not overwrite or discard them.
2. When the worktree is clean, synchronize `main` with `origin/main` using a
   fast-forward-only pull and confirm both revisions match.
3. Edit the XML source first. For Shortcut changes, validate the plist and run
   the Shortcuts Playground validator. Fix validation findings before signing.
4. Sign from the validated XML, verify that the signed `.shortcut` exists and
   is non-empty, then test import/behavior when the change requires it.
5. Rebuild ZIP and checksum files when release contents change. Run the local
   CI-equivalent checksum and privacy checks before publication.
6. Do not create a commit, push, tag, GitHub Release, or iCloud-link update
   unless explicitly requested. Public changes are tested locally first.

## File Structure

```text
Shortcuts/
|-- .github/workflows/release-status.yml
|-- CHAT_TEMPLATE.md
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
- The HTML card and its public preview use the same higher-contrast ice-blue
  city label so the place name remains readable on phones.
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
- Work only on `main`; do not create branches, pull requests, or temporary
  workflows for this repository.
- Publication workflow: build and verify changes locally first, then wait for
  explicit approval before pushing to GitHub or replacing release assets.
- Each shortcut must include its own privacy report.
- Local work archives, screenshots, `.DS_Store`, and private local files are
  not published.
- The shortcut name is always English in public files: `Weather for City`.
- Start-page shortcut entries include a small preview image, not just text.
- Update checks can open the latest GitHub release, but Apple still requires
  user confirmation to import or replace a shortcut.
- German is shown only for the supported DACH/Liechtenstein device context;
  English is the fallback for all other devices. Do not add automatic external
  translation services without an explicit decision.
- A newly shared iCloud shortcut has a new link. Update visible repository
  references only after the new link has been supplied and publication is
  approved.
- Use only `Schrotty74` in public-facing text. Never add personal names, local
  paths, credentials, tokens, private test data, or backups to the repository.
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
- Only German and English visible Shortcut text is currently implemented.
- The exact device permission prompts are controlled by Apple Shortcuts and
  can vary by platform and selected menu item.
- No project-owned build script is currently documented; signing and release
  packaging are manual, validated steps.

## Maintenance Note

For larger changes, new shortcuts, new releases, or important decisions,
update this file, [NEXT_STEPS.md](NEXT_STEPS.md), and the matching German
context files before considering the task complete.
