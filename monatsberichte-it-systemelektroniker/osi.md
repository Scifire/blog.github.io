---
layout: page
title: Bericht 21 – Das OSI-Modell
permalink: /monatsberichte-it-systemelektroniker/bericht-21-das-osi-modell/
---

Das OSI-Modell (Open Systems Interconnection Reference Model) ist ein offenes Schichtenmodell für die Kommunikation Informationsverarbeitender Systeme, also Computer. Es handelt sich um vereinheitlichte Verfahren und Regeln für den Austausch von Daten.

Das OSI-Modell untergliedert Instanzen für die Netzwerkkommunikation in sieben Schichten. Jede Schicht ist so konzipiert, dass sie die zugeordnete Aufgabe unabhängig von den anderen Schichten ausführen kann. Jede Schicht erbringt für die nächsthöhere Dienstleistungen.

Im OSI-Modell nimmt der Abstraktionsgrad der Funktionen von Schicht 1 bis Schicht 7 extrem stark zu. Die Kommunikation erfolgt vertikal, d. h. die Daten werden von Schicht zu Schicht weitergeleitet. Auf der Senderseite läuft die Kommunikation von oben nach unten, auf der Empfängerseite von unten nach oben. Physisch gesehen werden die Daten auf der Untersten Schicht übertragen, logisch gesehen erfolgt die Kommunikation zwischen Sender und Empfänger horizontal auf jeder Schicht.

| # | Bezeichnung | englische Bezeichnung |
| ----- | ----- | ---- |
| 7 | Anwendungsschicht | Application-Layer |
|6 | Darstellungsschicht | Presentation-Layer |
|5 | Sitzungsschicht | Session-Layer |
|4 | Transportschicht |	Transport-Layer |
|3 | Vermittlungsschicht | Network-Layer |
|2 | Sicherungsschicht | Data Link-Layer |
|1 | Bitübertragungsschicht | Physical-Layer |

Die einzelnen Schichten

Die Schicht 7 stellt den Anwendungen eine Vielzahl von Funktionen zur Verfügung. Z. B. eMail, Datenübertragung, etc.

Schicht 6 setzt die Systemabhängige Darstellung bzw. Kodierung der Daten in eine unabhängige Form und ermöglicht somit syntaktisch korrekten Datenaustausch zwischen verschiedenen Systemen. Datenkompression und Verschlüsselung gehören zu Schicht 6.

Die Schicht 5 stellt Dienste für einen organisierten und synchronisierten Datenaustausch zur Verfügung. Damit werden Zusammenbrüche einer Sitzung und ähnliche Probleme behoben. Es werden Fixpunkte eingeführt an denen die Sitzung nach einem Transportausfall wieder synchronisiert werden kann ohne, dass die Übertragung wieder von vorne beginnen muss.

Schicht 4 stellt unter anderem Segmentierung von Datenpaketen und Stauvermeidung zur Verfügung. Sie bietet den Schichten 5 bis 7 einen einheitlichen Zugriff, so das diese die Eigenschaften des Kommunikationsnetzes nicht berücksichtigen müssen. Multiplex-Mechanismen und Fehlersicherungs- sowie Behebungsverfahren gehören zu dieser Schicht.

Die Schicht 3 sorgt bei leitungsorientierten Diensten für das Schalten von Verbindungen und bei Paketorientierten Diensten für die Vermittlung von Paketen. Auf dieser Schicht findet also Routing statt.

Aufgabe der Schicht 2 ist es eine sichere, d. h. weitgehend fehlerfreie Übertragung zu gewährleisten und den Zugriff auf das Übertragungsmedium zu regeln.

Schicht 1 stellt mechanische, elektrische und funktionelle Hilfsmittel zur Verfügung um eine physikalische Verbindung zu ermöglichen. Das sind z. B. elektrische Signale, Lichtimpulse, etc. . Die Datenleitungen selbst gehören auch dazu.