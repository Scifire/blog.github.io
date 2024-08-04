---
layout: page
title: Bericht 4 – Programmieren in C
permalink: /monatsberichte-it-systemelektroniker/bericht-4-programmieren-in-c/
---

In der Schule lernen wir zurzeit die Programmiersprache „C“. Sie ist eine der einfachsten und dennoch gängigsten Programmiersprachen die zurzeit in gebrauch sind. Viele Systemkerne und Programme sind in C Programmiert. Auch viele andere Programmiersprachen orientieren sich an den Eigenschaften von C.

Geschichte

C wurde von Dennis Ritchie in den Jahren 1971-1973 für das neue Unix-Betriebssystem entwickelt. Auch der erste C Compiler wurde von Richtie geschrieben. Im Jahr 1978 veröffentlichten D. Ritchie und Brian W. Kernighan ein Buch in dem die Programmiersprache C um neue Schlüsselwörter erweitert wurde, ebenfalls wurden erstmals I/O Standartbibliotheken eingeführt. Bis zur Standarisierung von C diente das Werk als informelle Referenz für alle C Programmierer.

Allgemeines

Neben Programmen für Endbenutzer wird C heutzutage hauptsächlich für die Programmierung von Betriebssystemen und eingebeteten Systemen verwendet. Der Grund dafür ist einfach die Möglichkeit die Hardware direkt ansprechen zu können und dennoch nur geringe Anforderungen an die Laufzeitumgebung zu haben.

C verfügt über verschiedene Datentypen die allerdings in Datentypen für Ganzzahlen und Gleitkommazahlen aufgeteilt werden. Die verschiedenen Typen ermöglichen das speichern verschiedener Werte aus einem maximalen Wertebereich bei unterschiedlicher Speichergröße. Der Vorteil besteht darin das es einem ermöglicht wird sehr Speicher sparend zu programmieren.

Als Beispiel die drei häufigsten Variablen Typen:

int: Dies ist der Standart Typ für ganzzahlige Werte. Dies ist auch der kleinste Variablen Typ.

float: Dies ist der Standart Typ für Gleitkommazahlen. Da es hier deutlich mehr Zahlen gibt ist dieser Typ auch um einiges größer, was den Speicherbedarf angeht.

char: Dies ist der Standart Typ für Buchstaben. Weil bei diesem Typ zusätzlich zu den Ganz- und Gleitkommazahlen auch Buchstaben eingebunden werden können ist es der größte Variablen Typ.

Alle drei Typen können durch verschiedene Zusätze noch in der größe erweitert werden.

Bevor man jetzt allerdings diese Variablen verwenden kann müssen sie erst deklariert werden. Die Vergabe des Namens (Bezeichner) der Variable ist allerdings an Regeln gebunden:

- Das erste Zeichen eines Variablennamens muss ein Buchstabe oder Unterstrich sein.
- Die folgenden Zeichen dürfen nur die Buchstaben A–Z und a–z, Ziffern und der Unterstrich sein.
- Ein Bezeichner darf kein Schlüsselwort der Sprache – zum Beispiel if, void und auto – sein.

Das folgende Beispiel deklariert die Variablen variable_1 und variable_2 als Integer.

```
void beispiel1()
{
int variable_1, variable_2;
}
```