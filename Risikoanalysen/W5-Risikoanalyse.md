# Risikoanalyse Woche 4

- **Datum**: 17.03.2026

## 1. Verzögerungen durch gegenseitige Abhängigkeiten von Funktionen

- **Eintrittswahrscheinlichkeit**: Gross (da klare Abhängigkeiten bestehen, z. B. müssen zuerst die Views programmiert werden, bevor die Filter mittels Turbo eingebunden werden können).
- **Gewichtung**: Mittel, zwar blockiert die Wartezeit den Fortschritt der Implementationen, diese Zeit kann jedoch produktiv überbrückt werden (z.B. durch Tests schreiben für die Models)
- **Gegenmassnahmen beim Eintreten des Ereignisses**: Transparente Kommunikation in der Gruppe. Werden Rückstande sichtbar, unterstützen sich die Teammitglieder gegenseitig bei der Implementierung (z.B. durch pair Programming).

## 2. Hoher Zeitaufwand durch UI-Perfektionismus

- **Eintrittswahrscheinlichkeit**: Mittel (Detailanpassungen verleiten oft dazu die Zeit zu verlieren, obwohl das UI auch in späteren Iterationen verbessert werden kann)
- **Gewichtung**: Mittel. Ein übermässiger Fokus auf das Design blockiert die weiterführung der Funktionen, wodurch Zeit und Ressourcen für Kernfunktionen fehlen oder sich diese verzögern können. Das Projekt scheitert daran nicht komplett, aber wird ineffizient.
- **Gegenmassnahmen beim Eintreten des Ereignisses**: Frühzeitig und regelmässig Feedback von Luca einfordern. So kann schnel gemeinsam entschieden werden, ob der aktuelle Stand ausreichend ist.