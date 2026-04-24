# Protokoll Kunden-Meeting vom 22.04.2026

- **Wann**: 22.04.2026, 10:30 - 11:15 Uhr
- **Wo**: Garaio REM Ag
- **Protokollführung**: Jon Jampen
- **Anwesende**:
  - Team: Noah, Sebastian, Silvan, Olaf, Jon
  - HA: Elisa
  - Garaio: Luca, Sven

## Besprochene Themen

### Probleme?

Luca erkundigt sich nach Problemen und Noah erwähnt das Inline-Editing. Jon erklärt, dass es nach mehreren Versuchen und mithilfe des Videos von Luca gelöst werden konnte.

### Demo

Jon demonstriert die Änderungen.

### Feedback

Lucas Feedback sei nur positiv. Er ist zufrieden und hatte auch Freude, mit Noah zusammen die Änderungen durchzugehen, und findet, dass wir die Anpassungen gut und wie gewünscht vorgenommen haben.

Er hat noch einige UI-Änderungswünsche und hat diese im Issue "UI Fixes" notiert.

Folgende Tasks für die letzte Iteration (I4) wurden besprochen:

- run stubbed job (1): Provision Button, dann Weiterleiten zu Provision-Log-Entry; Provisionlog Entry mit Broadcast Refreshes updaten, Farben für Status
- table (2): Spaltensortierung alphabetisch, Service-Cards und -Tabelle zusammen zu einer Tabelle
- ui fixes (3)
- mission control jobs (4): Jobs sehen zum Debuggen; Rails Guides active-jobs mit Solid
- translations (5): I18n Gem vorinstalliert, Rails Guides, Timezone "Bern"
- endpoints, deployments: Fehlen noch. Da wir nicht im richtigen Netz sind, führt dies zu Schwierigkeiten. Deshalb wird Luca versuchen, einen Test-Server aufzusetzen zum Deployen und Endpunkte finden fürs Testen. Wir werden dazu noch informiert.
- Icon designen `icon.png` und `icon.svg` als ein "P"
- ascii Art-Banner erstellen

Wir müssen keine Import-Scripts erstellen, das macht Luca.

### Fragen:

Jon fragt: Wie sieht es mit der Dokumentation aus?

- RoR basiert auf CoC (convention over configuration), der Code spricht für sich. Doku können wir so machen, wie wir wollen (auch mit KI). Als Idee, falls wir Interesse haben, können wir mit Jekyll auf GitHub-Pages eine Dokumentation erstellen.

## Nachbesprechung im Team

Folgende Aufgaben wurden für nächste Woche (bis Montag, 27.04.2026) definiert:

| Was                       | Wer       |
| ------------------------- | --------- |
| Planung fürs Testen       | Jon       |
| Actually run Jobs         | Olaf      |
| Table improvements        | Sebastian |
| UI improvements           | Noah      |
| Configure mission-control | Noah      |
| Translations              | Silvan    |

## Nächstes Kunden-Meeting

- **Was**: PSE Abschluss & Kundenschulung
- **Wann**: 13.05.2026, 10:30 - 11:30 Uhr
- **Wo**: Garaio Ag
