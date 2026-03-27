# Testkonzept v2

- **Projekt**: Garaio REM
- **Datum**: 01.04.2026
- **Version**: v2

In unserem Projekt arbeiten wir mit Ruby on Rails (RoR). Dies ist ein Framework mit starkem Fokus auf das Model-View-Controller (MVC) Pattern und es gibt eine klare Best-Practice fürs Testing vor. In Absprache mit unserem Kunden richten wir uns danach (vgl. https://guides.rubyonrails.org/testing.html).

## Continuous Integration

Wir verwenden Continuous Integration (CI), um beim Erstellen jedes Pull-Requests automatisch alle Tests durchzuführen und eine einheitliche Formattierung (durch Linting mit RuboCop) zu garantieren.

## Unit Tests

Der Fokus in diesem Projekt liegt beim Testen der einzelnen Units. Jeder `controller`, jedes `model` und jeder `job` wird individuell getestet.

## Testdaten

Testdaten (Fixtures) generieren wir selbst, dies haben wir im 1. Kunden-Meeting abgemacht. Diese Daten werden für die restlichen Tests verwendet, jedoch wird die Datenbank anderweitig nicht automatisiert getestet, da in RoR die Datenbank sehr nahe an die Models (die bereits über Unit Tests getestet werden) gekoppelt ist.

## Integrationstests

Die Stories werden mit dem RoR Integrations-Testtyp getestet. Wir setzen den Fokus auf folgende Use Cases:

1. Server erstellen, provisionierte Schnittstellen bearbeiten, Server löschen
2. Service erstellen, provisionierte Server bearbeiten, Service löschen
3. Authentifizierungsprozess

Es werden noch weitere Use Cases dazukommen, da uns Luca am nächsten Meeting über bestimmte Änderungen an den Models informieren wird.

## Installationstest

Wir entwickeln und testen die RoR-Applikation in Dev-Containers. Dies ermöglicht es, die Applikation auf einem beliebigen System laufen zu lassen, ohne dass verschiedene Spezifikationen der Systeme zu Problemen führen können. Die installation wird manuell getestet.

## GUI Test

RoR unterstützt System Testing (mittels Capybara), um die Integrationen aus Sicht der User\*innen zu testen. System-Tests haben aber auch Nachteile (hoher Wartungsaufwand, lange Ausführungszeit etc.), weshalb wir automatisierte GUI Tests nur für die wichtigsten Stories erstellen. Primär also für Login, Registrierung, das Verwalten von Services und Servern und das Navigieren zwischen den Index/Show-Seiten. Das restliche GUI wird von Hand getestet.

## Stress-Test

Da die Software planmässig nicht hohen Belastungen ausgesetzt ist, verzichten wir auf Stress-Tests.

## Usability-Test

Usability-Tests sind auf Absprache mit dem Kunden nicht nötig.

## Erste Ergebnisse

Aktuell überprüfen wir 180 Assertions, welche die Models und Controllers der Servers, Services und ProvisionLogEntries testen. Wir haben auch bereits Integrationtests für ausgewählte Abläufe erstellt. Dank der CI-Pipeline wissen wir mit sicherheit, dass alle Tests erfolgreich sind.

Weitere Ergebnisse werden in der entsprechenden Präsentation präsentiert.
