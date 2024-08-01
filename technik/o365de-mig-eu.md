---
layout: page
title: "Migration Office 365 DE nach EU"
permalink: /technik/office-365-exchange-online-de/migration-office-365-de-nach-eu
---
*Published on: 2017-11-21*

Auch die Migration in die EU Cloud haben wir nun auch hinter uns. Die Planungen für die Migration vom Deutschen Office 365 Tenant in einen Europäischen bzw. Allgemein Tenant haben ca. einen Monat gedauert, waren aber weit nicht so anspruchsvoll wie die erste Migration. Dies hat zum einen den Grund das wir das Produkt an sich ja kannten und zum anderen gibt es nur einen einzigen Migrationsweg: Dritthersteller Software.
Von Microsoft selbst ist keine Migration zwischen Regionen vorgesehen. Dem entsprechend gibt es weder offizielle Technet Artikel oder anderweitige Hilfe seitens Microsoft.
## Vorbereitung

Seitens der Telekom wurden wir in den Vorbereitungen durch einen gut Vernetzten Consultant(Strato) beraten. Dies kam vermutlich vor allem daher das wir in der DE Cloud doch sehr große Probleme hatten und diese auch immer an den Telekom Support als auch an unseren Sales Ansprechpartner eskaliert haben.

Die Migration muss an sich in einem Schritt absolviert werden. Eine Stage Migration wie von On-Premise zu Online ist nicht möglich. Auch müssen alle Daten händisch oder mittels einer (Lizenzpflichtigen)Dritthersteller Lösung transferiert werden. Skype sowie OneDrive Daten können nicht migriert werden und müssen somit händisch vom User gesichert und wieder hergestellt werden. Sharepoint kann sehr aufwendig migriert werden.
## Die Migration

Unsere Migration lief folgendermaßen ab: Am Donnerstag vor der Migration wurden vom Telekom Support alle User&Freigegebenen Postfächer die im DE Tenant vorhanden waren parallel im EU Tenant angelegt.
Am Freitag wurde die Migration der Daten angestoßen sodass diese über das Wochenende laufen konnte.
Am Montag haben wir mit dann die Domain aus dem alten DE Tenant losgelöst und im neuen eingetragen. Hier kommt es zu einer unschönen Downtime im E-Mail verkehr. Um eine Domain aus einem Tenant zu lösen ist es nötig alle Verknüpfungen zu der Domain zu lösen. Das heißt von allen Postfächern muss die reguläre E-Mailadresse entfernt werden. Dies resultiert darin das eine Emails die reguläre Adresse geschickt werden gebounced werden (User not found). Daher ist es empfehlenswert vorher den MX Eintrag der Domain komplett zu löschen. Das hat zwar ebenfalls einen bounce( Server not found) zur folge, jedoch verwirrt dieser bounce den sender nicht so sehr wie “user not found“.
Sobald die Domain im alten Tenant gelöscht wurde, kann sie im neuen Tenant registriert werden und die regulären Mail Adressen können den Usern wieder zugeordnet werden. Sobald dies geschehen ist, sollte der MX Eintrag wieder gesetzt werden damit Mails wieder zugestellt werden konnen (von nun n im neuen Tenant).
Diese Downtime sollte mit min. ein bis zwei Stunden kalkuliert werden, auch ist es ratsam die TTL der DNS Einträge vorher herunter zu setzten damit diese schneller aktualisiert werden.
Die Umstellung der Tenant Domain ging soweit problemlos über die Bühne, somit konnten die User nach ca. zwei Stunden wieder Emails Empfangen und diese auch über das Web Portal abrufen.

Für uns lokal ging nun theoretisch die Arbeit erst richtig los. Jede Office Installation musste mittels eines VBscripts von Microsoft erst von der DE Cloud entlizenziert und das Outlook Profil gelöscht werden. Danach konnte sich der User erneut Anmelden und somit das Office Produkt wieder Lizenzieren sowie ein Outlook Profil erstellen.
Ich sage theoretisch, weil die Microsoft Lizenzierungsserver praktisch zwischen 48 und 72 Stunden gebraucht haben bis diesen bekannt war das unsere Domain sich nun in der EU Cloud befindet.
Diese Tatsache wurde uns auch durch den Telekom Techniker bestätigt, der uns bei der Migration begleitet hat. Leider war diese Problematik vorher niemandem bewusst. Somit haben wir wieder einmal einen ganzen Arbeitstage damit verbracht mögliche Problemlösungen zu testen, bis wir die Bestätigung hatten das wir an dieses Problem weder beheben noch beschleunigen können. Nach ca. 48 Stunden konnten wir dann an einigen Computern Office lizenzieren. Leider war aber auch dies ein Glücksspiel da allem Anschein nach nicht alle Lizenzierungsserver von Microsoft auf dem gleichen Stand waren (manchmal konnte man Office einfach nicht Lizenzieren am nächsten Tag dann schon).
Seitens Microsoft wurde dieses Problem leider überhaupt nicht kommuniziert obwohl unser Betreuer bei der Telekom ein sog. Premium Ticket eröffnet hat.

Nachdem auch dieses letzte Problem behoben war gab es nur noch ein paar kleinere Änderungen sowie manuelle Ergänzungen zu tun. So mussten zum Beispiel sämtliche Aliase sowie Zugriffsrechte der freigegebenen Postfächer manuell nachgepflegt werden. Im großen und ganze war unsere Migration allerdings abgeschlossen.
## Kosten

Nicht vergessen sollten werden dürfen die Kosten für die Migration die in unserem Fall für ca. 120 Postfächer im mittleren vierstelligen Bereich lagen. Die Kosten teilen auf hauptsächlich zwei posten auf: die Dritthersteller Software die pro Element (Postfächer etc.) Lizenziert werden muss und die Arbeitszeit des Telekom Technikers der die Software einsetzt sowie weitere Dinge vorbereitet oder durchführt. Des Weiteren bleibt zu klären ob man für die Zeit der Migration beide Tenants, die ja beide voll Lizenziert sein müssen, die vollen Kosten tragen muss oder ob diese erlassen werden.
## Resümee

Abschließend können wir sagen das die Migration vom DE Tenant in den EU Tenant zwar nicht fehlerfrei geklappt hat, jedoch schon deutlich besser als alles was uns im DE Tenant Wiederfahren ist.
Wir sind froh diesen Schritt der erneuten Migration gegangen zu sein und haben auch schon kurzfristig positives Feedback unserer User bekommen.
Der Fairness halber muss ich aber auch sagen das wir nicht die oben aufgeführten Kosten tragen mussten. Die Gründe hierfür sind mangelnde sowie Flasche Beratung durch unseren Partner und die vielen Probleme die wir hatten. Dies ist allerdings natürlich eine Einzelfall Entscheidung und muss entsprechend verhandelt werden.