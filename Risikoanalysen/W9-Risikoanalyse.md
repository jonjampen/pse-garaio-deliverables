# Risikoanalyse Woche 9
- **Datum**: 15.04.2026
## 1. Zeitprobleme aufgrund von last-Minute Änderungen vom Kunden
- **Eintrittswahrscheinlichkeit**: Hoch (Der Kunde hat in der letzten Woche seine Meinung bezüglich mehreren Issues geändert. Die Arbeit muss also noch mal gemacht werden, was wir nicht voraus gesehen haben)
- **Gewichtung**: Hoch (Man müsste diese Änderungen in die nächste Iteration verschieben, was dann mehr Arbeit hiesse oder das Projekt verzögern würde).
- **Gegenmassnahmen beim Eintreten des Ereignisses**: Die Arbeit in die nächste Iteration verschieben und dann fertig machen.
## 2. Weitere störende Migrationsprobleme in Ruby on Rails
- **Eintrittswahrscheinlichkeit**: Hoch (Wir hatten in dieser Iteration viele Probleme mit den Migrationsdateien, was den Entwicklungsprozess verlangsamt hat)
- **Gewichtung**: Klein, da wir jetzt wissen wie das Problem zu lösen ist, aber es verursacht dennoch Verzögerungen bis man das Problem gelöst hat
- **Gegenmassnahmen beim Eintreten des Ereignisses**: Das neuste Schema.rb übernehmen und per SQL Statement in der Rails-Console den Migrationsstand auf den neusten Stand setzen
