Ein Körper $\mathbb{K}$ ist ein [[Kommutative Ringe|kommutativer Ring]] für den gilt, dass $(\mathbb{K}\setminus \{0\}, \cdot, 1)$ eine [[Gruppen|Gruppe]] ist. Alternativ kann man auch sagen, dass [[Kommutative Ringe#Einheiten|$\mathbb{K}^{*}$]]$= \mathbb{K}\setminus \{0\}$.

###### Eigenschaften
- Jeder Körper ist ein [[#Nullteiler und Integritätsbereiche|Integritätsbereich]], denn wenn $a\neq 0$ und $ab=0\implies a^{-1}ab=0\implies b=0$.

#### Teilkörper
$U \subseteq \mathbb{K}$ eines Körpers heißt **Teilkörper**, wenn $U$ ein Körper mit Verknüpfung von $\mathbb{K}$ ist, also:
- $0,1\in U$
- $\forall a,b \in U : a-b \in U$
- $\forall a\in U, b\in U\setminus \set 0:\frac a b\in U$
## Charakteristik
Sei $\mathbb{K}$ ein Körper:
- Ist [[Abelsche Gruppen#Multiplikation|$n\cdot 1=1\cdot n = \underbrace{1 + ... + 1}_{n \text{ mal}}$]]$\neq 0$ für alle $n\in \mathbb{N}$, so ist $0$ die **Charakteristik** von $\mathbb{K}$.
- Sonst sei $p\in \mathbb{N}$ minimal mit $p\cdot 1 =0$. Dann ist $p$ die **Charakteristik** von $\mathbb{K}$. 

### Eigenschaften
- Wenn die Charakteristik von $\mathbb{K} \neq 0$ ist, ist sie eine [[Primzahlen|Primzahl]].
###### Beweis
Sei $p=m_{1}\cdot m_{2}$. Dann ist aber $$m_{1}\cdot m_{2}\cdot 1=\underbrace{(1+...+1)}_{m_{1}}\cdot\underbrace{(1+...+1)}_{m_{2}}=p\cdot 1 =0$$Da wir in einem [[#Eigenschaften|Integritätsbereich]] sind ist damit o.B.d.A. der erste Faktor $m_{1}\cdot 1=0$. Da aber $p$ minimal war ist damit $m_{1}=0$ oder $m_{1}=p$. Damit ist $p$ [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzibel]] also in $\mathbb{Z}$ insbesondere eine [[Primzahlen|Primzahl]].

#### kleinster Teilkörper
Sei $\mathbb{K}_{0}$ der kleinste Teilkörper von $\mathbb{K}$ (also enthält $\mathbb{K}_{0}$ keinen kleineren Teilkörper). Dann gilt:
- Wenn $\mathbb{K}$ Charakteristik 0 hat, ist $\mathbb{K}_{0}\cong \mathbb{Q}$.
- Wenn $\mathbb{K}$ Charakteristik $p< \infty$ hat ist $\mathbb{K}_{0} \cong F_{p}:=\mathbb{Z}/p \mathbb{Z}$.
###### Beweis
1) Betrachte $$\Phi:\mathbb{Z} \rightarrow \mathbb{K}_{0}, x\mapsto x\cdot 1=\underbrace{1+...+1}_{x\text{ mal}}$$Das ist ein [[Ringhomomorphismen|Ringhomorphismus]], denn unter Ausnutzung der [[Abelsche Gruppen#Multiplikation|Multiplikationseigenschaften in abelschen Ringen]] und des [[kommutative Ringe|Distributivitätsgesetzes]] gilt: $$\begin{align}\Phi(m_{1}+m_{2})&=m_{1}\cdot1+m_{2}\cdot 1\\\Phi(m_{1}\cdot m_{2})&=\underbrace{(1+...+1)}_{m_{1}\cdot m_{2}}=\underbrace{(1+...+1)}_{m_{1}}\cdot \underbrace{(1+...+1)}_{m_{2}}\end{align}$$Außerdem ist $\ker \Phi =\set 0$ und damit $\Phi$ injektiv. Außerdem gilt $\mathbb{Q}$ ist der *eindeutige* [[Quotientenkörper]] von $\mathbb{Z}$. Betrachte nun die Abbildung $$\hat \Phi:\mathbb{Q} \rightarrow \mathbb{K}_{0},\frac{m}{n}\mapsto \frac{\Phi(m)}{\Phi(n)}$$das ist also ein Körperhomomorphismus. Insbesondere ist es also injektiv und $\hat\Phi(\mathbb{Q})$ ein Körper in $\mathbb{K}_{0}$. Da $\mathbb{K}_{0}$ minimal war, ist $\hat \Phi(\mathbb{Q})=\mathbb{K}_{0}$. 

2) Betrachte $\Phi$ wie in 1). Dann gilt $\ker \Phi=p\cdot \mathbb{Z}$. Der [[Faktorgruppen#Isomorphiesatz|Isomorphiesatz]] lässt sich auf Ringe verallgemeinern (durch den selben Homomorphismus wie man leicht zeigt). Damit gilt $\mathbb{F}_{p}=\mathbb{Z}/p \mathbb{Z}\cong \text{Bild }\Phi$. Dadurch folgt $\text{Bild } \Phi$ ist ein Körper in $\mathbb{K}_{0}$ und da dieser der minimale Körper war, dass $\text{Bild }\Phi=\mathbb{K}_0$. Das beweist die Behauptung.

#### "binomische" Formel bei Charakteristik $\neq 0$
Sei $\mathbb{K}$ ein Körper der Charakteristik $p\neq 0$. Dann gilt $\forall x,y\in \mathbb{K}:$ $$(x+y)^{p}=x^{p}+y^{p}$$In anderen Worten ist $\varphi_{p}:\mathbb{K} \rightarrow \mathbb{K}, x\mapsto x^{p}$ ein [[Ringhomomorphismen|Körperhomomorphismus]].
###### Beweis
Es gilt $(x+y)^{p}=\sum\limits_{j=0}^{p}\binom{p}{j}x^{j}y^{p-j}$. 
Allerdings gilt für $j\neq0,p$, dass $\binom{p}{j}=\frac{p!}{j!(p-j)!}$  dass in dem Nenner nur Faktoren echt kleiner als $p$ sind und im Zähler $p$ als Faktor steht. Damit teilt kein Faktor im Nenner das $p$ im Zähler und $\binom{p}{j}$ durch $p$ teilbar. 
Insbesondere gilt aber $p\cdot 1=0$ also $(x+y)^{p}=x^{p}+y^{p}$.


### Endliche Multiplikative Untergruppen
Sei $K$ ein Körper,  $G$ eine [[Gruppen#Untergruppen|Untergruppe]] der multiplikativen [[Gruppen|Gruppe]] $(K\setminus\set 0, \cdot)$ und $n:= \lvert G\rvert< \infty$. Dann gilt:
- $G$ ist [[Gruppen#Zyklische Gruppen|zyklisch]]
- $G$ ist die Menge der Nullstellen von $X^{n}-1\in$[[Polynomringe|$K[X]$]] in $K$.
###### Beweis
1) Es gilt $G$ ist [[Abelsche Gruppen|abelsch]]. Insbesondere gilt nach [[Abelsche Gruppen#Klassifikation abelscher Gruppen|Klassifikation endlicher abelscher Gruppen]], dass $$G\cong G_{1}\times...\times G_{k}$$wobei $G_{1},...,G_{k}$ die [[Sylow-Sätze|Sylow-Untergruppen]] sind. Außerdem gilt, dass wenn alle $G_{i}$ zyklisch sind, auch $G$ zyklisch ist, denn dann ist $G_{i}\cong \mathbb{Z}/p_{i}^{l_{i}}\mathbb{Z}$, und $G$ nach [[Chinesischer Restsatz|Chinesischem Restsatz]] - da die Sylow-Untergruppen teilerfremde Ordnungen haben - isomorph zu $\mathbb{Z}/p_{1}^{l_{1}}\cdot ... \cdot p_{k}^{l_{k}}\mathbb{Z}$.
	Wir werden nachfolgend also zeigen, dass alle $G_i$ zyklisch sind. Da [[Abelsche Gruppen#Anzahl der Untergruppen der Ordnung $p$.|wissen]] wir, dass $G_{i}$ zyklisch ist genau dann, wenn es nur eine Untergruppe $T_{i} <G_{i}$ gibt, die Ordnung $p_{i}$ hat. Das ist äquivalent dazu, dass $\#\set{g\in G_{i} \mid g^{p_{i}}=1}=p_{i}$ ist, denn in einer [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklischen Gruppe primer Ordnung]], sind alle Elemente außer $1$ Erzeuger. Insbesondere sind alle solche $g$ eine Nullstelle von $X^{p_{i}}-1$, was allerdings höchstens $p_{i}$ Nullstellen hat, womit die Behauptung folgt.

3) Es gilt für alle $a\in G$: [[Gruppen#Ordnung#Eigenschaften|$a^{n}=1$]]. Insbesondere sind alle $a\in G$ also Nullstellen von $X^{n}-1$. Da ein Polynom vom [[Polynomringe#Grad|Grad]] $n$ [[Polynomringe#Teilbarkeit|höchstens $n$ Nullstellen hat]] und $G$ nun $n$ Nullstellen enthält, ist $G$ die Menge der Nullstellen von $X^{n}-1\in K[X]$. 

## Klassifikation endlicher Körper
Sei $K$ ein endlicher Körper mit $q=\lvert K\rvert<\infty$. Dann gilt:
- $q$ ist eine [[Primzahlen|Primzahlpotenz]], also $q=p^{n}$
- $K$ ist eine [[Körpererweiterungen#einfache Körpererweiterungen|einfache Erweiterung]] $\mathbb{F}_{p}(\alpha)$
- $K$ ist der [[Körpererweiterungen#Zerfällungskörper|Zerfällungskörper]] von $X^{q-1}-1 \in \mathbb{F}_{p}[x]$.
- $K$ ist durch $q$ bis auf [[Ringhomomorphismen|Isomorphie]] eindeutig bestimmt.

###### Beweis
1) Sei $p$ die [[#Charakteristik]] von $K$. Dann ist [[#kleinster Teilkörper|Satz über den kleinsten Teilkörper]] $K$ isomorph zu einem Körper, der $\mathbb{F}_{p}$ als Teilkörper enthält, denn $p$ muss $\neq 0$ sein, sonst würde es $\mathbb{Z}$ also unendlich viele Elemente enthalten.
	o.B.d.A. können wir also im Folgenden sagen $\mathbb{F}_{p}\subset K$ und aufgrund der Endlichkeit von $K$, dass [[Körpererweiterungen#Grad|$[K:\mathbb{F}_p]$]]$=n<\infty$. Außerdem gilt jeder Vektorraum der Dimension $n$ über $\mathbb{F}_{p}$ hat $\lvert \mathbb{F}_{p}\rvert^{n}=p^{n}$ Elemente.

2) Es gilt $\lvert K^*\rvert=\lvert K\setminus\set 0\rvert=q-1$. Insbesondere ist $K^*$ die [[Gruppen|Gruppe]] der [[Kommutative Ringe#Einheiten|Einheiten]] und eine [[Gruppen#Untergruppen|Untergruppe]] von sich selbst. Damit ist $K^*$ nach [[#Endliche Multiplikative Untergruppen|obigem Lemma]] zyklisch, d.h. es existiert ein $\alpha \in K\setminus \set 0$, sodass $\set{\alpha, \alpha^{2},...,\alpha^{q-1}=1}=K\setminus\set{0}$. Also gilt, dass $K=\mathbb{F}_{p}(\alpha)$, denn $\mathbb{F}_{p}(\alpha)$, muss mindestens $\alpha, \alpha^{2},...$ enthalten und der kleinste Körper sein, der dies tut.
3) Sei $m\in\set{1,...,q-1}$. Dann gilt alle alle $\alpha^{m}$ sind paarweise verschieden (da es genau $q-1$ solche gibt nach 2)). Außerdem ist $$(\alpha^{m})^{q-1}=(\alpha^{q-1})^{m}=1^{m}=1$$Damit ist $X^{q-1}-1=(X-\alpha)(X-\alpha^{2})...(X-\alpha^{q-1})$, denn wir haben genau $q-1$ Nullstellen und $X^{q-1}-1$ hat höchstens $q-1$ Nullstellen. Insbesondere gilt also $K$ ist der Zerfällungskörper von $X^{q-1}-1 \in \mathbb{F}_p$.
4) Weil der Zerfällungskörper [[Körpererweiterungen#Zerfällungskörper#Grad und Eindeutigkeit von Zerfällungskörpern|bis auf Isomorphie eindeutig ist]].


