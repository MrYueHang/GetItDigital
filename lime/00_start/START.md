# [Logo] LiMe – Layout into Model engine

## Gemeinsamer Einstieg
Stand: 28.10.2026. Domain lime.lichtreich.info ist das Ziel; Deployment noch nicht bestätigt.

- Repo-Einstieg: https://github.com/MrYueHang/GetItDigital/blob/docs/lichtreich-restart-handoff/README.md
- Verbindliches Branding: https://github.com/MrYueHang/GetItDigital/blob/docs/lichtreich-restart-handoff/lime/00_start/BRANDING.md
- Lokaler Sammelauftrag und Abfrage-Prompts für alle Prototypen: https://github.com/MrYueHang/GetItDigital/blob/docs/lichtreich-restart-handoff/docs/lichtreich/SAMMELAUFTRAG.md
- Restart-Handoff: https://github.com/MrYueHang/GetItDigital/blob/docs/lichtreich-restart-handoff/docs/lichtreich/RESTART_HANDOFF.md
- Aufgaben: https://github.com/MrYueHang/GetItDigital/blob/docs/lichtreich-restart-handoff/lime/04_aufgaben/README.md
- Inventar: https://github.com/MrYueHang/GetItDigital/blob/docs/lichtreich-restart-handoff/lime/01_inventar/README.md
- Feedback: https://github.com/MrYueHang/GetItDigital/blob/docs/lichtreich-restart-handoff/lime/03_feedback/README.md
- Änderungen/PR: https://github.com/MrYueHang/GetItDigital/pull/1
- Drive: https://drive.google.com/drive/folders/1q98Y_yHFksa8NmMwlMNxwNN2KEagaIFN

## Lokalen Agenten starten
Diesen Auftrag in einen lokalen Agenten geben:
„Lies den verlinkten SAMMELAUFTRAG.md und RESTART_HANDOFF.md. Sammle vorhandene LiMe-Prototypen aus lokalen Projektverzeichnissen, Downloads und der eindeutig zugehörigen synchronisierten Drive-Ablage. Erhalte Originale, dedupliziere Exporte und liefere Inventar, Vergleich, Feedback und nächste Schritte. Verwende die bestätigte Benennung und env-Version-Zuordnung. Implementiere erst nach Sichtung der vorhandenen v0-Basis. Private Inhalte bleiben außerhalb des öffentlichen Repos.“

Der lokale Agent wurde durch diese Dokumentation nicht automatisch gestartet.

## Prototypen abfragen
Abschnitt B des SAMMELAUFTRAG.md ist für jeden bestehenden v0-, Studio-, Manus- und Hercules-Chat gedacht. Abschnitt C ist der Prompt für einen neuen Sammelchat. Ein neuer Chat braucht zusätzlich Zugriff auf die jeweiligen Exporte.

## Repo verwenden
GetItDigital ist der Inhalt, nicht die fertige LiMe-App. Zunächst das vorhandene App-Repo identifizieren und mit einem fixierten Inhaltssnapshot verbinden. PDF.js, CircuitJS und QElectroTech gezielt wiederverwenden. Details und Abnahmen im Restart-Handoff.

## Branding
Name: LiMe
Untertitel: Layout into Model engine
Kopf: [Logo] LiMe – Layout into Model engine
Fuß: lime.lichtreich.info/{env}/{version} · {datum}
manus → v0; studio → v4711. Der Builder v0 ist davon getrennt.
Logo-Platz vorgesehen; Logo, App-Umbenennung und bestehende PDFs noch nicht umgesetzt.

## Ablage und Feedback
00_START: diese Übersicht
01_EINGANG: Exporte und PROTOTYP_HANDOFF.md
02_VERGLEICH: Vergleich und Inventar
03_FEEDBACK: Rückmeldungen und Screenshots
04_FREIGABE: ausdrücklich zur Weitergabe bestimmte Ergebnisse

Die Übersicht wird separat zum Lesen geteilt. Dies erteilt keinen Zugriff auf den gesamten Ordner oder künftige Dateien.

## Review
29.10.2026, 18:00–18:20 Uhr, Europe/Berlin, Erinnerung 15 Minuten vorher.
https://www.google.com/calendar/event?eid=YTgzYWRydWtub2ZlYTI4aDRrOWw4c21oa2cgc3RlZmFuQGJ1c3NlLmlu

# [Logo] LiMe – Layout into Model engine

## Verbindliche Aufgabenübersicht
GitHub Issues sind im Fork deaktiviert (API 410 am 28.10.2026). Diese versionierte Liste führt die Aufgaben, bis Issues aktiviert sind.

| ID | Aufgabe | Status | Abnahme |
|---|---|---|---|
| LIME-001 | Prototypen lokal einsammeln | offen | v0, Studio A/B, Manus, Hercules mit Fundort, Commit/Export und Startstatus erfasst |
| LIME-002 | Kanonisches App-Repo bestimmen | offen | bestehende v0-Basis identifiziert und reproduzierbar gestartet |
| LIME-003 | Branding in allen Varianten | teilweise | Repo-Doku vorbereitet; UI, Logo-Platz, Impressum, Handbuch, Materialliste, PDF-Export geprüft |
| LIME-004 | GetItDigital-Modul 1 anbinden | offen | echte Quelle, Aufgabe, Attribution und stabiler Quellstand sichtbar |
| LIME-005 | Vorhandene Komponenten integrieren | offen | PDF.js, passende CircuitJS-Simulation und QET-Beispieldatei tatsächlich verwendbar |
| LIME-006 | Zustand und Export prüfen | offen | Wiederöffnung erhält Lernfortschritt; Export enthält Herkunft und LiMe-Fußzeile |
| LIME-007 | Drive-Sammlung teilen | teilweise | Startdatei-Freigabe gesondert prüfen; Ordnerfreigabe vom Anschluss nicht unterstützt |
| LIME-008 | Review | geplant | Kalender: 29.10.2026, 18:00 Europe/Berlin, 20 Minuten |
| LIME-009 | Zieladresse bereitstellen | offen | lime.lichtreich.info tatsächlich erreichbar; keine DNS-/Deployment-Zusage |
| LIME-010 | Bestehende PDFs umbenennen | offen | alte Link-Sammlung und Folgeartefakte nach Brandingvorgabe überarbeitet |

## Arbeitsregel
Je Aufgabe ein Bearbeiter und Branch; Fortschritt mit Commit/Prüfbeleg hier aktualisieren. Keine Duplikate beim Wiederanlauf. Offene Eingänge verhindern nur abhängige Arbeit.

lime.lichtreich.info/handoff/0.1 · 2026-10-28


lime.lichtreich.info/handoff/0.1 · 2026-10-28
