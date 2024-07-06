Wir nennen eine [[Gruppen|Gruppe]] $(A,+)$ **abelsch** bzw. **kommutativ**, wenn 
- $\forall a,b \in A: a\cdot b=b\cdot a$ 

> [!Note] Notation
> In abelschen Gruppen bezeichnet man das neutrale Element oft als $0$ statt wie in allgemeinen Gruppen als $1$ oder $0$. Außerdem verwenden wir als Verknüpfung oft $+$, statt $\cdot$ und schreiben $x^{n}$ als $n\cdot x$. 


## Multiplikation
Wir bezeichnen für $n\in \mathbb{N}_{0}, x\in A$ die Potenzierung als $$n\cdot x:=x^{n}=\underbrace{x+...+x}_{n\text{ mal}}$$und $$(-n)\cdot x := -(n\cdot x)$$
Es gilt:
- $(n\cdot m) \cdot x = n\cdot (m \cdot x)$
- $n\cdot(x+y)=(n\cdot x) + (n\cdot y)$
- $(n+m)\cdot x = (n\cdot x)+(m\cdot x)$
Im Nachfolgenden verwenden wir "Punkt-vor-Strich". Aufgrund der zweiten Eigenschaft definieren wir für $n\in \mathbb{Z}$ einen [[Gruppenhomomorphismen|Gruppenhomomorphismus]]: $$n\cdot:A \rightarrow A,x\mapsto n\cdot x$$Es gilt ist $\lvert A\rvert<\infty$ ein [[Kommutative Ringe#Teiler|Teiler]] von $n$, dann gilt $n\cdot \equiv 0$. 
###### Beweis / Bemerkung
Die erste und letzte Eigenschaft gilt auch in allgemeinen [[Gruppen]] $(G,\cdot)$, denn$$\begin{align}(x^{n})^{m}=x^{nm}\\x^{n+m}=x^{m}\cdot x^{m}\end{align}$$für alle $g\in G$ und $n,m\in \mathbb{Z}$.
Für die zweite Eigenschaft brauchen wir die Kommutativität der Verknüpfung (das ist tatsächlich notwendig wie ÜB10.4 zeigt).
Dann gilt $n\cdot(x+y)=\underbrace{(x+y) +... + (x+y)}_{n \text{ mal}}\overset{\text{abelsch}}=\underbrace{x+...+x}_{n\text{ mal}}+ \underbrace{y+...+y}_{n \text{ mal}} = n\cdot x + n\cdot y$.

Die letzte Bemerkung folgt dadurch, dass in [[Gruppen#Ordnung#Eigenschaften|$\lvert A\rvert\cdot x=0$]].  

### Bild und Kern unter Multiplikation
Sei $A$ eine abelsche Gruppe und $n=m_{1}\cdot m_{2}$ mit $m_{1},m_{2}$ [[Kommutative Ringe#Teilerfremde Elemente|teilerfremd]]. Sei $n\cdot\equiv 0$ (z.B. wenn $n= k\cdot \lvert N\rvert$. Definiere für $i\in\set{1,2}$ $$A_{i}:=\ker(m_{i}\cdot)$$Dann gilt für $i\neq j \in \set{1,2}:$
1) $m_{j}:A_{i}\mapsto A_{i}$ ist ein [[Gruppenhomomorphismen|Isomorphismus]].
2) $\text{Bild} (m_{i}\cdot)=A_{j}$.
3) $A_{i}\cap A_{j}=\set{0}$
4) $A\cong A_{i} \times A_{j}$ (mit der natürlichen Verknüpfung wie auf ÜB8.1)
###### Beweis
Da $\mathbb{Z}$ [[Euklidische Ringe|euklidscher Ring]] ist, existieren $k_{1},k_{2}\in \mathbb{Z}$, sodass $k_{1}\cdot m_{1}+ k_{2}\cdot m_{2} =1$. Insbesondere gilt also für alle $a\in A$ wegen der Distributivität$$k_{1}\cdot m_1\cdot x+k_{2}\cdot m_{2} \cdot x=x \qquad(*)$$
1) Sei $x\in A_{i}$. Dann ist $k_{i}\cdot m_{i}\cdot x = k_{i}\cdot 0 = 0$, also $k_{j}\cdot m_{j}\cdot x =x \in A_{i}$. Dann ist insbesondere $k_{j}\cdot$ die Umkehrabbildung von $m_{j}\cdot$ und als Einschränkung $m_{j}\cdot$ immer noch ein Homomorphismus, also insgesamt $m_{j}:A_{i} \rightarrow A_i$ ein Isomorphismus (Wir benutzen hier auch, dass Multiplikation in $\mathbb{Z}$ kommutativ ist, um eine Rechts und Linksinverse zu erhalten)
2) $A_{j}\subseteq \text{Bild }(m_{i}\cdot)$ folgt aus 1). Sei $y\in$
3) Es gilt $x\in A_{i}\cap A_{j}$ impliziert mit $(*)$, dass $x=0+0=0$. 
4) Betrachte $\Phi:A_{1}\times A_{2} \rightarrow A, (x_{1},x_{2})\mapsto x_{1}+x_{2}$:
	Es gilt zunächst durch leichtes Nachrechnen $\Phi$ ist ein Gruppenhomomorphismus.
	Dann gilt $\ker \Phi = \set{(x_{1}, x_{2})\in A_{1}\times A_{2} \mid x_{1}+x_{2}=0}$ also $(x_{1},x_{2})\in \ker \Phi\iff x_{1}=-x_{2}$. Dann gilt aber insbesondere (da $A_{1},A_{2}$ [[Gruppen#Untergruppen|Untergruppen]] als [[Gruppenhomomorphismen|Kern]] sind), dass $x_{1}\in A_{1}\cap A_{2}$ also $x_{1}=0$ und damit $x_{2}=0$. Daraus folgt dass $\Phi$ [[Gruppenhomomorphismen#Eigenschaften|injektiv]] ist.
	Sei nun $x\in A$. Dann gilt mit $(*)$ $k_{1}\cdot m_1\cdot x+k_{2}\cdot m_{2} \cdot x=x$. Da $n\cdot \equiv 0$ ist, gilt insbesondere $m_{2}\cdot k_{1} \cdot m_{1}=(k_{1}\cdot n)\cdot x=0$, also $k_{1}\cdot m_{1}\cdot x \in A_{2}$ und analog $k_{2}\cdot m_{2}\cdot x \in A_{1}$. Damit folgt $x\in \text{Bild }\Phi$ und $\Phi$ surjektiv.


## endlich erzeugte abelsche Gruppen
Eine abelsche Gruppe $A$ heißt **endlich erzeugt**, wenn $x_{1},...,x_{n}\in A$ existieren, sodass $\set {x_{1},...,x_{n}}$ $A$ [[Gruppen#Erzeugnis|erzeugt]]. Bei abelschen Gruppen ist das genau dann der Fall, wenn gilt $$\forall a\in A:\exists k_{1},...,k_{n}\in \mathbb{Z}:a=\sum\limits_{i=0}^{n}n_{i}\cdot x_{i}$$
Das ist eine Verallgemeinerung von Erzeugendensystemen aus der linearen Algebra. $\mathbb{Z}^{m}$ wird z.B. von $e_{1}=(1,0,...,0), ..., e_{m}=(0,...0,1)$ erzeugt.
###### Beweis
Jede Untergruppe, die $x_1,...,x_{n}$ enthält muss die obenstehenden Linearkombinationen enthalten. Da wir in einer abelschen Gruppe sind, sind diese auch selbst eine Untergruppe.
# Klassifikation abelscher Gruppen
#### endliche abelsche Gruppen
Sei $A$ eine endliche abelsche Gruppe. Dann ist $A$ [[Gruppenhomomorphismen|isomorph]] zu $$A\cong A_{1}\times A_{2} \times ... \times A_{k}$$wobei $A_{i}=\mathbb{Z}/p_{i}^{a_{i}} \mathbb{Z}$, für [[Primzahlen]] $p_{i}$ und $a_{i}\geq 1$. Insbesondere ist $p_{i}=p_{j}$ möglich.

### Beweis
#### A Produkt von p-Sylow Untergrupprn
Sei $\lvert n\rvert=A=p_{1}^{a_{1}}\cdot...\cdot p_{k}^{a_{k}}$, wobei die $p_{i}$ [[Kommutative Ringe|teilerfremd]], $a_{i}\geq 1$ und wir $n$ in seine [[Kommutative Ringe#Primfaktoren|Primfaktoren]] zerlegen. Dann gilt $$A\cong A_{1}\times...\times A_{k}$$wobei $A_{i}=\ker(p_{i}^{a_{i}}\cdot)$ die eindeutige [[Sylow-Sätze|$p_{i}-$Sylow Untergruppe]] ist.
###### Beweis
Führe Induktion nach $k$. 
*Induktionsanfang:* $k=1$ ist klar.
*Induktionsschluss*: 
TODO