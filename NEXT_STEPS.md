# Next Steps: Shortcuts

Updated: 2026-07-17

Repository:
`https://github.com/Schrotty74/Shortcuts`

Deutsch: [NEXT_STEPS.de.md](NEXT_STEPS.de.md)

## Priority 1: Open Tasks

- Verify GitHub Actions after the English/bilingual release structure update.
- Check GitHub Release `v1.0`.
- Test downloading the `Weather for City` ZIP from the shortcut folder.
- Test importing the published `.shortcut` file from the weather folder.

## Priority 2: Bugs And Robustness

- Check whether spaces in `Weather for City.shortcut` behave cleanly in all
  download contexts.
- Check whether the ZIP extracts cleanly on iPhone and Mac.
- Add more privacy patterns to the GitHub Action if needed.

## Priority 3: Planned Improvements

- Publish additional shortcuts in their own folders below `shortcuts/`.
- Use the same minimum structure for new shortcuts:
  `VERSION`, `README.md`, `CHANGELOG.md`, `RELEASE_NOTES.md`,
  `PRIVACY_REPORT.md`, `CHECKSUMS.txt`, `dist/`.
- Optionally add one screenshot or demo GIF per shortcut, as long as no private
  content is visible.
- Optionally automate ZIP creation in GitHub Actions from each shortcut folder.

## Ideas For Future Development

- Shortcut catalog in the root README with categories.
- Latest-version badges per shortcut.
- Shared privacy template for new shortcuts.
- Automated checks for `.DS_Store`, local paths, and old archive files.

## Maintenance Note

Update this file together with `PROJECT_CONTEXT.md` for larger changes, new
shortcuts, new releases, or important decisions.
