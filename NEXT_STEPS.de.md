# Nächste Schritte: Shortcuts

Stand: 2026-07-23

Repository:
`https://github.com/Schrotty74/Shortcuts`

English: [NEXT_STEPS.md](NEXT_STEPS.md)

## Priorität 1: Vor Dem Nächsten Öffentlichen Release

- Import der neu gebauten signierten `.shortcut`-Datei nach jedem zukünftigen
  Release-Neubau testen.
- Gespeicherte Position und Erstlauf-Berechtigungen von Apple Kurzbefehle auf
  Mac und iPhone prüfen, wenn ein Release das Verhalten verändert.
- Den neutralen öffentlichen Shortcuts-Sammlungs-Link im Schrotty74-Profil bei
  neuen Shortcuts prüfen; dort keine konkreten Shortcut-Release-Versionen
  ergänzen.

## Priorität 2: Bugs und Robustheit

- Prüfen, ob Leerzeichen im Dateinamen `Weather for City.shortcut` in allen
  Download-Kontexten sauber funktionieren.
- Prüfen, ob das ZIP auf iPhone und Mac problemlos entpackt werden kann.
- Die HTML-Wetteransicht nach künftigen Layout-Änderungen auf kleinen
  Mac-/iPhone-Fenstern beobachten, besonders einzeilige Temperatur und lesbare
  Ortsdarstellung.
- Zusätzliche Datenschutzmuster in der GitHub Action nur ergänzen, wenn ein
  konkretes übersehenes Muster festgestellt wurde.

## Priorität 3: Geplante Verbesserungen

- Weitere Shortcuts jeweils in eigenem Ordner unter `shortcuts/` veröffentlichen.
- Für neue Shortcuts dieselbe Mindeststruktur verwenden:
  `VERSION`, `README.md`, `CHANGELOG.md`, `RELEASE_NOTES.md`,
  `PRIVACY_REPORT.md`, `CHECKSUMS.txt`, `dist/`.
- Pro Shortcut ein kompaktes Vorschaubild ergänzen und auf der
  Repository-Startseite anzeigen, sofern keine privaten Inhalte sichtbar sind.
- Erstlauf-Berechtigungen von Apple Kurzbefehle für jeden neuen Shortcut
  dokumentieren.
- Optional automatische ZIP-Erstellung in GitHub Actions aus den jeweiligen
  Shortcut-Ordnern einrichten.

## Ideen für zukünftige Entwicklungen

- Shortcut-Katalog im Root-README mit Kategorien.
- Badges für neueste Version je Shortcut.
- Ein gemeinsames Datenschutztemplate für neue Shortcuts.
- Automatisierte Prüfung auf `.DS_Store`, lokale Pfade und alte Archivdateien.

## Pflegehinweis

Diese Datei bei größeren Änderungen, neuen Shortcuts, neuen Releases oder
wichtigen Entscheidungen gemeinsam mit [PROJECT_CONTEXT.de.md](PROJECT_CONTEXT.de.md)
aktualisieren.

Künftige Shortcut-Änderungen nicht sofort pushen oder veröffentlichen. Erst
lokal bauen und prüfen, vom Nutzer testen lassen und nur nach ausdrücklicher
Freigabe veröffentlichen.
