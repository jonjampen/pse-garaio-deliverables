# Protokoll Kunden-Meeting vom 25.02.2026

- **Wann**: 25.02.2026, 10:30 - 11:15 Uhr
- **Wo**: Garaio Ag
- **Leitung**: Noah Baumgartner
- **Protokollführung**: Jon Jampen
- **Anwesende**:
    - Team: Noah, Sebastian, Silvan, Olaf, Jon
    - HA: Elisa
    - Garaio: Luca, Sven

## Traktanden

- Projektvision & Anforderungen
- Technisches Setup & Rahmenbedingungen
- Organisatorisches & Zusammenarbeit
- Planung Iteration 1 (Planning Game 1)

## Besprochene Themen

### Einführung in Garaio REM Ag

Sven (Chef von Luca) stellt die Firma und deren Aufbau vor. Garaio REM bietet ein ERP System für Mieter (inkl. Tools für Mietende) zur Verwaltung der Immobilien. Garaio REM ist eine sogenannte Property Technology Company.

Es gibt 2 Hauptteile vom ERP: core (das ERP zur Verwaltung von Verträgen, Buchhaltung, etc.) und untercore (Addons, primär im Mobile-Bereich)

Garaio REM Ag ist in einer flachen Hierarchie aufgebaut und setzt Fokus auf Domänenspezialisierung.

### Präsentation Luca

Luca beantwortet unsere Fragen (per Mail im Voraus eingereicht) mit einer Präsentation.

#### Projektvision & Anforderungen

**Provisionary** (= Provision + Visionary): Eine App zur Überwachung, Aktualisierung und Editierung des Zustands der Provision der Services auf den Servern von Garaio.

Kunden können bestimmte Services dazu lösen. Die Provisionary Web-App soll die Verwaltung dieser Services ermöglichen (z.B. wer auf welchen Service Zugriff hat).

Die Services laufen auf Servern, welche über RabbitMQ (RMQ) mit dem RMQ-Server von Garaio kommunizieren. Ziel ist es nun, einen zentralisierten Konfigurationsmanager zu erstellen, der den Scope (Zugriff auf welche Services) der Kunden verwaltet.

#### Technisches Setup & Rahmenbedingungen

Ruby on Rails (RoR, ein fullstack Web-Framework) Applikation.

Luca hat bereits das Repo aufgesetzt (wir sind nicht mehr im Team wegen Berechtigungen, trotzdem Zugriff auf Repo: https://github.com/Garaio-REM/provisionary). Wir sollen mit Docker-Containers arbeiten (erlaubt systemunspezifische Entwicklung, da alles im Container drin ist).

Anforderungen:

- Semilineare Git-History: Pull-Requests (PRs) auf `main`: zuerst `main` in den Feature-Branch mergen, bevor dieser ins `main` gemerged wid.
- 4 Augen Prinzip: PR immer von jemandem reviewen lassen, vor dem Merge
- Tests: alle Controllers, Models und Jobs müssen getestet sein.
- Tools: keine bis kaum Unterstützung von KI. Bei Problemen auf Luca zugehen, statt KI. Beim hinzufügen von weiteren Dependencies immer vorher abklären (wird aber wohl nicht nötig sein).

#### Organisatorisches & Zusammenarbeit

- Dokumentation: in den letzten 2 Wochen. Tests sollten als Dokumentation dienen, also primär Fokus auf Tests schreiben
- Kommunikation über GitHub (taggen in Issues, PRs), Email, Slack (TODO: erstellen für Team)

Ende der Präsentation 10:53

##### Fragen

Noah erkundigt sich, ob es Testfiles von ihnen gibt?
Luca erklärt, dass wir eigene Fixtures (dummy Data) erstellen können.
Sven ergänzt, dass wir unbedingt Fragen stellen sollen, und betont Wichtigkeit des Testens.

### Planung Iteration 1 (Planning Game 1)

Start Planning Game: 10:57

Luca erklärt, er habe für uns das Planning Game grösstenteils gemacht. Er habe selbst die Wichtigkeit und das Risiko eingeschätzt.

Luca hat ein GitHub Project erstellt in Form von Kanban. Enthält alle Aufträge der 1. Iteration. Diese Tickets haben eine Wichtigkeit, wobei P0 für Iteration 1 wichtig ist.

Tickets:

- Set-Up von der lokalen Entwicklungsumgebung: Im Repository existiert ein Set-Up Guide. Docker Desktop wird empfohlen. VS-Code wird empfohlen anstatt Ruby Mine (JetBrains). Die "Hallo"-Message sollte entfernt werden.
- Resources: Einarbeiten in RoR und andere Tools. Wichtig: `irb` sollte in der devconsole gemacht werden, da sonst eine alte Version verwendet wird. RoR habe klare Wege, wie man Sachen erledigen soll, dafür ist der Guide von RoR hilfreich.

##### Fragen:

Luca fragt nach dem Zeitplan, Dauer und Anzahl der Iterationen. Sebastian erklärt, dass eine Iteration immer 3 Wochen dauert und es insgesamt 4 Iterationen gibt.

Wir einigen uns, uns am Ende jeder Iteration zu treffen, um die neue Iteration zu Planen. Dabei müssen nicht immer alle (aber mind. 2-3) der Gruppe anwesend sein. Der nächste Termin (siehe unten) wurde vereinbart.

## Nachbesprechung im Team

Folgende Aufgaben wurden für nächste Woche (bis Mittwoch, 04.03.2026) definiert:

| Was                                        | Wer                 |
| ------------------------------------------ | ------------------- |
| Slack aufsetzen & Luca einladen            | Noah                |
| 1. Präsentation vorbereiten und halten     | Sebastian und Noah  |
| Statusbericht, Risikoanalyse & Arbeitsplan | Olaf                |
| Protokoll fertigstellen                    | Jon                 |
| Entwicklungsumgebung einrichten            | Alle aus der Gruppe |
| Einlesen in RoR                            | Alle aus der Gruppe |

## Nächstes Kunden-Meeting

- **Was**: PSE Iteration 1
- **Wann**: 11.03.2026, 10:30 - 11:30 Uhr
- **Wo**: Garaio Ag
