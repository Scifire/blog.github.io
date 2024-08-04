---
layout: page
title: Bericht 23 – Netzwerkgeräte
permalink: /monatsberichte-it-systemelektroniker/bericht-23-netzwerkgerate/
---

In diesem Bericht möchte ich kurz die verschiedenen Netzwerkgeräte erläutern, mit denen ich bisher zu tun hatte.
## Repeater

Ein Repeater verstärkt ein Signal um es über größere Entfernungen übertragen zu können. Repeater sind Geräte der Schicht 1 des OSI-Modells. (Bsp. W-Lan Repeater)

## Hub

Hubs sind sehr einfache Geräte, die ein eingehendes Signal an alle Ports senden. Man unterscheidet aktive und passive Hubs. Aktive Hubs werden auch Multiport-Repeater genannt, sie verstärken das Signal zusätzlich. Passive Hubs verteilen es nur.

Da ein Hub ein Signal an alle Geräte sendet, entstehen sehr schnell Datenkollisionen, die das Netzwerk schon bei einer geringen Anzahl an Geräten zum Erliegen bringen können.

In Netzwerken werden aktive Hubs nur noch bei sehr wenigen Geräten eingesetzt (bis ca. 5). Passive Hubs werden in Netzwerken gar nicht eingesetzt. Man findet passive Hubs aber z. B. als USB Verteiler.

## Bridge

Eine Bridge verbindet zwei Netze, die auch unterschiedliche Zugriffsverfahren einsetzen. (Bsp. W-Lan Bridge, wird oft bei Entertain Kunden eingesetzt um den Media Receiver kabellos an das Internet (bzw. den Router) anzubinden)

## Medienkonverter

Ein Medienkonverter verbindet physikalisch unterschiedliche Medien untereinander. (Bsp. Kupfer und Glasfaser)

## Switch

Ein Switch verteilt den Netzwerkverkehr. Allerdings sendet er ein Paket nur an den Port, an dem der Empfänger angeschlossen ist. Somit werden Kollisionen weitgehend vermieden. Ein einfacher Switch arbeitet auf Schicht 2 des OSI-Modells und entscheidet anhand von MAC-Adressen, wohin ein Paket geschickt wird. Für erhöhte Anforderungen gibt es “Managed“ Switches, die auch auf Schicht 3 des OSI-Modells arbeiten. Hierauf läuft eine Art eigenes Betriebssystem und der Switch lässt sich per Webinterface bzw. spezieller Software konfigurieren. Man kann mit diesen Switches weit mehr realisieren als mit einfachen Layer 2 Switches. Dazu gehören zum Beispiel VLANs (virtuelle LANs), IP-Filterung, Routing und was heutzutage immer wichtiger wird Priorisierung für Quality of Service(QoS).QoS ist ein wichtiger Bestandteil dafür das IP Telefonie flüssig funktioniert. Auch die Bündelung mehrerer Ports ist möglich um höhere Übertragungsraten zu erreichen.

## Router

Ein Router arbeitet auf Schicht 3 des OSI-Modells. Er hat für jedes Netzwerk, mit dem er verbunden ist, mindestens eine Schnittstelle. Ein Router muss beim Eintreffen eines Datenpakets entscheiden, wohin es geschickt wird. Dazu hat jeder Router eine Routingtabelle, die angibt, an welcher Schnittstelle welches Netzwerk angeschlossen ist. Router gibt es sowohl in Hardware als fertige Geräte als auch als Programme, meistens Teil eines Betriebssystems. Ein großer Nachteil beim Software Routing ist allerdings das der Stromverbrauch in keinem Verhältnis zur erbrachten Leistung steht.

Die DSL-Router, die bei uns im Privatkunden Bereich eingesetzt werden, sind allerdings meist keine richtigen Router da sie lediglich für den Zugang in das Internet dienen und nur mit aktiviertem PPPoE und NAT funktionieren.