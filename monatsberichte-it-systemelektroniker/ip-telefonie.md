---
layout: page
title: Bericht 10 – IP-Telefonie
permalink: /monatsberichte-it-systemelektroniker/bericht-10-ip-telefonie/
---

## Geschichte/Entwicklung

Seit Beginn des Ausbaus des Internets, anfangs noch auf den Leitungen der Telefonnetzwerke, stieg die Übertragungsleistung stetig an. Erst dies macht die IP-Telefonie möglich.

1989 wird erstmals die digitale Sprachübertragung in einer guten Qualität durch die Einführung von ISDN möglich.

1992 wird das GSM-Mobilfunk-Netz in Deutschland eingeführt.

1995 entwickeln israelische Programmierer ein Windows-Programm, welches die Internet-Telefonie im Halbduplexbetrieb ermöglicht. Allerdings muss zum Sprechen auf beiden Rechnern die Software installiert sein. Auch die Sprachqualität ist sehr schlecht und die Verbindungspartner können immer nur einzeln sprechen.

1996 QuickTime Conferencing erlaubt die Ton- und Bildübertragung im Vollduplexbetrieb über das IP-Netz und über AppleTalk.

2004 die Software Skype erscheint. Sie verwendet die Peer-to-Peer Technik mit einem nicht offen gelegten Protokoll.

## Funktionsweise

Das Telefonieren über VoIP stellt sich für den Endnutzer genauso dar wie das Telefonieren über die herkömmliche Telefonie. Der Nutzer baut seine Verbindung auf (wählt eine Nummer), spricht mit dem Angerufenen (Gesprächsübertragung) und beendet seine Verbindung (legt auf).

Der Unterschied zur klassischen Telefonie liegt darin, dass VoIP keine dedizierteVerbindung direkt zum Gesprächspartner aufbaut, sondern die Sprache digitalisiert und in kleinen Daten-Paketen zum Empfänger geschickt.

Um mit einem Gesprächpartner in einem IP-basisierten Netz eine Verbindung herzustellen, muss die IP dieses Partners im Netz bekannt sein, jedoch muss der Anrufende die IP nicht kennen.

Die Erreichbarkeit des Angerufenen wird ähnlich wie in Mobilfunkenetzen durch seine momentane Adresse ermittelt, die er in einer vorhergegangenen Authentifizierung im Netz bekannt gegeben hat. Die Adresse wird dann auf dem Server des jeweiligen Providers in Verbindung mit der VoIP Nummer gespeichert. Der Anrufende fragt mit Hilfe der VoIP-Nummer dann die IP seines Gesprächspartners ab, um anschließend eine Verbindung mit ihm aufbauen zu können.

In der Regel schickt jedes Endgerät die Sprachdaten „direkt“, also nicht über die Server eines VoIP-Providers, über das Netzwerk (oder das Internet) an die angerufene Gegenstelle.

Ein Feature dieses Systems ist, dass der Anschluss nicht vom Aufenthaltsort des Nutzers abhängig ist. Man kann sich also von jedem Telefon oder PC in dem IP-Netz anmelden und ist dort unter seiner normalen VoIP Nummer erreichbar.

 

Die Übertragung der Daten erfolgt meistens über das Real-Time Transport Protocol (RTP), welches wiederum das UDP (User Datagram Protocol) nutzt. UDP hat im Gegensatz zu TCP (Transmission Control Protocol) den Vorteil, dass es eine weitaus geringere Latenzzeit hat. Dies kommt daher, dass das TCP jedes Paket bestätigt und evt. fehlerhafte Daten neu schickt. Das UDP hat dadurch zwar keine Übertragungsgarantie, dies ist aber auch gar nicht nötig, da das menschliche Gehör diese minimalen Ausfälle gar nicht wahrnehmen kann.