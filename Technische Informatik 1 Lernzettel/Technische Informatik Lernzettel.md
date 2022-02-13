# 1 Zahlendarstellung

Es gibt eine Basis b und einen Faktor a

## $z = \sum^n_i{=1}a_ib^i$

## Konvertierung zwischen Zahlensystemen
Vorkommaanteil durch Basis b dividierren,
Ende sobald 0 vor dem Rest rauskommt
![[Pasted image 20220209133014.png]]


Nachkommaanteil mit Basis b multiplizieren
Ende sobald 0 nach dem Komma rauskommt
![[Pasted image 20220209133129.png]]


## Negative Zahlendarstellung
- Vorzeichenbit (erstes Bit speichert Vorzeichen)
- Einerkomplement (negative Zahlen sind invertiert)

Probleme bei der **Addition**:
	- Der negative Zahlenbereich geht nur **fast** in den positiven über
	- Durch die Doppeldarstellung der 0 ist das Ergebnis um 1 zu klein

- Zweierkomplement (Idee der Zahlenstrahl wird begradigt)
## BCD (Binary Coded Decimals)
- Dezimalzahlen werden Ziffer für Ziffer codiert
- Jede Ziffer wird **durch 4 Bits dargestellt** 
- nur 10 Bitkombinationen von den 16 werden benötigt

## Festkommazahlen
- Darstellbarer Zahlenbereich ]-1;1\[
- Konstanter Abstand zwischen benachbarten Zahlen
- Zahlenbereich ist bezüglich der Multiplikation abgeschlossen

## Gleitkommazahlen
![[Pasted image 20220209133851.png]]
![[Pasted image 20220209133911.png]]	
![[Pasted image 20220209133925.png]]

## Normalisierung
Da die Gleitkommadarstellung nicht eindeutig ist, legen wir fest:
 ![[Pasted image 20220209134013.png]]
 ![[Pasted image 20220209134021.png]]
 Daraus folgt
 ![[Pasted image 20220209134049.png]]
 
## IEEE754 Floating Point Standard
 ![[Pasted image 20220209134125.png]]
 ![[Pasted image 20220209134139.png]]
### Beispiel
21,875
1. Zahl in Binärzahl umwandeln
	1. Vorkommaanteil durch 2 dividieren
	2. Nachkommaanteil mit 2 multiplizieren
 2. Vorkommanormalisieren
	 1. Exponent dabei in Form C - 127 bringen
 VZ hinschreiben
C in binär hinschreiben
M in hinschreiben
3. Fertiges Bitmuster hinschreiben
 ___
# 2 Boolesche / Schaltalgebra

## Boolesche Funktionen
![[Pasted image 20220209134641.png]]

## Grundlegende Gesetze
![[Pasted image 20220209134452.png]]

## Weitere Rechengesetze
![[Pasted image 20220209134802.png]]

$a \implies b \Leftrightarrow \bar a \lor b$
___
# 3 Schaltnetze
Paritätsfunktion
![[Pasted image 20220209143536.png]]

==**Stufigkeit**==: 2

- Es gibt Wahrheitstabelle
- Jede Schaltfunktion lässt sich in Hardware 1:1 umsetzen
___
# 4 Minimierung
- Normalformdarstellungen sind sehr aufwendig
	- Basieren auf ==Mintermen== und ==Maxtermen== 
	- Jeder Min- bzw Maxterm enthält alle Eingangsvariablen
	- Formellänge steigt ==exponentiell== mit der Anzahl der Einfangsvariablen
	
## Kostenfunktion
- "Güte" einer Schaltung ist relativ und hängt vom Ziel ab
### Typische Optimierungsziele
- Hohe Taktrate
- Geringer Platzverbrauch
--> Ziele sind komplementär, d.h. die schnellste Schaltung benötigt viel Platz und
die kleinste Schaltung beitet nur geringte Taktrate

###  1. Modellierung mit Kostenfunktion
![[Pasted image 20220209144453.png]]

### Beispiel
![[Pasted image 20220209144512.png]]

### 2. Verbesserte Kostenfunktion
![[Pasted image 20220209144625.png]]
![[Pasted image 20220209144638.png]]
![[Pasted image 20220209144646.png]]
### Beispiel 
![[Pasted image 20220209144707.png]]

## Minimierung
KNF und DNF erzeugen einen Term für jede 1-Zeile der Wahrheitstabelle.
Optimierung: Zusammenfassung mehrerer Zeilen in einen Term
![[Pasted image 20220209144836.png]]

Identisch belegte Variablen heißen ==gebunden== (dcb)
Unterschiedlich belegte Variablen heißen ==frei== (a)

### KV-Diagramme jeder Größe
![[Pasted image 20220209145118.png]]
### Vorgehen
Maximal große Blöcke (==Primblock==) umkreisen
![[Pasted image 20220209145323.png]]
- Für DNF 1-Blöcke bilden
Für KNF 0-Blöcke bildend
- Ziel: Überdeckung mit der geringsten Anzahl an Primblöcken
- Bei DNF Implikanten, für die der Block innerhalb liegt, aufsammeln
Bei KNF Implikanten, für die der Block außerhalb liegt, aufsammeln
___
# 5 Standardschaltnetze
haben nur kombinatorische Logik und kein Gedächtnis
## Multiplexer
![[Pasted image 20220209145735.png]]
### Anwendung
z.B. um zu Steuern, ob das Ergebnis von einem Addierer oder von einem Multiplizierer weitergeleitet wird.
## Demultiplexer
![[Pasted image 20220209145937.png]]
### Anwendung
![[Pasted image 20220209150120.png]]
## Programmierbarge Logikbauseine ==PALs,PLAs==
### Beispiel
![[Pasted image 20220209150410.png]]
## Addierer
### Halbaddierer
- Addiert zwei Binärziffern
- Ergebnis ist der Summenwert und ein Übertrag
- Es werden ==2== Eingänge und ==2== Ausgänge benötigt
![[Pasted image 20220209150609.png]] ![[Pasted image 20220209150615.png]]
### Volladdierer
- Addiert zwei Binärziffern unter Berücksichtigung eines Übertrags
- Ziel: Addition mehrstelliger Binärzahlen
![[Pasted image 20220209151447.png]]
![[Pasted image 20220209151457.png]] ![[Pasted image 20220209151502.png]]
### Carry-Ripple-Addierer
Idee: Sequentielle Aneinanderschaltung von Volladdierern
![[Pasted image 20220209151543.png]]
### Parallele Berechnung der Übertrags-Bits
Zweistufiges Schaltnetz
![[Pasted image 20220209151639.png]]
## ALU
![[Pasted image 20220209151749.png]]
___
# 6 Schaltwerke
## Kurze Zusammenfassung
Arten von Speicherelementen
![[Pasted image 20220209154333.png]]
Arten von Schaltsymbolen
![[Pasted image 20220209154324.png]]
## D-Flipflop
![[Pasted image 20220209152050.png]]
## Takt
Interne Zustände:
- Schaltelemente sind zu jedem Zeitpunkt in einem bestimmten Zustand
- Zustandsänderungen werden über den Takt gesteuert

Pegelsteuerung:
- Zustandsänderungen während eine 1 auf der Taktleitung anliegt

Flankensteuerung:
- Zustandsänderung bei positiver und/oder negativer Taktflanke
![[Pasted image 20220209152245.png]]
### Flanken beim D-FlipFlop
![[Pasted image 20220209152331.png]]

## T-Flipflop
![[Pasted image 20220209153234.png]]
Bei einer positiven Taktflnke
- wird bei t=0 der Zustand q beibehalten
- wird bei t=1 der Zustand q ==invertiert==

### Asynchroner Zähler
![[Pasted image 20220209153436.png]]
### Synchroner Zähler VS Asynchroner Zähler
![[Pasted image 20220209153613.png]]
## Schaltwerke - Allgemeines Schema Moore/Mealy
![[Pasted image 20220209153753.png]]
## Flipflops
Flankengesteuert
![[Pasted image 20220209153822.png]]
## Latches
Phasengesteuert
![[Pasted image 20220209153843.png]]
## RS-Flipflops
 ![[Pasted image 20220209153942.png]]
 ## RS-Latches
 ![[Pasted image 20220209154039.png]]
 ## JK-Flipflops
 Sind wie RS-FlipFlops, bloß, dass der Verbote Zustand 11 toggelt
 -> quasi RS-FlipFlop und T-FlipFlop vereint
 ![[Pasted image 20220209154205.png]]
 ___
# 7 Standardschaltwerke
## Register
Funktion:
- Speicherung von Datenworten
- Typische Wortbreiten: 8, 16, 32 , 64 oder 128 Bit
- ==Jedes Bit wird in einem separaten FlipFlop gespeichert==
	-> Registerbreits = Anzahl der FFs
	-> Alle FFs werden über den gleichen Takt gesteuert
	
Anwendeung:
	- Standardspeicher in Prozessoren
		- Mehrere für den Benutzer sichtbare Registewr
		- Viele interne Registr für Zwischenergebnisse

Bevorrechtigte Eingänge
- Wirken auf alle Register-FFs
		- Set oder Reset (synchron oder asynchron)
		- Clock enable
		
![[Pasted image 20220209154657.png]]
## Akkumulator
![[Pasted image 20220209154729.png]]
## Schieberegister
Aufbau
- Mehrere in Serie geschaltete FFs
	- synchron getaktet
- Das Ausgangssignal wird mit jeder Taktflanke nach rechts weitergereicht
### Beispiel
4-Bit-Schieberegister mit zusätzlichem Enable-Eingang
![[Pasted image 20220209154842.png]]
### Anwendung
- Serielle Datenübertragung
	- Parallel-Seriell-Wandler
	- Seriell-Parallel-Wandler
- Rechenoperationen
	- Schieben nach links: Multiplikation mit 2
	- Schieben nach rechts: Division durch 2
- Verzögerung
### Eingänge
Reset: Zurücksetzen aller FFs auf 0
Load: Paralleles Ladesn des Schieberegisters
Enable: Es wird nur geschoben, falls enable = 1
Direction: Richtung, in die geschoben wird
___
# Modellrechner
![[Pasted image 20220210123843.png]]
## Speicherkomponenten
1.  Das **Instruktionsregister** und das **Datenregister** lassen bei positiver Taktflanke von clk die Eingänge rein und schalten danach durchgängig ihren internen Zustand zum Ausgang
-> sie dienen also als ==Zwischenspeicher== für die **Instruktionen** und **Daten**
2. **Instruktionsdecoder** bekommt Werte vom Register und liefert dem **Steuerwerk**, welcher Befehl als nächstes ausgeführt werden soll.
3. Das **Steuerwerk** bekommt zusätzlich  die Werte des **Statusregisters** (womit es Branch-Befehle umsetzt) und gibt die entsprechenden Steuersignale aus.
4. Der **Instruktionszähler** bekommt das **Datenregister** und Steuersignal vom **Steuerwerk**. Es kann den Instruktionszähler inkrementieren (kontinuierliche Programmausführung), addieren und laden.
5. Das **Statusregister** ist ein Zwischenspeicher, das aus den Werten Z,C,N besteht. Es spiegelt die Ergebnisse der letzten ausgeführten Operation des Akkumulator wieder.
6. Der **Akkumulator** besteht aus einem 4-Bit-Register für das Ergebnis von Lade- und Rechenoperationen. Außerdem hat er eine **ALU**, die hier addieren und subtrahieren kann.
Er berechnet zur negativen Taktflanke und übernimmt das Ergebnis und gibt es kontinuierlich ans **RAM** und an das **Statusregister** aus.
7. Das **RAM** ist geteilt in **Daten-RAM** und **Befehls-RAM** (jeweils 4-Bit breit).
Es gibt **16 Addressen** mit je 4-Bit.
8. Der **Adressbus** wählt eine Zeile des RAMs aus und gibt die Zeile am Ausgang vom **Daten-RAM** und vom **Befehls-RAM** aus.

Das Lesen des RAMs erfolgt kontinuierlich.
Das Schreiben erfolgt zur negativen Taktflanke (Nur Daten-RAM kann geschrieben werden).
### RAM
![[Pasted image 20220210121359.png]]
## Zeitliche Befehlsabarbeitung
Beispiel für LDA \#5 in **Adresse 0** (Soll den Wert 5 in den Akku laden)
5 ist im Daten-RAM (0101) Op-Code ist (0001) für Befehls-RAM

==Fetch-Phase==
1. Beginnt im Instruktionszähler mit Wert 0000.
==Positive Takflanke kommt==
2. Instruktionsregister schalten 0001 und Datenregister schaltet 0101.
==Decode-Phase==
3. Der Befehl wird dekodiert und entsprechende Steuersignale werden an das Steuerwerk weitergegeben.
4. Das Steuerwerk ermittelt sämtliche Steuersignale für alle Komponenten in unserem Modellrechner. (sofort). Die Komponenten beginnen sofort mit der Abarbeitung.
==Execute-Phase==
5. 0101 des Datenregisters geht zum Multiplexer $m_1$ und wird durchgeleitet.
==Write-Phase==
6. Vorbereitung, um das Ergebnis zu schreiben
==Negative  Taktflanke kommt==
7. Der Akku übernimmt das, was am Eingang einsteht und gibt das Ergebnis aus.
Die 5 0101 ist im Akku angekommen.
8. Der Instruktionszähler wird modifiziert. Da hier kein Sprungbefehl vorliegt, wird der Instruktionszähler inkrementiert.

Anmerkung:
Die Decode-, Execute-, und Write-Phasen laufen alle gleichzeitig ab. Dabei entstehen die ganze Zeit 'falsche Ergebnisse'.
Wichtig ist nur, dass, sobald die negative Taktflanke kommt, alle Phasen durchgelaufen sind und dann das richtige Ergebniss ausgegeben wird.

Kann man den Zeitraum zwischen den Flanken verkürzen?
Man muss sich die konkreten Implementierungen der Komponenten anschauen. Man kann eine **maximale Gatterlaufzeit** ermittln, die für alle Operationen auftreten kann und muss dann sicherstellen, dass die negative Taktflanke erst danach passiert.

Beim Overclocking wird die Sicherheitsreserve for der negativen Taktflanke verkürzt. Dadurch kann die Taktrate erhöht werden.