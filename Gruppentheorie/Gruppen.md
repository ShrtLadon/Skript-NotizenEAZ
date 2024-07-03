Eine **Gruppe** $(G,\cdot)$ ist eine Menge $G$ mit einer Verknüpfung $\cdot:G \times G \rightarrow G$ mit 
- (G1) $\forall a,b, c \in G : (a\cdot b)\cdot c = a \cdot (b\cdot c)$ *Assoziativ*
- (G2) $\exists e \in G : \forall a \in G : a\cdot e=a$ *Existenz eines neutralen Elements*
- (G3) $\forall a \in G \exists b \in G: a \cdot b = e$, wobei $e$ neutrales Element sei. *Existenz eines Inversen*

Wir nennen eine Gruppe **abelsch** bzw. **kommutativ**, wenn 
- $\forall a,b \in G: a\cdot b=b\cdot a$ 

> [!Note] neutrales Element
> In abelschen Gruppen bezeichnet man das neutrale Element oft als $0$ in allgemeinen Gruppen als $1$. In der Vorlesung wurden sowohl $1$ als auch $e$ verwendet, was hier ebenso getan wurde, damit in der Klausur beide Notationen geläufig sind.

#### Eigenschaften
- Für $a,b \in G$ mit $a\cdot b=e$ gilt $b\cdot a=e$
- Für alle $a \in G$ gilt $e\cdot a =a$ 
- Wenn für $a,b,b' \in G$ schon $a\cdot b=a\cdot b'=e$ gilt, so gilt auch $b'=b$ 
- Sei $e' \in G$, sodass für ein $a\in G$ gilt, dass $a\cdot e'=a$, dann gilt auch $e=e'$ 

Insbesondere sind Inverse und neutrales Element eindeutig. Wir nennen also $b=a^{-1}$. Außerdem ist $(a^{-1})^{-1}=a$ 
###### Beweis
- Es ex. wegen (G3) $c \in G$ mit $b*c = e$. Dann gilt $b\cdot a=b\cdot a\cdot e =b\cdot (a\cdot b)\cdot c=b\cdot e\cdot c=b\cdot c=e$ 
- Wegen erster Eigenschaft gilt $e\cdot a=a\cdot b\cdot a=a\cdot e=a$, wobei $b$ Element aus (G3)
- Es gilt dann auch $b\cdot a\cdot b=b\cdot a\cdot b'\overset{1}=e\cdot b=e\cdot b'\overset{2}=b=b'$ 
- Es ex. wegen (G3) ein $b$ s.d. $b\cdot a\cdot e'=b\cdot a\implies e\cdot e'=e \implies e'=e$. 

## Untergruppen
Eine Teilmenge $H \subseteq G$ heißt **Untergruppe** bzgl. $G$ gdw. die Einschränkung der Verknüpfung $\cdot\vert_{H\times H}^{H}$ eine Verknüpfung (also wohldefiniert) ist und $H$ eine Gruppe ist, also genau
- $\forall a,b \in H : a\cdot b\in H$
- $\forall a \in H:  a^{-1} \in H$
- $e_{G}\in H$ 

#### Untergruppenkriterium
Es gilt eine Teilmenge $\varnothing \neq H \subseteq G$  ist eine Untergruppe genau dann wenn:$$\forall a,b \in H: a\cdot b^{-1}\in H$$
###### Beweis
"$\Rightarrow$" klar. 
"$\Leftarrow$" Sei $a \in H\neq \varnothing$. Dann ist $a\cdot a^{-1}=e_{G}\in H$. Dann ist aber auch $e\cdot a^{-1}=a^{-1}\in H$. Sei außerdem noch $b \in H$. Dann ist also $b^{-1} \in H$, dann gilt aber auch $a\cdot (b^{-1})^{-1}=a\cdot b\in H$ also ist $H$ Untergruppe bzgl. $G$ und wir schreiben $H \leq G$.

### Erzeugnis
Sei $M \subseteq G$. Dann ist das **Erzeugnis** von $M$ definiert als $$\langle M\rangle:=\bigcap_{M\subseteq U \leq G}U$$das ist die kleinste Untergruppe von $G$ die auch $M$ enthält. In der Übung wurde das definiert als $\langle M \rangle := \set{g_1\cdot...\cdot g_{k} \mid g_{i}\in M \lor g_{i}^{-1}\in M}$ 

## Zyklische Gruppen
Es gilt eine Gruppe $G$ heißt **zyklisch**, falls ein Element $a \in G$ existiert, sodass für jedes $g \in G$ ein $k \in \mathbb{Z}$ existiert mit $g=a^{k}$ also $\langle a\rangle = G$. Dann heißt $a$ *Erzeuger*. 
### Ordnung
Für $x \in G$ ist $\text{ord}(x):= \min\set{n \in \mathbb{N}_{>0}:g^{n}=e}$. Außerdem definieren wir die **Ordnung** von $G$ als $\lvert G\rvert$.

#### Eigenschaften
Sei $G$ endlich.
- Für $g \in G$ gilt $\text{ord}(g) \mid \lvert G\rvert$. Die [[Gruppen#Ordnung|Ordnung]] teilt $\lvert G\rvert$. 
- Für $g \in G$ ist $g^{\lvert G\rvert} =e$ 
- Wenn $\lvert G\rvert$ [[Primzahlen|prim]], dann ist $G$ zyklisch und wird von jedem Element in $G \setminus \set {e_{G}}$ erzeugt.
- Wenn $g^{k}=e$ für ein $k\in \mathbb{N}_{>0}$. Dann gilt $\text{ord}(g)\mid k$ 
	-> haben wir in VL verwendet, aber nicht bewiesen.
###### Beweis
- folgt direkt mit [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]].
- Es gilt $g^{\text{ord}(g)}=e_{G}$. Weil $\text{ord}(g)$ aber $\lvert G\rvert$ teilt, folgt die Behauptung
- Es gilt wegen Lagrange, dass das [[Gruppen#Erzeugnis|Erzeugnis]] $\langle g\rangle$ eine Untergruppe ist und $\text{ord}(g)\mid \lvert G\rvert$. Da aber $\lvert G\rvert$ prim ist, muss $\text{ord}(g)=1$ oder $\lvert G\rvert$ sein. Aber $\lvert \langle g \rangle\rvert =1 \iff g = e_{G}$. Also muss das Erzeugnis $\langle g \rangle = G$ sein für $g \neq  e_{G}$. Das sagt aber genau, dass $G$ zyklisch ist.
- Annahme: $\text{ord}(g) \not \mid p$. Dann [[Euklidische Ringe|existieren]] $a \in \mathbb{N}, r\in \mathbb{N}_{>0}$ mit $r<\text{ord}(g)$. Dann ist aber $$e=g^{p}=(g^{\text{ord}(g)})^{a}\cdot g^{r}=e^{a}\cdot g^{r}=g^{r}$$also insbesondere $\text{ord}(g)$ nicht minimal. Widerspruch!


#### Theorem von Cauchy
Sei $G$ eine endliche Gruppe, $p$ eine [[kommutative Ringe#Prim- und irreduzible Elemente|Primzahl]] die $\lvert G\rvert$ [[kommutative Ringe#Teiler|teilt]]. Dann existiert ein $g \in G$ mit $$\text{ord}(g)=p$$
##### Beweis
Betrachte $Y:=G^{p}=\set{(g_{1},...,g_{p}) : g_{1},...,g_{p} \in G}$. Es gilt $\lvert Y\rvert = \lvert G\rvert^{p}$ und die Teilmenge $$X:= \set{(g_{1},...,g_{p})\in Y:g_{1}\cdot ... \cdot g_p=e_{G}}$$Da wir die ersten $p-1$ Elemente frei wählen können und das letzte durch das Inverse des Produktes [[#Eigenschaften|eindeutig]] festgelegt ist, ist $\lvert X\rvert =\lvert G\rvert^{p-1}$. 

Wir wollen uns wenn möglich (fast) nur mit den Elementen befassen, für die gilt $g_{1}=...g_{p}$ und dann Aussagen von [[Gruppenwirkung]] über Kardinalititäten nutzen. Dazu definieren wir die Gruppe $$H:=\set{1, \xi,...,\xi^{p-1}}\cong \mathbb{Z}_{p}\cong \mathbb{Z}/p \mathbb{Z}$$mit $\xi= e^{\frac{2 \pi i}{p}}$ und der Multiplikation als Verknüpfung. Darauf betrachten wir die [[Gruppenwirkung]] $*:H \times X \rightarrow X, \xi^{i} * (g_{1},...,g_{p}):=(g_{i},...,g_{p},g_{1},...,g_{i-1})$ also eine Rotation der Elemente.
Insbesondere ist das wohldefiniert, weil $g_{1}\cdot ... \cdot g_{p} = e$ $\implies$ $(g_{i}\cdot ... \cdot g_{p}) \cdot (g_{1},...,g_{i-1})=e$ 

Wegen der [[Gruppenwirkung#Bahnenformel|Bahnenformel]] gilt nun$$p=\lvert H\rvert = \lvert H \cdot x\rvert \cdot \lvert H_{x}\rvert$$für alle $x \in X$. Insbesondere gilt also, weil $p$ prim, dass $\lvert H\cdot x\rvert \in \set{1,p}$ also dass die [[Gruppenwirkung#Bahn und Stabilisator|Bahnen]] Länge 1 oder p haben.

Es gilt $\lvert G\rvert^{p-1} =\lvert X\rvert = 1 \cdot \#(\text{Bahnen der Länge 1}) + p \cdot \#(\text{Bahnen der Länge p})$wobei wir hier nutzen, dass Bahnen $X$ [[Gruppenwirkung#Bahn und Stabilisator#Eigenschaften|partitionieren]]. Wir müssen dazu auf der rechten Seite noch mit $p$ multiplizieren, weil in den Bahnen der Länge $p$ genau $p$ Elemente enthalten sind.

Da $p$ teilt $\lvert G\rvert$ gilt, teilt $p$ auch $\lvert G\rvert^{p-1}$ ($p-1 \geq 1$). Dann folgt aber weil $p$ die rechte Seite der Summe teilt, dass $p$ auch $\# (\text{Bahnen der Länge 1})$ teilt.

Weiter unten wird gezeigt, dass $\#(\text{Bahnen der Länge 1})=\#(\text{Anzahl der Elemente von Ordnung p}) +1\geq 1$.  Insbesondere muss also wenn $p$ das teilt $\#(\text{Bahnen der Länge 1})\geq p$ sein also $\#(\text{Anzahl der Elemente von Ordnung p}) \geq p-1 > 0$, was die Behauptung zeigt.
###### Bahnen der Länge 1
Sei $x:=(g_{1},...,g_{p})\in X$ in einer Bahn der Länge 1. Dann gilt $$\begin{aligned}\xi^{0}*(g_{1},...,g_{p})=(g_{1},...,g_{p})\quad\\=\xi^{1}*(g_{1},...,g_{p})=(g_{2},...,g_p,g_{1})\\\vdots\qquad\qquad\qquad\qquad\\=\xi^{p-1}*(g_{1},...,g_{p})=(g_{p},g_{1},...,g_{p-1})\end{aligned}$$damit ist aber $g_{1}=...=g_{p}$. Umgekehrt gilt auch, dass für $g_{1}=...=g_{p}$ gilt dass $\lvert H \cdot x\rvert =1$. 

D.h. für $(g_{1},...,g_{p})\in X$ gilt $\lvert H\cdot x\rvert =1 \iff g_{1}=...=g_{p}$. 

In diesem Fall sei $g:= g_{1}=...=g_{p}$. Dann gilt $g^{p}=e$. Es [[#Ordnung#Eigenschaften|gilt]] $\text{ord}(g) \mid p$ also da $p$ prim ist, $\text{ord}(g) \in \set{1,p}$. 

Es gilt $\text{ord}(g)=1 \iff g=e$ also ist $\#(\text{Bahnen der Länge 1})=\#(\text{Anzahl der Elemente von Ordnung p}) + 1$

### Beispiele
Insbesondere ist jeder [[kommutative Ringe|Ring]] eine Gruppe mit der Addition, also sind z.B.
- $(\mathbb{Z}, +), (\mathbb{Q}, +), (\mathbb{R}, +), (\mathbb{C}, +)$ Gruppen
- $(\mathbb{Z}/n \mathbb{Z}, +_{n})$ bzw. $\mathbb{Z}_{n}=({0,...,n-1}, +_{n})$ sind Gruppen (beim Zweiten wird direkt Wahl von Repräsentant getroffen)

Wenn man sich in einem [[kommutative Ringe|Ring]] auf die Einheiten einschränkt erhält man eine Gruppe bzgl. der Multiplikation also z.B. $(\mathbb{R}\setminus \set {0},\cdot)$ oder auch $GL_{n}(\mathbb{R})=(\set{A\in \mathbb{R}^{N\times N} : \det{A}\neq 0},\cdot)$.

Man kann davon auch [[#Untergruppen]] betrachten wie z.B. $(\mathbb{R}_{>0},\cdot)$ und $SL_{n}(\mathbb{R})=(\set{A \in \mathbb{R}^{N\times N} : \det{A}=1},\cdot)$ 

#### Untergruppen von $(\mathbb{Z},+)$ 
Es gilt die Untergruppen von $(\mathbb{Z},+)$ sind genau durch $(n \mathbb{Z}, +)$ mit $n \in \mathbb{N}_{0}$, wobei $n \mathbb{Z}$ wie in [[Ideale#Hauptideale|Hauptideale]]. 
###### Beweis
"$\Rightarrow$" klar, weil Ideale abgeschlossen sind. 
"$\Leftarrow$" Sei $S \leq \mathbb{Z}$.
*Fall* $S = \set{0}$. Dann $S=0\cdot \mathbb{Z}$. 
*Fall* $S \neq \set{0}$. Dann gibt es ein kleinstes positives Element $n= \min\set{\lvert x \rvert : x\in S\setminus \set 0}$. Außerdem gilt $n \mathbb{Z}\subseteq S$, denn Multiplikation ist nur iterierte Subtraktion oder Addition.
	*Angenommen* es ex. ein $x \in S \setminus n \mathbb{Z}$. Dann existiert ein $k \in \mathbb{Z}$, sodass $kn<x<(k+1)n$. 
	$\implies$ $0<x-kn<n$ und $x -kn \in S$. Das ist allerdings ein *Widerspruch* zu Minimalität von $n$. 
#### Diedergruppe
Sei $n \geq 3$. Dann ist die Menge der Symmetrien (also [[Bewegungen|Isometrien]], die Ecken auf Ecken abbilden) des regulären $n$-Ecks eine Gruppe $D_{2n}$ bezüglich der Komposition und hat $2n$ Elemente. 
##### Beweis
Es gilt ein n-Eck hat genau die Ecken $1, e^{\frac{2 \pi i \cdot 1}{n}}, e^{\frac{2 \pi i \cdot n-1}{n}}$. Außerdem gilt, dass die Komposition in $D_{2n}$ abgeschlossen ist.

(G1), (G2): folgt, weil Komposition assoziativ ist und $Id_{\mathbb{C}}$ ein neutrales Element.

(G3) und $\#D_{2n}=2n$:
Wir zeigen das, indem wir uns Elemente in der Gruppe anschauen, die die gesamte Gruppe erzeugen:
###### Rotation
- $r:\mathbb{C} \rightarrow \mathbb{C}, r(z)= z\cdot e^{\frac{2 \pi i}{n}}$ 
Das ist eine Rotation um den Winkel $\frac {2\pi}{n}$. Es gilt $r\left(e^{\frac{2 \pi i \cdot k}{n}}\right)= e^{\frac{2 \pi i \cdot (k+1)}{n}}$ wobei für $k=n$, die $2\pi$-Periodizität der $e$-Funktion dafür sorgt, dass $e^{\frac{2 \pi i \cdot n}{n}}=e^0=1$. Außerdem gilt $\lvert r(z)-r(w)\rvert = \lvert (z-w) e^{\frac{2 \pi i}{n}}\rvert=\lvert z-w\rvert$, denn $\lvert e^{\frac{2 \pi i}{n}}\rvert =1$.  Also ist $r$ eine Isometrie. Außerdem gilt $r^{n}=r\circ ... \circ r = Id$, also ist $r$ invertierbar.
<iframe scrolling="no" title="r in der Diedergruppe" src="https://www.geogebra.org/material/iframe/id/q2xnr59x/width/1300/height/800/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="492px" style="border:0px;"> </iframe>
###### Spiegelung
- $s:\mathbb{C} \rightarrow \mathbb{C}, z \mapsto \overline z$
Das ist eine Spiegelung an der x-Achse. Es gilt $\lvert s(z)-s(w)\rvert ^{2}= (\overline z - \overline w) \cdot \overline{(\overline z - \overline w)}=(\overline z - \overline w)\cdot (z-w)=\lvert z-w\rvert^2$, also ist $s$ eine Isometrie. Außerdem gilt $\overline {e^{\frac{2 \pi i \cdot k}{n}}} = e^{-\frac{2 \pi i \cdot k}{n}}\overset{2\pi\text{-periodisch}}=e^{\frac{2n\pi - 2 \pi i \cdot k}{n}}$ also werden Ecken auf Ecken abgebildet und $s$ ist eine Symmetrie des regulären $n$-Ecks. Zusätzlich ist $s^{2}=s\circ s = Id$ also ist $s$ invertierbar.

<iframe scrolling="no" title="s In Diedergruppe" src="https://www.geogebra.org/material/iframe/id/jvh7k7wu/width/1300/height/800/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="492px" style="border:0px;"> </iframe>
##### $D_{2n}$ wird dadurch erzeugt.

###### Vorüberlegung / Lemma
Seien $q,p,u \in \mathbb{C}$ und $q,p,u$ auf keiner Geraden:
Dann gilt, wenn die Abstände $r_{1}, r_{2}, r_{3}$ bekannt:$$\begin{cases}(x-q_{1})^{2}+(y-q_{2})^{2} =r_{1}^{2} \\(x-p_{1})^{2}+(y-p_{2})^{2} =r_{2}^{2} \\(x-u_{1})^{2}+(y-u_{2})^{2} =r_{3}^{2} \end{cases}$$Abziehen der dritten von den ersten beiden Zeilen impliziert ein LGS, da sich $x^{2},y^{2}$ genau wegheben. Da $p,q, u$ auf keiner Geraden, sind die Zeilen linear unabhängig also das LGS eindeutig lösbar. Also ist $(x,y)$ durch seine Abstände zu $u, p,q$ eindeutig charakterisiert in $\mathbb{C}$. (Anmerkung die Implikation ist keine Äquivalenzumformung es gibt Abstände die nicht lösbar sind).

Daraus folgt auch direkt, dass für eine Symmetrie eines regulären $n$-Ecks gilt, dass $\Phi(0)=0$.
###### eigentlicher Beweis

Wir zeigen $D_{2n}=\set{Id, r, ..., r^{n-1}, s, r\circ s,..., r^{n-1}\circ s}$. Insbesondere gilt alle $r^{i}$ sind verschieden. Für $n\geq 3$ ist auch mindestens eine Ecke komplex, also $s \neq Id$. Außerdem ist eine Spiegelung keine Rotation, also $r^{-i}\neq s$. Also ist $\# D_{2n}=2n$. 

Sei $f \in D_{2n}$ beliebig. Dann gibt es ein $k \in \set{0,...,n-1}$, sodass $f(1)= e^{\frac{2 \pi i \cdot k}{n}}$. Das heißt für $g:=r^{-k}\circ f$, gilt $g(1)=1$. Da $g$ eine Symmetrie ist, muss $g(e^{\frac{2 \pi i}{n}})\in \set{e^{\frac{2 \pi i}{n}}, e^{\frac{2 \pi i \cdot (n-1)}{n}}}$ sein, da der Abstand zwischen $g(1) =1$ und $g(e^{\frac{2 \pi i}{n}})$ genau dem Abstand zwischen $1$ und $e^{\frac{2 \pi i}{n}}$ entsprechen muss und $g(e^{\frac{2 \pi i}{n}})$ eine Ecke treffen muss.

*Fall* $g\left(e^{\frac{2 \pi i}{n}}\right)= e^{\frac{2 \pi i}{n}}$
Außerdem wissen wir $g(0)=0$ wegen [[#Vorüberlegung / Lemma]]. Wir haben also 3 Fixpunkte, weshalb wir wegen diesem Lemma auch wissen, dass $g=Id$. Daraus folgt $f = r^{k}$. 

*Fall* $g\left(e^{\frac{2 \pi i}{n}}\right)= e^{\frac{2 \pi i \cdot(n-1)}{n}}$
Dann gilt $(s\circ g)(1)=1, (s \circ s)(0)=0$ und $(s\circ g)(e^{\frac{2 \pi i}{n}})=e^{\frac{2 \pi i}{n}}$. Also ist $s \circ g = Id$. Damit ist aber $f=(s\circ r^{-k})^{-1}=r^{k}\circ s$. 

Insbesondere sind alle Elemente invertierbar, $D_{2n}$ also eine Gruppe.