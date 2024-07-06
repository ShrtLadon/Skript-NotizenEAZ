Wir bezeichen einen [[Kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereich $R$]] als **Hauptidealring**, falls jedes [[Ideale|Ideal]] ein [[Ideale#Hauptideale|Hauptideal]] ist.


### Eigenschaften
##### Aufsteigende Ketten von Idealen
Sei $\mathcal{A}\neq \varnothing$ eine Menge von Idealen in $R$. Dann existiert ein $I\in \mathcal{A}$, so dass jedes $J\in A$ mit $I \subset J$ gleich $I$ ist. 

In anderen Worten existiert in $R$ keine unendlichen echt aufsteigenden Ketten von Idealen $$I_{1}\subsetneq I_{2}\subsetneq...$$
###### Beweisidee
Nehme Gegenteil an und bilde Vereinigung einer solchen Kette $J=\bigcup_{j=1}^{\infty}I_{j}$. Das ist wieder ein Ideal und weil $R$ Hauptidealring, ist $J = (a)$. Das heißt aber auch, dass $a \in I_{n}$ für ein $n$, also $J = I_{n}$, also ein Widerspruch.


#### Euklidische Ringe
Es gilt jeder [[Euklidische Ringe|Euklidischer Ring]] ist ein Hauptidealring
##### Beweisskizze
Wähle minimales $N(a)\in I$ und zeige für $b\in I$ dass Teilen mit Rest, Rest 0 haben muss mithilfe eines Widerspruchs. 
#### Größten Gemeinsamen Teiler
Finde für $a,b$ das ein $d$ mit $(d) = (a,b)$. Dann ist $d$ der [[Kommutative Ringe#Nullteiler und Integritätsbereiche|größte gemeinsame Teiler]] und es gibt $r,s \in R$ mit $d = r\cdot a + s \cdot b$. 
##### Begründung
$a,b\in (d)\implies d\mid a, d\mid b$. Da aber jedes $d'$ mit $d' \mid a,b$  auch $d = ra+sb$ teilt und wir wegen $d \in (a,b)$ es als Linearkombination darstellen können folgt die Aussage.

#### Faktorielle Ringe
Es gilt jeder Hauptidealring ist ein [[Kommutative Ringe#faktorielle Ringe|faktorieller Ring]]. 

##### Beweisidee:
z.Z. das jedes [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzible]] Element auch prim ist, funktioniert wie bei [[Euklidische Ringe#Beweis das Euklidische Ringe faktoriell sind|Euklidischen Ringen]], da wir in Hauptidealringen die gleiche Eigenschaft wegen Abschnitt: [[#Größten Gemeinsamen Teiler]] haben.

z.Z. jedes $a \in R \setminus \{0\}$ ist Produkt $a\cdot p_{1}\cdot ... \cdot p_{k}$ mit $e$ Einheit und $p_{i}$ irreduzibel $(*)$

Betrachte $G := \{a\in R \setminus \{0\}: a \text{ erfüllt } (*)\}$ und $S := (R \setminus \{0\})\setminus G$ und die Menge an Idealen $\mathcal{A}:= \{a\cdot R, a \in S\}$.
Annahme: $S \neq \varnothing \implies S \neq \varnothing$
Dann existiert ein $(a)\in R$ wie in [[#Aufsteigende Ketten von Idealen]]. 

Fall: $a$ ist irreduzibel oder Einheit, dann ist $a=a$ Zerlegung wie in $(*)\implies a \in G↯$ 
	
Fall: $a$ nicht irreduzibel und keine Einheit. Dann existieren $b,c\in R$:  $a=b\cdot c$, keine Einheiten und nicht zu $a$ assoziiert. Dann ist aber $(b),(c) \supsetneq (a)$ und dementsprechend nach Wahl von $a$ $\implies$ $b,c\in G$ liefert also als Produkt aber eine Zerlegung von $a$ ↯