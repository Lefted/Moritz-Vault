# 1 Grundlagen
## Euklidscher Algorithmus
(n teilt a) schreiben wir n|a
$a_0=q_1*a_1 +a_2$ mit $0 \leq a_2 \leq a_1$
$a_1=q_2*a_2+a_3$ usw.
Wir schreiben $ggT(a_0,a_1)=a_{j+1}$

### Beispiel
![[Pasted image 20220211182843.png]]

Ein Teiler von zwei Zahlen a und b ist auch Teiler von a+b
___
# 2 Relationen und Funktionen
Karteisisches Produkt ist eine zweistellige Relation auf zwei Mengen
$A \times B:=\{(a,b)|a\in A, b \in B\}$
## Umkehrrelation
$R^{-1}:=\{(y,x)|(x,y) \in R\}$
## 2.2.1 Äquivalenzrelation
 muss reflexiv, transitiv und symmetisch sein
 ## 2.3 Äquivalenzklassen
 $K_g:=\{x \in G|xRg\}$ ist die Menge aller Element, die zu g äquivalent sind
 - Für jedes g $\in G$ gibt es ein Äquivalenzklasse $K_g$
 - Falls zwei Äquivalenzklassen ein gemeinsames Element haben, sind sie identisch
 ## 2.4 Modulo-Rechnung mit Restklassen
 $9-5 \equiv 4~mod~7$
 1. Methode. Rechnen mit eindeutigem Vertreter der Klasse
 2. Methode. Wir lassen beliebigew Vertreter zu:
 
 Addition, Subtraktion und Multiplikation funktionieren
Division funktioniert anders!

Multiplikationstafel mit eindeutigen Repräsentanten Modul n = 6
![[Pasted image 20220211183847.png]]

In jeder Zeile und Spalte steht jede Zahl (ungleich 0) **genau einmal**.
Daher ist jede Gleichung $a*x=b$ **eindeutig lösbar**
z.B. $5x=5$ ergibt $x=4$

Weil in jeder Zeile genau eine 1 steht gibt es für jedes a ein **inverses Element** $a^{-1}$
## 2.4.2 Kürzungsregel
$x*y \equiv x*z ~mod~n \implies y\equiv z~mod~n,~falls~ggT(x,n)=1$
Wenn der modul und die Zahl mit der gekürzt wird teilerfremd sind, kann man kürzen

Beispiel (nicht anwendbar): $2*2 \equiv 5*x ~mod~6$, aber $2 \not\equiv 4$
Beispiel (anwendbar): $5*2 \equiv 5*x~mod~5 \implies 2 \equiv x~mod~6$, da ggT(5,6)=1

Wenn der Modul eine Primzahl ist kann man mit allen Zahlen ungleich 0 kürzen

## 2.4.4 Satz von Fermat
p sei Primzahl x eine naturliche Zahl mit $x \not\equiv 0~mod~p$
Es gilt:
$x^{p-1} \equiv 1 ~mod~p$

### Beispiel
p = 7 Dann gilt:
$2^{p-1} \equiv 2^6 \equiv 2*2*2*2*2*2 \equiv 1~mod~7$

## Berechnung der Inversen mit Satz von Fermat
$x^{-1} \equiv x^{p-2}~mod~p$

Beispiel: n=7: $3*5^{-1}=?~mod~7$
$5^{-1} \equiv 5^{p-2} \equiv 5^5 \equiv 3~mod~7$

Somit gilt: $3*5^{-1} \equiv 3*3 \equiv 2~mod~7$

Test: $5*2 \equiv 10 \equiv 3~mod~7$

## Effizientes Potenzieren mit Satz von Fermat
$5^{93}\equiv ?~mod~11$
aus dem kl. Satz von Fermat folgt: $5^{10} \equiv 1~mod~11$
Bei der Berechnung möglichst viele solche Potenzent verwenden:

![[Pasted image 20220211190050.png]]

## 2.5.3 Permutation
Umordnung einer endlichen Menge von n Elementen
![[Pasted image 20220211190145.png]]
Zyklenschreibweise:
![[Pasted image 20220212125513.png]]
## 2.5.4 Surjektivität, Injektivität und Bijektivität
![[Pasted image 20220211190242.png]]
Elemente aus dem Definitionsbereich eindeutig ein Element aus dem Bildbereich zugeordnet wird. Falls die Zuordnung auch in der umgekehrten Richtung eindeutig ist, dann sprechen wir von einer eineindeutigen oder bijektiven Zuordnung
## 2.5.5 Umkehrfunktion
![[Pasted image 20220211190434.png]]

### Beispiel
![[Pasted image 20220211190552.png]]
1. Injektivität zeigen ![[Pasted image 20220211190610.png]]
![[Pasted image 20220211190631.png]]
2. Für die Surjektivität folgende Gleichung nach x auflösen![[Pasted image 20220211190709.png]]
![[Pasted image 20220211190717.png]]
da für alle y ausführbar ist, gibt es zu jedem y ein passende x. Die Funktion ist somit auch surjektiv
3. Umkehrfunktion angeben:
![[Pasted image 20220211190810.png]]

Fallunterscheidung bei gebrochen rationalen Funktionen

## Parameterfunktion
![[Pasted image 20220211190911.png]]
Beispiel Kreis ![[Pasted image 20220211190919.png]]

## Verknüpfung von Abbildungen
![[Pasted image 20220211190943.png]]
erst links hinschreiben, dann rechts
# 3 Gruppen, Ringe und Körper
## 3.1.1 Operationen
Jede Abbildung *
![[Pasted image 20220211194429.png]]
ist eine **zweistellige Operation** mit dem **Operator *** und den beiden Operanden a,b

Wir schreiben (M,*)

Beispiel: ($ \mathds{N}$)

$$
(\mathbb{N},+), (\mathbb{Z,+}), (\mathbb{R},*)
$$

## 3.1.2 Assoziativgesetz
$a*(b*c)=(a*b)*c$
## 3.1.3 Kommutativgesetz
$a*b=b*a$
## 3.1.4 Neutrales Element
$a*e=a=e*a$
## 3.1.5 Inverses Element
b ist **inverses Element** zu a, falls gilt:
$a*n=e*b=a$

Beispiel: Addition -a, Multiplikation 1/a

## 3.2 Gruppen
Sind
- abgeschlossen (gehört zu der Operation schon dazu)
- assoziativ
- neutrale Elemente
- inverse Elemente

**abelsche Gruppe**
- kommutativ 

Beispiel modul = p $(\mathbb{Z}/_{mod~p},~\{0\},*)$
ist abelsche Gruppe sowie $(\mathbb{Z}/_{mod~p},~+)$
## 3.2.3 Gruppentheorie
- Exakt 1 neutrales Element
- Kürzungsregeln:
	- $a*b=a*c \implies b=c$
	- $b*a=c*a \implies b=c$
- Zu jedem Element gibt es genau ein Inverses Element
- Es gilt:
	$(a*b)^{-1}=b^{-1}*a^{-1}$
## 3.2.4 Untergruppe
Eine Gruppe ist eine Untergruppe, falls die Teilmenge mit der Operation wieder eine Gruppe ist.
Beispiel: die geraden Zahlen bilden eine Untergruppe von $(\mathbb{Z},+)$. 
(die ungeraden nicht, weil sie bzgl. Addition nicht abgeschlossen sind)

## 3.2.5 Erzeugendensystem
Hier geht es allg. um Operationen:
Eine Teilmenge einer Menge ist ein Erzeugendensystem, falls für die "Obergruppe", falls sich jedes Element aus M mit diesen Elementen darstellen lässt

![[Pasted image 20220211201129.png]]

Beispiele:
![[Pasted image 20220211201206.png]]

## 3.2.6 Zyklische Gruppn
sind  Gruppen mit einem Erzeugendensystem, das nur aus einem Element besteht.
Alle zykl. Gruppen sind abelsch. 
Dann lassen sich zwei beliebige Elemente b und c als Potnzen von a darstellen:
![[Pasted image 20220211201341.png]]

## 3.3.1 Ringe
R sei eine beliebige Menge mit zwei Operationen + und *. Wir nenen (R,+,*) einen Ring, falls gilt:
![[Pasted image 20220211201458.png]]

Beispiel: $(\mathbb{Z},+,*)$ bildet einen Ring, aber keinen Körper (keine inversen Elemente bzgl. Multiplikation)

![[Pasted image 20220211201919.png]]

## 3.3.2 Körper
Sei (K,+,*) ein Ring, bei dem die Multiplikation *  die Gruppengesetze erfüllt.
Es muss gelten:

- (K \ {neutrales Element bzgl. +}, *) bildet eine abelsche Gruppe

Dann nennen wir (K,+,*) einen **Körper**.

Beispiele: $(\mathbb{Q},+,*), (\mathbb{R,+,*})$
![[Pasted image 20220211201925.png]]
## 3.3.3 Eigenschaften von Ringen
![[Pasted image 20220211202011.png]]
## 3.3.4 Nullteiler
sind Zahlen, die ungleich 0 sind und zusammen multipliziert 0 ergeben.

Beispiel: ![[Pasted image 20220211202120.png]]

## 3.4 Polynomringe
Polynome:
$(\mathbb{R},+,*)$ bilden einen Körper
Polynome haben Form: ![[Pasted image 20220211202355.png]]

die Menge aller Polynome in x über $\mathbb{R}$ schreibt man als:
$\mathbb{R}[x]$

Ein Polynom heißt **normiert**, falls der Koeffizient des höchsten Grades = 1 ist

$(\mathbb{R}[x],+,*)$ ist ein **Polynomring**
- Addition ist abgeschlossen
- Addition ist assoziativ (es kommt nicht auf die Klammerung der Polynome an)
- neutrales Element p=0
- es gibt inverse Polynome:
![[Pasted image 20220211202942.png]]

-> $(\mathbb{R}[x],+)$ bildet eine Gruppe

- Multiplikation ist assoziativ
- Für Addition und Multiplikation gelten die Distributivgesetze

(kein Körper, da es für ale Polynome mit Grade $\geq$ 1 keine Inversen gibt:
p=x inverses Element wäre $\frac{1}{x}$ aber das ist kein Polynom!).

## 3.4.3 Weitere Polynomringe
$\mathbb{Z}~mod~2$ ist $\mathbb{F}_2$

Regeln:
- Addition entspricht XOR
- Multiplikationsverfahren:

Sind Shift-Operationen und danach wieder Additionen
![[Pasted image 20220211203506.png]]
Wir müssen für jede Eins der rechten Bitfolge
die linke Bitfolge einmal rechtsbündig hinschreiben

## 3.4.4. Division mit Rest
 ![[Pasted image 20220211211747.png]]
 
 ### Beispiel:
 ![[Pasted image 20220211211823.png]]
 ![[Pasted image 20220211211828.png]]
 
 oder 
 ![[Pasted image 20220211211842.png]]
 
 ## 3.4.5 Modulo-Rechnung für Polynome
 Es seien u und v Polynome aus einem Polynomring $\mathbb{F}_2[x]$.
 Mit einem weiteren Polynom q als Module können wir eine Division mit Rest durchführen:
 ![[Pasted image 20220211212016.png]]
 
 es gibt eine Äquivalenzrelation
 ![[Pasted image 20220211212031.png]]
 
 ### Beispiel
 $\mathbb{F}_2[x]$ modul sei ![[Pasted image 20220211212106.png]]
 
 Es gibt eindeutige Repräsentanten: 0,1,x,x+1
 Die Additionstabelle lautet:
 ![[Pasted image 20220211212215.png]]
 
 Die Multiplikationstafel lautet:
 ![[Pasted image 20220211212310.png]]
 
 Es gibt also Nullteiler: ![[Pasted image 20220211212323.png]]
 
 Da es zu (x+1) kein Inverses gibt, erhalten wir bei
$\mathbb{F}_2[x]~mod~(x^2+1)$ nur einen Ring und keinen Körper

## Reduzibel und Irreduzibel
Ein Polynom ist reduzibel, wenn es sich in zwei Polynome zerlegen lässt, die beide vom Grad $\geq$ 1 sind.
Bsp: ![[Pasted image 20220211212504.png]]

Ansonsten irreduzibel

==Es gilt==
Für irreduzible Polynome q als Module bildet $\mathbb{F}_2[x]/~mod~q$
einen **Körper**.
Wenn q den Grad n hat, dann gibt es $2^n$ verschiedene Reste vom Grad kleiner n.
Dies ist die **Anzahl der Elemente dieses Körpers**.
 
 ## 3.4.7 Effiziente Berechnug der Modulo-Reduktion in $\mathbb{F}_2[{x}]$
 
 Zunächst kann ein solches Polynom als Bitstring notiert werden, indem wir die Koeffizienten notieren:
![[Pasted image 20220211213135.png]] -> ![[Pasted image 20220211213140.png]]

dann können wir wieder Multiplikation mit Shifts durchführen und Addition mit  XOR

## 3.4.7.1 Fehlererkenndende und fehlerkorrigierende Codes
Prüfbit:
die XOR-Summe soll gleich 1 sein:
![[Pasted image 20220212090259.png]]
Übertragen wird also
![[Pasted image 20220212090602.png]]

genau ein falsches Bit übertragen → Quersumme ist 0

Wiederholende Codes:
das Viertupel wir dreimal wiederholt übertragen:
![[Pasted image 20220212090546.png]]
- ein einziger Fehler kann mit den anderen  Widerholngn korrigiert werden
- zwei Bitfehler können erkannt, aber nicht mehr korrigiert werden

nicht besonders effizient

**Besseres Verfahren**
Polynome über $\mathbb{F}_2$ (hier vom Grad kleiner oder gleich drei)
![[Pasted image 20220212091024.png]]
wir hängen 3 weitere **Kontrollbits** an, die wir mit einem irreduiblen Polynom vom Grad 3, das gleicheitig ein Teiler von $x^7+1$ ist:
z.B. ![[Pasted image 20220212091046.png]]
Der übertragende Vektor V ist ![[Pasted image 20220212091203.png]]

Der Empfänger erhälten den möglichen fehlerhaften Vektor W.
Für einen korrekt übertragenen Vektor ergibt eine Division mit Rest durch das Polynom G immer den Rest 0
Alternativ können wir mit einem Kontrollpolynom multiplizieren und modulo $x^7+1$ rechnen. $H:=(x^7+1)$/G (G ist Generatorpolynom)

Alle diese Rechnungen können sehr gut mit XOR- und Shift-Operationen durchgeführt werden.

### Beispiel
Für ![[Pasted image 20220212091247.png]]
erhalten wir für V ![[Pasted image 20220212091259.png]]
Kontrolle von W durch Division mit Rest: ![[Pasted image 20220212091409.png]]
Alternative mit Kontrollpolynom:
	Kontrollpolynom ist dann ![[Pasted image 20220212091556.png]]
	Der Test ergibt ![[Pasted image 20220212091612.png]]

## Codewörter und Codes
Alle dieser 7er Vektoren heißen **Codewörter** und alle solchen Codewörter bilden zusammen den jeweiligen **Code**.

hier die Hälfte: ![[Pasted image 20220212091825.png]]

a) Das ==Hamming-Gewicht== eines Codewortes ist die Anzahl Einsen, die in einem Codewort auftreten. z.B: Hamming-Gewicht($c_2$)=3

b) Die ==Hamming-Distanz== von zwei Codewörtern $c_i$ und $c_j$ ist gleich dem **Hamming-Gewicht der XOR Summer** der beiden Codewörter.

z.B. Hamming-Distanz($c_2,c_4$)= Hamming-Gewicht($c_{2}\oplus c_4$)=4

c) Die ==Minimal-Distanz== eines Codes C ist das **Minimum aller Hamming-Distanzen die zwischen zwei verschiedenen Codewörtern** auftreten.
Für unseren Code beträgt die Minimal-Distanz=3.

Bei unserem Code ist es eine Eigenschaft, dass sich je zwei Codewörter immer mindestens an drei Stellen unterscheiden (Minimal-Distanz).
Wenn also ein Codewort bei der Übertragung 3 Fehler enthalten würde, dann könnte es als falsches anderes Codewort interpretiert werden.
Enthält es maximal 2 Fehler, dann kann es zumindest als fehlerhaft identifiziert werden.
Sollten wir wissen, dass maximal 1 Fehler auftreten kann, dann können wir sogar den Fehler korrigieren (weil der fehlerhafte Vektor zu genau einem Codewort die Hamming-Distanz 1 hat)

Allgemein: ein Code mit Minimal-Distanz d
![[Pasted image 20220212092443.png]]
### Beispiel
7 Infobits und 8 Kontrollbits = 15 Bit Codewörter
Polynom ![[Pasted image 20220212092537.png]] kann verwendet werden.

Der Code, der mit G erzeugt wird, hat die Minimaldistanz d=5.
Es können also 4 Fehler erkannt werden oder alternativ
$\frac{5-1}{2}=2$ Fehler korrigiert werden.
___
# 4 Vektorräume
Ortsvektor $\vec a= \vec OP$
Mit V fassen wir die **Menge aller Ortsvektoren** zusammen
Addition mit Vektoren
- Die Addition ist abgeschlossen
- Der Nullvektor ist das neutrale Element der Addition
- es gibt inverse Elemente $- \vec a$ bzgl. der Addition
- die Addition ist kommutativ
- die Addition ist assoziativ

→ abelsche Gruppe (V,+)

Multiplikation mit reellen Zahlen
- aus den Strahlensätzen ergibt sich, dass es ein **Skalar** c gibt, mit dem ein Vektor multipliziert werden kann
- 1 ist das neutrale Element

Es gilt:
![[Pasted image 20220212110217.png]]

Wir nennen $(V,\mathbb{R},+,*)$ einen ==Vektorraum==

### Strahlensätze:
![[Pasted image 20220212105800.png]]
![[Pasted image 20220212105804.png]]
![[Pasted image 20220212105814.png]]
## 4.1.2 Linearkombination
Es lässt sich folgende Summe aus Vektoren und Skalaren bilden:
![[Pasted image 20220212110442.png]]
Wir nennen diese Summe ==Linearkombination==.
## 4.1.3 Lineare Hülle und Unterraum
Die ==lineare Hülle== oder der ==Unterraum== ist die **Menge aller Lienarkombinationen**, die wir mit einer festen Menge von Vektoren bilden können:
![[Pasted image 20220212110607.png]]
Lineare Hülle von $\vec a_{1,}\vec a_{2,}...,\vec a_3$
Wir schreiben dafür: ![[Pasted image 20220212110753.png]]

$\vec b \in [\vec a_{1,}\vec a_{2,}..., \vec a_k]$
heißt, dass es passende, reelle Zahlen gibt, so dass die Linearkombination $\vec b$ gebildet werden kann.

Es gilt, dass die Menge U, die eine Teilmenge von V ist, **selbst auch wieder** einen Vektorraum bildet:
$(U,\mathbb{R},x,*)$

Heißt das für den Unterraum gilt:
- hat neutrales Element der Addition (Nullvektor)
- hat inverse Elemente der Addition
- ist kommutativ und assoziativ (bleiben in der Teilmenge enthalten)
- Addition ist abgeschlossen (Summe zweier linear Komb. ist wieder eine linear Komb.)
- Mit Skalar multiplizier ergibt es wieder eine Linearkombination

Die Linearkombination von zwei Vektoren im $\mathbb{R}^3$, spannt eine Ebene auf
Für einen Vektor bekommen wir eine Gerade.

### 4.1.3.1 Beispiel
Geg. ![[Pasted image 20220212111539.png]]
Menge aller Linearkomb: ![[Pasted image 20220212111554.png]]
Bildet wieder einen Vektorraum:
![[Pasted image 20220212111647.png]]
(Wäre die letzten zwei Komponenten ungleich 0, dann nicht teil des Unterraums)

## 4.2 Lineare Abhängigkeit
Mehrere Vektioren heißen ==linear abhängig==, wenn sich der Nullvektor als Linearkombination dieser Vektoren darstellen lässt, **ohne dass alle Skalare gleich Null sind**.
![[Pasted image 20220212112208.png]]

- Ein Vektor heißt linear abhängig, falls er der Nullvektor ist
- Wenn zwei Vektoren linear abhängig sind, dann liegen sie **auf einer Geraden**.

## 4.2.2 Lineare Unabhängigkeit
Mehrer Vektoreb heißen ==linear unabhängig==, wenn aus der Linearen Hülle = dem Nullvektor:
![[Pasted image 20220212112341.png]]
stets folgt, dass alle Skalare = 0 sind.

- Die Skalare von einer linear Kombination, heißen Koordinaten bzgl. der Vektoren

### 4.2.2.1 Beispiel Parallelogramm
Die Vektoren müssen linear unabhängig  sein, damit sie eine Fläche aufspannen.
![[Pasted image 20220212112637.png]]

Wenn es sich um  ein Parallelogramm handelt muss gelten:
- Punkt S teilt die beiden Strecken DE und AC im Verhältnis 1:2

Dies gilt es zu beweisen:
- zunächst aufstellen der Gleichungen
![[Pasted image 20220212112839.png]]
- Die Gerade g, die durch A und C verläuft
![[Pasted image 20220212112916.png]]
- Die Gerade h, die durch D und E verläuft
![[Pasted image 20220212113003.png]]
- Für den Schnittpunkt beide Ausdrücke gleichsetzten und unformen
![[Pasted image 20220212113046.png]]
- Weil die Vektoren linear unabhängig sind, müssen beide Skalare = Nullvektor sein
- Somit erhalten wir
![[Pasted image 20220212113337.png]]
- Dann einsetzten und Formel für S erhalten, die zeigt, dass das gewünschte Verhältnis gilt

## 4.3.1 Basis
Die Menge linear unabhängiger Vektoren (nicht auf einer Geraden), die den gesamten Vektorraum V erzeugen, nennt man ==Basis== des  Vektorraumes.
Es gilt also:
![[Pasted image 20220212113602.png]]

- Die Anzahl der  Elemente einer Basis ist stets gleich

## 4.3.3 Dimension
Die **Anzahl der Vektoren einer Basis** heißt  ==Dimension== und ist Eigenschaft des Vektorraumes.

## Kanonische Einheitsvektoren und Kanonische Basis
Für den $\mathbb{R}^3$ ist die Basis
![[Pasted image 20220212114055.png]],
die aus den ==kanonischen Einheitsvektoren== besteht. Sie heißt ==kanonische Basis==

## 4.3.4 Koordinaten
Ein Vektor lässt sich als eine Linearkombination aus Skalaren und Kanonischen Einheitsvektoren beschreiben.
Wir nennen die Skalare dann ==Koordinaten== bzgl. der Basis
![[Pasted image 20220212122916.png]]
# 5 Lineare Gleichungssysteme
![[Pasted image 20220212125923.png]]
- m lineare Gleichungen
- n Unbekannte
- links ist $(m \times n)$-==Matrix==
![[Pasted image 20220212125822.png]]
erster Index ist der Zeilenindex, zweiter der Spaltenindex
- rechts ist Vektor

## 5.1 Lösungsverfahren
- Vertauschen von Gleichungen
- Unnummerieren der Unbekannten (später wieder auslösen)
- Addition eines Vielfachen
- Multiplikation einer Gleichung mit einem Faktor $\neq$ 0

Endform eines LGS
![[Pasted image 20220212130122.png]]

## 5.1.1 Lösungsverhalten
- Keine Lösung
- Genau eine eindeutige Lösung
- Unendlich viele Lösungen

## 5.1.2 Gauß-Jordan-Verfahren
erste Zeile ist Arbeitszeile

1. durch Vertauschen und Unnummerieren $a_{11} \neq 0$ erreichen
2. wir addieren das ==$(-a_{i1}/a_{11})$==-fache der Arbeitszeile, auf die i-te Zeile
Jetzt soll die erste Spalte so aussehen: ![[Pasted image 20220212130543.png]]
3. Falls dies noch nicht der Fall ist, können wir Spalte vertauschen (dabei umbennen)
Danach wieder das i-iwas-fache der zweiten Zeile auf die übrigen Zeilen

...

### Beispiel Umbenennung von Variablen
![[Pasted image 20220212135611.png]]
durch Vertauschen von $x_3$ und $x_4$ erhalten wir
![[Pasted image 20220212135719.png]]
die umbenannten Variablen bezeichnen wir mit
![[Pasted image 20220212135812.png]]

die Lösung für die umbenannten Variablen ist
![[Pasted image 20220212135831.png]]

danach vertauschen wir die 3. und die 4. Zeile und setzten für $\hat x_4$ wieder $x_3$ ein:
![[Pasted image 20220212135925.png]]

## 5.1.3 Rang eines Gleichungssystems
Der Wert k ist der Rang des Gleichungssystems

### 5.1.3.1 Beispiel
![[Pasted image 20220212130929.png]]
$x_1$ und $x_2$ sind ==abhängige Variablen==, $x_3$ und $x_4$ sind ==freie Variablen==.

"k ist die Anzahl linear unabhängiger Gleichungen"

## 5.2 Beschreiben der Lösungsmengen mit Vektoren
- Gleichungen nach abhängigen Variablen umformen
- danach
![[Pasted image 20220212134034.png]]

## 5.2.1 Homogenes Gleichungssystem
Ein Gleichungssystem heißt ==homogen==, falls alle Koeffizienten der rechten Seite = 0 sind.
Fall mindestens ein Koeffizient ungleich null ist, so heißt es ==inhomogen==.

- ein homogenes LGS ist immer lösbar

## 5.2.2 Darstellung der Lösungsmenge mit Vektoren
![[Pasted image 20220212134334.png]]

- für die ersten k Zeilen kann $b_{1}$ bis $b_k$ aus der Endform übernommen werden
- die $a_{ij}$ (i=1..k und j=k+1,..n) müssen nur mit einem negativen Vorzeichen versehen werden
- für die weiteren Zeilen (k+1-te bis n-te) muss der erste Vektor nur mit Nullen aufgefüllt werden. Alle weiteren Vektoren werden mit den kanonischen Einheitsvektoren der Länge n-k aufgefüllt.

### Beispiel
![[Pasted image 20220212135031.png]]
- Eingerahmte 0 → LGS ist lösbar
- Einsen in der Diagonalen → Rang k = 2
- Freie Variablen = Anzahl Unbestimmten 3 - Rang 2 = 1
- Eingerahmten Werte 1 und 4 müssen mit umgekehrten Vorzeichen versehen werden
- 3 und 2 der rechten Seite werden unverändert übernommen
- Im unteren Bereich wird der Vektor $\vec x_s$ mit einer Null aufgefüllt
- Im unteren Bereich wird der Vektor $\vec r_3$ mit einer Eins aufgefüllt

![[Pasted image 20220212135303.png]]

Lösungsmenge ist eine Gerade g
![[Pasted image 20220212135439.png]]

## 5.2.3 Dimenon des Lösungsraumes eines homogenen Gleichungssystems
Dimension = Anzahl der Variablen n - Rang k
- Das allgemeine System besitzt genau dann eine eindeutige Lösung, wenn das zugehörige homogene System nur genau die triviale Lösung $\vec 0$ besitzt
## 5.3.1 Determinante einer 2x2-Matrix
Sei das LGS
  ![[Pasted image 20220212164300.png]]
Dann ist die Determinante
$a_{11}a_{22}-a_{12}a_{21}$

1. Determinante = 0:
	1. unlösbar, falls ![[Pasted image 20220212164702.png]] 
	2. Falls beide Werte der rechten Seite gleich null sind, dann gibt es unendlich viele Lösungen
2. Determinante $\neq$ 0:
	Dann besitzt es genau eine Lösung:
	![[Pasted image 20220212164807.png]]

Für Matrizen gilt:
Sei ![[Pasted image 20220212164844.png]] ![[Pasted image 20220212164848.png]]

Die Determinante der 2x2-Matrizen ist:
![[Pasted image 20220212164908.png]]

Die Lösungen sind dann (det $\neq$ 0) (==Regel von Cramer==)
![[Pasted image 20220212165028.png]] ![[Pasted image 20220212165035.png]]

→ **Jedes LGS hat eine eindeutige Lösung, wenn $det~A \neq 0$ ist.

- **Im $\mathbb{R}^3$ ist die Determinante von einer 3x3 Matrix das aufgespannte Volument**
- **Im $\mathbb{R}^2$ ist die Determinante von einer 2x2 Matrix die aufgespannte Fläche**

## Regel von Sarrus
Berechung der Determinate einer 3x3-Matrix
![[Pasted image 20220212165417.png]]

## 5.3.4 Laplace Entwicklungssatz
nach einer bestimmten Spalte/Zeile entwickeln (mit möglichst vielen Nullen)
![[Pasted image 20220212165553.png]]
![[Pasted image 20220212165548.png]]

## 5.3.5 Determinanten von oberen Dreiecksmatrizen
![[Pasted image 20220212170151.png]]
![[Pasted image 20220212170205.png]]
## 5.3.7 Transponierte Matrix
Man spiegelt von links oben nach rechts unten
![[Pasted image 20220212170343.png]]→ ![[Pasted image 20220212170349.png]]
Bezeichung: $A^t$

## 7 Rechenregeln für Determinanten
![[Pasted image 20220212170835.png]]
## 5.3.9 Lösbarkeit von quadratischen Matrizen
![[Pasted image 20220212172919.png]]
![[Pasted image 20220212172923.png]]

### Beispiel
![[Pasted image 20220212173005.png]]
→ eindeutig lösbar

Regel von Cramer:
3. Spalte der Matrix durch den Vektor 
![[Pasted image 20220212173200.png]]
ersetzen
![[Pasted image 20220212173224.png]]


## 5.3.10 Regel von Cramer
![[Pasted image 20220212173114.png]]

## Determinante berechnen nach Gauß-Jordan-Verfahren
- Zeilentausch und Spaltentausch verändern das Vorzeichen
- Multiplikation mit Faktor c muss am Ende rückgängig gemacht werden, indem
mit $\frac{1}{c}$ multipliziert wird

### Beispiel
![[Pasted image 20220212173806.png]]

Determinante der Matrix der Endform
![[Pasted image 20220212173823.png]]
ergibt -20
- Danach noch mit $\frac{5}{4}$ multiplizieren ergibt
![[Pasted image 20220212173932.png]]

Wenn nur die Determinante berechnet werden sollte, hätten die beiden ersten Umformungsschritte genügt. (hier wurden noch die Lösungen berechnet)
![[Pasted image 20220212174012.png]]