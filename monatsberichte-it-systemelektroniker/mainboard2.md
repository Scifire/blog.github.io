---
layout: page
title: Bericht 7 – Mainboard Teil 2
permalink: /monatsberichte-it-systemelektroniker/bericht-7-mainboard-teil-2/
---

Der Chipsatz

Der Chipsatz eines Mainboards besteht im Wesentlichen aus zwei Chips, der Northbridge und der Southbridge. Der Namen der Bridges bezieht sich auf die Position der Chips vom CPU aus gesehen. Die Northbridge verbindet die CPU, die Grafikkarte und den Arbeitsspeicher, die Southbridge verbindet die eher unwichtigeren Sachen wie zum Beispiel PCI-Slots, Soundkarte Flashdatenträger und Ethernet-Anschlüsse. Aufgrund der hohen Datentransfers werden die Bridges meist passiv bzw. selten wird die Northbridge auch aktiv gekühlt.

Der Frontsidebus ist die Verbindung von dem Prozessor und der Northbridge. Die Taktung beläuft sich zwischen 33 und 266MHz und ist somit für die Geschwindigkeit des Mainboards verantwortlich. Je nach Technologiestand können bis zu vier Datenpakete pro Takt versendet werden. Frontsidebus-Taktraten von bis zu 800MHz, wie sie häufig in Werbeangeboten stehen, errechnen sich durch die 200MHz-Taktrate und vier Pakete pro Takt. Von einer Übertaktung des Frontsidebuses ist generell abzuraten, außer wenn man sich sehr gut in dem Bereich auskennt. Zusätzliche muss man die Chips entsprechend der neuen Wärmeentwicklung kühlen. Eine Untertaktung bringt in der Regel nur eine geringfügig erhöhte Lebensdauer der Bauteile, dafür aber auch weniger Leistung.

Eine Datenleitung verbindet die Southbridge direkt mit der Northbridge. Diese ist direkt in das Mainboard eingelötet.

Die Southbridge steuert sämtliche Peripherie-Geräte, Festplatten Anschlüsse, Netzwerkkarten und andere Geräte, die über die PCI-Slots laufen. Um eine möglichst schnelle Verbindung zu den Geräten zu haben, liegen sie alle in der Nähe der Southbridge. Da die genannten Geräte ein relativ geringes Datenaufkommen haben, ist eine aktive Kühlung meist nicht notwenig.

Für Laptops oder ähnliche Geräte gibt es inzwischen auch schon die Möglichkeit beide Chips in einem Bauteil unterzubringen.

Hier ein typisches Bussystem eines Mainboards.

Man kann auf dem Bild sehr gut erkennen das die Southbridge alle Peripheriegeräte miteinander verbindet. Die Northbridge dagegen verbindet die CPU mit dem RAM und der Grafikkarte. Beide bridges sind dann noch mit einem High-Speed-Bus verbunden um auch untereinander kommunizieren zu können.