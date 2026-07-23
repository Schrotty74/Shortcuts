# Next Steps: Shortcuts

Updated: 2026-07-23

Repository:
`https://github.com/Schrotty74/Shortcuts`

Deutsch: [NEXT_STEPS.de.md](NEXT_STEPS.de.md)

## Priority 1: Before The Next Public Release

- Test import of the rebuilt signed `.shortcut` after every future release
  rebuild.
- Verify the saved-location flow and first-run Apple Shortcuts prompts on both
  Mac and iPhone when a behavior-changing release is prepared.
- Check the neutral public Shortcuts collection link in the Schrotty74 profile
  when a new shortcut is published; do not add per-shortcut release versions
  there.

## Priority 2: Bugs And Robustness

- Check whether spaces in `Weather for City.shortcut` behave cleanly in all
  download contexts.
- Check whether the ZIP extracts cleanly on iPhone and Mac.
- Keep observing the HTML weather view on small Mac/iPhone windows after future
  layout changes, especially the one-line temperature and readable city label.
- Extend GitHub Action privacy patterns only when a concrete missed pattern is
  identified.

## Priority 3: Planned Improvements

- Publish additional shortcuts in their own folders below `shortcuts/`.
- Use the same minimum structure for new shortcuts:
  `VERSION`, `README.md`, `CHANGELOG.md`, `RELEASE_NOTES.md`,
  `PRIVACY_REPORT.md`, `CHECKSUMS.txt`, `dist/`.
- Add one compact preview image per shortcut and show it on the repository
  start page, as long as no private content is visible.
- Document first-run Apple Shortcuts permission prompts for each new shortcut.
- Optionally automate ZIP creation in GitHub Actions from each shortcut folder.

## Ideas For Future Development

- Shortcut catalog in the root README with categories.
- Latest-version badges per shortcut.
- Shared privacy template for new shortcuts.
- Automated checks for `.DS_Store`, local paths, and old archive files.

## Maintenance Note

Update this file together with [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) for
larger changes, new shortcuts, new releases, or important decisions.

Do not push or publish future shortcut changes immediately. Build and verify
locally, let the user test the result, and publish only after explicit approval.
