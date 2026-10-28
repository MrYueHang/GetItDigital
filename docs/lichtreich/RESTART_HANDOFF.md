# LICHTREICH Elektrotechnik — Restart und gemeinsamer Handoff

Stand: 28.10.2026. Status: Arbeitsvorgabe und Bestandsaufnahme, keine fertig integrierte App.

## 1. Entscheidung

GitHub ist die gemeinsame, versionierte Quelle. Dieser Fork ist jetzt die bestätigte Fachinhaltsbasis und der Einstieg für den Handoff:
https://github.com/MrYueHang/GetItDigital

Die vorhandene v0-Oberfläche ist nach Nutzerbewertung der bevorzugte Ausgangspunkt für Praxisabläufe und Design. Sie wird nach Identifikation ihres Codes weiterentwickelt. Die beiden AI-Studio-Prototypen liefern gezielt Interaktion und Lernführung. Hercules und Manus bleiben weitere Kandidaten, bis ihre Exporte vorliegen. Keine neue parallele Voll-App erzeugen.

**Arbeitsentscheidung:** Fachinhalte hier belassen. Ein bereits existierendes v0-App-Repo wird nach Nachweis zum einzigen App-Repo. Bis dahin kein zusätzliches App-Repo erfinden oder anlegen. Dieses Dokument bleibt der Einstieg; später den verifizierten App-Repo-Link hier ergänzen.

## 2. Tatsächlich geprüft

- Fork unter MrYueHang erreichbar, öffentlich, Default-Branch main.
- Basis-Commit: 11d4bade3ffbaba68675f033a99991f22bb1e1d6.
- Zwölf Modulordner, LaTeX-Skripte, Aufgaben, Templates und Video-Verzeichnis vorhanden.
- README beschreibt elektrotechnische Grundlagen. LICENSE enthält CC BY 4.0.
- Rekursiver Baum vollständig geliefert; keine package.json und keine AGENTS.md im geprüften Baum gefunden.
- Vorhandener Devcontainer ist für LaTeX eingerichtet, nicht für einen nachgewiesenen Web-App-Stack.
- Workflow .github/workflows/komplett.yml baut PDFs mit LaTeX und hat SFTP-Uploadschritte mit SFTP_KEY/SFTP_USERNAME/SFTP_SERVER.
- Der Workflow reagiert auf main-Pushes und Pull Requests. Seine erfolgreiche Ausführung im Fork ist nicht bestätigt.
- In der gelieferten Liste erreichbarer Nutzer-Repos und der Suche nach „elektro“ konnte kein Elektro-v0-/Studio-/Manus-/Hercules-Prototyp eindeutig identifiziert werden. Das ist kein Nachweis ihrer Nichtexistenz.

Prüfquellen:
- [README](../../README.md)
- [LICENSE](../../LICENSE)
- [LaTeX-Workflow](../../.github/workflows/komplett.yml)
- [Devcontainer](../../.devcontainer/devcontainer.json)

## 3. Prototypen zusammenführen

| Kandidat | Gewünschte Übernahme | Evidenz/Status | Nächste Aktion |
|---|---|---|---|
| v0 | Praxisführung, Layout, Design, vorhandene Komponenten | Nutzerpräferenz; Code und Deployment nicht zugeordnet | GitHub-Verknüpfung/Export ermitteln, Build prüfen, als App-Basis markieren |
| AI Studio A | dynamische Interaktionen | Nutzerbeschreibung; genaue Variante offen | Export separat inventarisieren, passende Komponenten übernehmen |
| AI Studio B | Lernstruktur, Erklärungen, Aufgabenführung | Nutzerbeschreibung; genaue Variante offen | Lernablauf als Funktionsvergleich erfassen und gezielt übernehmen |
| Hercules | noch offen | nicht geprüft | nur nach sichtbarem Projekt/Export bewerten |
| Manus | noch offen | nicht geprüft | nur nach sichtbarem Projekt/Export bewerten |
| GetItDigital | echte Fachinhalte, Aufgaben, Abbildungen, Herkunft | Repo geprüft | Modul 1 als ersten vertikalen Anwendungsfall anbinden |

Für jeden Export erfassen: Projekt-URL, Repo-URL, Commit, Framework, Paketmanager/Lockfile, Startbefehl, funktionierende Funktionen, Mock-Daten, Screenshots, Lizenz und benötigte Umgebungsvariablen (nur Namen, keine Werte).

Kein pauschales Zusammenkopieren verschiedener node_modules-, Lockfile- oder App-Router-Strukturen. Die App-Basis bestimmt Framework und Paketmanager. Änderungen der anderen Prototypen werden komponentenweise in Branches übernommen.

## 4. Open Source konkret wiederverwenden

### A. GET it digital — fertiger Inhalt

- Upstream: https://github.com/GetItDigital/GetItDigital
- Eigener Fork: https://github.com/MrYueHang/GetItDigital
- Fertige PDFs: https://getitdigital.uni-wuppertal.de/module/
- Materialübersicht: https://getitdigital.uni-wuppertal.de/index.php?site=handreichung

Direkt nutzbar: Lehrtexte, Aufgaben, Abbildungen und Skripte. Die LaTeX-Quellen sind kein fertiges JSON-CMS und keine fertige Lern-Web-App. Zunächst fertige PDFs anzeigen und einen kleinen, quellgebundenen Inhaltsindex erzeugen. Später die relevanten LaTeX-Bestandteile gezielt konvertieren. Komplexe Makros und TikZ nicht blind mit regulären Ausdrücken entfernen.

Attribution mitführen: Autorenschaft, Titel, Originalquelle, Lizenz, Änderungsvermerk. Ausnahmen einzelner Medien beachten. Eigenen App-Code und fremde Lehrinhalte nicht pauschal unter eine gemeinsame Lizenz umetikettieren.

### B. PDF.js — fertige PDF-Anzeige

- Repo: https://github.com/mozilla/pdf.js
- Demo: https://mozilla.github.io/pdf.js/web/viewer.html

Geprüftes README: HTML5-PDF-Viewer und PDF-Rendering. Übernehmen für Skripte und Planansicht statt eines selbstgebauten PDF-Renderers. Kein OCR- oder Schaltplanverständnis versprechen. Integration, Worker-Konfiguration und Browser-Kompatibilität im gewählten App-Stack testen.

### C. CircuitJS1 — fertige interaktive Simulation

- Repo: https://github.com/sharpie7/circuitjs1
- Nutzbare Anwendung laut README: http://www.falstad.com/circuit/

Geprüftes README: Browser-Schaltungssimulator; Einbettung per iframe und Startparameter für Schaltungsbeispiele dokumentiert. GPL-2.0-or-later laut README. Für Lernschaltungen verwenden, zum Beispiel Spannungsteiler oder RC-Verhalten. Zunächst verlinken; bei eigener Bereitstellung passenden Build und Einbettung testen. Alte Build-/Electron-Angaben im README nicht ungeprüft übernehmen.

Kein Ersatz für Installationsplanung, Schutzkonzept oder Netzberechnung. Keine automatische Übersetzung beliebiger QET-Pläne in eine Simulation behaupten.

### D. QElectroTech — fertige Stromlaufplan-Arbeit

- Projekt: https://qelectrotech.org/
- GitHub: https://github.com/qelectrotech/qelectrotech-source-mirror
- Funktionen: https://qelectrotech.org/test/lang-en/features.php

Fertige Desktop-Anwendung für Stromlaufpläne. Dokumentiert sind unter anderem PDF/SVG-Ausgabe, CSV-Bauteillisten und XML-basierte Elemente/Projekte. Zunächst QET-Originale als Dateien behalten, PDF/SVG-Vorschau und Metadaten in der App darstellen. Ein QET-Browsereditor, ein sicherer Roundtrip oder ein automatischer CAD-Adapter sind zusätzliche Entwicklungsarbeiten.

### E. React Flow / xyflow — optional für Systemübersichten

- Repo: https://github.com/xyflow/xyflow
- Dokumentation: https://reactflow.dev/learn

Geprüftes README: MIT-lizenzierte Bibliothek für knotenbasierte React-/Svelte-Oberflächen. Nur einsetzen, wenn der vorhandene Prototyp einen entsprechenden Editor benötigt. Passend für Anlagenübersichten und didaktische Knotenansichten. Elektrische Symbolik, Anschlusssemantik und Prüfregeln sind dadurch noch nicht vorhanden.

**Priorität:** GET-Inhalte + PDF.js zuerst; CircuitJS als fertiges Lernwerkzeug; QET-Dateien als Praxisbeispiele. React Flow erst bei belegtem Bedarf. Nicht alle Projekte forken oder installieren.

## 5. Zielablauf der ersten brauchbaren Version

1. Nutzer öffnet Fachmodul oder Praxisbeispiel.
2. App zeigt echten Inhalt mit sichtbarer Herkunft.
3. Passende Aufgabe oder Schaltung ist direkt daneben erreichbar.
4. Eine vorhandene Simulation wird geöffnet, wenn sie fachlich passt.
5. Eigene Notiz bzw. Antwort lässt sich speichern und exportieren.
6. Rückkehr in dasselbe Projekt stellt den gespeicherten Zustand wieder her.

Erster Demonstrator: Modul 1, mindestens ein echtes Aufgabenbeispiel und ein Quellenverweis. Zweiter Demonstrator: ein geprüftes Schaltungsbeispiel mit Originaldatei und PDF-Vorschau. Keine Kundenpläne im öffentlichen Repo.

## 6. Vertrag für Daten und Quellen

Vorgeschlagener Datensatz, erst nach Abgleich mit dem App-Code implementieren:

~~~json
{
  "id": "getitdigital:modul-01:quelle-001",
  "type": "lesson",
  "title": "Titel aus der Originalquelle",
  "source": {
    "repository": "MrYueHang/GetItDigital",
    "commit": "11d4bade3ffbaba68675f033a99991f22bb1e1d6",
    "path": "modul-01-elektrische-grundgroessen/1_Ladung.tex",
    "locator": "Abschnitt bzw. Zeilenbereich beim Import bestimmen",
    "license": "CC-BY-4.0",
    "attribution": "Aus konkreter Quelle übernehmen"
  },
  "review_status": "unreviewed",
  "derived": false
}
~~~

IDs müssen bei wiederholtem Import stabil bleiben. Quell-Commit und Inhaltshash getrennt halten: neuer Commit aktualisiert eine Quelle, erzeugt nicht automatisch ein zweites Lernobjekt. Hash gleicher Inhalte dedupliziert; Ortsverweise zu mehreren Fundstellen bleiben erhalten. Kennzeichnung für Original, Bearbeitung und KI-Entwurf beibehalten.

Für Schaltungen zusätzlich: Originalformat, Vorschaudatei, Komponenten-IDs, Anschluss-IDs, bestätigte Verbindungen, offene Verbindungen und Prüfstatus. SVG beschreibt zunächst eine Darstellung, keine verlässlich abgeleitete elektrische Topologie.

## 7. Zusammenarbeit ohne neue Inseln

- Eine Aufgabe hat eine ID, einen Branch und einen verantwortlichen Bearbeiter.
- Jeder Builder liest zuerst diesen Handoff sowie später die Projektdateien des kanonischen App-Repos.
- Vor Änderungen: Ausgangscommit und betroffene Dateien festhalten.
- Nach Änderungen: Commit, Startbefehl, durchgeführte Prüfungen und verbleibende Einschränkungen dokumentieren.
- Änderungen über PRs zusammenführen; keine parallelen Komplett-Neugenerierungen.
- Gleiche Quelle erneut importieren ergibt keinen doppelten Datensatz.
- Exporte aus nicht direkt angebundenen Buildern werden als klar benannter Commit übernommen; keine GitHub-Synchronisierung behaupten, bevor sie getestet ist.
- NotebookLM und AI Studio erhalten abgeleitete Exportpakete mit Quellstand. Bearbeitbare Originale bleiben im Repo.
- Kein automatischer Rückschreibkanal aus NotebookLM wird vorausgesetzt.

## 8. Restart-Aufträge mit Abnahme

| ID | Auftrag | Fertig, wenn |
|---|---|---|
| ELT-001 | v0-Code identifizieren und sichern | Repo/Commit, Lockfile und reproduzierbarer Start bekannt |
| ELT-002 | Prototypen vergleichen | Funktionsmatrix mit echten Screenshots/Codebelegen vorhanden |
| ELT-003 | Modul 1 anbinden | Inhalt, Quelle und Aufgabe sichtbar; kein Platzhaltertext |
| ELT-004 | PDF.js anbinden | echtes Skript öffnet, Seitenwechsel und Zoom funktionieren |
| ELT-005 | CircuitJS-Beispiel verknüpfen | geprüfte Lernschaltung startet; Rückweg zum Lernmodul vorhanden |
| ELT-006 | QET-Praxisbeispiel aufnehmen | Original und Vorschau gehören nachweisbar zum selben Planstand |
| ELT-007 | Speichern und Export prüfen | Neustart erhält Zustand; Export nennt Quellstand |
| ELT-008 | Fork-Build bereinigen | PDF-Build und optionale Veröffentlichung getrennt; keine fremden SFTP-Ziele erforderlich |

ELT-008: Vorhandene Builddateien erhalten und gezielt anpassen. Dokumentationsänderungen sollen keinen vollständigen LaTeX-/SFTP-Lauf benötigen. Veröffentlichung explizit vom Build trennen. In diesem Handoff wurden Workflows nicht verändert und keine Secrets eingerichtet.

## 9. Copy-paste-Auftrag für v0 / Studio / Codex / Manus

> Arbeite am vorhandenen LICHTREICH-Elektrotechnik-Prototyp weiter. Lies zuerst diesen Handoff und prüfe den tatsächlichen Projektcode. Nutze die vorhandene v0-Oberfläche als bevorzugte Basis, sobald ihr Export identifiziert ist. Erhalte funktionierende Praxisabläufe und Design. Binde die Fachinhalte aus MrYueHang/GetItDigital an; verwende echte Quellen und stabile IDs. Nutze PDF.js für PDFs, CircuitJS für geeignete Lernsimulationen und QElectroTech-Dateien für praktische Stromlaufplanbeispiele. Baue diese Funktionen nicht neu. Übernimm aus den AI-Studio-Prototypen nur belegte bessere Interaktionen und Lernabläufe. Halte Änderungen im kanonischen App-Repo als Branch/PR fest. Liefere zuerst einen durchgängigen Ablauf mit Modul 1, Quellenanzeige, echter Aufgabe und gespeichertem Fortschritt. Markiere fehlende Exporte als offen; erfinde keine Funktionen oder Integrationen. Liefere Commit, Startbefehl, Prüfresultate und nächste Aufgabe. Elektrische Entwürfe benötigen fachliche Prüfung.

## 10. Lokal den Handoff holen

Nur Clone/Aktualisierung, kein Installer und kein App-Start. Vorhandene lokale Änderungen bleiben erhalten.

~~~bash
(
  set -eu
  project_dir="$HOME/Projects/GetItDigital"
  mkdir -p "$HOME/Projects"
  if [ ! -e "$project_dir" ]; then
    git clone https://github.com/MrYueHang/GetItDigital.git "$project_dir"
  fi
  git -C "$project_dir" rev-parse --git-dir >/dev/null
  actual_origin="$(git -C "$project_dir" remote get-url origin)"
  case "$actual_origin" in
    https://github.com/MrYueHang/GetItDigital.git|https://github.com/MrYueHang/GetItDigital|git@github.com:MrYueHang/GetItDigital.git) ;;
    *) printf '%s\n' "Anderes origin im Zielordner; keine Änderung."; exit 1 ;;
  esac
  git -C "$project_dir" fetch origin
  git -C "$project_dir" show origin/docs/lichtreich-restart-handoff:docs/lichtreich/RESTART_HANDOFF.md
)
~~~

## 11. Grenzen dieser Übergabe

Der Handoff ist im GitHub-Fork hinterlegt. Prototypen wurden nicht zusammengeführt, keine App installiert oder veröffentlicht. Ihre Links/Exporte sind der verbleibende konkrete Eingang für die Implementierung. Die Fachinhalte können unabhängig davon bereits als Grundlage dienen.
