---
layout: page
title: Bericht 33 – Raid
permalink: /monatsberichte-it-systemelektroniker/bericht-33-raid/
---
RAID (Redundant Array of Independed Disks) ist eine Technik mit der die Datensicherheit und/oder die Geschwindigkeit beim speichern und lesen großer Datenmengen erhöht werden kann. Das Konzept wurde 1987 von D. A. Patterson, G. Gibson und R. H. Katz von der University of California vorgestellt.

RAID beschreibt die Zusammenschließung mehrerer Datenträger zu einem logischen Laufwerk. Die Datenträger (meist Festplatten) selbst arbeiten dabei nicht schneller als gewöhnlich aber mehrere davon können in einem RAID-Verbund zusammengefasst werden. RAID ist als Hardwarelösung mittels spezieller Controller möglich und im Serverbereich seit Jahren Standard. RAID lässt sich aber auch mit einfachen Festplattencontrollern über eine Software betreiben. Meistens bietet das Betriebsystem die Funktion an. Bei einem solchen Software-RAID verwaltet ein Programm den Festplattenzugriff. Das Problem dabei ist, dass hier der gesamte RAID Controller vom Programm durch den Hauptprozessor simuliert wird was erhebliche Leistung kosten kann.

Langsam zieht aber RAID auch in PC Systeme ein. Die einfachste Ausführung eines RAID-Controllers ist ein auf dem Mainboard verlöteter Chip mit zwei Anschlüssen. Die anfallende Rechenlast wird vom Prozessor bewältigt. Im Serverbereich setzt man auf Controller auf einer Steckkarte die eine eigene XOR-Einheit (Prozessor), eine Batterie und eigenen Speicher besitzen. RAID wurde erstmals nur für SCSI eingesetzt da gewöhnliche IDE Laufwerke nicht für eine solch lange Betriebsdauer ausgelegt waren und auch eine zu geringe Grundgeschwindigkeit hatten. Es gibt zwar auch IDE RAID Controller aber sie sind keine ernsthafte Konkurrenz für SCSI. Erst mit SATA erhält eine Technik die Möglichkeit die Geschwindigkeit und das Durchhaltevermögen von SCSI zu übertreffen. Durch die serielle Übertragung von SATA lässt sich eine höhere Geschwindigkeit mit längeren und dünneren Datenkabeln erreichen.

RAID wird in verschiedene Level aufgeteilt, die wichtigsten sind Level 0, 1, 5 und 6.

### Level 0

Level 0 kommt zum Einsatz wenn möglichst viel Geschwindigkeit auf Kosten der Datensicherheit gefordert ist. Hier werden auf zwei oder mehr Platten die Daten verteilt bzw. abwechselnd geschrieben und gelesen. Fällt jedoch eine der Platten aus sind alle Daten unwiederbringlich zerstört. Man nennt dieses Level auch “stripping“.

### Level 1

Bei Level 1 werden die Dateien einfach gespiegelt. Auf zwei oder mehr Platten werden die gleichen Informationen geschrieben. Solange mindestens eine Festplatte noch funktioniert sind die Daten noch erhalten. Einen Geschwindigkeitszuwachs erhält man hier nicht jedoch erhöht sich die Datensicherheit allein mit drei Platten schon massiv. Man bezeichnet dieses Level auch als “mirroring“. Level 5

### Level 5

ist das am häufigsten eingesetzte Level. Die Daten werden wie bei Level 0 auf den Platten verteilt. Es wird zusätzlich aber noch ein ECC-Code errechnet der ebenfalls mit auf den Platten verteilt wird. Daher sind für Level 5 mindestens 3 Festplatten nötig. Fällt eine Platte aus lassen sich die ursprünglichen Daten anhand der vorhandenen Daten und der ECC-Codes wieder herstellen was der Controller automatisch übernimmt. Die Leistungsfähigkeit sinkt ab diesem Moment etwas ab da die nicht vorhandenen Daten erst durch den Controller errechnet werden müssen.

### Level 6

Level 6 stellt eine Erweiterung zu Level 5 dar. Hier werden die ECC-Codes auf zwei Festplatten verteilt wodurch mindestens 4 Festplatten benötigt werden und bis zu zwei Festplatten ohne Datenverlust ausfallen können.

RAID-Level lassen sich fast beliebig kombinieren da jedes erstellte RAID sich vom Controller wie eine einzelne Festplatte verwenden lässt. Es lässt sich z. B. ein RAID Level 51 erstellen welches aus gespiegelten Level 5-Arrays besteht. Dazu werden mehrere gleich aufgebaute Level 5- Arrays erstellt (mindestens zwei) und diese dann wiederum per Level 1 gespiegelt. Ein Level 15 wäre dann wiederum mehrere Level 1-Arrays die in einem Level 5-Array zusammengefasst sind.

Ein “Zwischenlevel“ wurde 2003 von Highpoint für PC Systeme entworfen und erhöhte Lesegeschwindigkeit und Datensicherheit mit nur zwei Festplatten. Highpoint nennt dieses Level “1.5“. Dieses Level verbindet die Vorteile von Level 0 und 1. Dabei werden die Daten beim schreiben wie bei Level 1 auf den Platten gespiegelt. Gelesen werden die Daten aber abwechselnd von den Platten. Die Ausfallsicherheit entspricht der von Level 1, die Lesegeschwindigkeit der von Level 0. Die Schreibgeschwindigkeit bleibt allerdings auf normalem Niveau und es steht nur der Speicherplatz von einer Festplatte zur Verfügung.