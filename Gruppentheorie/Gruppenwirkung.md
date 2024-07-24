Die **Wirkung** (oder auch Operation oder Aktion) einer [[Gruppen|Gruppe]] $(G,\cdot)$ auf einer Menge $X$ ist eine Abbildung $*:G \times X \rightarrow X$ für die gilt:
- (A1) $\forall g,g' \in G, x \in X: g*(g'*x)=(g\cdot g')*x$
- (A2) $\forall x \in X : e * x = x$

Analog kann man auch eine **Rechtswirkung** $*:X\times G \rightarrow X$ definieren, bei der (A1) und (A2) dann auch von der rechten Seite definiert werden müssen. Im Nachfolgenden werden hauptsächlich nur Linksoperationen betrachtet. Das funktioniert aber für Rechtsoperationen analog.

### Eigenschaften
#### Zusammenhang zu symmetrischer Gruppe
Wirkungen $*:G\times X \rightarrow G$ stehen in 1 zu 1 Korrespondenz zu [[Gruppenhomomorphismen|Homomorphismen]] $$\rho:G \rightarrow S_{(X)}$$ von $G$ zur [[Symmetrische Gruppe|symmetrischen Gruppe]]
###### Beweis
Sei $*:G \times X \rightarrow X$. Dann definiere $\rho:G \rightarrow S_{(X)}, g \mapsto (x \mapsto g*x)$. Das ist wohldefiniert, da $x\mapsto g^{-1}*x$ Inverse von $\rho(g)$ ist und damit $\rho(g)$ bijektiv also in $S_{(X)}$. 

Außerdem ist $\rho(g\cdot g')(x)=(g\cdot g')*x\overset{A1}=g*(g'*x)=(\rho(g)\circ \rho(g'))(x)$. Also gilt $\rho(g\cdot g')=\rho(g) \circ \rho(g')$ und damit ist $\rho$ ein [[Gruppenhomomorphismen|Homomorphismus]]. 


Sei nun ein Homomorphismus $\rho:G \rightarrow S_{(X)}$ gegeben. Dann ist $*:G\times X \rightarrow X,g*x =\rho(g)(x)$ eine Wirkung, denn:
- $g*(g'*x)=(\rho(g)\circ \rho(g'))(x)\overset{\text{Homom.}}=\rho(g\cdot g')(x)=(g\cdot g')*x$
- $e*x=\rho(e)(x)\overset{\text{Homom.}}=Id(x)=x$


### Bahn und Stabilisator
Sei $G$ eine Gruppe und $*:G\times X \rightarrow X$ eine Wirkung auf die Menge $X$. 
- Die **Bahn** (bzw. **Orbit**) eines Elementes $x \in X$ ist $$G\cdot x:=\set{g*x : g\in G}$$
- Der **Stabilisator** von $x \in X$ ist$$\text{Stab}_G(x):=G_{x}:=\set{g \in G : g* x =x}$$
- Der **Kern** der Wirkung ist gegeben durch $$\ker:=\bigcap_{x\in X} G_{x}=\ker\rho$$wobei $\rho$ die [[#Zusammenhang zu symmetrischer Gruppe|Zuordnung]] zu einem Homomorphismus in die symmetrische Gruppe $S_{(X)}$ ist. Die Gleichheit gilt, weil der Kern genau die Elemente $g \in G$ enthält, für die für alle $x \in X$ gilt, dass $g*x=x$ also $\rho(g)=Id$.

Der **Bahnenraum** ist die Menge $$G\setminus X:=\set{G\cdot x: x\in X}$$und nach den unteren [[#Bahn und Stabilisator#Eigenschaften|Eigenschaften]] eine Partitionierung von $X$.
Für Rechtsoperationen ist der Bahnenraum definiert als $$X/G:=\set{x\cdot G: x\in X}$$

#### Eigenschaften
Sei $G\times X \rightarrow X$ eine Wirkung. Dann gilt:
- $\set{G\cdot x : x \in X}$ partitioniert $X$
- $\text{Stab}_G(x)=G_{x}\leq G$ ist eine [[Gruppen#Untergruppen|Untergruppe]].

###### Beweis
- Es gilt $x \in Gx\subseteq X$ also $\bigcup_{x\in X} Gx=X$. Seien $Gy, Gx$ mit $Gx\cap Gy \neq \varnothing$. Dann existiert ein $h \in Gx \cap Gy$. Das heißt allerdings, dass $g, g' \in G$ existieren mit $h=g*x=g'*y$. Dann ist insbesondere $((g')^{-1}\cdot g)*x =y$ also $y \in Gx$ also $Gy \subseteq Gx$ und analog $x \in Gy$ also $Gx \subseteq Gy$. D.h. $Gx=Gy$ also ist die angegebene Menge eine Partition
- Es gilt $e \in G_{x}$ also $G_{x}\neq \varnothing$. Seien also $a,b \in G_{x}$. Dann gilt $(a\cdot b^{-1})*x=(a\cdot b^{-1})*(b*x)=a*((b^{-1}\cdot b) *x) = a*(e*x)=a*x=x$ also ist $a\cdot b^{-1} \in G_{x}$ und wegen dem [[Gruppen#Untergruppenkriterium|Untergruppenkriterium]] $G_{x}$ eine Untergruppe von $G$.

##### Satz von Lagrange
Sei $G$ eine endliche [[Gruppen|Gruppe]] und $H \leq G$ eine [[Gruppen#Untergruppen|Untergruppe]]. Dann gilt$$\lvert G\rvert =\lvert G/H\rvert \cdot \lvert H\rvert $$also insbesondere auch $\lvert H\rvert \mid \lvert G\rvert$.
###### Beweis
Sei $g \in G$. Dann ist $H \rightarrow g\cdot H, h\mapsto g\cdot h$ ist eine Bijektion, denn $x \mapsto g^{-1}\cdot x$ ist Inverse Funktion.
Damit ist aber $\lvert H\rvert =\lvert g\cdot H\rvert$. Da außerdem $G/H$ eine Partition von $G$ bildet, gilt$$\lvert G\rvert =\sum\limits_{g\cdot H\in G/H}\lvert gH\rvert =\sum\limits_{g\cdot H\in G/H}\lvert H\rvert =\lvert H\rvert \cdot \lvert G/H\rvert$$

##### Orbit-Stabilisator-Theorem
Sei $G$ eine Gruppe, die auf $X$ mit $*:G\times X \rightarrow X$ operiert. Dann sind die folgenden Abbildungen wohldefiniert und Inverse voneinander$$\begin{gather}\Phi:G/G_{x} \rightarrow G\cdot x,g\cdot G_{x} \mapsto g*x \\ \Psi:G\cdot x \rightarrow G/G_{x}, g*x\mapsto g\cdot G_{x}\end{gather}$$wobei $G/G_{x}$ die Menge der [[#Rechts und Linksnebenklassen|Linksnebenklassen]] ist.
###### Beweis
Sei $g\cdot G_{x}=g'\cdot G_{x}$. Dann gibt es ein $h \in G_{x}=\text{Stab}_{G}(x)$, sodass $g'=g\cdot h$. 
Dann gilt $g'*x=(g\cdot h)*x\overset{\text{(A1)}}=g*(h*x)\overset{h\in G_{x}}=g*x$. Also ist $\Phi(g\cdot G_{x})=\Phi(g'\cdot G_{x})$.

Sei nun $g*x=g'*x$. Dann gilt wegen A1 $(g^{-1}\cdot g)*x\overset{\text{(A2)}}=x=(g^{-1}\cdot g')*x$. Also ist $g^{-1}\cdot g' \in G_{x}=\text{Stab}_{G}(x)$. Dann ist aber insbesondere $g\cdot G_{x}=g'\cdot G_{x}$ und damit auch $\Psi$ wohldefiniert. Insbesondere sind die Abbildungen offensichtlich invers zueinander, wenn sie wohldefiniert sind.

##### Bahnenformel
Sei $G$ eine endliche [[Gruppen|Gruppe]] und $*:G\times X \rightarrow X$ eine Wirkung. Dann gilt $$\forall x \in X: \lvert G\rvert =\lvert G_{x}\rvert \cdot \lvert G\cdot x\rvert$$
###### Beweis
Es gilt wegen dem [[#Orbit-Stabilisator-Theorem]], dass eine Bijektion zwischen $G/G_{x}$ und $G\cdot x$ existiert also $\lvert G/G_{x}\rvert =\lvert G\cdot x\rvert$ für alle $x \in X$ gilt.

Außerdem ist $G_{x}$ eine [[Gruppen#Untergruppen|Untergruppe]] von $G$ und damit gilt nach [[#Satz von Lagrange]], dass $$\lvert G\rvert =\lvert G/G_{x}\rvert \cdot \lvert G_{x}\rvert =\lvert G\cdot x\rvert \cdot \lvert G_{x}\rvert$$

#### Index
Sei $U \leq G$ eine Gruppe. Dann ist der **Index** definiert als $$\text{ind}(U):=\lvert G:U\rvert$$dabei kann $G:U$ sowohl [[#Rechts und Linksnebenklassen|$G/U$ oder $U\setminus G$]] sein, denn wegen ÜB7.1.3 sind die gleich mächtig.
### Beispiele
 - Für eine beliebige Gruppe $G$ und eine beliebige Menge $X$ ist $g*x:=x$ die **triviale Wirkung**
- Die [[Symmetrische Gruppe]] $S_{(X)}$ operiert auf $X$ mit $f*x := f(x)$

##### Rechts und Linksnebenklassen
Sei $U \leq G$ eine [[Gruppen#Untergruppen|Untergruppe]]. Dann gilt:
- $U$ operiert auf $G$ von links (*Linkstranslation*) mit $U \times G \rightarrow G, (u,g)\mapsto u\cdot g$. Der [[#Bahn und Stabilisator|Orbit]] $U\cdot g$ heißt **Rechtsnebenklasse**
- $U$ operiert auf $G$ von rechts (*Rechtstranslation*) mit $G \times U \rightarrow G, (g,u)\mapsto g\cdot u$. Der [[#Bahn und Stabilisator|Orbit]] $g \cdot U$ heißt **Linksnebenklasse**
##### Diedergruppe
- $X=\set{\text{Ecken eines regulären n-Ecks}}$ und [[Gruppen#Diedergruppe|$G=D_{2n}$]] hat die Wirkung $g*x:= g(x)$. Es gilt für jedes $x \in X$ ist $\#G\cdot x=n$, weil wir jeden Punkt aus $X$ erreichen können (durch Rotation). Für $G_{x}$ gilt, dass es die Identität und die Reflektion bezüglich einer Gerade durch $0$ und $x$ enthält:<iframe scrolling="no" title="DiedergruppeZweitesBahnelelement" src="https://www.geogebra.org/material/iframe/id/dna8zvvp/width/1300/height/800/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="492px" style="border:0px;"> </iframe>
