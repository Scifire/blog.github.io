---
layout: page
title: Bericht 25 – FileTransferProtocol (FTP)
permalink: /monatsberichte-it-systemelektroniker/bericht-25-filetransferprotocol-ftp/
---

FTP ist ein Datenübertragungsprotokoll welches 1985 unter der Norm RFC 959 veröffentlicht wurde. Es ist ein Netzwerkprotokoll welches speziell für die Übertragung von Dateien in IP basierenden Netzwerken entwickelt wurde. Im OSI-Modell ist FTP in der Schicht sieben angesiedelt. Meist werden Dateien beziehungsweise Verzeichnisse auf einem Server bereitgestellt und diese können dann von einem Client heruntergeladen werden. Der Client kann aber, sofern er die Rechte besitzt, auch Dateien hochladen oder neue Verzeichnisse erstellen.

Bei FTP werden für die Steuerung und die Dateiübertragung verschiedene Ports verwendet. Zu Beginn einer Sitzung sendet der Client über den Controll Port 21 eine Anfrage an den Server. Der Server antwortet auf den Port von dem er die Anfrage erhalten hat. Die komplette Befehls-Kommunikation findet über diesen Port 21 statt. Wenn der Client sich erfolgreich authentifiziert hat, kann nun eine Dateiübertragung standardmäßig über Port 20 stattfinden.

Für den Aufbau dieser Dateiübertragung gibt es zwei Möglichkeiten, den Activ Mode und den Passiv Mode.

Activ Mode: Im Activ Mode öffnet der Client einen zufälligen Port (größer gleich 1023) und teilt diesem den Server inklusive seiner IP Adresse mit. Serverseitig wird der Port 20 für die Übertragung geöffnet.

(Beispielbild darf selber gesucht werden)

Passive Mode: Im Passive Mode sendet der Client einen sogenannten PASV- Kommando an den Server und dieser antwortet mit einer IP und einem Port, über welchen die Dateiübertragung läuft. Auch im Passiv Mode werden nur Ports die größer als 1023 sind, geöffnet.
Der Passive Mode wird meistens dann verwendet wenn der Server keine direkte Verbindung zum Client aufbauen kann, weil dieser zum Beispiel hinter einer Firewall oder einem Router sitzt.

(Beispielbild darf selber gesucht werden)

Öffentliche FTP Server: Im Word Wide Web gibt es eine ganze Reihe von sogenannten öffentlichen FTP Servern, diese werden meistens von Universitäten oder Fachlochschulen bereitgestellt. Auf diesen Servern kann man sich mit dem Benutzernamen „Anonymous“, keinem Benutzernamen, beziehungsweise einem beliebigen Passwort anmelden.

Um FTP zu nutzen sind ein Client sowie ein Server nötig. Die meisten aktuellen Browser besitzen allerdings schon einen integrierten Client. Die Gegenseite, also der Server braucht natürlich auch die entsprechende Software.