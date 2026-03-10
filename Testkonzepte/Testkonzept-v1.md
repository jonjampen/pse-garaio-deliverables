# Testkonzept v1

- **Projekt**: Garaio REM
- **Datum**: 11.03.2026
- **Version**: v1

In unserem Projekt arbeiten wir mit Ruby on Rails (RoR). Dies ist ein Framework mit starkem Fokus auf das Model-View-Controller (MVC) Pattern und es gibt eine klare Best-Practice fürs Testing vor. In Absprache mit unserem Kunden richten wir uns danach (vgl. https://guides.rubyonrails.org/testing.html).

## Continuous Integration

Wir verwenden Continuous Integration (CI), um beim Erstellen jedes Pull-Requests automatisch alle Tests durchzuführen und eine einheitliche Formattierung (durch Linting mit RuboCop) zu garantieren.

## Unit Tests

Der Fokus in diesem Projekt liegt beim Testen der einzelnen Units. Jeder `controller`, jedes `model` und jeder `job` wird individuell getestet.

## Datenbank Tests

Testdaten (Fixtures) generieren wir selbst mittels `factory_bot`, dies haben wir im 1. Kunden-Meeting abgemacht. Diese Daten werden für die restlichen Tests verwendet, jedoch wird die Datenbank anderweitig nicht automatisiert getestet, da in RoR die Datenbank sehr nahe an die Models (die bereits über Unit Tests getestet werden) gekoppelt ist.

## Integrationstests

Die Stories werden mit dem RoR Integrations-Testtyp getestet. Wir setzen den Fokus auf folgende Use Cases:

- Verwaltung der Schnittstellen
- (weitere werden im Testkonzept v2 erweitert, sobald die Details der Applikation im 2. Kunden-Meeting besprochen wurden)

## Installationstest

Wir entwickeln und testen die RoR-Applikation in Dev-Containers. Dies ermöglicht es, die Applikation auf einem beliebigen System laufen zu lassen, ohne dass verschiedene Spezifikationen der Systeme zu Problemen führen können. Die installation wird manuell getestet.

## GUI Test

RoR unterstützt System Testing (mittels Capybara), um die Integrationen aus Sicht der User\*innen zu testen. System-Tests haben aber auch Nachteile (hoher Wartungsaufwand, lange Ausführungszeit etc.), weshalb wir automatisierte GUI Tests nur für die wichtigsten Stories erstellen. Primär also für Login, Registrierung und das Erstellen neuer Schnittstellen. Das restliche GUI wird von Hand getestet.

## Stress-Test

Da die Software planmässig nicht hohen Belastungen ausgesetzt ist, verzichten wir auf Stress-Tests.

## Usability-Test

Usability-Tests sind auf Absprache mit dem Kunden nicht nötig.
