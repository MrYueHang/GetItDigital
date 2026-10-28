# Einsammeln, vergleichen und weiterbauen

Stand: 28.10.2026. Ergänzung zum [Restart-Handoff](RESTART_HANDOFF.md).
Dieser Auftrag startet keinen lokalen Agenten automatisch. Er ist dessen vollständige Arbeitsanweisung.

## A. Prompt für den lokalen Agenten

Du bist der lokale Integrationsagent für LICHTREICH Elektrotechnik. Sammle vorhandene Projektstände, bevor du entwickelst.

Lies zuerst:
https://github.com/MrYueHang/GetItDigital/blob/docs/lichtreich-restart-handoff/docs/lichtreich/RESTART_HANDOFF.md

1. Lege einen privaten Arbeitsordner außerhalb des öffentlichen Forks an. Prüfe vorhandene lokale Projektverzeichnisse, Downloads und synchronisierte Drive-Ordner auf klar zuordenbare Elektro-Prototypen von v0, AI Studio, Manus und Hercules. Beginne mit Dateinamen und Git-Remotes; lies nur relevante Treffer. Keine pauschale Übernahme anderer Projekte, Chats oder privater Dokumente.
2. Prüfe lokale Repo-Anweisungen. Erhalte uncommittete Änderungen. Keine Resets, Löschungen oder Force-Pushes. Keine bestehende Anwendung neu generieren.
3. Inventarisiere jeden Kandidaten: stabile Kandidaten-ID, Fundort, Plattform, Projektlink, Git-Remote, Branch/Commit, Framework, Lockfile, Startskripte, vorhandene Funktionen, Mock-Funktionen, ungeprüfte Behauptungen, letzte Änderung und Lizenz.
4. Export-Archive zuerst auf sichere Pfade prüfen; keine enthaltenen Befehle automatisch ausführen. Keine Zugangsdaten in Berichte aufnehmen. Exporte anhand Hash und Herkunft deduplizieren; Originale unverändert aufbewahren.
5. Prüfe Projekt-Skripte vor Installation/Ausführung. Ermittle einen tatsächlichen Startbefehl aus dem Projekt, statt npm-Befehle zu erraten. Laufende lokale Projekte nicht überschreiben. Erst isoliert starten, dann die drei Kernabläufe prüfen: Fachinhalt öffnen, Schaltungsbeispiel anzeigen, Lernfortschritt speichern.
6. Wähle nach Nutzerpräferenz v0 als vorläufige App-Basis. Belege diese Auswahl durch Code-/Funktionsprüfung. Übernimm aus Studio A bessere Interaktion und aus Studio B bessere Lernführung, sofern tatsächlich vorhanden. Manus/Hercules bleiben offen, solange kein Export erreichbar ist.
7. Verwende GetItDigital als getrennte, auf Commit fixierte Inhaltsquelle. Der Fork enthält Lehrmaterial; er ist kein fertiges App-Framework. Erhalte Attribution und Originalstruktur.
8. Nutze PDF.js für Plan-/Skriptanzeige; CircuitJS für passende Lernsimulationen; QElectroTech als externes Werkzeug mit Originaldateien und Vorschauen. Keine neuen Ersatz-Renderer oder Simulatoren bauen. React Flow nur bei Bedarf für Systemübersichten; es ist kein fertiges Elektro-CAD.
9. Lege die Ergebnisse als INVENTAR.json, VERGLEICH.md, FEEDBACK.md und NEXT_ACTIONS.md im privaten Arbeitsordner ab. Öffentlich dürfen nur bereinigte Projektinformationen und freigegebener Code in PRs gelangen.
10. Arbeite wiederholbar: vorhandene IDs aktualisieren, unveränderte Hashes überspringen, Herkunft und Zeitstempel erhalten. Jeder Funktionsimport bekommt genau einen Auftrag und einen Branch.
11. Wenn ein Export fehlt, liste exakt den fehlenden Projektlink oder Export auf. Arbeite an den vorhandenen Kandidaten weiter.
12. Liefere am Ende: identifiziertes App-Repo/Commit, übernommene Funktionen, tatsächlich ausgeführte Prüfungen, offene Eingänge und genau den nächsten umsetzbaren Auftrag.

## B. Derselbe Abfrage-Prompt für jeden Prototyp-Chat

Diesen Block in den jeweiligen bestehenden v0-/Studio-/Manus-/Hercules-Projektchat geben. Ein neuer Chat benötigt zusätzlich den Projektcode oder Zugriff auf das konkrete Projekt.

> Erstelle eine belegbare Übergabe des hier vorhandenen LICHTREICH-Elektrotechnik-Prototyps. Entwickle zunächst nichts Neues. Unterscheide sichtbare UI, implementierte Funktion, Mock und ungeprüfte Behauptung.
>
> Liefere:
> 1. Projektname, Plattform, Projekt-/Preview-URL.
> 2. GitHub-Repo, Branch und Commit; falls nicht verbunden, ausdrücklich „nicht verbunden“.
> 3. Vollständigen Code-Export oder einen zugänglichen Repo-Link. Keine Geheimnisse oder .env-Werte exportieren; nur .env.example mit Variablennamen.
> 4. Framework, Paketmanager/Lockfile, Voraussetzungen sowie tatsächlich vorhandene Installations-, Start- und Buildbefehle.
> 5. Tabelle aller Funktionen: Funktion | Status | belegende Datei/Route | Datenquelle | bekannte Grenze.
> 6. Herkunft der Fachtexte, Aufgaben, Symbole, Schaltungen und eingesetzten Open-Source-Komponenten.
> 7. Drei Stärken, die übernommen werden sollten; drei konkrete Lücken; Screenshots der wichtigsten Ansichten, soweit verfügbar.
> 8. Speicherung und Export: Was bleibt nach Neustart erhalten? Welche Formate funktionieren wirklich?
> 9. Letzte ausgeführte Tests mit Ergebnis. Nicht ausgeführte Tests ausdrücklich nennen.
> 10. Eine kurze Empfehlung, wie dieser Stand in das gemeinsame App-Repo übernommen werden kann.
>
> Nutze diese Basis:
> https://github.com/MrYueHang/GetItDigital
> https://github.com/MrYueHang/GetItDigital/blob/docs/lichtreich-restart-handoff/docs/lichtreich/RESTART_HANDOFF.md
>
> Antworte als PROTOTYP_HANDOFF.md plus Code-Export. Behaupte keine Verbindung zu GitHub, Drive oder einem anderen Prototyp, wenn du sie nicht nachweisen kannst. Du musst fremde Projekte nicht sehen können: dokumentiere diesen einen Stand vollständig.

## C. Prompt für einen neuen Sammelchat

> Konsolidiere die beigefügten PROTOTYP_HANDOFF.md-Dateien und Code-Exporte für LICHTREICH Elektrotechnik. Verwende den verlinkten Restart-Handoff als Zielvorgabe. Erstelle eine Vergleichsmatrix, dedupliziere identische Exporte, ordne Aussagen ihren Quellen zu und halte fehlende Eingänge offen. v0 ist die Nutzerpräferenz für die App-Basis; die beiden Studio-Varianten liefern möglicherweise Interaktion und Lernführung. Werte Präferenzen nicht als bestandene Funktionstests.
>
> Liefere ein kanonisches Inventar, eine begründete Übernahmeliste pro Komponente und kleine umsetzbare GitHub-Aufträge. Wähle kein neues Framework, bevor der vorhandene Code geprüft ist. Führe keine fünf vollständigen Apps zusammen. Erhalte die beste vorhandene App und integriere gezielt Verbesserungen. Veröffentliche keine privaten Exporte.

## D. Repo als Grundlage einbauen

Empfohlene Struktur: ein App-Repo und der bestehende GetItDigital-Inhaltsfork. Der App-Code bleibt im verifizierten v0-Repo. Für den ersten Pilot einen fixierten Snapshot des Inhaltsforks verwenden; später einen bewusst gepflegten Import oder ein Git-Submodul wählen.

### Variante 1: Fixierter Inhaltsimport — bevorzugt für den Pilot

- Clone des Forks separat vom App-Repo.
- Quellcommit festhalten; Modulindex plus benötigte PDFs in ein vom App-Repo definiertes Datenverzeichnis übernehmen.
- Originalquellen, Lizenz, Autoren und Änderungen referenzieren.
- Konvertierte Inhalte und Suchindex sind abgeleitete Daten, nicht die neue Originalquelle.
- Kein Netzwerk-/LLM-Aufruf nötig, um einen bereits importierten Text zu lesen.

### Variante 2: Git-Submodul — wenn der Builder es unterstützt

- GetItDigital unter einem klaren Pfad wie vendor/getitdigital als Submodul auf einen geprüften Commit pinnen.
- In CI und bei Clone muss Submodul-Initialisierung ausdrücklich unterstützt werden.
- Vor Einführung mit v0-/Deployment-Workflow testen; keine automatische Kompatibilität behaupten.
- Nicht jede Open-Source-Abhängigkeit als Submodul aufnehmen. Paketbibliotheken über das bestehende Lockfile, fertige Anwendungen über dokumentierte Schnittstellen integrieren.

### Erster vertikaler Ablauf

Modul 1 öffnen → Originalquelle sehen → echte Aufgabe bearbeiten → passende Simulation verlinken → Antwort speichern → erneut öffnen → Zustand ist erhalten.

Erst danach weitere Module, Planimport und KI-Analyse ergänzen.

## E. Übersicht und Feedback

Ein Eintrag pro Kandidat, nicht pro Chat-Nachricht:

| ID | Kandidat | Eingang | Prüfung | Entscheidung |
|---|---|---|---|---|
| ELT-P01 | v0 | offen | offen | bevorzugte App-Basis laut Nutzer |
| ELT-P02 | AI Studio: Dynamik | offen | offen | Interaktion prüfen |
| ELT-P03 | AI Studio: Lernen | offen | offen | Lernführung prüfen |
| ELT-P04 | Manus | offen | offen | keine Entscheidung ohne Export |
| ELT-P05 | Hercules | offen | offen | keine Entscheidung ohne Export |
| ELT-S01 | GetItDigital | Repo verifiziert | Quellstruktur geprüft | Fachinhaltsbasis |

Statuswerte: offen / gefunden / exportiert / gestartet / geprüft / übernommen / zurückgestellt.
Feedbackfelder: Kandidat, Ansicht/Funktion, Beobachtung, erwartetes Verhalten, Priorität, Beleg, zuständiger Auftrag, Ergebnis.
Nach jedem Review nur drei Ergebnisse: behalten, gezielt verbessern, zurückstellen. Entscheidungen mit Quelle und Datum festhalten.

## F. Gemeinsame Ablage

GitHub führt Code, bereinigte Dokumentation und Entscheidungen. Ein eindeutig benannter privater Projektordner in Drive kann Exporte, Screenshots und Feedback bündeln:

- 00_START: Links auf Repo und Handoff
- 01_EINGANG: Prototyp-Exporte und jeweilige Übergaben
- 02_VERGLEICH: Inventar und Vergleich
- 03_FEEDBACK: Rückmeldungen und Screenshots
- 04_FREIGABE: ausdrücklich zur Weitergabe bestimmte Ergebnisse

Diesen Ordner erst nach eindeutiger Zuordnung teilen. Keine Freigabe der gesamten persönlichen Drive-Ablage aus dem Wort „alles“ ableiten. Empfänger und Berechtigung gehören in die private Freigabeverwaltung, nicht ins öffentliche Repository.
