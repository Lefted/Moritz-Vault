# Technische Informatik 1 Lernzettel
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
 

# 2 Boolesche / Schaltalgebra

## Boolesche Funktionen
![[Pasted image 20220209134641.png]]

## Grundlegende Gesetze
![[Pasted image 20220209134452.png]]

## Weitere Rechengesetze
![[Pasted image 20220209134802.png]]


# 3 Schaltnetze
Paritätsfunktion
![[Pasted image 20220209143536.png]]

==**Stufigkeit**==: 2

- Es gibt Wahrheitstabelle
- Jede Schaltfunktion lässt sich in Hardware 1:1 umsetzen

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