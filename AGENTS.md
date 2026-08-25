# AGENTS.md

Dieses Repository ist eine öffentliche Sammlung von Apple Shortcuts. Es ist keine einzelne App. Root-Dokumente beschreiben die Sammlung; shortcut-spezifische Dokumentation und Release-Dateien gehören in den jeweiligen Unterordner unter `shortcuts/`.

Vor jeder Projektarbeit zuerst `PROJECT_CONTEXT.md`, `NEXT_STEPS.md`, `README.md` und bei Bedarf die deutschen Gegenstücke lesen. Anschließend nur die für den konkreten Shortcut relevanten Dateien und Dokumente prüfen.

## Verbindliche Arbeitsregeln

- `PROJECT_CONTEXT.md` und `PROJECT_CONTEXT.de.md` beschreiben Struktur, Workflows, veröffentlichte Shortcuts und dauerhafte Sammlungsregeln.
- `NEXT_STEPS.md` und `NEXT_STEPS.de.md` enthalten nur tatsächlich offene Aufgaben und bestätigte Probleme.
- Root-Dateien bleiben für die Sammlung reserviert. Shortcut-spezifische Versionen, Changelogs, Release Notes, Privacy Reports, Checksums, Assets und Release-Dateien gehören in den jeweiligen Shortcut-Ordner.
- Englische und deutsche Begleitdokumente müssen dort, wo beide existieren, inhaltlich gleichwertig bleiben. Changelog und Release Notes bleiben nach den bestehenden Projektregeln Englisch.
- Bestehende Shortcut-Struktur, Datenformate und Veröffentlichungsabläufe erhalten, sofern eine Änderung nicht ausdrücklich verlangt oder technisch notwendig ist.
- Keine unnötigen Refactorings, neuen Abhängigkeiten, Branches, Pull Requests oder temporären Workflows ohne klaren Auftrag erstellen.
- Für dieses Repository gilt der dokumentierte `main`-Workflow. Keine zusätzlichen Branches nur zur Vereinheitlichung anlegen.
- Keine Projektzustände, Testergebnisse, Signaturen, Builds, Checksums, Prüfungen oder offenen Punkte erfinden. Einen Erfolg nur behaupten, wenn die betreffende Prüfung tatsächlich ausgeführt wurde.
- Fragen nicht automatisch als Änderungsauftrag behandeln. Dateien, Tests, Signierung, Paketierung, Commits, Pushes, Tags, Releases oder iCloud-Link-Änderungen nur ausführen, wenn der Auftrag dies verlangt oder sie für eine ausdrücklich beauftragte Änderung notwendig sind.
- Keine Commits, Pushes, Tags, GitHub Releases oder Änderungen öffentlicher iCloud-Links ohne ausdrücklichen Auftrag.
- Öffentliche Entwicklerangaben verwenden ausschließlich `Schrotty74`.
- Keine Regeln zur Vorbereitung oder Fortsetzung eines neuen Chats aufnehmen. Solche Anweisungen gehören ausschließlich in `CHAT_TEMPLATE.md` beziehungsweise in einen separaten Start-Prompt.

## Sammlungs- und Shortcut-spezifische Regeln

- Jeder veröffentlichte Shortcut bleibt vollständig in seinem eigenen Unterordner unter `shortcuts/` dokumentiert.
- Jeder öffentliche Shortcut benötigt nach den bestehenden Projektregeln einen eigenen Datenschutzbericht.
- Signierte `.shortcut`-Dateien, lesbare XML-/Plist-Quellen, Versionsdateien, Checksums und Release-Pakete nur aus tatsächlich geprüftem Stand veröffentlichen.
- Bei Änderungen an einem Shortcut die zugehörige Dokumentation, Versionierung, Checksums, Privacy Reports und gegebenenfalls Portfolio-/Profil-Verweise nach den vorhandenen Projektregeln prüfen.
- Änderungen an einem Shortcut dürfen andere Shortcuts in der Sammlung nicht unbeabsichtigt verändern.
- Gespeicherte lokale Shortcut-Daten, persönliche Automationen, private iCloud-Inhalte oder gerätespezifische Zustände gehören nicht in das Repository.

## Datenschutzregel für das öffentliche Repository

Dieses Repository und seine Git-Historie sind öffentlich. Jeder eingecheckte oder veröffentlichte Inhalt muss deshalb ohne weitere Bereinigung öffentlich vertretbar sein.

Nicht veröffentlicht oder dokumentiert werden dürfen insbesondere:

- private, personenbezogene oder vertrauliche Daten
- reale Namen oder private Kontaktdaten
- Informationen über persönliche Fähigkeiten, Kenntnisse, Gewohnheiten oder Arbeitsweise des Entwicklers
- lokale Benutzernamen, Home-Verzeichnisse sowie konkrete lokale Benutzer-, Volume- oder Backup-Pfade
- private Hostnamen, interne Netzwerkadressen oder interne URLs
- Gerätekennungen, Seriennummern, Hardware-IDs oder vergleichbare Identifikatoren
- Passwörter, API-Keys, Tokens, Secrets, Zugangsdaten oder private Accountdaten
- private Signing-Informationen, Zertifikatsgeheimnisse oder andere vertrauliche Veröffentlichungsdaten
- Lizenzschlüssel oder private Lizenzdaten
- echte Benutzer-, Gesundheits-, Finanz-, Katalog-, Scan-, Mess-, Export- oder sonstige Nutzerdaten
- echte Backups, Datenbanken oder private Arbeitsdateien
- persönliche Shortcut-Eingaben, gespeicherte Orte, persönliche Automationen oder private iCloud-Daten
- Logs, Diagnoseausgaben, Screenshots oder Medien mit privaten oder identifizierenden Informationen
- Metadaten, aus denen private Informationen rekonstruiert werden können
- Inhalte aus privaten Chats, E-Mails oder anderen nicht öffentlichen Quellen

Beispiele, Testdaten, Vorschauen und Screenshots müssen ausschließlich synthetische, anonymisierte oder eindeutig fiktive Daten verwenden. Bewusst öffentliche Assets dürfen verwendet werden.

Pfade in öffentlicher Dokumentation müssen neutral sein, zum Beispiel `/Users/example/...`. Echte lokale Benutzernamen oder persönliche Volume-Namen dürfen nicht verwendet werden.

Vor Commit, Push oder Veröffentlichung prüfen, dass keine privaten oder sensiblen Daten enthalten sind. Vor öffentlichen Shortcut-Releases zusätzlich die vorhandenen shortcut-spezifischen Datenschutz- und Integritätsprüfungen durchführen.

Wenn unklar ist, ob eine Information öffentlich sein darf, wird sie nicht veröffentlicht, bis dies eindeutig geklärt ist.
