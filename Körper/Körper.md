Ein Körper $\mathbb{K}$ ist ein [[Kommutative Ringe|kommutativer Ring]] für den gilt, dass $(\mathbb{K}\setminus \{0\}, \cdot, 1)$ eine [[Gruppe]] ist. Alternativ kann man auch sagen, dass [[Kommutative Ringe#Einheiten|$\mathbb{K}^{*}$]]$= \mathbb{K}\setminus \{0\}$.

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

## Körpererweiterungen
Ist $L$ ein Körper und $K$ ein [[#Teilkörper]] von $L$ so heißt $L$ **Erweiterungskörper** von $K$ und das Paar $(L,K)$ geschrieben als $L/K$ heißt **Körpererweiterung** und wird auch gelesen als *L über K*.

>[!Danger] Aufpassen
>$L/K$ ist nur eine Notation und nicht wie ein [[Faktorringe|Faktorring]] aufzufassen

Aufgrund der Körperaxiome folgt direkt, dass $L$ ein $K$-Vektorraum ist, was die folgende Definition motiviert:
### Grad
Der **Grad** einer Körpererweiterung $L/K$ ist die Dimension von $L$ als $K$-Vektorraum und wir schreiben dafür $$[L:K]$$Wenn $[L:K]<\infty$, nennen wir $L/K$ **endliche Körpererweiterung**. 

##### Gradsatz
Seien $K \subseteq L \subseteq A$ Körper. Dann gilt:$$[A:K]=[A:L]\cdot[L:K]$$das funktioniert auch für nicht endliche Körpererweiterungen, wenn die Multiplikation mit $\infty$ wieder $\infty$ ist.
###### Beweis
Beweisen werden wir das hier nur für endliche Körpererweiterungen. Betrachte dazu eine Basis $B_{A}:=\set{a_{1},...,a_{m}}$ von $A$ als $L$-Vektorraum und eine Basis $B_{L}:=\set{b_{1},...,b_{n}}$ von $L$ als $K$-Vektorraum.

Wir wollen zeigen, dass $B:=\set{a_{i}\cdot b_{j} \mid 1\leq i \leq m, 1 \leq j \leq n}$ eine Basis von $A$ als $K$-Vektorraum ist.
**Erzeugendensystem:**
Es gilt für alle $a\in A$ existieren $\lambda_{1},...,\lambda_{m}\in L$, sodass $a=\sum\limits_{i=1}^{m}\lambda_{i}a_{i}$. Außerdem existieren für alle $\lambda_{i}\in L$ Skalare $\mu_{ij}\in K$ für $1\leq i \leq m$ und $1 \leq j \leq n$ mit $$\forall 1\leq i \leq m :\quad \lambda_{i}= \sum\limits_{j=0}^{n}\mu_{ij}b_{j}$$In Kombination ergibt sich also $$a=\sum\limits_{i=1}^{m}\sum\limits_{j=1}^{n}\mu_{ij}\cdot (a_{i}\cdot b_{j})$$Also ist $B$ ein Erzeugendensystem.

**lineare Unabhängigkeit:**
Seien $\mu_{ij}\in K$ für $1\leq i \leq m$ und $1 \leq j \leq n$ mit $\sum\limits_{i=1}^{m}\sum\limits_{j=1}^{n}\mu_{ij}\cdot (a_{i}\cdot b_{j})=0$. Dann gilt: $$\begin{align}0&=\sum\limits_{i=1}^{m}(\sum\limits_{j=1}^{n}\mu_{ij}b_{j})a_{i} \\\overset{B_{A}\text{ l.u.}}\implies &\forall 1\leq i \leq m : \sum\limits_{j=1}^{n}\mu_{ij}b_{j}=0\\\overset{B_{L} \text{ l.u.}}\implies \forall &1\leq i\leq m,1\leq j \leq n: \mu_{ij}=0\end{align}$$
### Erzeugte Körper
Sei $L/K$ eine Körpererweiterung und $U \subset L$ eine Teilmenge. Dann ist der von **U erzeugte Körper K(U)** der kleinste [[#Teilkörper]] von $L$ der $K$ und $U$ enthält.

**Beispiele:**
- $\mathbb{Q}(\sqrt{2})=\set{q_1+q_{2}\sqrt 2 \mid q_1,q_{2} \in \mathbb{Q}}$
- $\mathbb{Q}(\sqrt{2},\sqrt{3})=\set{q_1+q_{2}\sqrt 2 +q_{3}\sqrt 3+q_{4}\sqrt 2\cdot\sqrt 3\mid q_1,q_{2},q_{3},q_{4} \in \mathbb{Q}}$
- $\mathbb{Q}(\sqrt{2},\sqrt{8})=\set{q_1+q_{2}\sqrt 2 \mid q_1,q_{2} \in \mathbb{Q}}=\mathbb{Q}(\sqrt 2)$, denn $\sqrt{8}=2\cdot\sqrt{2}$
- $\mathbb{Q}(\sqrt[3]{2})=\set{q_1+q_{2}\sqrt[3] 2 +q_{3}\sqrt[3] 2^{2}\mid q_1,q_{2},q_{3} \in \mathbb{Q}}$.
### einfache Körpererweiterungen
Sei $L/K$ eine [[#Körpererweiterungen|Körpererweiterung]]. Dann heißt $L/K$ **einfache** Körpererweiterung, wenn ein $a\in L$ existiert mit $L=K(a)$ der erzeugte Körper von $\set{a}$ ist.

#### Beispiel: Körper der Polynomrestklassen modulo p
Sei $K$ ein Körper und $p \in K[X]$ ein [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzibles]] [[Polynomringe|Polynom]] von [[Polynomringe#Grad|Grad]] $n$. Dann gilt:
0) Der [[Faktorringe|Faktorring]] $L:=K[X]/p\cdot K[X]$ ist ein Körper
1) Für $a=\overline{X}=X+p\cdot K[X]\in L$ gilt $L=K(a)$ 
2) $1,a,...,a^{n-1}$ ist eine $K$-Basis von $L$.
3) Es gilt $p(a)=0$

###### Beweis
Zunächst bemerken wir:
Sei $q \in K[X]$. Dann existiert mit [[Polynomringe#Polynomdivision mit Rest|Polynomdivision]] eindeutige $s,r \in K[X]$ mit $grad(r) < grad(p)=n$, sodass $q=s\cdot p + r$. Insbesondere gibt es also für jedes $\bar q\in K[X]/p\cdot K[X]$ einen eindeutigen Repräsentanten vom Grad $\leq n-1$.
Insbesondere ist $grad(p)>1$, also gilt für alle $b_{i}\in K$, dass alle $\overline{b_{i}}\in K[X]/p\cdot K[X]$ paarweise verschieden. Wir können also alle ${b_{i}}$ mit $\overline{b_{i}}$ assoziieren.  

0) Jeder Körper ist ein [[Euklidische Ringe#Beispiele|Euklidischer Ring]] also ein [[Hauptidealringe#Euklidische Ringe|Hauptidealring]] und damit $p\cdot K[X]$ ein [[Ideale#Prim- und maximale Ideale#Eigenschaften|maximales Ideal]] und damit ist $K[X]/p\cdot K[X]$ ein Körper.
1) Betrachte den [[Polynomringe#Einsetzungshomomorphismus|Einsetzungshomorphismus]] $$\varphi_a:K[X]\mapsto K(a), q\mapsto q(a)$$Es gilt dann $\ker \varphi_{a}=(p)$, denn $\sum\limits_{i=1}^{m}b_{i}\cdot a^{i}=(\sum\limits_{i=1}^{m}b_{i}X^{i})+p\cdot K[X]$. Wegen dem Isomorphiesatz folgt $\text{Bild} \varphi_{a}\cong K[X]/p\cdot K[X]$ ist ein Körper, der $a$ und $K$ enthält. Da $K(a)$ der minimale solcher Körper ist, ist $\varphi_{a}$ surjektiv und damit ein Isomorphismus.
2) Wegen der obigen Bemerkung genügt es Polynome vom Grad $\leq n-1$ zu betrachten: 
	Für diese gilt, dass $1,X,...,X^{n-1}$ eine Basis ist. D.h. es existieren für alle $r\in \set{w\in K[X] \mid grad(w) \leq n-1}$ eindeutige $c_{0},...,c_{n-1}\in K$, sodass $$\begin{align}&r=c_{0}+c_{1}\cdot X + ... +c_{n-1}\cdot X^{n-1}\\\iff&\overline r=c_{0} + c_{1}\cdot a+...+c_{n-1}\cdot a\end{align}$$Damit ist $\set{0,a,...,a^{n-1}}$ eine Basis
3) In 1) gezeigt.

#### Charakterisierung von einfachen Körpererweiterungen
Sei $K(a)/K$ eine einfache Körpererweiterung und $\varphi_{a}:K[X]\rightarrow L$ der [[Polynomringe#Einsetzungshomomorphismus|Einsetzungshomorphismus]], also $\varphi_{a}(p)=p(a)$. 
*Fall:* $\varphi_{a}$ ist injektiv:
	 Dann gibt es eine eindeutige Erweiterung von $\varphi_{a}$ zu einem [[Ringhomomorphismen|Isomorphismus]] $\Phi:K(X) \rightarrow L$ also dem [[Quotientenkörper#Beispiele|Körper der "rationalen Funktionen" auf $K$]] zu $L$. Insbesondere ist also $L/K$ eine unendliche Körpererweiterung.
*Fall:* $\varphi_{a}$ ist nicht injektiv:
	- das [[Ringhomomorphismen#Kern#Eigenschaften|Ideal $\ker(\varphi_a)$]] wird von einem [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzible]] [[Polynomringe#Teilbarkeit|Polynom]] $p$ erzeugt.
	- $L\cong K[X]/p\cdot K[X]$
	- [[#Grad|$[L:K]$]]$=\text{grad}(p)<\infty$

###### Beweis
*Fall:* $\varphi_{a}$ ist injektiv.
Dann betrachte $\Phi:K(X) \rightarrow L, \frac p q \mapsto \frac{\varphi_{a}(p)}{\varphi_{a}(q)}$. 
Zunächst gilt, dass wir hier nicht durch $0$ teilen, da $\varphi_{a}$ injektiv, also $\ker \varphi_{a} = \set{0}$. Außerdem gilt für $\frac{k\cdot p}{k\cdot q} = \frac{p}{q}$ mit einem $k\in K[X]$, dass$$\Phi(\frac{k\cdot p}{k\cdot q})=\frac{\varphi_{a}(k\cdot p)}{\varphi_{a}(k\cdot q)}\overset{\varphi_{a}\text{ Hom.}}=\frac{\varphi_{a}(k)\cdot \varphi_{a}(p)}{\varphi_{a}(k)\cdot\varphi_{a}(q)}=\frac{\varphi_{a}(p)}{\varphi_{a}(q)}=\Phi(\frac p q)$$also ist $\Phi$ wohldefiniert. Dass $\Phi$ ein [[Ringhomomorphismen|Homorphismus]] ist folgt auch direkt, da $\varphi_{a}$ Homomorphismus ist.
Außerdem ist $\ker \Phi =\ker \varphi_{a}=\set{0}$, also $\Phi$ injektiv. Damit ist $\text{Bild} \Phi$ ein Körper in $L$ der $a$ enthält. Da $L=K(a)$ der kleinste solche Körper ist, folgt $\Phi$ ist surjektiv.

*Fall:* $\varphi_{a}$ ist nicht injektiv
1. Sei $0\neq p\in K[X]$ ein Erzeuger von $\ker \varphi_{a}$, also $\set{p\cdot s \mid s\in K[X]}$.
	Zunächst bemerken wir, dass $\ker \varphi_{a}$ nur Polynome von [[Polynomringe#Grad#Rechenregeln|Grad]] $-\infty$ oder $\geq grad(p)$ enthält.

	Seien nun $0\neq p_{1},p_{2}\in K[X]$ mit $p_{1}\cdot p_{2} =p$. Dann gilt $$0=p(a)=p_{1}(a)\cdot p_{2}(a)$$Da allerdings $K$ als Körper ein [[#Eigenschaften|Integritätsbereich]] ist, ist [[Polynomringe#Polynomringe von Integritätsbereichen.|$K[X]$]] auch ein Integritätsbereich. Daraus folgt $p_{1}(a)=0$ oder $p_{2}(a)=0$, also $p_{1}\in \ker\varphi_{a}$ oder $p_{2}\in \ker \varphi_{a}$. Dann muss aber wegen unserer anfänglichen Beobachtung $grad(p_{1})\geq p$ oder $grad(p_{2})\geq p$ und wegen [[Polynomringe#Rechenregeln|Rechenregeln für den Grad]] das jeweils andere Polynom Grad 0 haben, also eine [[Polynomringe#Polynomringe von Integritätsbereichen.|Einheit]] sein. Damit ist $p$ irreduzibel nach [[Kommutative Ringe#Prim- und irreduzible Elemente|Definition]].

2. Ist recht analog wie im Beweis zum [[#kleinster Teilkörper|kleinsten Teilkörper]]. Wegen Isomorphiesatz ist $K[X]/\ker \varphi_{a}=K[X]/p\cdot K[X]\cong \text{Bild}\varphi_{a}$.

	 Außerdem ist [[#Beispiel Körper der Polynomrestklassen modulo p|$K[X]/p\cdot K[X]$ ein Körper]] und damit $\text{Bild}\varphi_{a}$ auch ein Körper, der insbesondere auch $a\in L$ enthält, denn $\varphi_{a}(X)=a$. Da $L=K(a)$ der kleinste Körper ist, der $K$ und $a$ enthält, ist $\Phi$ surjektiv.

3.  Folgt direkt mit 2. und [[#Beispiel Körper der Polynomrestklassen modulo p]] 


### algebraische und transzendente Elemente
Sei $L/K$ eine [[#Körpererweiterungen|Körpererweiterung]]. Dann heißt $a\in L$ **algebraisch**, wenn $$[K(a):K]<\infty$$und **transzendent** über $K$, wenn $$[K(a):K]=\infty$$Mit der obigen [[#Charakterisierung von einfachen Körpererweiterungen|Charakterisierung]] ist das äquivalent zu, dass $$a\text{ algebraisch} \iff \exists 0\neq p \in K[X]: p(a)=0$$
Alternativ existiert die folgende Charakterisierung:
- $a$ transzendent $\implies 1, a,a^{2},...$ sind linear unabhängig
- $a$ algebraisch mit $[K(a):K]=n \implies 1, a,...,a^{n-1}$ ist eine $K$-Basis von $L$.
###### Beweis
Wenn $a^{k}=c_{1}+ ... + c_{k}\cdot a^{k-1}$, dann ist $X^{k}-c_1-...-c_{k}\cdot X^{k-1}$ eine Polynom in $K$ mit Nullstelle $a$, was ein Widerspruch wäre.
Der zweite Teil folgt aus der dem Isomorphismus aus der [[#Charakterisierung von einfachen Körpererweiterungen]] und [[#Beispiel Körper der Polynomrestklassen modulo p]]. (Wir ersetzen $a \mapsto \overline X$) 

#### Minimalpolynom
Wenn $a\in L$ algebraisch über $K$ ist, existiert ein eindeutiges normiertes und [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzibles]] $p_{\min}\in K[X]$, sodass $p_{\min}(a)=0$. Wir nennen $p_{\min}$ das **Minimalpolynom von $a$ über $K$**. Es gilt:
- $grad(p_{\min})=[K(a):K]$ und $K(a)=K[X]/p_{\min}\cdot K[X]$
Das folgt direkt mit der [[#Charakterisierung von einfachen Körpererweiterungen]].

Wir sagen $K(a)$ entsteht durch **Adjunktion einer Nullstelle** von $p_{\min}$ zu $K$. 
Entsteht ein anderer Körper $L'$ durch Adjunktion einer Nullstelle $a'$ von $p_\min$, dann gibt es einen [[Ringhomomorphismen|Körperisomorphismus]] $\Phi:K(a) \rightarrow L'$ mit $\Phi(a)=a'$ und $\phi(k)=k$ für alle $k\in K$. 