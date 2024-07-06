Eine Abbildung $s:\mathbb{R}^{n} \rightarrow \mathbb{R}^{n}$ heißt **Bewegung** bzw. **Isometrie** gdw.$$\forall u, v \in \mathbb{R}^{n}: \lVert s(u)-s(v)\rVert^{2}=\lVert u-v\rVert^2$$Bezüglich der Komposition ist die Menge der Bewegungen im $\mathbb{R}^{n}$ eine [[Gruppen|Gruppe]].
### Eigenschaften aus der Linearen Algebra
Das nachfolgende wird nicht bewiesen und sollte sich in einem LA2 Skript finden lassen.
- Isometrien (auf sich selbst) sind bijektiv.
- Jede Isometrie $\varphi$ lässt sich schreiben als $\varphi(z)=\tau_{\varphi}+A_{\varphi}z$ mit $\tau_{\varphi}\in \mathbb{R}^{n}$ ein Translationsvektor und $A\in O(n)=\set{A\in \mathbb{R}^{n\times n} \mid A^{T}A=\mathbb{1}_n}$ eine Normerhaltende lineare Abbildung.
- Die Elemente aus $O(n)$ haben Determinante $\pm 1$, je nachdem ob sie die Orientierung erhalten. 
- $SO(n):=\set{A\in O(n)\mid \det A = 1}$ ist die Gruppe der Drehungen im $\mathbb{R}^{n}$.  
- Wenn Untervektorraum $U$ von $\mathbb{R}^{n}$ invariant unter einer Isometrie $g$ ist - also $g(U)\subseteq U$ - ist auch $U^\perp$ invariant unter $g$, also $g(U^{\perp})\subseteq U^\perp$. (Wegen der Bijektivität gilt hier auch Gleichheit).

# Endliche Bewegungsgruppen
### Existenz von Fixpunkten
Sei $G$ eine endliche [[Gruppen|Gruppe]] von Bewegungen des Euklidischen Raums $\mathbb{R}^n$. Dann existiert ein $x\in \mathbb{R}^{n}$ mit $g\cdot x=x$ für alle $g\in G$, indem man ein beliebiges $z\in \mathbb{R}^{n}$ wählt und $$x=\frac 1 {\lvert G\rvert}\sum\limits_{g\in G}g(z)$$betrachtet.

Im Nachfolgenden kann man sich also o.B.d.A. auf lineare Funktionen (also mit Fixpunkt 0) beschränken, indem man $g\in G$ durch $\varphi \circ g \circ \varphi^{-1}$ ersetzt mit $\varphi(v):=v-x$, wobei $x$ ein Fixpunkt ist (die Ersetzung ist wie Nachrechnen zeigt ein [[Gruppenhomomorphismen|Isomorphismus]], wenn man sich auf das Bild einschränkt). 
###### Beweis
Sei $h \in G$. Dann hat nach den [[#Eigenschaften aus der Linearen Algebra]] $h$ die Form $\tau_{h}+A_{h}z$ mit $\tau_{h}\in \mathbb{R}^n$ und $A_{h}\in O(n)$. Es gilt $$\tau_{h}+x=\tau_{h}+\left(\frac 1 {\lvert G\rvert}\sum\limits_{g\in G}g(z)\right)=\frac 1 {\lvert G\rvert}\sum\limits_{g\in G}g(z)+\tau_h$$Da $A$ linear ist, können wir also $h\cdot x$ in die Summe ziehen:$$\begin{align}h\cdot x&=\frac 1 {\lvert G\rvert}\sum\limits_{g\in G}h(g(z))\\&=\frac 1 {\lvert G\rvert}\sum\limits_{g\in G}(h\cdot g)(z)\\&=\frac 1 {\lvert G\rvert}\sum\limits_{g'\in G}g'(z)=x\end{align}$$wobei wir ausnutzen, dass $G \rightarrow G,g\mapsto hg$ mit Inverse $G\rightarrow G, g\mapsto h^{-1}g$ eine Bijektion ist.


## im $\mathbb{R}^2$
Sei $G$ eine endliche [[Gruppen#Untergruppen|Untergruppe]] der Bewegungsgruppe. Dann ist $G$ [[Gruppenhomomorphismen|isomorph]] zu der [[Gruppen#Diedergruppe|Diedergruppe]] oder einer [[Gruppen#Zyklische Gruppen|zyklische]] Gruppe, was auf Übungsblatt 7.4 bewiesen wurde.

## im $\mathbb{R}^3$
Sei $G$ eine endliche [[Gruppen#Untergruppen|Untergruppe]] der Drehungen [[#Eigenschaften aus der Linearen Algebra|$SO(3)$]]. Wir wollen sie im Nachfolgenden nun klassifizieren:

### Drehachsen
Jedes $1\neq g \in SO(3)$ hat eine eindeutige Gerade $l$ (also einen eindimensionalen Untervektorraum), sodass gilt $$\forall x\in l: g(x)=x$$So ein $l$ nennen wir auch **Achse**.
Auf dem orthogonalen Komplement $l^\perp$ ist $g$ eine Drehung um den Winkel $\varphi$. Wenn $\text{ord}(g)<\infty$ ist $\varphi =\frac{2\pi}{m}$ für ein $m\in \mathbb{N}$. 

<iframe scrolling="no" title="Drehachse und zyklischerzeugte Gruppe" src="https://www.geogebra.org/material/iframe/id/udmtxw2j/width/1280/height/720/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="640px" height="360px" style="border:0px;"> </iframe>

#### Untergruppen der Drehungen in Ebene $l^\perp$
Sei $l$ eine Achse von $G$. Dann ist $$G_{l}:=\set{g\in G\mid \forall x\in l:g(x)=x}$$die Menge aller $g\in G$ die $l$ punktweise fixieren eine Untergruppe von $G$ und enthält Drehungen in der Ebene $l^\perp$. Außerdem ist $G_{l}$ eine [[Gruppen#Zyklische Gruppen|zyklische Gruppe]] der [[Gruppen#Ordnung|Ordnung]] $1<O_{l}<\infty$.

###### Beweis
Es gilt immer $1 \in G_{l}$ und für $g,h\in G_{l}$, dass für jedes $x\in l$ gilt: $g\cdot h^{-1}(x)=g(x)=x$, also $g\cdot h^{-1}\in G_{l}$ und nach [[Gruppen#Untergruppenkritierum|Untergruppenkriterium]] $G_{l}$ eine Untergruppe von $G$.
Insbesondere haben wir Achsen nur definiert, wenn es tatsächlich $1\neq g \in G_{l}$ gibt, also ist $G_{l}\neq \set{1}$ und damit auch die Ordnung von $G_{l}$ echt größer als 1. Außerdem ist da $G$ endlich die Ordnung von $G_{l}$ kleiner als $\infty$. 
Es verbleibt zu zeigen, dass $G_{l}$ zyklisch ist. Sei dazu $g\in G\setminus\set{1}$ das Element mit dem kleinsten Drehwinkel $\varphi=\frac{2\pi}{m}$ (also dem größten $m$). 
**Annahme**: Es existiert ein $h\in G_{l}$ mit Drehwinkel $\frac{2\pi}{n}$, sodass $h\not\in$[[Gruppen#Erzeugnis|$\langle g\rangle$]].
Es gilt es existiert ein $k\in \mathbb{N}$, sodass $\frac k m < \frac 1 n < \frac {k+1} m$. Betrachte nun $$w:=h\cdot g^{-k}\in G_{l}\setminus\set 1$$Das ist eine Drehung mit Drehwinkel $\frac{2\pi}{n}-\frac{2k\pi}m<\frac{2\pi}{m}$ was ein **Widerspruch** zur Minimalität von $\varphi$ ist.

#### Pole
Es gilt jede Achse $l$ schneidet die Einheitssphäre in genau zwei Punkten $\pm x_{l}$. Die Punkte $\pm x_l$ nennen wir **Pole** und $P$ die Menge aller Pole.
Dann gilt für ein $g\in G$, dass  $g\in G_{l}\iff g(x_{l})=x_{l}$. Denn die Achse ist ein Untervektorraum des Eigenraums zum Eigenwert 1 für eine Drehung um sie.

Außerdem definieren wir die folgende [[Gruppenwirkung|Wirkung]] $$*:G\times P \rightarrow P, (h,x)\mapsto h(x)$$
###### Beweis
Die Wirkung ist wohldefiniert, denn für ein $x\in P$ Pol von $g\in G$ ist  $h\cdot g\cdot h^{-1}(h(x))=h(x)$ also $h(x)$ ein Pol von $h\cdot g\cdot h^{-1}$. Außerdem gilt $e*x=x$ und $(h\cdot g)*x=h(g(x))=h*(g*x)$. 

### Charakterisierung (Satz von Klein)
Jede endliche nicht-triviale Untergruppe $G$ der 3-dimensionalen Bewegungsgruppe ist die Gruppe der orientierungserhaltenden Symmetrien einer der folgenden Figuren:
- einer Pyramide über einem regulärem m-Eck
- einer Doppelpyramide über einem regulärem m-Eck
- eines regulären Tetraeders
- eines Würfels (äquivalent eines Oktaeders)
- eines Ikosaeders (äquivalent eines Dodekaeders)

> [!Note] triviale Untergruppe
> In einem gewissen Sinne, fällt die triviale Untergruppe auch mit in die Charakterisierung, wenn man die "Pyramide über einem 0-Eck" betrachtet, also einen einzelnen Punkt.
#### Beweis
Ausgehend von der [[#Pole|Wirkung von $G$ auf die Pole]], stellen wir zunächst einige Gleichungen auf und prüfen, wann sie lösbar sind.
Es gilt jedes $g \in G\setminus\set{1}$ hält genau seine Drehachse punktweise fest und keine weitere Achse. Alternativ formuliert gilt für ein $x\in P$ für seinen [[Gruppenwirkung#Bahn und Stabilisator|Stabilisator $G_{x}$]], dass$$g\in G_{x}\iff g\in G_{-x}\iff \text{x auf Drehachse von g}$$Also gilt $$\sum\limits_{x\in P}(\lvert G_{x}\rvert-1)=2\cdot(\lvert G\rvert-1)$$
Seien nun $B_{1},...,B_{m}$ die verschiedenen $G$-[[Gruppenwirkung#Bahn und Stabilisator|Bahnen]] in $P$, also $B_{i}=G\cdot x_i=\set{g*x_i\mid g\in G}$ für geeignete $x_{i}\in B_{i}$.
Wir bemerken zunächst, dass für $x,x'\in B_i$ mit [[Gruppenwirkung#Orbit-Stabilisator-Theorem|Orbit-Stabilsator-Theorem]] gilt $\lvert G_{x'}\rvert=\lvert G\cdot x'\rvert=\lvert B_{i}\rvert=\lvert G\cdot x\rvert=\lvert G_{x}\rvert$. Setze im Nachfolgenden $N:=\lvert G\rvert$ und $n_{i}:= \lvert G_{x_{i}}\rvert$. Außerdem gilt mit [[Gruppenwirkung#Bahnenformel|Bahnenformel]] $b_{i}:=\lvert B_{i}\rvert=\frac{N}{n_{i}}$.
Damit erhalten wir mit obiger Gleichung durch Gruppieren der $x\in P$ in die Bahnen $B_{i}$, da diese $P$ [[Gruppenwirkung#Bahn und Stabilisator#Eigenschaften|partitionieren]]:   $$2\cdot(N-1)=\sum\limits_{i=1}^{m}\left(\sum\limits_{x\in B_{i}}\lvert G_{x}\rvert-1\right)=\sum\limits_{i=1}^{m}b_{i}\cdot (n_{i}-1)=\sum\limits_{i=1}^{m}\frac{N}{n_{i}}\cdot(n_{i}-1)$$Durch Division mit $N$ (in $\mathbb{Q}$) erhalten wir $$\underbrace{2\cdot(1-\frac 1 N)}_{\begin{gathered}<2\\\geq1\end{gathered}}=\sum\limits_{i=1}^{m}(1-\frac 1 {n_{i}}) \qquad (*)$$wobei wir für die Abschätzung benutzen, dass $G$ nicht-trivial ist, also mindestens $N=2$ gilt. Dann gilt außerdem, dass mit der ersten Bemerkung mindestens 2 Elemente in jedem $G_x$ sind also $n_{i}>1$. 
Dadurch folgern wir, dass erstmal $2\leq m$ - denn sonst stünde auf der rechten Seite ein Term, der kleiner als $1$ ist - und $m\leq 3$, denn $(1-\frac{1}{n_{i}})>(1-\frac{1}{2})=\frac 1 2$ und bei $m\geq 4$ wäre die rechte Seite also $\geq 2$. 
##### Fall $m=2$
Dann $n_{i}\leq N$ gilt damit $2\cdot(1-\frac 1 N)=2 + \frac 1 {n_{1}} + \frac 1 {n_{2}}\iff n_{1}=n_{2}=N$. Nach Definition vom [[Gruppenwirkung#Bahn und Stabilisator|Stabilsator]] gilt also für alle $g\in G$ und für alle $x\in P: g(x)=x$. Damit muss aber $G$ nur Drehungen um eine Achse $l$ enthalten wegen unserer Bemerkung zu [[#Pole|Polen]]. Dann ist [[#Untergruppen der Drehungen in Ebene $l perp$|$G_{l}=G$]], was ja eine zyklische Gruppe war. Das sind aber genau die orientierungserhaltenden Symmetriegruppen der Pyramide über einem regulärem $m$-Eck, wobei $m$ die Ordnung von $G$ ist:
<iframe scrolling="no" title="Pyramide über regulärem m-Eck" src="https://www.geogebra.org/material/iframe/id/yhqr3zqv/width/1280/height/720/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="640px" height="360px" style="border:0px;"> </iframe>

##### Fall $m=3$ 
o.B.d.A. sei $n_{1}\leq n_{2} \leq n_{3}$.
Wenn man in $(*)$ einsetzt und umstellt erhält man die Gleichung$$\frac 2 N= \frac 1 {n_{1}} + \frac 1 {n_{2}}+ \frac 1 {n_{3}} - 1$$
Da $2 \leq n_{1}$ muss also $n_{1}=2$ sein, sonst ist  $\frac 1 {n_{1}} + \frac 1 {n_{2}}+ \frac 1 {n_{3}} - 1 \leq \frac 1 3 + \frac 1 3+ \frac 1 3 - 1 = 0< \frac 2 N$. 

###### Fall $n_{2}=2$
Dann ist $\frac 2 N = \frac 1 2 + \frac 1 2 + \frac 1 {n_{3}}-1=\frac{1}{n_{3}}$ also $N= 2\cdot n_{3}$. Weiter oben haben wir gesehen $\lvert B_{3}\rvert=\frac{N}{n_{3}}$ also ist $\lvert B_{3}\rvert=2$ und damit liegen in $B_{3}$ nur 2 Pole, wobei jeder von genau $n_{3}=\frac N 2$ Elementen fixiert wird ($n_{i}=\lvert G_{x_{i}}\rvert$). Sei also $B_{3}=\set{x,y}$ und $g\in G\setminus\set 1$ mit $g(x)=x$. Dann ist insbesondere auch wegen der [[#Eigenschaften aus der Linearen Algebra|Bijektivität von $g$]] auch $g(y)=y$. Da $g\neq 1$ eine [[#Drehachsen|eindeutige Drehachse]] hat, gilt also $y=-x$.
Insbesondere gilt jedes Element $g\in G$ schickt $x$ auf $\pm x$ bzw. die Drehachse durch $x, -x$ ist ein $g$-Invarianter Untervektorraum.

[[#Eigenschaften aus der Linearen Algebra|Dann]] gilt insbesondere auch $g(x^{\perp})=x^{\perp}$. Das heißt auf der Ebene $x^\perp$ ist $G$ eine endliche Bewegungsgruppe und [[#im $ mathbb{R} 2$|damit]] auf $x^\perp$ eine Diedergruppe oder eine zyklische Gruppe. 

Außerdem gilt wenn für $g, h \in G$ gilt, dass $g\vert_{x^{\perp}}=h\vert_{x^{\perp}}$. Dann muss $g=h$ sein, denn sonst hätte man eine Spiegelung an der Ebene, was nicht mit einer Drehung im $\mathbb{R}^3$ möglich ist - und wir betrachten ja nur Drehungen im $\mathbb{R}^3$.

Das heißt $G$ ist generell isomorph zu einer Diedergruppe oder einer zyklischen Gruppe. Da aber nur $\frac N 2$ Elemente $x$ auf $x$ abbilden (also genau Rotationen in $x^\perp$ sind), muss es eine Diedergruppe sein (wenn $N>2$, sonst zyklische Gruppe aus [[#Fall $m=2$]]) .
Das ist genau die Symmetriegruppe einer Doppelpyramide über einem regulären $m$-Eck, wobei $m$ die Ordnung einer Drehung um die Achse durch $x$ ist:
<iframe scrolling="no" title="doppelte Pyramide - zur Diedergruppe isomorph" src="https://www.geogebra.org/material/iframe/id/d8hffj3j/width/1280/height/720/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="640px" height="360px" style="border:0px;"> </iframe>


###### Fall $n_{2} \geq 3$
Wäre $n_{2} \geq 4$, wäre $\frac 1 {n_{1}} + \frac 1 {n_{2}}+ \frac 1 {n_{3}} - 1 \leq \frac 1 2 + \frac 1 4 + \frac 1 4 -1 =0< \frac 2 N$, also muss $n_{2}=3$ gelten.
Es muss also auch $n_{3} \geq 3$ sein:
Wäre $n_{3}\geq 6$ dann wäre $\frac 1 {n_{1}} + \frac 1 {n_{2}}+ \frac 1 {n_{3}} - 1 = \frac 1 2 + \frac 1 3 + \frac 1 {n_{3}}-1 \leq \frac 1 2 + \frac 1 3 + \frac 1 6 -1 = 0 < \frac 2 N$. 
Das heißt wir wissen $n_{3}\in \set{3,4,5}$. Damit erhalten wir durch einsetzen in $(*)$ die entsprechenden Werte für $N$ und $b_{1}, b_{2}, b_{3}$:

| $n_3$ | $N$  | $b_1$ | $b_2$ | $b_3$ |
| :---: | :--: | :---: | :---: | :---: |
|  $3$  | $12$ |  $6$  |  $4$  |  $4$  |
|  $4$  | $24$ | $12$  |  $8$  |  $6$  |
|  $5$  | $60$ | $30$  | $20$  | $12$  |

**Fall** $n_{3}=3$:
Dann hat $B_2$ $4$ Pole bzw. Punkte. Es gilt 4 Pole, die jeweils von genau $3$ Elementen festgehalten werden.
Insbesondere liegen die 4 Pole nicht alle in einer Ebene, denn dann wären die Elemente nicht unter zwei verschiedenen Rotationen um Achsen in $B_{2}$ abgeschlossen. Weil aber 3 Punkte im $\mathbb{R}^3$ immer in einer Ebene (können auch in einer Gerade liegen, aber das ist hier ausgeschlossen) liegen müssen, erhalten wir also die Eckpunkte eines Tetraeder.

Seien $g,h\in G$, sodass für alle $x\in B_{2}$  $g(x)=h(x)$ gilt. Da aber $3$ von $4$ Punkten aus $B_{3}$ linear unabhängig sein müssen, ist $g,h$ durch den Fortsetzungssatz von linearen Abbildungen bereits eindeutig auf $\mathbb{R}^3$ bestimmt. Das heißt $G$ ist bereits eindeutig festgelegt durch sein Verhalten auf $B_{3}$, in welchem nur Elemente vertauscht werden.

Also ist $G$ [[Gruppenhomomorphismen|isomorph]] zu einer Untergruppe $U$ der [[Symmetrische Gruppe|symmetrischen Gruppe]] $S_{4}$. Dann gilt [[Gruppenwirkung#Index|$G:U$]]$=2$ also [[Gruppenwirkung#Eigenschaften|$U \trianglelefteq S_{4}$]] und [[Symmetrische Gruppe#$n>4$|$U=\mathcal{A}_4$]], was genau isomorph zur orientierungserhaltenden Symmetriegruppe des regelmäßigen Tetraeders ist:
<iframe scrolling="no" title="orientierungserhaltende Symmetrien eines regelmäßigen Tetraeder" src="https://www.geogebra.org/material/iframe/id/xrrvm4qg/width/1280/height/720/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="640px" height="360px" style="border:0px;"> </iframe>

**Fall:** $n_{3}=4$
Dann hat $B_{2}$ 8 Elemente, $B_{3}$ 6 Elemente und $N=24$.
Man kann nun (mit einiger Arbeit) zeigen, dass $B_{3}$ die Ecken eines Oktaeders bilden und $G$ darauf die Gruppe der orentierungserhaltenden Symmetrien bildet bzw. isomorph zu $S_{4}$ ist.
<iframe scrolling="no" title="Oktaeder" src="https://www.geogebra.org/material/iframe/id/vgf5z5kp/width/1280/height/720/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="640px" height="360px" style="border:0px;"> </iframe>
Alternativ kann man zeigen, dass $B_{2}$ die Eckpunkte eines Würfels sind und $G$ die orientierungserhaltende Symmetriegruppe des Würfels ist:
<iframe scrolling="no" title="orientierungserhaltende Symmetrien eines Würfels" src="https://www.geogebra.org/material/iframe/id/kpfzp55u/width/1280/height/720/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="640px" height="360px" style="border:0px;"> </iframe>

**Fall:** $n_{3}=5$
Dann ist $N=60$ und $B_{3}=12$. Man kann zeigen, dass $B_{3}$ die Eckpunkte eines regelmäßiges Ikosaeders sind und $G$ die orientierungserhaltenden Symmetrien davon:
<iframe scrolling="no" title="Ikosaeder" src="https://www.geogebra.org/material/iframe/id/bczntgya/width/1280/height/720/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="640px" height="360px" style="border:0px;"> </iframe>
Alternativ kann man zeigen, dass $B_{2}$ die Eckpunkte eines regelmäßigen Dodokaeder und $G$ die entsprechenden Symmetrien:
<iframe scrolling="no" title="Dodekaeder" src="https://www.geogebra.org/material/iframe/id/f3yr4efg/width/1280/height/720/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="640px" height="360px" style="border:0px;"> </iframe>
Alternativ kann man zeigen, dass $G \cong \mathcal{A}_{5}$ ist.