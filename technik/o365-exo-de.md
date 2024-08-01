---
layout: page
title: "Office 365 / Exchange Online DE"
permalink: /technik/office-365-exchange-online-de
---
*Published on: 2017-11-21*

Aufgrund mangelnder Erfahrungsberichte zu Office 365 sowie zum Exchange Online in Deutschland habe ich mich entschlossen unsere Probleme die wir sowohl bei der Migration als auch beim Betrieb der Cloud Lösung von Microsoft und Telekom hier zu Dokumentieren. Ich werde versuchen möglichst objektiv zu bleiben und auch Dinge die nachträglich verbessert wurden entsprechend zu aktualisieren.

## Migration Exchange 2007 On-Prem nach Exchange Online DE
### Stand pre-migration:

- Ein Exchange 2007 auf aktuellem Patch Level lokal bei uns in der Firma gehostet
- Als Spam und Antiviren Lösung wird eine Barracuda Appliance eingesetzt die vor den Exchange geschaltet ist
- Signatur Management wird mittels Third Party Software Exclaimer auf dem Exchange einheitlich und ohne User Aktion angehängt
- Der Exchange ist nicht direkt aus dem Internet erreichbar, nur über die Spam Firewall, ein SSL Gateway oder VPN
- Salesforce nutzt die Spam Firewalls als relay um Mails im Namen der Firma zu versenden
- Es handelt sich um ca. 120 Postfächer

Mit diesen Setup sind wir in die Migration gestartet, fairerweise muss man sagen das wir im selben Zug auch noch unsere Domäne umgestellt haben, dies ist aber bei sämtliche Problemen die aufgetreten sind eher nebensächlich.

### Angebot Telekom

Durch den Microsoft Partner Deutsche Telekom wurde uns ein Angebot hierfür unterbreitet welches im groben drei Pakete enthält unterbreitet. Da diese ja mit Deutscher Cloud und Deutschen Datenschutz beworben werden sind diese natürlich merkbar teurer.
Was leider im vorhinein nicht erwähnt wird ist dass das Deutsche Produkt von Microsoft bei weitem nicht über dem Funktionsumfang vom Internationalen Produkt verfügt.

Zusätzlich hat die Telekom uns noch ein “Umzugspaket” angeboten bei welchem ein sogenannter Experte einen beispielhaft bei der Migration hilft. Aufgrund der Einfachheit Migration an sich sowie der Erfahrungen mit dem Support haben wir uns dagegen entschieden.

### Migration Exchange nach DE Cloud

Nach einer mehrmonatigen Test und Planungspanne in der ich so gut wie nichts anderes gemacht habe als mich mit dem Thema zu beschäftigen haben wir die Migration dann gestartet.
im nachhinein kann ich sagen das diese Phase eigentlich zu kurz war da ich oder wir nicht alle Probleme ausfindig machen konnten die Office 365 bietet.

Die Migration der Mails sowie der Öffentlichen Ordner und was sonst so alles auf dem Exchange liegt ging relativ reibungslos. Wir sind nach der Stage Migration Anleitung von Microsoft vorgegangen.

Was leider nicht so gut funktioniert ist nun die Nutzung aller Dinge um Exchange die über die reine E-Mail Kommunikation hinausgehen.
Dies macht jedoch in meinen Augen genau einen Exchange Server aus.

## Entscheidung nach zwei Monaten DE Cloud

Wir haben uns nun nach Absprache mit allen beteiligten dazu entschlossen in die EU Cloud zu migrieren. Sowohl die Support Techniker als auch der Consultant der Telekom hat dazu geraten: “Ist man nicht auf durch Verträge verpflichtet in DE zu hosten sollte man aktuell in jedem fall die EU Cloud nutzen“.
Aussage der Telekom Techniker.

Erfahrungen mit der DE Cloud sowie die Migration in die EU Cloud sind hier verlinkt:

[Telekom](telekom.md)   
[Exchange Online DE](exo-de.md)     
[Office 365/Exchange Online DE](office365-exo-de.md)     
[Office 365 DE](o365de.md)    
[Migration Office 365 DE nach EU](o365de-mig-eu.md)     