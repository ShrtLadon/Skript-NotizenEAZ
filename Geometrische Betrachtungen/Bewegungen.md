Eine Abbildung $s:\mathbb{R}^{n} \rightarrow \mathbb{R}^{n}$ heißt **Bewegung** bzw. **Isometrie** gdw.$$\forall u, v \in \mathbb{R}^{n}: \lVert s(u)-s(v)\rVert^{2}=\lVert u-v\rVert^2$$Bezüglich der Komposition ist die Menge der Bewegungen im $\mathbb{R}^{n}$ eine [[Gruppen|Gruppe]] und wir nennen sie auch $
### Eigenschaften aus der Linearen Algebra
Das nachfolgende wird nicht bewiesen und sollte sich in einem LA2 Skript finden lassen.
- Isometrien (auf sich selbst) sind bijektiv.
- Jede Isometrie $\varphi$ lässt sich schreiben als $\varphi(z)=\tau_{\varphi}+A_{\varphi}z$ mit $\tau_{\varphi}\in \mathbb{R}^{n}$ ein Translationsvektor und $A\in O(n)=\set{A\in \mathbb{R}^{n\times n} \mid A^{T}A=\mathbb{1}_n}$ eine Normerhaltende lineare Abbildung.
- Die Elemente aus $O(n)$ haben Determinante $\pm 1$, je nachdem ob sie die Orientierung erhalten. 
- $SO(n):=\set{A\in O(n)\mid \det A = 1}$ ist die Gruppe der Drehungen im $\mathbb{R}^{n}$.  

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

