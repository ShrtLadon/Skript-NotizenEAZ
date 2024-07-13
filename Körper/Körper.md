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