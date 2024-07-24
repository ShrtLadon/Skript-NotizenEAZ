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

Die letzte Bemerkung folgt dadurch, dass [[Gruppen#Ordnung#Eigenschaften|$\lvert A\rvert\cdot x=0$]].  

### Bild und Kern unter Multiplikation
Sei $A$ eine abelsche Gruppe und $n=m_{1}\cdot m_{2}$ mit $m_{1},m_{2}$ [[Kommutative Ringe#Teilerfremde Elemente|teilerfremd]]. Sei $n\cdot\equiv 0$ (z.B. wenn $n= k\cdot \lvert N\rvert$. Definiere für $i\in\set{1,2}$ $$A_{i}:=\ker(m_{i}\cdot)$$Dann gilt für $i\neq j \in \set{1,2}:$
1) $m_{j}:A_{i}\mapsto A_{i}$ ist ein [[Gruppenhomomorphismen|Isomorphismus]].
2) $\text{Bild} (m_{i}\cdot)=A_{j}$.
3) $A_{i}\cap A_{j}=\set{0}$
4) $A\cong A_{i} \times A_{j}$ (mit der natürlichen Verknüpfung wie auf ÜB8.1)
###### Beweis
Da $\mathbb{Z}$ [[Euklidische Ringe|euklidscher Ring]] ist, existieren $k_{1},k_{2}\in \mathbb{Z}$, sodass $k_{1}\cdot m_{1}+ k_{2}\cdot m_{2} =1$. Insbesondere gilt also für alle $a\in A$ wegen der Distributivität$$k_{1}\cdot m_1\cdot x+k_{2}\cdot m_{2} \cdot x=x \qquad(*)$$
1) Sei $x\in A_{i}$. Dann ist $k_{i}\cdot m_{i}\cdot x = k_{i}\cdot 0 = 0$, also $k_{j}\cdot m_{j}\cdot x =x \in A_{i}$. Dann ist insbesondere $k_{j}\cdot$ die Umkehrabbildung von $m_{j}\cdot$ und als Einschränkung $m_{j}\cdot$ immer noch ein Homomorphismus, also insgesamt $m_{j}:A_{i} \rightarrow A_i$ ein Isomorphismus (Wir benutzen hier auch, dass Multiplikation in $\mathbb{Z}$ kommutativ ist, um eine Rechts und Linksinverse zu erhalten)
2) $A_{j}\subseteq \text{Bild }(m_{i}\cdot)$ folgt aus 1). Sei $y\in \text{Bild}(m_{i}\cdot)$. Dann existiert ein $x \in A$, sodass $m_{i}\cdot x = y$. Insbesondere gilt $m_{j} \cdot y = m_{j}\cdot m_{i} \cdot x = n\cdot x =0$. Also ist $y\in A_{j}$.
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
## endliche abelsche Gruppen
Sei $A$ eine endliche abelsche Gruppe. Dann ist $A$ [[Gruppenhomomorphismen|isomorph]] zu $$A\cong A_{1}\times A_{2} \times ... \times A_{k}$$wobei $A_{i}=\mathbb{Z}/p_{i}^{a_{i}} \mathbb{Z}$, für [[Primzahlen]] $p_{i}$ und $a_{i}\geq 1$. Insbesondere ist $p_{i}=p_{j}$ möglich.
Die Zerlegung ist bis auf Vertauschung eindeutig.
### Beweis
#### Existenz
Die Existenz folgt direkt aus Kombination der folgenden Lemmata.
##### A ist Produkt von p-Sylow Untergruppen
Sei $\lvert n\rvert=A=p_{1}^{a_{1}}\cdot...\cdot p_{k}^{a_{k}}$, wobei die $p_{i}$ [[Kommutative Ringe|teilerfremd]], $a_{i}\geq 1$ und wir $n$ in seine [[Kommutative Ringe#Primfaktoren|Primfaktoren]] zerlegen. Dann gilt $$A\cong A_{1}\times...\times A_{k}$$wobei $A_{i}=\ker(p_{i}^{a_{i}}\cdot)$ die eindeutige [[Sylow-Sätze|$p_{i}-$Sylow Untergruppe]] ist.
###### Beweis
Zu Beginn ist klar, dass die $p$-Sylow Untergruppen eindeutig sind, weil abelsche Untergruppen ein [[Normalteiler#Äquivalente Formulierungen|Normalteiler]] sind und damit [[Sylow-Sätze#Weitere Eigenschaften von $n_{p}$|eindeutig]].

Außerdem bemerken wir als zusätzliche Eigenschaft in [[#Bild und Kern unter Multiplikation]], dass für $m_{1}\cdot m_{2}=n=\lvert A\rvert$, mit $m_{1},m_{2}$ teilerfremd gilt:
$\ker(m_{i}\cdot)$ enthält genau alle Elemente, die eine [[Gruppen#Ordnung|Ordnung]] haben, die $m_i$ teilt, wegen einer [[Gruppen#Ordnung#Eigenschaften|Eigenschaft]] der Ordnung. Würde $\lvert \ker(m_{i}\cdot)\rvert$ einen Primfaktor von $m_{j}$ enthalten, würde nach [[Gruppen#Theorem von Cauchy|Theorem von Cauchy]] aber ein Element in $A_{i}$ existieren, was $m_{i}$ nicht teilt. Weil aber $\lvert \ker(m_{1}\cdot)\rvert \cdot \lvert\ker(m_{2}\cdot)\rvert=\lvert A\rvert$ gilt, muss also $\lvert \ker(m_{i} \cdot)\rvert=m_{i}$ sein.

Damit folgt aber induktiv die Behauptung des Satzes, weil $A_{i}$ wirklich genau die p-Sylow Untergruppen sind.

##### Anzahl der Untergruppen der Ordnung $p$.
Es gilt eine endliche abelsche Gruppe $A$ mit $\lvert A\rvert=p^{a}$ und $a\geq 1$ hat nur eine [[Gruppen#Untergruppen|Untergruppe]] $T$ der [[Gruppen#Ordnung|Ordnung]] $p$ genau dann, wenn $A$ [[Gruppen#Zyklische Gruppen|zyklisch]] ist.
###### Beweis
"$\Leftarrow$"
Dann gilt $A\cong \mathbb{Z}/p^{a} \mathbb{Z}$. Dann sind die Elemente der Ordnung $\leq p$ die, für die gilt $p\cdot \bar x = 0$ also für die $p^{a} \mid p\cdot x$. Das sind genau die Elemente$$\set{\overline {p^{a-1}},\overline {2\cdot p^{a-1}},...,\overline {p^{a}}=0}$$Das sind $p$-Elemente, die zusammen genau eine Untergruppe bilden, wie man direkt sieht.

"$\Rightarrow$"
Führe Induktion nach $a$ 
*Induktionsanfang:* $a=1$. Dann ist $A$ immer [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]].
*Induktionsschluss:* 
Sei $a\geq 2$ und die Aussage für $a-1$ richtig. Sei $T< A$ die einzige Untergruppe mit Ordnung $p$. Dann gilt $\ker (p\cdot)=T$, denn $\ker(p\cdot)$ enthält genau die Elemente deren Ordnung $p$ teilt.

Außerdem [[Gruppenhomomorphismen#Eigenschaften|gilt]] $B:= \text{Bild} (p\cdot)<A$ und wegen [[Faktorgruppen#Isomorphiesatz|Isomorphiesatz]] ist $\lvert B\rvert=\lvert A/T\rvert= \frac {\lvert A\rvert}{\lvert T\rvert}=p^{a-1}$. Weil $B$ eine Untergruppe ist und alle ihre Untergruppen auch Untergruppen von $A$ sind, hat $B$ höchstens eine Untergruppe der Ordnung $p$ und wegen [[Gruppen#Theorem von Cauchy|Theorem von Cauchy]] auch genau eine. Dann gilt wegen Induktionsvoraussetzung $B$ ist zyklisch und damit existiert ein $y\in B$ mit $\text{ord}(y)=p^{a-1}$. 
Da aber $B=\text{Bild}(p\cdot)$ ist, existiert ein $x\in A$ mit $$p\cdot x=y$$Damit hat $x$ Ordnung $p^a$ und $A$ ist zyklisch.

##### Zerlegung in Produkt von Untergruppen
Sei $\lvert A\rvert=p^{a}$ eine abelsche Gruppe mit $a\geq 1$ und $x\in A$ ein Element mit maximaler [[Gruppen#Ordnung|Ordnung]] $p^{r}$. Sei außerdem [[Gruppen#Erzeugnis|$C=\langle x\rangle$]]. Dann existiert eine Untergruppe $B<A$, sodass $B\cap C=\set 0$ und $A= B\times C$.

Anmerkung: Hier meinen wir mit dem "$=$" statt "$\cong$" den natürlichen Homomorphismus$$\Phi:B\times C\rightarrow A, (b,c)\mapsto b+c$$ 
###### Beweis
Führe Induktion nach $a$.
*Induktionsanfang* $a=1$. Dann ist $A$ [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] also $\text{ord}(x)=p$. Mit Wahl von $B=\set 0$ folgt die Behauptung direkt

*Induktionsschluss*
Sei $a\geq 2$ und die Aussage wahr für $a-1$. 
*Fall* $A$ zyklisch. Dann ist $A= C\times \set 0$.

*Fall* $A$ nicht zyklisch:
Da $C$ zyklisch ist, enthält $C$ nach obigem [[#Anzahl der Untergruppen der Ordnung $p$.|Lemma]] nur eine Untergruppe der Ordnung $p$, aber $A$ mindestens 2. Da [[Gruppen#Zyklische Gruppen#Eigenschaften|jedes]] Element außer $0$ in einer Untergruppe der Ordnung $p$ selbst die Ordnung $p$ hat, existiert ein $T<A$ mit $\lvert T\rvert=p$ und $T\cap C =\set 0$ (Wäre ein nicht-triviales Element im Schnitt, wäre es in der einzigen Untergruppe der Ordnung $p$ in $C$).

Außerdem ist $T$ - weil $A$ abelsch ist - [[Normalteiler#Äquivalente Formulierungen|normal]]. Betrachte also [[Faktorgruppen|$A':=A/T$]]. Dann hat $A'$ nach [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] die Ordnung $p^{a-1}$. Es gilt $\forall a\in A$, dass $\text{ord}(a)\cdot(aT)=0T$ also $\text{ord}(a)\geq \text{ord}(aT)$. 
Betrachte den [[Gruppenhomomorphismen|Gruppenhomomorphismus]]$$\pi:A \rightarrow A', a\mapsto aT$$Dann gilt außerdem $\text{ord}(\pi(x))=\text{ord}(x)$. Denn wenn $k:=\text{ord}(\pi(x))<\text{ord}(x)$ wäre, so wäre $\pi(k\cdot x)=0T$, also $k\cdot x\in \ker \pi=T$, aber $0\neq k\cdot x\in C$. 
Insgesamt erhalten wir so, dass $\pi (x)$ die maximale Ordnung in $A'$ hat.
Sei also $C':=\langle \pi(x)\rangle = \pi(C)$.

Dann existiert aber nach Induktionsvoraussetzung ein $B'<T$ mit $C'\times B = A'$ und $B'\cap C' = \set 0$.
Wähle also $B:= \pi^{-1}(B)$. Sei $a\in B\cap C$. Dann gilt $\pi(a)\in B'\cap C'$ also $a\in T$ und damit $a=0$. Außerdem gilt wegen [[Faktorgruppen#Isomorphiesatz|Isomorphiesatz]] und [[Gruppenwirkung#Satz von Lagrange|Lagrange]], dass $\frac {\lvert \pi^{-1}(B')\rvert}{\lvert T\rvert}=\lvert \pi(\pi^{-1}(B'))\rvert=\lvert B'\rvert$. Da gilt $\lvert A'\rvert=\lvert B'\times C'\rvert=\lvert B'\rvert\cdot \lvert C'\rvert$ und $\lvert C'\rvert=\text{ord}(x)= \lvert C\rvert$ erhalten wir so$$\lvert A\rvert=\lvert A'\rvert\cdot \lvert T\rvert=\lvert B\rvert\cdot \lvert C\rvert$$Damit folgt die Behauptung mit ÜB8.1

#### Eindeutigkeit
TODO. Wurde in der VL (noch?) nicht behandelt, ist aber in hochgeladenen Vorlesungsnotizen zu VL 20

## Klassifikation endlich erzeugter abelscher Gruppen
Sei $A$ eine [[#endlich erzeugte abelsche Gruppen|endlich erzeugte abelsche Gruppe]]. Dann ist $A$ isomorph zu $$A\cong \mathbb{Z}/p_{1}^{a_{1}}\mathbb{Z}\times... \times \mathbb{Z}p_{k}^{a_{k}}\times \underbrace{\mathbb{Z}\times ...\times \mathbb{Z}}_l$$also das Produkt zyklischer Gruppen. Außerdem sind die Faktoren bis auf Vertauschung bestimmt.