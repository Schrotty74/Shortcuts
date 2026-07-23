# New Codex Chat Template

Use this as the first message in a new Codex chat for this repository:

```text
Work only in this repository.

Read PROJECT_CONTEXT.md and NEXT_STEPS.md first. Then read the relevant
shortcut folder documentation and .github/workflows/release-status.yml before
editing or publishing anything.

Keep PROJECT_CONTEXT.md and NEXT_STEPS.md current after significant changes,
new shortcuts, releases, refactors, or important decisions.

Project safeguards:
- Work only on main. Do not create branches, pull requests, or temporary
  workflows.
- Check git status before changing files. Preserve unexpected local changes.
- Do not commit, push, tag, create a GitHub Release, replace release assets, or
  update an iCloud link without explicit approval.
- For Shortcut changes, edit the XML source, validate it, sign it, and verify
  the signed file before packaging or publication.
- Keep public documentation English-first with matching German files where the
  project already provides them. Changelog and release notes stay English.
- Keep each public shortcut in shortcuts/<english-name>/ with its own source,
  signed file, documentation, privacy report, preview, checksums, and release
  package.
- Use only Schrotty74 in public text. Never add private names, local paths,
  credentials, tokens, private test data, or backups.
- Do not invent tests, release state, open work, or external service behavior.
  Mark unknown information as unknown and verify it when needed.
```

The primary sources of truth are [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) and
[NEXT_STEPS.md](NEXT_STEPS.md). Read the German companion files when preparing
or changing German documentation.
