# Definition
Ein kommutativer Ring (mit Eins) ist eine [[Gruppen|abelsche Gruppe]] $(R,+,0)$ mit einer Verknüpfung $\cdot:R \times R \rightarrow R$, mit:
1) $\exists 1\in R \forall a \in R : 1\cdot a = a$ 
2) $\forall a,b,c \in R: (a\cdot b)\cdot c = a \cdot (b\cdot c)$ 
3) $\forall a,b,c \in R:  a \cdot (b+c) = (a\cdot b) + (a \cdot c)$ 
4) $\forall a,b \in R: a\cdot b = b\cdot a$ 

# Eigenschaften
- Es gilt $\forall a \in R: 0 \cdot a = (a-a)\cdot a = a^{2}-a^{2}= 0$ 
- Es gilt $a + (-1)\cdot a = 1 \cdot a + (-1)\cdot a = (1-1) \cdot a = 0 \implies (-1)\cdot a = -a$  

# Teilringe
Wir bezeichnen $A \subset R$ als **Teilring** von $R$, wenn gilt:
- $\forall a,b\in R: a-b \in R$ 
- $\forall a,b \in A: a\cdot b\in A$
- $0,1 \in A$ 
Insbesondere ist jeder Teilring eines kommutativen Rings wieder ein kommutativer Ring.


# Teilbarkeit
Wir sagen für $a,b \in R$ :  $a \mid b$ bzw. a **teilt** b, falls es ein $c\in R$ gibt, sodass $a \cdot c = b$.

### Nullteiler und Integritätsbereiche
$a \neq 0 \in R$ heißt **Nullteiler**, falls es ein $b \neq 0 \in R$ gibt, sodass $a\cdot b = 0$, sich also 0 als Produkt  von zwei von 0 verschiedenen Faktoren schreiben lässt.

Wir nennen einen Ring **Integritätsbereich**, falls er vom [[#Nullring]] verschieden ist und keine Nullteiler enthält.

In einem Integritätsbereich nennen wir ein $d\in R$ mit $c\mid a \land c \mid b \iff c \mid d$ den **größten gemeinsamen Teiler** von $a,b$ und schreiben auch $ggT(a,b)$.

##### Eigenschaften
In Integritätsbereichen gilt, dass man kürzen darf, d.h. für $a,b\in R$ und $c \neq 0 \in R$ gilt $$a\cdot c \equiv b \cdot c \implies a \equiv b \text{ für } \equiv \in \{=, \sim\}$$
##### Teilerfremde Elemente
Wir nennen in einem Integritätsbereich $a,b\in R$ **teilerfremd**, falls jeder gemeinsame Teiler eine Einheit ist.
### Einheiten
$a\in R$ heißt **Einheit**, falls $a \big \vert 1$. Das ist äquivalent dazu, dass $a$ invertierbar bezüglich der Multiplikation ist. Wir bezeichnen $R^{*} := \{a \in R : a \text{ ist Einheit}\}$ als die Menge der Einheiten. Das bildet insbesondere eine Gruppe bezüglich der Multiplikation.
##### Eigenschaften
- Ist eine Einheit ein [[#Nullteiler und Integritätsbereiche|Nullteiler]], so ist $R$ der [[#Nullring]] 

### Assoziiertheit
Wir nennen zwei Elemente **assoziiert**, falls es eine [[#Einheiten|Einheit]] $c \in R^{*}$gibt, sodass $a=b\cdot c$. Wir schreiben dann auch $a \sim b$.

In einem Integritätsbereich gilt $a \mid b \land b \big\vert a \implies a$ ist assoziiert zu $b$. 

### Prim- und irreduzible Elemente
Sei $p \in R$ in einem [[#Nullteiler und Integritätsbereiche|Integritätsbereich]] keine [[#Einheiten|Einheit]] und $p \neq 0$. 

- Gilt für alle $a,b \in R$ mit $p = b\cdot a$, dass $a\in R^{*}$ oder $b\in R^{*}$ so heißt $p$ **irreduzibel**. 
- Gilt für alle $a,b\in R$, dass $p \big\vert ab \implies p \big\vert a \lor p \big\vert b$ so heißt $p$ **prim**

#### Eigenschaften
- $p$ prim $\implies p$ irreduzibel. 
- $p$ prim und $p \big\vert a_{1} \cdot ... \cdot a_{k} \implies \exists j \in \{1,...,k\}: p \big\vert a_{j}$ 


#### Primfaktoren
Ist $0 \neq a \in R$ so gilt, wenn eine Zerlegung $$a = e \cdot p_{1}\cdot ... \cdot p_{k}$$mit einer Einheit $e$ und Primelementen existiert, so $k$ eindeutig und die sonstige Zerlegung durch Primelemente bis auf Vertauschung und [[#Assoziiertheit]] eindeutig. 

##### faktorielle Ringe
Ein [[#Nullteiler und Integritätsbereiche|Integritätsbereich]] $R$ heißt **faktoriell**, falls für alle $a \in R \setminus \{0\}$ mit $a \not \in R^{*}$ gilt, dass:
- Es gibt irreduzible Elemente $p_{1}, ..., p_{k} \in R$ mit $a=p_{1}\cdot ... \cdot p_{k}$ 
- $k$ ist durch $a$ bestimmt
- Die Elemente $p_{j}$ sind eindeutig bestimmt bis auf Permutation und Assoziiertheit.

###### Äquivalente Darstellung
Integritätsbereich $R$ ist faktoriell genau dann wenn:
- Jedes $a \neq 0$ als Produkt $a = e \cdot p_{1}\cdot ... \cdot p_{k}$ mit $e \in R^{*}$ und irreduziblen $p_{j}$ darstellbar ist und
- $p$ irreduzibel $\implies$ $p$ prim.

###### Teiler
Es gilt jeder Teiler von $a =e \cdot p_{1}\cdot ... \cdot p_{k}$ in einem faktoriellen Ring mit $e$ Einheit und $p_{i}$ irreduziblen Elementen ist eine Einheit oder assoziiert zu $p_{i_{1}}\cdot ... \cdot p_{i_{l}}$ mit $1 \leq i_{1} < ... < i_{l} \leq k$. 

###### Potenzen
Für teilerfremde Elemente $a,b$ gilt $a\cdot b \sim z^{k}$ für ein $z \in R$ mit $k \in \mathbb{N}$. Dann existieren $x,y\in R$ mit $$x^{k}\sim a, y^{k}\sim b$$Das erhält man wegen der Teilerfremdheit und Primfaktorzerlegung einfach durch Aufteilung der Primfaktoren.



# Beispiele
### Nullring
Der Nullring $\{0\}$ ist der Ring, der nur aus der 0 mit den eindeutigen Verknüpfungen besteht. Er ist der einzige Ring, in dem gilt, dass $0 = 1$ ist

### Ganze Zahlen
Das klassische Beispiel für einen Ring mit 1 sind die ganzen Zahlen $\mathbb{Z}$, wie in der Schule.

### Restklassen
 $\mathbb{Z}n\mathbb{Z} := \mathbb{Z}/_{\equiv}$   mit $[a]+[b] := [a+b]$ und $[a]\cdot [b] := [a\cdot b]$ ist ein kommutativer Ring. Es ist nur ein Körper, wenn $n$ eine Primzahl ist.
### Körper
Ein Körper $\mathbb{K}$ ist ein [[Kommutative Ringe|kommutativer Ring]] für den gilt, dass $(\mathbb{K}\setminus \{0\}, \cdot, 1)$ eine Gruppe ist. Alternativ kann man auch sagen, dass $\mathbb{K}^{*}= \mathbb{K}\setminus \{0\}$ 
Jeder Körper ist ein [[#Nullteiler und Integritätsbereiche|Integritätsbereich]], darunter fallen z.B.
- $\mathbb{R}$
- $\mathbb{C}$ 
### Gaußsche Zahlen
$\mathbb{Z}[i] := \{a+b i : a,b\in \mathbb{Z}\}$ ist ein [[#Teilringe|Teilring]] von $\mathbb{C}$ und insbesondere ein [[#Nullteiler und Integritätsbereiche|Integritätsbereich]]. Es gilt $(Z[i])^{*} = \{1, -1, i, -i\}$. Dieser Ring ist mit $N(a) := \vert a \vert^2$ ein [[Euklidische Ringe|euklidischer Ring]].
###### Beweisskizze
Die erste Eigenschaft zeigt man mithilfe der allgemeinen Eigenschaft über den Betrag der komplexen Zahlen und zwar $\vert a\cdot b \vert = \vert a \vert \cdot \vert b \vert$. 

Die zweite ist etwas technischer. Dazu bilde $\frac{b}{a} = q'$ in den komplexen Zahlen und bestimme $s, t\in \mathbb{Z}$ mit $\vert s - Re(q')\vert, \vert t - Im(q')\vert \leq \frac{1}{2}$. Für $q := s + t \cdot i$ gilt dann für $r := b - qa = b-qa + q'a -q'a = (q'-q)a$ sich in der Norm als $< N(a)$ abschätzen lässt.

### Polynomringe
Es gilt jeder [[Polynomringe|Polynomring]] $R[X]$ eines kommutativen Rings $R$ ist wieder ein kommutativer Ring. Wenn $R$ ein Integritätsbereich ist, vererbt sich das.

### Analysis 
#### stetige Funktionen
Es gilt $\mathcal{C}(\mathbb{R})$ der Ring der stetigen Funktionen mit punktweiser Addition und Multiplikation ist ein Ring. 