---
layout: page
title: "Exchange Online DE"
permalink: /technik/office-365-exchange-online-de/exchange-online-de
---
*Published on: 2017-11-21*

Nachdem die eigentliche Migration von Usern und Inhalten vom Exchange on Premise nach Exchange Online DE relativ schmerzfrei von statten ging fangen danach die Probleme leider erst wirklich an.

## Spam Filter & Signatur Management

Dadurch das man vom Exchange Online nicht mehr als eine Webseite zu Gesicht bekommt werden Dinge wie Signatur Management oder Spam Filter zu einer mehr oder weniger komplexen Aufgabe. Wenn man sich zusätzlich noch in der DE Cloud befindet wird der Kreis der Möglichkeiten schon sehr klein, man möchte ja schließlich nicht überall Deutsches Datenschutzrecht genießen aber dann jede Mail über einen Filter sonst wo in der Welt leiten.

Während Exclaimer als unser Signatur Management auch einen Dienst in der DE Cloud anbietet haben wir bei der Spam Filter Lösung leider keine Angebote von unserem bisherigen Anbieter in der DE Cloud. Dafür jedoch eins von der Telekom direkt sowie das von Microsoft ( ja die Telekom vermarktet hier auch ein eigenes Angebot). Das diese teurer sind als vergleichbare Angebote muss ich ja nicht erwähnen(Ist ja schließlich DE…).
Sollte man sich für einen Spam Filter entscheiden der nicht von Microsoft direkt kommt muss jede Mail schon bevor Sie sich auf den Weg zum Empfänger macht eine kleine Reise durch Deutschland hinlegen.

Mail Absender -> Exchange Online -> Signatur Management -> Exchange Online -> Spam Filter —> Mail Empfänger

Alle Dienste müssen hier natürlich mehr oder minder aufwendig konfiguriert werden wobei Support meist eher schwach ist. Sowohl die Telekom als auch die Anbieter berufen sich meist darauf das der andere Partner Schuld ist und man bei dessen Support nachfragen soll.

Die Fehlersuche macht natürlich extrem viel Spaß da man in einer Online Version, welche alle Dienste ja darstellen, keinerlei wirkliche Logs hat sondern lediglich das was der Anbieter einem zur Verfügung stellt.
## Mysteriöse Blacklist Einträge

Während unserer Stage Migration wurden die Mails von unserem on-Prem Exchange Server angenommen und an den Exchange Online weitergeleitet. Hierfür wurde auf dem Exchange Online eine @firma.onmicrosoft.de Adresse angelegt.

Zu einem Zeitpunkt der sich leider nicht genau definieren lässt, ich tippe jedoch auf die Abschaltung unseres On-Prem Exchanges, sind einige unserer User bei einigen Mailversendern auf Blacklists gelandet. Ein Beispiel wäre hier Github.
## Connectoren

Um einen Partner an den eigenen Exchange Online anzubinden gibt es sogenannte Connectors. Diese sind dafür zuständig  das z.B. Salesforce unseren Exchange Online als mail relay nutzn kann und darf sodass unsere User aus dem Salesforce Portal Mails senden können und diese so aussehen als ob sie direkt von uns kommen.

Der Connector zu Salesforce funktioniert mittels IP Whitelisting. Die Zertifikatsprüfung funktioniert leider aktuell wohl noch nicht.
## Addons

In Exchange Online gibt es theoretisch die Möglichkeit Third Party Programme oder Dienste mittels Addon anzubinden. Das diese Addons auch im OWA genutzt werden können müssen sie auch im Exchange Online aktiviert beziehungsweise installiert werden.

Leider funktionieren aktuell(28.01.18) keine Addons im Exchange Online in der DE Cloud!
Aussage des Telekom Supports.

Einen workaround gibt es wohl nicht oder ist nicht bekannt. Man kann dieses Feature also schlicht und ergreifend nicht nutzen.
## Öffentliche Ordner /Kalender /Kontakte im OWA anzeigen

Auch wenn Microsoft klar die Freigegebenen Postfächer den alten Öffentlichen Ordnern bevorzugt (siehe unten) bieten diese leider nicht die Möglichkeit der ganzen Firma einen Kalender oder Kontakte bereitzustellen ohne das diesen jeder bearbeiten kann oder jeder die Freigabe für ein zusätzliches Postfach haben muss.
Mit Öffentlichen Ordnern bzw. Kalendern kann man allerdings genau dies abbilden.

Anfänglich konnte man sich diesen Kalender auch im OWA als Favorit markieren und unter Kalender anzeigen lassen.
Nach einigem Wochen betrieb ging das auf einmal nicht mehr. Man konnte weder den Kalender hinzufügen noch in ansehen.
Einige Tage später konnte man den Kalender immerhin wieder anzeigen aber noch nicht hinzufügen.
Nach ca. zwei weitern Wochen funktioniert auch das hinzufügen wieder.

Weder die Telekom noch Microsoft haben hier Einschränkungen gemeldet. Der Telekom Support konnte das Problem nachstellen, wollte aber kein Ticket bei Microsoft aufmachen ” da dies vermutlich sowieso irgendwo untergeht“.
Ich wurde gebeten doch bitte einen workaround zu finden zu zu nutzen.
## Öffentliche Ordner – Mail Empfang

Bis heute(21.11.2017) ist es nicht möglich einen Öffentlichen Ordner zu erstellen und für diesen Mail Empfang zu aktivieren. Sowohl intern als auch extern kommen schlicht keine Mails in dem Ordner an. Die Adresse ist allerdings vergeben und der Absender bekommt keine Fehlermeldung.

Auch hier kann der Telekom Support das Problem nachstellen. Die Aussage hierzu lautet:
“Microsoft möchte die Öffentlichen Ordner ja sowieso mehr oder weniger abschaffen, man möge doch bitte die Freigegebenen Postfächer nutzen”