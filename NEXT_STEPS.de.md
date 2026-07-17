# Nächste Schritte: Shortcuts

Stand: 2026-07-17

Repository:
`https://github.com/Schrotty74/Shortcuts`

English: [NEXT_STEPS.md](NEXT_STEPS.md)

## Priorität 1: Offene Aufgaben

- Import der veröffentlichten `.shortcut`-Datei aus dem Wetter-Ordner testen.
- GitHub-Profil-README `Schrotty74/Schrotty74` bei öffentlichen
  Versionsänderungen mit dem aktuellen Shortcuts-Release synchron halten.

## Priorität 2: Bugs und Robustheit

- Prüfen, ob Leerzeichen im Dateinamen `Weather for City.shortcut` in allen
  Download-Kontexten sauber funktionieren.
- Prüfen, ob das ZIP auf iPhone und Mac problemlos entpackt werden kann.
- Die HTML-Wetteransicht auf kleinen Mac-/iPhone-Fenstern beobachten, damit der
  große Temperaturwert dauerhaft einzeilig bleibt.
- Bei Bedarf zusätzliche Datenschutzmuster in der GitHub Action ergänzen.

## Priorität 3: Geplante Verbesserungen

- Weitere Shortcuts jeweils in eigenem Ordner unter `shortcuts/` veröffentlichen.
- Für neue Shortcuts dieselbe Mindeststruktur verwenden:
  `VERSION`, `README.md`, `CHANGELOG.md`, `RELEASE_NOTES.md`,
  `PRIVACY_REPORT.md`, `CHECKSUMS.txt`, `dist/`.
- Pro Shortcut ein kompaktes Vorschaubild ergänzen und auf der
  Repository-Startseite anzeigen, sofern keine privaten Inhalte sichtbar sind.
- Optional automatische ZIP-Erstellung in GitHub Actions aus den jeweiligen
  Shortcut-Ordnern einrichten.

## Ideen für zukünftige Entwicklungen

- Shortcut-Katalog im Root-README mit Kategorien.
- Badges für neueste Version je Shortcut.
- Ein gemeinsames Datenschutztemplate für neue Shortcuts.
- Automatisierte Prüfung auf `.DS_Store`, lokale Pfade und alte Archivdateien.

## Pflegehinweis

Diese Datei bei größeren Änderungen, neuen Shortcuts, neuen Releases oder
wichtigen Entscheidungen gemeinsam mit `PROJECT_CONTEXT.md` aktualisieren.

Künftige Shortcut-Änderungen nicht sofort pushen oder veröffentlichen. Erst
lokal bauen und prüfen, Martin testen lassen und nur nach ausdrücklichem OK
veröffentlichen.
