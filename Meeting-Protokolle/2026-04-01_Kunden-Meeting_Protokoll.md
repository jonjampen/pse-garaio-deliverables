---
datum: 2026-04-01
typ: Kunden-Meeting
projekt: GARAIO App
teilnehmer: Noah, Olaf, Jon, Sebastian, Elisa, Luca, Sven
status: abgeschlossen
---

# Protokoll Kunden-Meeting vom 01.04.2026

**Wann:** 01.04.2026, 10:30 Uhr  
**Wo:** GARAIO AG  
**Leitung:** Noah Baumgartner  
**Protokollführung:** Sebastian Bürki  

**Anwesende:**
* **Team:** Noah, Olaf, Jon, Sebastian
* **HA**: Elisa
* **GARAIO:** Luca, Sven

---

## Traktanden
1. Demo Iteration 2
2. Feedback Design & Technik
3. Team-Status & Workflow
4. Planning Game (Iteration 3)

---

## Rückblick auf Iteration 2 & Demo
Olaf präsentiert den aktuellen Stand der Applikation:

* **Demo-Inhalte:** Login-Prozess, verschiedene Views (Servers/Services) sowie die Erstellungs-Funktionen.
* **Kontext:** Luca erläutert Sven den Fortschritt; das alte Tool wird im Projektverlauf nicht als Referenz herangezogen.

### Feedback zur KI-Nutzung
* **Transparenz:** Das Theme der Login-Page wurde KI-generiert. Luca und Sven merken an, dass man dies als Entwickler direkt erkennt (u. a. an Kommentaren und Effekten).
* **Vorgabe:** Ehrlichkeit ist wichtig. KI-Einsatz soll nicht verheimlicht, sondern offen kommuniziert werden.

---

## Feedback Design & Technik

### UI/UX & CSS
* **Branding:** Login- und "New"-Buttons sollen kein Standard-Tailwind-Blau nutzen, sondern eine eigene Corporate-Farbe erhalten.
* **Kontrast:** Der Gradient im Darkmode verwirrt das Auge und bietet zu wenig Kontrast.
* **Konsistenz:** Edit-Buttons müssen an konsistenten Stellen platziert werden. Die Farben Orange/Rot sollten dezenter sein.
* **Navigation:** Der "Back to services"-Button ist logisch problematisch, da Services von vielen Seiten erreichbar sind. Die Notwendigkeit des Buttons wird hinterfragt.
* **Layout:** Cards sollten mehr Platz einnehmen. Untertitel bei Servers (z. B. "5 of 5 online (100%)") sind unnötig.
* **Performance:** Die Transition-Farbe bei Tabellen wirkt zu langsam.

### Funktionalität & Code
* **Sprache:** Die gesamte Applikation wird konsistent auf **Englisch** umgestellt.
* **Suche:** Ein "Debounce" muss hinzugefügt werden, um die Last zu optimieren.
* **Tailwind:** Klassen/Designs nicht unnötig auslagern; Layouts, die nur wenig genutzt werden, direkt im Code lassen.
* **Security:** Die "Sign up"-Funktion wird entfernt, da die Registrierung nicht für alle möglich sein soll.
* **Bugs:** Typo in der `filter_bar` (Zeile 3: `turbo_fram(e)`). Empfehlung: Nutzung von **herb LSP** zur Fehlererkennung.

### Views & Models
* **Provisioning Log:** Anzeige von Datum und Status. Name statt E-Mail verwenden, um Platz zu sparen. Informationen grösser ("als Titel") darstellen.

---

## Team & Workflow
* **Personal:** Die Zusammenarbeit im Team war gut, jedoch fehlte die volle Unterstützung von Silvan aufgrund seiner Abwesenheit (Zivil-Schutz).
* **Ticket-Management:** Luca gibt das Feedback, dass Tickets ausschliesslich aus dem "Ready"-Status gezogen werden dürfen, nicht direkt aus dem Backlog.

---

## Planning Game (Iteration 3)
Fokus der nächsten Phase liegt auf Jobs und Provisioning:

* **Provisioning:**
    * Implementierung von stubbed Jobs.
    * Pro Service/Server-Konfiguration ein `ProvisionJob`.
    * Provision-Button löst Job-Erstellung aus.
* **Datenmodell:**
    * Erweiterung des Service-Models.
    * Beziehung: Ein Service kann nur einmal pro Server existieren (1:N in diesem Kontext).
    * Logs: N:M wird zu 1:N / N:1 transformiert.
* **Skalierung & Features:**
    * **Servers:** Fokus auf Performance (Test mit 10, Realität bis 400 Server).
    * Statt Pagination soll **Infinite Scrolling** genutzt werden.
    * Einführung von **Multi-Select** für Massenaktionen.
    * Logs sollen Filter mit Multi-Select erhalten.

---

## Sonstiges
* **Offene Punkte:** Status-Filterung und Sortierung werden in einer späteren Phase implementiert.
* **Nächstes Meeting (GARAIO):** 
	* 22.04.2026, 10:30 - 11:30 Uhr
	* Bei Garaio Ag
	* Thema: Iteration 3

---

# Nachbesprechung (Intern)

## Interne Aufgabenverteilung (Überarbeitung)
Jedes Teammitglied übernimmt die Korrekturen im eigenen Code:

* **Sebastian:**
    * Fix des Turbo-Frame Typos.
    * Implementierung des Debounce für die Suche.
    * Issue: `create ProvisionJob`.
* **Jon:**
    * Entfernung des Gradients und der Color-Transition bei Tabellen.
    * Layout-Anpassung: Cards vergrössern und unnötige Untertitel bei Servers entfernen.
    * Risikoanalyse erstellen.
* **Olaf:**
    * Konsistenz-Check: Services-Layout an das Server-Layout anpassen.
    * Statusbericht erstellen.
* **Noah:**
    * Erstellung Objekt-Button (mit Funktion und Layout).
    * View-Anpassung: "Add Server"-Button auf Services-Seite hinzufügen.
* **Noah & Jon:**
    * View-Anpassung: "Add Services"-Button auf Server-Seite hinzufügen.
* **Silvan**: 
	* "Sign-Up"-Button entfernen
	* KI-Effekte entfernen
	* KI-Kommentare entfernen
	* Farben anpassen (primary etc. verwenden)

## Teaminterne Besserung & Prozess
* **Pull Requests:** In PRs soll ab sofort alles aufgeführt werden, was bei der Korrektur auffällt. Dies soll als konstruktives Feedback und nicht als negative Kritik verstanden werden.

## Termine & Abgaben
* **Nächste Woche:** Aufgrund der Ferien fallen die Weekly Deliverables weg.
* **Präsentation (22.04.2026):** Wird von **Silvan und Noah** vorbereitet und durchgeführt.
* **Nächstes internes Meeting:** 13. April 2026, 14:15 Uhr im Bistro.