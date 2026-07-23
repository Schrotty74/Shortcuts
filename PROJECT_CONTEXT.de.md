# Projektkontext: Shortcuts

Stand: 2026-07-23

Repository:
`https://github.com/Schrotty74/Shortcuts`

English: [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md)

## Zuerst Lesen Bei Einem Neuen Chat

Vor Änderungen diese Dateien in dieser Reihenfolge lesen:

1. diese Datei für das dauerhafte Projektmodell und feste Regeln
2. [NEXT_STEPS.de.md](NEXT_STEPS.de.md) für die aktuell offenen Arbeiten
3. [CHAT_TEMPLATE.md](CHAT_TEMPLATE.md) beim Start eines neuen Codex-Chats
4. README, Datenschutzbericht, Changelog und Release Notes des betroffenen
   Shortcut-Ordners
5. `.github/workflows/release-status.yml` vor Änderungen an Release-Dateien
   oder CI

Für englische Dokumentation die jeweils verlinkte englische Datei verwenden.
Alte Release-Dateien oder ignorierte lokale Arbeitsdateien sind keine aktuelle
Wissensquelle.

## Projektziel und Zweck

Dieses Repository stellt öffentliche Apple-Kurzbefehle bereit. Es ist als
Sammlung angelegt: Jeder Kurzbefehl lebt vollständig in einem eigenen Ordner
unter `shortcuts/`.

Der erste veröffentlichte Kurzbefehl ist `Weather for City` in Version `1.2.3`.

## Architektur und technische Entscheidungen

- Root-Dateien beschreiben nur die Sammlung.
- Jeder Shortcut hat einen eigenen Ordner mit Version, README-Dateien,
  Changelog, Release Notes, Datenschutzberichten, Prüfsummen, Assets und ZIP.
- Englisch ist die Hauptsprache des Repositorys. Deutsche Dokumentation liegt
  als `.de.md` vor und ist gegenseitig verlinkt.
- Changelog und Release Notes bleiben immer Englisch.
- Jeder öffentliche Shortcut soll ein kompaktes Vorschaubild im eigenen
  Shortcut-Ordner enthalten und dieses Bild auf der Repository-Startseite
  anzeigen.
- Aktueller Shortcut-Ordner: `shortcuts/weather-for-city/`
- Das ZIP für `Weather for City` liegt unter:
  `shortcuts/weather-for-city/dist/weather-for-city-1.2.3.zip`
- GitHub Actions prüft die erwartete Ordnerstruktur, Prüfsummen und einfache
  Datenschutzindikatoren.
- Der Wetter-Kurzbefehl nutzt öffentliche Open-Meteo-APIs und benötigt keinen
  API-Schlüssel.

## Datenformate Und Arbeitsablauf

- `Weather_for_City.xml` ist die lesbare Plist-Quelle des Kurzbefehls.
- `Weather for City.shortcut` ist die signierte, importierbare Shortcut-Datei.
- `VERSION` enthält die Release-Version als Klartext.
- `CHECKSUMS.txt` und die Datei `.zip.sha256` enthalten SHA-256-
  Integritätsprüfungen.
- `dist/` enthält Release-ZIP-Pakete; `assets/` enthält nur öffentliche
  SVG- und PNG-Vorschaubilder.
- Die Workflow-Plist enthält sichtbare Shortcut-Texte, Open-Meteo-Anfragen,
  gespeicherte Positionsdaten und die eingebettete HTML-Wetterkarte.
- Zeitgestempelte Arbeitskopien und `.DS_Store` werden von Git ignoriert und
  gehören nicht zu den Release-Eingaben.

## Build-, Test- Und Release-Ablauf

1. `git status --short` prüfen und auf `main` bleiben. Unerwartete lokale
   Änderungen erhalten und niemals überschreiben oder verwerfen.
2. Bei sauberem Arbeitsbaum `main` per Fast-Forward mit `origin/main`
   synchronisieren und gleiche Revisionen bestätigen.
3. Zuerst die XML-Quelle ändern. Bei Shortcut-Änderungen die Plist und den
   Shortcuts-Playground-Validator ausführen; Befunde vor dem Signieren beheben.
4. Aus der validierten XML signieren, die nicht-leere `.shortcut`-Datei prüfen
   und bei relevanten Änderungen Import und Verhalten testen.
5. ZIP- und Prüfsummen-Dateien neu bauen, wenn sich Release-Inhalte ändern.
   Vor einer Veröffentlichung die lokalen CI-äquivalenten Prüfsummen- und
   Datenschutzprüfungen ausführen.
6. Keinen Commit, Push, Tag, GitHub Release oder iCloud-Link ohne ausdrückliche
   Anforderung erstellen. Öffentliche Änderungen zuerst lokal testen.

## Dateistruktur

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

## Umgesetzte Funktionen

- Öffentliches Repository für Shortcuts eingerichtet.
- Sammlungsstruktur eingeführt: jeder Shortcut in eigenem Unterordner.
- `Weather for City` Version `1.2.3` bereitgestellt.
- Signierte `.shortcut`-Datei und XML-Quelle veröffentlicht.
- Wetter-spezifische Version, Changelog, Release Notes, Portfolio-Update,
  Datenschutzbericht, Assets und ZIP in `shortcuts/weather-for-city/`
  einsortiert.
- Kompaktes HTML-Vorschaubild ergänzt unter
  `shortcuts/weather-for-city/assets/html-preview.svg`.
- Reddit-taugliche PNG-Vorschaubilder ergänzt unter
  `shortcuts/weather-for-city/assets/reddit/`.
- Reddit-Post-Vorlage ergänzt unter `shortcuts/weather-for-city/REDDIT_POST.md`.
- Die Repository-Startseite zeigt das kompakte Vorschaubild direkt neben dem
  Shortcut-Eintrag, damit Besucher sofort sehen, wie der Shortcut aussieht.
- Version `1.1` behebt die Temperatureinheit, indem Celsius oder Fahrenheit
  aus dem Länder-Code der gefundenen Stadt ausgewählt wird.
- Version `1.2.1` ergänzt ein Startmenü und eine GitHub-Latest-Release-
  Update-Prüfung.
- Version `1.2.1` wurde innerhalb derselben Version neu gebaut, damit der große
  Temperaturwert und die Einheit in der HTML-Wetteransicht einzeilig bleiben.
- Version `1.2.2` behebt UTF-8-Darstellung in der HTML-Karte und wurde innerhalb
  derselben Version neu gebaut, um mehrdeutige Open-Meteo-Ortssuchen mit einer
  Ortsauswahl zu reparieren.
- Version `1.2.3` verwendet die zuletzt gewählte Open-Meteo-Position über eine
  lokale Kurzbefehle-Datei namens `Weather for City Last Location.json` wieder;
  `Wetter abrufen` verwendet sie direkt, `Stadt ändern` ersetzt sie.
- GitHub-Dokumentation und Reddit-Post-Vorlage erklären, dass Apple Kurzbefehle
  beim ersten und teilweise zweiten Lauf Berechtigungen anfragen kann, abhängig
  davon, ob `Wetter abrufen`, `Stadt ändern` oder `Nach Update suchen` gewählt
  wird.
- Die signierte `.shortcut`-Datei wird zusätzlich zum ZIP als direktes
  Release-Asset veröffentlicht.
- HTML-Karte und öffentliches Vorschaubild verwenden dieselbe kontrastreiche,
  eisblaue Ortsdarstellung, damit der Ortsname auf Telefonen lesbar bleibt.
- GitHub Actions Release-Status-Automatik eingerichtet.
- GitHub Release `v1.2.3` mit ZIP, direktem Shortcut-Asset und SHA-256-Datei
  erstellt.
- Das GitHub-Profil-Repository `Schrotty74/Schrotty74` muss mit einem neutralen
  Link zur öffentlichen Shortcuts-Sammlung synchron bleiben, darf dort aber
  keine konkrete Shortcut-Release-Version anzeigen.

## Wichtige Designentscheidungen

- Keine Shortcut-spezifischen Release-Dateien im Repository-Root.
- Root bleibt für Sammlung, Lizenz, Projektkontext und nächste Schritte.
- Nur auf `main` arbeiten; keine Branches, Pull Requests oder temporären
  Workflows für dieses Repository anlegen.
- Veröffentlichungsablauf: Änderungen zuerst lokal bauen und prüfen, dann auf
  ausdrückliches OK warten, bevor etwas zu GitHub gepusht oder ein
  Release-Asset ersetzt wird.
- Datenschutzbericht ist pro Shortcut Pflichtbestandteil.
- Nicht veröffentlicht werden lokale Arbeitsarchive, Screenshots, `.DS_Store`
  oder private lokale Projektdateien aus dem ursprünglichen Arbeitsordner.
- Der öffentliche Shortcut-Name bleibt immer Englisch: `Weather for City`.
- Shortcut-Einträge auf der Startseite enthalten ein kleines Vorschaubild,
  nicht nur Text.
- Update-Prüfungen können den neuesten GitHub Release öffnen, aber Apple
  verlangt weiterhin eine Nutzerbestätigung beim Importieren oder Ersetzen.
- Deutsch wird nur für den unterstützten DACH-/Liechtenstein-Gerätekontext
  angezeigt; alle anderen Geräte erhalten Englisch. Keine automatischen
  externen Übersetzungsdienste ohne ausdrückliche Entscheidung ergänzen.
- Ein neu geteilter iCloud-Kurzbefehl hat einen neuen Link. Sichtbare
  Repository-Verweise erst aktualisieren, nachdem der neue Link vorliegt und
  eine Veröffentlichung freigegeben wurde.
- In öffentlichen Texten ausschließlich `Schrotty74` verwenden. Niemals
  persönliche Namen, lokale Pfade, Zugangsdaten, Tokens, private Testdaten oder
  Backups in das Repository aufnehmen.
- Bei jedem öffentlichen Shortcut-Release/Update auch die GitHub-Profilseite
  prüfen und den neutralen Shortcuts-Sammlungseintrag aktuell halten. Dort keine
  einzelnen Shortcut-Release-Links ergänzen, weil das Repository mehrere
  Shortcuts enthalten kann.

## Bekannte Einschränkungen oder Probleme

- Die Release-Status-Automatik ist eine statische Prüfung und ersetzt kein
  manuelles Datenschutzreview.
- Der Wetter-Kurzbefehl sendet den eingegebenen Stadtnamen und Koordinaten an
  Open-Meteo, wie im Datenschutzbericht beschrieben.
- Der Wetter-Kurzbefehl kann die zuletzt gewählte Position lokal im
  Kurzbefehle-Dateibereich speichern. Das ist lokaler Nutzerzustand und darf
  nicht in Release-Archive oder Screenshots aufgenommen werden.
- GitHub Release `v1.2.3` bleibt ein Release für den Wetter-Kurzbefehl, auch wenn
  das Repository künftig weitere Shortcuts enthält.
- Sichtbare Shortcut-Texte existieren derzeit nur auf Deutsch und Englisch.
- Die genauen Berechtigungsdialoge werden von Apple Kurzbefehle gesteuert und
  können je nach Plattform und Menüauswahl variieren.
- Es ist kein projektinternes Build-Skript dokumentiert; Signieren und
  Release-Paketierung sind manuelle, validierte Schritte.

## Pflegehinweis

Bei größeren Änderungen, neuen Shortcuts, neuen Releases oder wichtigen
Entscheidungen müssen diese Datei, [NEXT_STEPS.de.md](NEXT_STEPS.de.md) und die
jeweiligen englischen Kontextdateien aktualisiert werden.
