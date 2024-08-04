---
layout: page
title: Bericht 26 – Firewall
permalink: /monatsberichte-it-systemelektroniker/bericht-26-firewall/
---

Eine Firewall schützt einen Computer oder ein Netzwerk vor Unerlaubten zugriffen aus dem Internet und vor eventuellen nicht gewünschten Zugriffen auf das Internet. Sämtliche Daten die aus dem Internet kommen oder ins Internet geschickt werden, müssen durch die Firewall hindurch und werden von dieser gefiltert beziehungsweise geblockt. Vom Grundgedanken her kennt eine Firewall zwei Software-Konfigurationen:
“Es ist alles erlaubt, was nicht verboten ist” und “Es ist alles verboten, was nicht erlaubt ist”. Die erste Konfiguration ist eher benutzerfreundlich, da man noch alles machen kann und nur bestimmte Dienste oder Verbindungen verhindert, wodurch sie aber nicht sehr sicher ist.

Die zweite Konfiguration ist zwar sehr umständlich einzustellen, bietet jedoch den besten Schutz.
Im Großen und Ganzen gibt es zwei Arten von Firewalls.

Software Firewall: Unter einer Software Firewall (auch Desktop- beziehungsweise Personal-Firewall genannt) versteht man eine Software die den Netzwerkverkehr regelt. Diese Art ist wird meistens für kleine Unternehmens-Netzwerke oder private Computer verwendet. Je nach Umfang und Grundkonfiguration sind sie relativ einfach einzurichten und zu bedienen. Eine Software Firewall läuft grundsätzlich auf dem Rechner den sie überwachen soll, beziehungsweise auf dem Server über den der ganze Verkehr des Netzwerkes geht.

Hardware Firewall: Eine Hardware Firewall ist ein externes System das zwei Netze auch physisch voneinander trennt. Sie ist der Software Firewall in jedem gemeinsamen Punkt überlegen, da eine physische Trennung der beiden Netze besteht, hierdurch ist es auch deutlich schwieriger die Firewall zu manipulieren. Eine Hardware Firewall basiert allerdings nicht nur auf Hardware, viel mehr läuft sie auf einem eigenen Betriebssystem welches nur für die Firewall Funktionen zuständig ist.

Grundsätzliche Funktionsweise einer Firewall: Eine Firewall hat mehrere Möglichkeiten ihre Schutzfunktion umzusetzen. Die erste wäre ein Filter der zum Beispiel IP oder MAC Adressen filtert oder gar nur bestimmte Adressen zulässt.

Eine weitere Möglichkeit ist eine Sperre einzubinden, somit kann der User bestimmte URLs oder Domains nicht aufrufen. Das Gegenteil wäre eine sogenannte Whitelist, bei dieser Funktion kann der User lediglich die URLs und Domains aufrufen die vorher in die Liste eingetragen wurden.

Die letzte Möglichkeit wäre ein Paketfilter, dieser schaut sich jedes Packet im Einzelnen an und entscheidet dann anhand der Regeln ob das Paket durchgelassen wird oder nicht.

Kein perfekter Schutz: Wenn die Firewall den Schutz eines Netzes auch erhöht, so ist sie dennoch nicht perfekt. So kann es dennoch Schwachstellen in der Programmierung geben die dann wiederum ausgenutzt werden. Das größte Problem sind allerdings wohl User, die unvorsichtig schädliche Software direkt in das Netz schleusen.