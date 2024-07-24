Für einen [[Kommutative Ringe|Ring]] $R$ ist der Polynomring $$R[X]:= \{\sum\limits_{i=0}^{\infty}a_{i}X^{i}: a_{i}\in R, \exists n_{0}\in \mathbb{N}: \forall n \geq n_{0}: a_{n}=0\}$$mit der natürlichen Addition und Multiplikation (ausmultiplizieren und zusammenfassen) wieder ein Ring. Oft identifizieren wir $R$ mit den Konstanten in $R[X]$. 

##### Polynomringe von Integritätsbereichen.
Sei $R$ [[Kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereich]]. Dann gilt
- $R[X]$ Integritätsbereich
- Die Gruppe der [[Kommutative Ringe#Einheiten|Einheiten]] ist genau $(R[X])^{*} = R^{*}$ 

##### Grad
Für ein Polynom $p = \sum\limits_{i=0}^{\infty}a_{i}X^{i}$ ist der **Grad** von $p$ definiert als $grad(p) = \sup \{n\in \mathbb{N}: a_{n} \neq 0\}$ also insbesondere $grad(0) = - \infty$

###### Rechenregeln
- $grad(f\cdot g) \leq grad(f) + grad(g)$. Für $R$ [[Kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereich]] gilt hier Gleichheit. 
- $grad(f+g) \leq \max\set{grad(f),grad(g)}$ 

### Einsetzungshomomorphismus
Man sieht formal Polynome nicht als Funktionen an, denn auf endlichen [[Körper|Körpern]] gibt es zwar unendlich viele Polynome, aber nur endlich viele Funktionen. Trotzdem ist mit den folgenden Dingen ein Polynom auch als Funktion "benutzbar":

Für einen [[Kommutative Ringe#Teilringe|Teilring]] $R$ eines [[Kommutative Ringe|kommutativen Rings]] $L$ und $a \in L$ ist die **Einsetzung von a** $$\varphi ^{a}:R[X] \rightarrow L, \varphi^{a}\left(\sum\limits b_{i}X^{i}\right):= p(a):=\sum\limits b_{i}a^{i}$$ein [[Ringhomomorphismen|Ringhomomorphismus]].

Seien $L,R$ weiterhin wie oben. Dann ist der **Einsetzungshomomorphismus** $$\mathcal{E}:R[x] \rightarrow \set{f:L \rightarrow L}, \mathcal{E}(p)(a):= \varphi^{a}(p) = p(a)$$ein Ringhomomorphismus. 


#### Eigenschaften
In einem [[Kommutative Ringe|Integritätsbereich]] $R$, gilt für $0 \neq p \in R[X]$, wenn $grad(p) < \#R$, dann ist $\mathcal{E}(p)\neq 0$. Das ergibt sich wegen dem Abschnitt zu [[#Teilbarkeit]].

Außerdem ist in einem Integritätsbereich $R$ injektiv $\iff$ $\#R = \infty$   


## Polynomdivision mit Rest 
Sei $\mathbb{K}$ ein [[Kommutative Ringe#Körper|Körper]]. Dann ist $\mathbb{K}[X]$ mit Grad als Euklidische Normfunktion ein [[Euklidische Ringe|Euklidischer Ring]], also insbesondere ein Hauptidealring und faktoriell.
#### Beweis / Konstruktion
Seien $a = \sum\limits_{i=1}^{n}a_{i}X^{i}, b = \sum\limits_{i=1}^{m}b_{i}X^{i}$ mit $a \neq 0$ und $grad(a) = n, grad(b) = m$

Halte $a$ fest und mache starke Induktion nach $m$.

**Fall** $m < n$ (deckt auch Induktionsanfang ab):
	Dann setze $q = 0, r=b$ und erhalte $b = qa + r$ mit $grad(r)< grad(a)$

**Fall** $m \geq n$ 
	Dann schreibe $b = b_{n}X^{n}+ \tilde{b}$, $grad(\tilde{b}) < m$. Da $a_{n} \neq 0$ konstruiere$$b_{n}X^{n} = a\cdot\left(\frac{b_{m}}{a_{n}}X^{m-n}\right)- \sum\limits_{i=0}^{m-1} \frac{b_{m}}{a_{n}}X^{m-n+i} = a\cdot\left(\frac{b_{m}}{a_{n}}X^{m-n}\right) - \tilde{\tilde{b}}$$Also ist $b=a\cdot\left(\frac{b_{m}}{a_{n}}X^{m-n}\right) + (\tilde{b}-\tilde{\tilde{b}})$. Da aber $grad(\tilde{b}-\tilde{\tilde{b}})<m$ verwende Induktionsvorraussetzung. Es existieren also $q,r$ mit $grad(r)<n$, sodass$$\tilde{b}-\tilde{\tilde{b}} = qa+r$$ Also ist $$b=a\cdot\left(\frac{b_{m}}{a_{n}}X^{m-n} + q\right)+r$$

> [!Book] Anmerkung
> Sofern $a_{n}$ eine Einheit ist funktioniert der Beweis auch für [[Kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereiche]] generell.


## Teilbarkeit
Sei $R$ ein [[Kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereich]], $a \in R$ und $0\neq p \in R[X]$. Dann gilt
1) $(X-a) \mid p \iff p(a) = 0$
2) $p$ hat höchstens $grad(p)$ Nullstellen
3) Ist $p$ [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzibel]], mit $grad(p) > 1$, dann $p(a) \neq 0$
4) $grad(p)=1 \implies$ p [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzibel]]
5) Sei $grad(p) \in \set{2,3}$. Dann ist $p$ irreduzibel $\iff$ $p$ hat keine Nullstellen
###### Beweis
1) Wegen der Anmerkung in dem [[#Beweis / Konstruktion|Beweis von Polynomdivision mit Rest in Körpern]] und weil $1$ eine Einheit ist, können wir $p$ mit Rest durch $1X - a$ teilen. Es existieren also $q,r \in R[X]$ mit $p=qa+r$ und $grad(r)< 1$ also $r \in R$. Wegen $p(a) = q(a)(a-a)+r = r$ ergibt sich folgende Äquivalenzkette$$p \text{ durch } X-a \text{ teilbar} \iff r = 0 \iff p(a)=0$$
2) Mache eine Induktion nach $grad(p)$
	**Induktionsanfang** Für $grad(p) = 0$ hat $p$ keine Nullstellen
	**Induktionsschluss** Ist $p(a) = 0$, dann ist $p = q(X-a)$ bzw. $\forall x \in R$ $p(x)= q(x)(x-a)$. Da wir in $R$ in einem Integritätsbereich sind ist $p(x) = 0 \iff q(x) = 0 \lor x-a = 0$. Die zweite Bedingung ist genau für ein $x \in R$ erfüllt, für die erste Bedingung können wir die Induktionsvorraussetzung anwenden, denn wegen den [[#Rechenregeln|Rechenregeln für den Grad]] gilt $grad(q) = grad(p) - 1$. Also hat $q$ höchstens $grad(p)-1$ Nullstellen.

3) Gilt, denn Einheiten sind genau $x\in R$ und wegen Rechenregeln für Grad.
4) Wegen Rechenregeln für Grad muss immer mindestens eine Einheit bei Teilern beteiligt sein.
5) Beweise $p$ nicht irreduzibel $\iff$ $p$ hat Nullstelle: 
	"$\Leftarrow$" wegen 3)
	"$\implies$" Dann sei $p = p_{1}p_{2}$ mit $p_{1},p_{2}$ keine Einheiten. Dann hat $p_{1}$ oder $p_{2}$ Grad 1 und eine Nullstelle $\implies$ $p$ hat Nullstelle

## Polynome mit mehreren Variablen
Induktiv definiert man den **Ring der Polynome in n Variablen über $R$** mit
$R[X_{1}, \dots , X_{n}] := R[X_{1}, \dots, X_{n-1}][X_{n}]$ 
###### Beispiel
Ein Element aus $\mathbb{Z}[X_{1},X_{2}]$ ist $(2X_{1}^{2}+3X_{1})\cdot X_{2}^{3} - 1 = 2X_{1}^{2}X_{2}^{3}+3X_{1}X_{2}^{3}-1$  

##### Eigenschaften
- Wenn $R$ [[Kommutative Ringe#faktorielle Ringe|faktoriell]] ist wegen [[Quotientenkörper#Polynomringe von faktoriellen Ringen mit Quotientenkörper|Quotientenkörpern]] induktiv auch $R[X_{1},\dots, X_{n}]$ faktoriell.
## Komplexe und reele Polynome
### Fundamentalsatz der Algebra
Es gilt $p\in \mathbb{C}[x]$ irreduzibel $\iff$ $grad(p)=1$ und weil $\mathbb{C}[x]$ [[Kommutative Ringe#faktorielle Ringe|faktoriell]] (weil es ein [[#Polynomdivision mit Rest|euklidischer Ring]] ist), ist jedes $p\in \mathbb{C}[x]$ mit $grad(p)\geq 1$ ein Produkt von Polynomen mit Grad 1.

### Polynome ungeraden Grades
Jedes $p\in \mathbb{R}[x]$ mit ungeradem Grad hat eine Nullstelle.
###### Beweis
Es gilt für $p$, dass $\lim_{x\to\infty} p(x) = \pm \infty$ und $\lim_{x\to-\infty}p(x) = \mp \infty$. Daraus folgt, da $\mathcal{E}(p)$ stetig ist wegen dem Zwischenwertsatz, dass ein $y\in \mathbb{R}$ existiert, sodass $p(y)=0\in (-\infty, + \infty)$

### irreduzible Polynome in $\mathbb{R}[x]$ 
Jedes [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzible]] Polynom $p \in \mathbb{R}[x]$ hat $grad(p) \in \set{1,2}$.
###### Beweis
Sei $p \in \mathbb{R}[x]$ mit $grad(p)>2$ irreduzibel, hat also wegen [[#Teilbarkeit|der Aussage über irreduzible Polynome]] keine reelle Nullstelle.
Da $p \in \mathbb{C}[x]$ folgt es ex. $\alpha \in \mathbb{C}\setminus{\mathbb{R}}$ mit $p(\alpha)=0$ wegen dem [[#Fundamentalsatz der Algebra]].
$\implies 0 = p(a)^{*}=\sum\limits_{i=0}^{m}p_{i}^{*}\cdot(\alpha^{*})^{i} = p(\alpha^{*})$ wobei $^*$ das komplex konjugierte meint und wir dessen Eigenschaften nutzen (wobei $p_{i}\in \mathbb{R}$).
Insgesamt erhalten wir so, dass $p$ in $\mathbb{C}[x]$ durch $(X-\alpha)\cdot(X-\alpha^{*}) = (X^{2}-2\text{Re}(\alpha)X + \vert \alpha\vert^{2})=: q\in \mathbb{R}[X]$ teilbar ist also ein $r \in \mathbb{C}[X]$ existiert, sodass $\forall x\in \mathbb{R} : p(x) = q(x)r(x)$ also auch $(p(x))^{*} = (q(x)r(x))^{*}= q(x)(r(x))^{*}\in \mathbb{R}$
$\implies r(x)^{*}=r(x)$ also $r(x)\in \mathbb{R}$ also $r\in \mathbb{R}[X]$. Insbesondere also $q \mid p$ in $\mathbb{R}[X]$. 

Da $p$ irreduzibel und die [[Kommutative Ringe#Einheiten|Einheiten]] genau $f$ mit $grad(f)=0$ sind folgt $grad(p)=grad(q)> 2$ was aber ein Widerspruch ist, da $grad(q)=2$. 



## Ganzzahlige Polynome
### Primitive Polynome
Wir nennen $p\in \mathbb{Z}[X]$ **primitiv**, wenn 1 der [[kommutative Ringe#Nullteiler und Integritätsbereiche|größte gemeinsame Teiler]] der Koeffizienten von $p$ ist. 
##### Eigenschaften
- Jedes Polynom $0\neq p \in \mathbb{Z}[X]$ ist ein Produkt von $d\in \mathbb{Z}$ und einem primitiven $p_{0}\in \mathbb{Z}[X]$, wenn man $d$ als den $ggT$ der Koeffizienten von $p$ wählt.
- $p$ ist primitiv $\iff$ $p$ wird durch keine Primzahl geteilt (wegen Eigenschaften von faktoriellen Ringen)
- $p=r\cdot q\in \mathbb{Z}[X]$ ist primitiv $\iff$ $r$ und $q$ primitiv
###### Beweis
"$\Rightarrow$" Kontraposition. Sei o.B.d.A. $r$ nicht primitiv, also $r=\lambda \hat r$ mit $\lambda \in \mathbb{Z}$ keine Einheit. Dann teilt aber $\lambda$ auch alle Koeffizienten in $p=\lambda \cdot\hat r\cdot q$ also ist $p$ nicht primitiv.

"$\Leftarrow$" Kontraposition. Sei $p$ nicht primitiv. Dann existiert eine Primzahl $a\in \mathbb{Z}$, sodass $a\mid p$. Betrachte $p = \sum\limits_{k=0}^{m+n}p_{k}X^{k}=r\cdot q \mod a$, wobei $r = \sum\limits_{i=0}^{m}r_{i}X^{i}$ und $q =\sum\limits_{j=0}^{m}q_{j}X^{j}$ . Da [[Faktorringe|die Projektion auf den Faktorring $\mathbb{Z}/a\mathbb{Z}$]] ein [[Ringhomomorphismen|Ringhomomorphismus]] ist, ist $\mathbb{Z}[X] \rightarrow \mathbb{Z}/a\mathbb{Z}[X], \sum\limits_{i=0}^{n}b_{i}X^{i} \mapsto \sum\limits_{i=0}^{n}\overline{b_{i}}X^{i}$ 
auch eine, also ist:$$0=\sum\limits_{k=0}^{m+n}\overline{c_{k}}X^{k}=\overline r\cdot\overline q$$Da allerdings $\mathbb{Z}/a\mathbb{Z}$ ein [[Körper]], also insbesondere ein [[kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereich]] ist, ist der zugehörige Polynomring auch ein Integritätsbereich, also $\overline r=0$ oder $\overline q=0$. D.h. $a$ teilt alle Koeffizienten von $r$ oder von $q$ also ist $r$ oder $q$ nicht primitiv.
#### Zusammenhang zu $\mathbb{Q}[X]$ 
$p\in \mathbb{Z}[X]$ primitiv ist [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzibel]] $\iff$ $p$ in $\mathbb{Q}[X]$ irreduzibel. 

Insbesondere kann man bei [[#Polynomdivision mit Rest]] beim Überprüfen, ob etwas irreduzibel ist, in $\mathbb{Q}[X]$ teilen.
###### Beweis
 "$\Leftarrow$" 
Sei $p= p_{1}p_{2}\in \mathbb{Z}[X]$ mit $p_{1},p_{2}\in \mathbb{Z}[X]$. Ist $grad(p_{1}), grad(p_{2})> 0$ ist $p$ reduzibel in $\mathbb{Q}[X]$, also ist $grad(p_{1})=0$ oder $grad(p_{2})=0$ und $p_{1}$ oder $p_{2}$ Einheiten in $\mathbb{Z}$ oder $p$ ist nicht primitiv.

"$\Rightarrow$"
Sei $p=p_{1}p_{2}\in \mathbb{Z}[X]$ mit $p_{1}, p_{2} \in \mathbb{Q}[X]$. Dann gilt wir können $p_{i}$ schreiben als $\frac{m_{i}}{n_{i}}q_{i}$ mit $m_{i},n_{i} \in \mathbb{Z}$ und $q_{i}\in \mathbb{Z}[X]$ primitiv. (Das funktioniert durch erweitern der Brüche und Nenner nach vorne ziehen. Dann bringt man noch den $ggT$ der Koeffizienten nach vorne.)
Wir erhalten also $p=\frac{m_{1}m_{2}}{n_{1}n_{2}}q_{1}q_{2}$. Da $q_{1}q_{2}$ und $p$ primitiv sind, gilt $\frac{m_{1}m_{2}}{n_{1}n_{2}}=\pm 1$. Insbesondere ist also $p=\pm q_{1}q_{2}$ und damit $q_{1}$ oder $q_{2}$ eine Einheit in $\mathbb{Z}[X]$ also $p_{1}$ oder $p_{2}$ eine Einheit in $\mathbb{Q}[X]$, also $p$ in $\mathbb{Q}[X]$ irreduzibel.  

### $\mathbb{Z}[X]$ ist faktoriell
1) Ist $p\in \mathbb{Z}[X]$ irreduzibel und $grad(p)>0$, so ist $p$ primitiv und prim.
2) Jedes $p\in \mathbb{Z}[X]$ ist ein Produkt einer ganzen Zahl und irreduzibler $p_{i}\in \mathbb{Z}[X]$
3) $\mathbb{Z}[X]$ ist faktoriell
4) Die Primelemente von $\mathbb{Z}[X]$ sind die Primzahlen in $\mathbb{Z}$ und die primitiven Polynome, die in $\mathbb{Q}[X]$ irreduzibel sind

#### Beweis
###### 1)
*Annahme* $p$ nicht primitiv. Dann $p= a\cdot\tilde{p}$, mit $a\in \mathbb{Z}$ keine Einheit in $\mathbb{Z}$ und $\tilde{p}$ keine Einheit in $\mathbb{Z}[X]$ (wegen Grad). Dann ist aber $p$ nicht irreduzibel  ↯

*z.Z. $p$ prim* Seien $p_{1},p_{2}\in \mathbb{Z}[X]$, sodass $p\mid p_{1}p_{2}$ in $\mathbb{Z}[X]$, also insbesondere auch $p\mid p_{1}p_{2}$ in $\mathbb{Q}[X]$. Aber da $\mathbb{Q}[X]$ ein [[Euklidische Ringe|Euklidischer Ring]] ist, wegen [[#Polynomdivision mit Rest]], ist $\mathbb{Q}[X]$ [[Kommutative Ringe#faktorielle Ringe|faktoriell]] also insbesondere $p$ prim in $\mathbb{Q}[X]$. Dann gilt aber insbesondere es ex. ein $f\in \mathbb{Q}[X]$ s.d. $p\cdot f = p_{1}$ oder $p\cdot f = p_{2}$. 

Schreibe nun $f=\frac{m}{n}\cdot \hat f$, mit $\hat f\in \mathbb{Z}[X]$ primitiv. Dann ist $\frac m n (p\cdot \hat f)= p\cdot f = p_{i}\in \mathbb{Z}[X]$, aber da $(p\cdot \hat f)$ als Produkt primitiver Elemente primitiv, teilt $n \mid p\cdot \hat f$ nur, wenn $n$ eine Einheit ist, also gilt $\frac{m}{n}\in \mathbb{Z}$ also $f\in \mathbb{Z}[X]$ und damit teilt $p$ in $\mathbb{Z}[X]$ auch $p_{1}$ oder $p_{2}$, ist also prim

###### 2)
Zerlege in $\mathbb{Q}[X]$, da faktoriell und zerlege in primitive Zahlen und Faktoren. Dann Faktoren in $\mathbb{Z}$ wie in [[#1)]] 

###### 3)
folgt direkt mit 1), 2) und 4) wegen [[Kommutative Ringe#faktorielle Ringe#Äquivalente Darstellung|Äquivalenz]] und Zerlegung in $\mathbb{Z}$. 

###### 4)
Folgt wegen 1) und [[#Zusammenhang zu $ mathbb{Q}[X]$]] 

### Kriterium von Eisenstein
Sei $p=\sum\limits_{i=0}^{n}c_{i}X^{i}\in \mathbb{Z}[X]$ mit $grad(p)\geq 1$ und sei $r\in \mathbb{Z}$ [[Kommutative Ringe#Prim- und irreduzible Elemente|prim]] mit 
- $r\not\mid c_{n}$
- $r\mid c_{i}$ für $0\leq i \leq n-1$ 
- $r^{2}\not\mid c_{0}$

Dann gilt $p$ ist irreduzibel in $\mathbb{Q}[x]$.
##### Beweis
Es gilt in $\mathbb{Q}[X]$ ist $p$ eine Einheit $\iff grad(p) = 0$, also ist hier $p\neq 0$ keine Einheit.

Wie in [[#Primitive Polynome#Eigenschaften#Beweis| dem Beweis von Produkten primitiver Polynome]] betrachte $p=p_{1}p_{2} \mod r$. 
Dann gilt $\sum\limits_{i=0}^{n}\overline c_{i} X^{i} = \overline c_{n}X^{n}=\overline c_{n}\cdot X\cdot \cdot \dots \cdot X$ Zerlegung in Primelemente und Einheit, die eindeutig ist, da wir uns als [[Euklidische Ringe|Euklidischer Ring]] $\mathbb{Z}/r \mathbb{Z}[X]$ in einem [[Kommutative Ringe#faktorielle Ringe|faktoriellem Ring]] befinden. Wegen der Eindeutigkeit folgt $\overline p_{1}=\overline a_{m} X^{m}$ und $\overline p_{2} = \overline b_{n}X^{n}$. Wären sowohl $n,m \neq 0$ also $p_{1},p_{2}$ keine Einheiten in $\mathbb{Q}[X]$, dann gilt $r\mid a_{0}, b_{0}$ und damit $r^{2} \mid a_{0}\cdot b_{0}= c_{0}$, was ein Widerspruch wäre. Also muss $p_{1}$ oder $p_{2}$ eine Einheit in $\mathbb{Q}[X]$ sein und damit $p$ irreduzibel.

#### Beispiel
Sei $p$ eine Primzahl und $P = X^{p}-1 \in \mathbb{Z}[X]$. Dann gilt $P =T \cdot (X-1)$ mit $$T = X^{p-1}+X^{p-2}+\dots+1$$Dann ist aber $T\cdot (X-1)$ schon die Zerlegung in irreduzible Elemente in $\mathbb{Q}[X]$.
###### Beweis
Da $(X-1)$ irreduzibel verbleibt zu zeigen, dass $T$ irreduzibel ist. Dazu genügt es zu zeigen, dass $\tilde T := (X+1)^{p-1} + \dots + 1$ also $\tilde T(x) = T(X+1)$ irreduzibel ist. Denn wäre $\tilde T = QV$ eine Zerlegung in nicht-Einheiten, so wäre $Q(X-1)\cdot V(X-1)$ eine Zerlegung für $T$ aus nicht-Einheiten, da sich der Grad durch einsetzen hier nicht verändert.

Es gilt $\tilde T(x) = P(x+1)/x$, also $\tilde T$ quasi $P(X+1)$, nur dass die Koeffizienten um 1 "nach rechts verschoben" werden. Es gilt:
$$P(x+1) = (x+1)^{p}-1 = \left(\sum\limits_{i=0}^{p}\binom p i X^{i}\right)  - 1 = \sum\limits_{i=1}^{p}\binom p i X^{i}$$

Also ist $\tilde T = \sum\limits_{i=0}^{p-1}\binom {p} {i+1} X^{i}$ und dementsprechend hat $\tilde T$ Leitkoeffizient $1$ und alle anderen Koeffizienten sind durch $p$ teilbar, da $p$ Primzahl und wenn man $\binom p {i+1}$ expandiert unter dem Bruchstrich für $i \neq p-1$ nicht $p$ nicht den Nenner teilt, aber den Zähler. Außerdem ist $\binom {p}{1} = p$ und dementsprechend ist nach [[#Kriterium von Eisenstein]] $\tilde T$ irreduzibel.
### Nullstellen von Polynomen mit Leitkoeffizient 1
Sei $p=X^{n}+\sum\limits_{i=0}^{n-1}c_{i}X^{i}\in \mathbb{Z}[X]$. Dann gilt:
	$s \in \mathbb{Q}$ Nullstelle von $p$ $\implies$ $s \in \mathbb{Z}$ und $s \mid c_{0}$

###### Beweis
Sei $\frac{a}{b} \in \mathbb{Q}\setminus \mathbb{Z}$ eine Nullstelle von $p$ und o.B.d.A. $\frac{a}{b}$ maximal gekürzt.
Dann gilt $\mathbb{Z} \ni 0 = p(\frac{a}{b})= p(\frac{a}{b})(b^{n-1}) = \frac{a^{n}}{b} + b^{n-1}\left(\sum\limits_{i=0}^{n-1} c_{i}\left(\frac{a}{b}\right)^i \right)$
Da der rechte Summand in $\mathbb{Z}$, aber $\frac{a^{n}}{b}\not\in \mathbb{Z}$ entsteht ein Widerspruch.


Sei $s \in \mathbb{Z}$ mit $p(s)=0$.  Dann ist aber $c_{0} = - (s^{n}+ \sum\limits_{i=1}^{n-1}c_{i}s^{i})$ und wird durch $s$ geteilt.