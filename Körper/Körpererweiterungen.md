Ist $L$ ein Körper und $K$ ein [[#Teilkörper]] von $L$ so heißt $L$ **Erweiterungskörper** von $K$ und das Paar $(L,K)$ geschrieben als $L/K$ heißt **Körpererweiterung** und wird auch gelesen als *L über K*.

>[!Danger] Aufpassen
>$L/K$ ist nur eine Notation und nicht wie ein [[Faktorringe|Faktorring]] aufzufassen

Aufgrund der Körperaxiome folgt direkt, dass $L$ ein $K$-Vektorraum ist, was die folgende Definition motiviert:
## Grad
Der **Grad** einer Körpererweiterung $L/K$ ist die Dimension von $L$ als $K$-Vektorraum und wir schreiben dafür $$[L:K]$$Wenn $[L:K]<\infty$, nennen wir $L/K$ **endliche Körpererweiterung**. 

### Gradsatz
Seien $K \subseteq L \subseteq A$ Körper. Dann gilt:$$[A:K]=[A:L]\cdot[L:K]$$das funktioniert auch für nicht endliche Körpererweiterungen, wenn die Multiplikation mit $\infty$ wieder $\infty$ ist.
###### Beweis
Beweisen werden wir das hier nur für endliche Körpererweiterungen. Betrachte dazu eine Basis $B_{A}:=\set{a_{1},...,a_{m}}$ von $A$ als $L$-Vektorraum und eine Basis $B_{L}:=\set{b_{1},...,b_{n}}$ von $L$ als $K$-Vektorraum.

Wir wollen zeigen, dass $B:=\set{a_{i}\cdot b_{j} \mid 1\leq i \leq m, 1 \leq j \leq n}$ eine Basis von $A$ als $K$-Vektorraum ist.
**Erzeugendensystem:**
Es gilt für alle $a\in A$ existieren $\lambda_{1},...,\lambda_{m}\in L$, sodass $a=\sum\limits_{i=1}^{m}\lambda_{i}a_{i}$. Außerdem existieren für alle $\lambda_{i}\in L$ Skalare $\mu_{ij}\in K$ für $1\leq i \leq m$ und $1 \leq j \leq n$ mit $$\forall 1\leq i \leq m :\quad \lambda_{i}= \sum\limits_{j=0}^{n}\mu_{ij}b_{j}$$In Kombination ergibt sich also $$a=\sum\limits_{i=1}^{m}\sum\limits_{j=1}^{n}\mu_{ij}\cdot (a_{i}\cdot b_{j})$$Also ist $B$ ein Erzeugendensystem.

**lineare Unabhängigkeit:**
Seien $\mu_{ij}\in K$ für $1\leq i \leq m$ und $1 \leq j \leq n$ mit $\sum\limits_{i=1}^{m}\sum\limits_{j=1}^{n}\mu_{ij}\cdot (a_{i}\cdot b_{j})=0$. Dann gilt: $$\begin{align}0&=\sum\limits_{i=1}^{m}(\sum\limits_{j=1}^{n}\mu_{ij}b_{j})a_{i} \\\overset{B_{A}\text{ l.u.}}\implies &\forall 1\leq i \leq m : \sum\limits_{j=1}^{n}\mu_{ij}b_{j}=0\\\overset{B_{L} \text{ l.u.}}\implies \forall &1\leq i\leq m,1\leq j \leq n: \mu_{ij}=0\end{align}$$
## Erzeugte Körper
Sei $L/K$ eine Körpererweiterung und $U \subset L$ eine Teilmenge. Dann ist der von **U erzeugte Körper K(U)** der kleinste [[#Teilkörper]] von $L$ der $K$ und $U$ enthält.

**Beispiele:**
- $\mathbb{Q}(\sqrt{2})=\set{q_1+q_{2}\sqrt 2 \mid q_1,q_{2} \in \mathbb{Q}}$
- $\mathbb{Q}(\sqrt{2},\sqrt{3})=\set{q_1+q_{2}\sqrt 2 +q_{3}\sqrt 3+q_{4}\sqrt 2\cdot\sqrt 3\mid q_1,q_{2},q_{3},q_{4} \in \mathbb{Q}}$
- $\mathbb{Q}(\sqrt{2},\sqrt{8})=\set{q_1+q_{2}\sqrt 2 \mid q_1,q_{2} \in \mathbb{Q}}=\mathbb{Q}(\sqrt 2)$, denn $\sqrt{8}=2\cdot\sqrt{2}$
- $\mathbb{Q}(\sqrt[3]{2})=\set{q_1+q_{2}\sqrt[3] 2 +q_{3}\sqrt[3] 2^{2}\mid q_1,q_{2},q_{3} \in \mathbb{Q}}$.
### einfache Körpererweiterungen
Sei $L/K$ eine [[#Körpererweiterungen|Körpererweiterung]]. Dann heißt $L/K$ **einfache** Körpererweiterung, wenn ein $a\in L$ existiert, sodass $L=K(a)$ der erzeugte Körper von $\set{a}$ ist.

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


## algebraische und transzendente Elemente
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

#### Beispiele
- Sei $p=X^{3}-2 \in \mathbb{Q}[X]$ ein [[Polynomringe|Polynom]]. Betrachte die primitive Einheitswurzel $\beta = e^{\frac{2\pi i }3}$. Dann sind die Nullstellen von $p$ in $\mathbb{C}$ genau $\sqrt[3]2, \beta \sqrt[3]2, \beta ^{2}\sqrt[3]2$ und $$\mathbb{Q}(\sqrt[3]2)\cong \mathbb{Q}(\beta\sqrt[3]2)\cong \mathbb{Q}(\beta^{2}\sqrt[3]2)$$  Insbesondere sind die Nullstellen algebraisch und $p$ das Minimalpolynom
- $X \in \mathbb{C}(X)$ ist transzendent über $\mathbb{C}$, denn kein Polynom in $\mathbb{C}$ hat $X$ als Nullstelle.
- Die Eulerzahl $e$ ist transzendent über $\mathbb{Q}$ (*Satz von Hermite*)
- Die Kreiszahl $\pi$ ist transzendent über $\mathbb{Q}$ (*Satz von Lindemann*)
- $i$ ist algebraisch über $\mathbb{Q}$ mit Minimalpolynom $p=X^{2}+1$.
- Sei $X^{n}-d\in K[X]$ [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzibel]]. Dann ist die Adjunktion $K(\sqrt[n]d)$ einer Nullstelle von $X^{n}-d$ eine Erweiterung von $K$ von [[#Grad|Grad]] $n$, denn $X^{n}-d$ Minimalpolynom

#### algebraische und transzendente Erweiterungen
Eine Körpererweiterung $L/K$ heißt **algebraisch**, wenn jedes $a \in L$ [[#algebraische und transzendente Elemente|algebraisch]] über $K$ ist. Sonst heißt sie **transzendent**. 

## Endliche Erweiterungen
Sei $L/K$ eine Körpererweiterung. Dann ist äquivalent:
1) $L/K$ ist endlich d.h. $[L:K]<\infty$
2) $L/K$ ist von endlich vielen Elementen [[#Erzeugte Körper|erzeugt]] und [[#algebraische und transzendente Elemente|algebraisch]].
3) Es gibt [[#algebraische und transzendente Elemente|algebraische]] $x_{1},...,x_{m}\in L$, sodass $L=K(x_{1},...x_{m})$
###### Beweis
$1 \implies 2$:
Sei $a \in L$. Dann gilt $K(a) \subseteq L$ also $[K(a):K]\leq[L:K]< \infty$. Durch Wahl einer endlichen Basis $\set{a_{1},...,a_{n}}$ von $L/K$ folgt auch $L=K(a_{1},...,a_{n})$.

$2 \implies 3$:
folgt direkt, weil $L/K$ von endlich vielen Elementen erzeugt ist.

$3 \implies 1$:
Führe Induktion nach $m$:
*Induktionsanfang:* $m=1$. Dann existiert ein $p\neq 0$ mit $p(x_{1})=0$ und es folgt mit der [[#Charakterisierung von einfachen Körpererweiterungen]], dass $[K(x_{1}):K]<\infty$.

*Induktionsschluss* $m-1 \leadsto m:$
Es gilt $L=K(x_{1},...,x_{m-1})(x_m)$. Außerdem existiert ein $p \neq 0 \in K[X]$ mit $p(x_{m})=0$. Außerdem ist $p \in K(x_{1},...,x_{m})[X]$. Damit wissen wir nach Begründung im Induktionsanfang:$$[K(x_{1},...,x_{m}):K(x_{1},...,x_{m-1})]<\infty$$und wegen [[#Gradsatz]] folgt die Behauptung mit der Induktionssvoraussetzung.

### algebraische Teilkörper und Verknüpfungen von algebraischen Elementen
1) Seien $L/K$ und $A/L$ [[#algebraische und transzendente Erweiterungen|algebraisch]]. Dann gilt $A/K$ ist algebraisch
2) Sei $L/K$ eine beliebige Körpererweiterung. Die Teilmenge $A \subset L$ aller über $K$ [[#algebraische und transzendente Elemente|algebraischer Elemente]] ist ein [[Körper#Teilkörper|Teilkörper]] von $L$.

Konkret bedeutet das, dass Verknüpfungen von algebraischen Elementen mit unter $n$-ten Wurzeln, Addition Multiplikation und Division abgeschlossen ist, also z.B. $\sqrt{\frac{\sqrt[3]{2} - \sqrt[7]2}{5+\sqrt{7}}}$ über $\mathbb{Q}$ algebraisch ist.  

###### Beweis
1) Sei $\alpha \in A$. Dann finden wir ein Polynom $c_{0}+c_{1}X+...+c_{m-1}X^{m-1} + X =: q \in L[X]$ mit $q(\alpha)=0$ und $c_{i}\in L$, die insbesondere algebraisch sind.
	Wir haben nun zu zeigen, dass $[K(a) : K]< \infty$. Dazu wissen wir wegen obigem [[#Endliche Erweiterungen|Satz]], dass $[K(c_{1},...,c_{m-1}):K]<\infty$. Insbesondere ist $\alpha$ auch algebraisch über $K(c_{1},...,c_{m-1})$, weil $q \in K(c_{1},...,c_{m-1})[X]$.
	Dann ist also $$[K(c_{1},...,c_{m-1})(\alpha): K(c_{1},...,c_{m-1})]<\infty$$ und wegen [[#Gradsatz]] $$[K(c_{1},...,c_{m-1},\alpha):K]< \infty$$Außerdem ist $K(\alpha)\subset K(c_{1},...,c_{m-1},\alpha)$ hat also über $K$ eine Dimension $< \infty$. Damit ist $\alpha$ algebraisch.

2) Seien $a,b \in A$. Dann gilt $K(a,b)$ ist mit dem Satz über [[#Endliche Erweiterungen|endliche Erweiterungen]] algebraisch. Insbesondere ist also $a-b \in K(a,b) \subset A$ und für $b \neq 0$ auch $\frac{a}{b} \in K(a,b)\subset A$. Außerdem gilt $K \subset A$, also ist $0,1 \in A$ und $A$ damit ein Teilkörper von $L$.
### Erweiterungen von Grad 1 und 2
Sei $L/K$ eine Erweiterung von [[#Grad]] 1 oder 2:
- Wenn $[L:K]=1$ gilt $L=K$ und das Minimalpolynom für jedes $a \in L$ ist $x-a \in K[X]$.
- Wenn $[L:K]=2$ und [[Körper#Charakteristik|Charakteristik]] von $K$ nicht $2$, dann existiert ein $d\in K$ mit $L=K(\sqrt{d})$.

>[!info] Charakteristik 2
> Betrachte $p=X^{2}+X+1\in \mathbb{F}_{2}[X]$, was in $F_{2}$ irreduzibel ist, denn $1^{2}+ 1 + 1 = 1$ und $0^2+0+$. Sei $\alpha$ eine abstrakte Nullstelle von $p$. Dann ist $[K(\alpha):K]=2$ aber da $0^{2}=0, 1^{2}=1$ jede Wurzel von $\mathbb{F}_{2}$ schon im Körper.


###### Beweis
- Gleichheit wegen Monotonie der Dimensionen aus LA. Das Minimalpolynom ist klar.
- Sei $a \in L\setminus K$. Dann ist wegen [[#Gradsatz]] $2 = [L:K]  \geq [K(a):K]$. Dann ist $a$ [[#algebraische und transzendente Elemente|algebraisch]] und das [[#Minimalpolynom]] also von $a$ hat höchstens Grad 2 und - da $a \not \in K$ - mindestens Grad 3.  Wir finden also $p=X^{2}+s\cdot X + t \in K[X]$ mit $p(a)=0$. Da die Charakteristik $\neq 2$ ist können wir quadratisch ergänzen und durch 2 bzw. Potenzen von 2 teilen. $$\begin{align}&0=a^{2}+s\cdot a+t\overset{\text{quadr. Ergänzung}}=(a+\frac s 2)^{2}+(t-\frac{s^{2}}{4})\\ \iff &(\underbrace{a+\frac s 2 }_{=:b})^{2}=\underbrace{\frac{s^{2}}4-t}_{=:d}\end{align}$$Es gilt $b \in K\setminus L$ und für $q=X^{2}-d$ gilt $q(b)=0$ und $q$ ist das Minimalpolynom von $b$ über $K$, denn einen kleineren Grad kann es nicht haben, sonst wäre $b\in K$. Damit folgt die Behauptung wegen Monotonie der Dimensionen aus LA.

## Zerfällungskörper
Sei $P\in$[[Polynomringe|$K[X]$]] beliebig. Dann heißt ein Erweiterungskörper $L$ von $K$ **Zerfällungskörper**, von $P$, wenn $P$ in Linearfaktoren in $L[X]$ zerfällt, also:$$P(X)=c\cdot\prod_{i=1}^{n}(X-a_{i}),\quad c,a_{1},...,a_{n}\in L$$und außerdem $$L=K(a_{1},...,a_{n})$$gilt.

### Beispiele
- $P=X^{2}+1$ zerfällt in $\mathbb{Q}(i)$ in Linearfaktoren, denn $-i\in \mathbb{Q}(i)$. 
- $P=X^{3}-2$ hat in $\mathbb{C}$ die Nullstellen $\sqrt[3]2, e^{\frac{2\pi i}{3}}\cdot  \sqrt[3]2, e^{\frac{2\cdot 2\pi i}{3}}\cdot  \sqrt[3]2$, allerdings gilt $\mathbb{Q}(\sqrt[3]2)\subseteq \mathbb{R}$ also sind die beiden komplexen Nullstellen nicht in $\mathbb{Q}(\sqrt[3]2)$ und $P$ zerfällt in diesem Körper nicht in Linearfaktoren
- Sei $P\in K[X]$ [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzibel]] von [[Polynomringe#Grad|Grad]] $n$ und sei $L=K(\alpha)$ außerdem eine [[#Minimalpolynom|Erweiterung von K durch Adjunktion einer Nullstelle von $P$]]. Dann ist $P\in L[X]$ Produkt eines Linearen Faktors $(X-\alpha)$ und eines Polynoms $Q\in L[X]$ von Grad $n-1$. $Q$ kann reduzibel sein oder auch nicht.

### Grad und Eindeutigkeit von Zerfällungskörpern
Sei $P\in K[X]$ mit $grad(P)=n\geq 1$.
- Dann existiert ein Zerfällungskörper $L$ von $P$ über $K$ mit [[#Grad|$[L:K]$]]$\leq n!$. 
- Ist $L'$ ein anderer Zerfällungskörper von $P$, so gibt es einen Isomorphismus $$\begin{gather}\Phi:L \rightarrow L'\\\forall k\in K: \Phi(k)=k \end{gather}$$
###### Beweis
Die Eindeutigkeit werden wir hier nicht beweisen. Für 1) führen wir starke Induktion über $n$:

*Induktionsanfang:* $n=1$
Dann ist $P=X-a$ und $K(a)=K$ ein Zerfällungskörper von $P$ über $K$.

*Induktionsschluss:*
**Fall**: $P$ ist irreduzibel:
Sei $\alpha$ eine (abstrakte) Nullstelle von $P$ und $L:= K(\alpha)$. Dann [[#Minimalpolynom|gilt]] $[L:K]=n$, denn $grad(P)=grad(p_\min)$. Außerdem existiert ein $q \in L[X]$ mit $P=(X-\alpha)\cdot q$ und $grad(q)\leq n-1$. 

Nach Induktionsvoraussetzung existiert ein Zerfällungskörper $A=L(\alpha_{2},...,\alpha_n)$ von $q$ mit $[A:L]\leq(n-1)!$, wobei $\alpha_{1},...,\alpha_{n}$ die Nullstellen von $q$ also von $P$ sind. Insbesondere zerfällt $P$ in $A$ in Linearfaktoren. Dann gilt wegen [[#Gradsatz]]$$[A:K]=[A:L]\cdot[L:K]\leq(n-1)!\cdot n=n!$$
**Fall**: $P$ ist reduzibel:
 Sei $\alpha\not\in K$ eine Nullstelle von $P$ und $L:= K(\alpha)$. Dann [[#Minimalpolynom|gilt]] $[L:K]<n$, denn $grad(P)> grad(p_\min)$, da $P$ reduzibel. Damit folgt der Rest wie im ersten Fall.

## Satz vom primitiven Element
Sei $L/K$ eine Körpererweiterung. Dann gilt:
- Wenn $\lvert L\rvert< \infty$, dann ist die Erweiterung [[#einfache Körpererweiterungen|einfach]]. 
- Wenn $L/K$ eine [[#Endliche Erweiterungen|endliche Erweiterung]] ist und $K$ [[Körper#Charakteristik|Charakteristik]] 0 hat, so ist die Erweiterung einfach.

###### Beweis
1) folgt aus der [[Körper#Klassifikation endlicher Körper|Klassifikation endlicher Körper]], denn $L=\mathbb{F}_{p}(\alpha)$ impliziert $L=K(\alpha)$.
2) werden wir hier nicht beweisen.

