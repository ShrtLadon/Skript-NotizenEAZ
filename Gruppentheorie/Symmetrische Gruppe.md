Die symmetrische Gruppe ist für eine Menge $X$ gegeben durch $$S_{(X)}=(\set{f:X \rightarrow X \quad:\quad \text{f ist bijektiv}},\circ)$$für $X=\set{1,...,n}$ mit $n \in \mathbb{N}$ nennt man $S_{(X)}$ auch $S_{(n)}$  

# Wiederholung aus der Linearen Algebra
Das nachfolgende wird größtenteils ohne Beweis eingeführt, dafür ist ein ein LA-Skript zu schauen:

- Es gilt $\lvert S_{n}\rvert=n!$
- Für $n>2$ ist $S_{n}$ nicht abelsch.

### Schreibweisen
Für eine $g\in S_{n}$ kann man $g$ schreiben als $\begin{pmatrix}1 & 2 & ... & n\\g(1) & g(2) & ... & g(n)\end{pmatrix}$. Alternativ gibt es noch die Zyklenschreibweise bestehend aus Tupeln $(x, g(x),...,g^i(x))$ mit paarweise unterschiedlichen Einträgen, sodass $g^{i+1}(x)=x$, wobei man oft noch Tupel der Länge 1 weglässt.
Ein Beispiel ist $g=\begin{pmatrix}1 & 2 & 3 & 4 & 5 & 6\\3 & 4 & 1 & 5 & 2& 6\end{pmatrix}=\begin{pmatrix}1 & 3\end{pmatrix} \begin{pmatrix}2 & 4 & 5\end{pmatrix}$. 
### Transpositionen
Eine Transposition ist ein $\begin{pmatrix}i & j\end{pmatrix}\in S_{n}$, das genau zwei Elemente vertauscht. Wir können jedes $g\in S_{n}$ als ein Produkt von Transpositionen schreiben. Dabei ist das Produkt nicht eindeutig, aber ob die Anzahl der Transpositionen gerade oder ungerade ist schon.

### Signum
Das Signum $\text{sgn}:S_{n} \rightarrow \set{1, -1}, x \mapsto \begin{cases}1 & \text{g besteht in Darstellung aus gerader Anzahl an Transpositionen}\\-1 & \text{sonst}\end{cases}$ist ein [[Gruppenhomomorphismen|Gruppenhomomorphismus]], wobei $\set{1,-1}$ mit der eindeutigen Gruppenstruktur isomorph zu $\mathbb{Z}/2\mathbb{Z}$ ist.

Wir bezeichnen dabei $\ker \text{sgn}=\mathcal{A_{n}}=\set{g\in S_{n}\mid \text{sgn}(g)=1}$ als *alternierende Gruppe*. Da [[Normalteiler#Beispiele|$\mathcal{A_{n}} \trianglelefteq S_{n}$]] ist $S_{n}/A_{n}\cong \set{-1, 1}$ nach [[Faktorgruppen#Isomorphiesatz|Isomorphiesatz]] (zumindest für $n>1$) und $\lvert \mathcal{A}_{n}\rvert=\frac{n!}{2}$ für $n>1$.
Man kann beobachten, dass ein einzelner Zyklus $(x_{1},...,x_{k})$ in $\mathcal{A_{n}}$ ist $\iff$ $k$ ungerade, denn $(x_{1},...,x_{k})=(x_{1},x_{2})\cdot (x_{2},x_{3})\cdot ...\cdot (x_{k-1},x_{k})$ ist ein Produkt von $k-1$ Transpositionen.

Es gilt $\mathcal{A_{n}}$ wird durch [[#Schreibweisen|Zykel]] der Länge 3 [[Gruppen#Erzeugnis|erzeugt]].
###### Beweis
Wir schauen uns hier nur $n \geq 3$ an, weil wir $n=2$ nur das leere Produkt betrachtet wird.
Es gilt $A_{n}$ wird erzeugt durch Produkte von jeweils 2 Transpositionen also $$(i,j)\cdot(k,l)$$Es gilt erstmal $(a,b,c)=(a,b)\cdot (b,c)$ also ist jeder 3-Zyklus in $\mathcal A_{n}$. Außerdem gilt für im Nachfolgenden paarweise verschiedene Elemente:
- $(a, b)\cdot (a,b)=(a,b,c)\cdot(c,b,a)=id$
- $(a,b)\cdot(a,c)=(a,c,b)$
- $(a,b)\cdot(c,d)=(a,b,c)(b,c,d)$
Also werden alle Möglichen Produkte von 2 Transpositionen auch durch Produkte von 3Zyklen dargestellt.


# Satz von Cayley
Es gilt jede Gruppe ist [[Gruppenhomomorphismen|isomorph]] zu einer Untergruppe einer symmetrischen Gruppe.

###### Beweis
Sei $G$ eine Gruppe und $*:G\times G \rightarrow G$ die [[Gruppenwirkung]] von $G$ auf sich selbst (also $g*h =g\cdot h$). Dann kann man dem einen [[Gruppenhomomorphismen|Gruppenhomomorphismus]] $\rho:G \rightarrow S_{(G)}$ [[Gruppenwirkung#Zusammenhang zu symmetrischer Gruppe|zuordnen]]. 

Sei $g \in \ker \rho$. Dann ist $\rho(g)=Id$, also $g*x=g\cdot x=x$ für alle $x \in G$. Damit ist aber $g=e$ wegen [[#Eigenschaften|der Eindeutigkeit des neutralen Elements]]. Also ist $\ker \rho =\set{e}$ und [[Gruppenhomomorphismen#Eigenschaften|damit]] $\rho$ injektiv. 
Dann ist allerdings $\rho: G \rightarrow \text{Bild}(\rho) \leq S_{(X)}$ ein Isomorphismus auf eine Untergruppe von $S_{(X)}$.

# Verhalten unter Konjugation
Für $g \in S_{n}$ und $h=(x_{1,1}, x_{1,2},...,x_{1,l_{1}}),...,(x_{k,1},...,x_{k,l_{k}})$ in [[#Schreibweisen|Zykelnotation]] gilt die [[Operation durch Konjugation|Konjugation]] ist $$ghg^{-1}=(g(x_{1,1}), g(x_{1,2}),...,g(x_{1,l_{1}})),...,(g(x_{k,1}),...,g(x_{k,l_{k}}))$$Insbesondere sind also die [[Operation durch Konjugation#Konjugationsklassen, Zentralisator und Kern|Konjugationklassen]] genau die Elemente mit der selben Anzahl der jeweiligen selben Zyklenlängen.

##### Beweis/Begründung
Für einen Zyklus $(x_{1},...,x_{k})$ betrachten wir den Zyklus von $ghg^{-1}$ der bei $g(x_{1})$ startet. Dann erhält man genau $(g(x_{1}), g(x_{2}),...,g(x_{k}))$, denn für ein $x_{i}$ gilt $h(x_{i})=x_{i+1}$ (bzw. $x_1$ für $i=k$, da aber analog). Dann ist $(ghg^{-1})(g(x_{i}))=(gh)(x_{i})=g(x_{i+1})$

# Auflösbarkeit
## $n\leq 4$
Für $n\leq 4$ ist $S_{n}$ [[Auflösbare Gruppen|auflösbar]]. 
#### Beweis
Für $S_{1},S_{2}$ sind die [[abelsche Gruppen|Gruppen abelsch]], also [[Auflösbare Gruppen#Beispiele|auflösbar]]. Für $S_{3}$ gilt $S_{3}\cong D_{6}$ zur [[Gruppen#Diedergruppe|Diedergruppe]], die nach dem [[Auflösbare Gruppen#Diedergruppe#Beweis|Beweis]] auflösbar ist. Es verbleibt also zu zeigen, dass $S_{4}$ auflösbar ist.

Dazu gilt die [[#Signum|alternierende Gruppe]] $\mathcal{A}_{4}$ ist ein [[Normalteiler]] von $S_{4}$ und $\lvert A_{4}\rvert=12$. Außerdem gilt für einen Zyklus $(i, j, k, l)$ dass $(i,j,k,l)=(i, j)\cdot (j, k)\cdot (k,l)$ also sind Zyklen der Länge 4 nicht in $A_{n}$, aber $(i, j)(k,l)=(i, j)(k,l)$ wenn $i, j, k$ und $l$ alle paarweise verschieden sind. Wenn $(i,j)=(k,l)$, dann ist das Produkt die Identität (hier ist mit = Gleichheit der Funktionen gemeint!) und wenn o.B.d.A $j=k$ dann ist das Produkt $(i,j,l)$. 

Das heißt $\mathcal{A}_4$ besteht genau aus $(i,j)(k,l)$ und $(i,j,l)$ und natürlich der Identität.
Betrachte nun $\mathcal{K}=\set{(1,2)(3,4), (1,3)(2,4),(1,4)(2,3),1}$ also genau $\mathcal{K}=\mathcal{A}_{4}\setminus\set{(i,j,k)\in \mathcal{A}_{4}}$. Man rechnet leicht (einfach für alle Elemente durchprobieren) nach, dass $\mathcal{K}$ eine [[Gruppen#Untergruppen|Untergruppe]] ist. Da nach [[#Verhalten unter Konjugation]] die Zykellängen erhalten bleiben, ist $g\mathcal{K}g^{-1}=\mathcal{K}$ ein [[Normalteiler]] von $\mathcal{A}_{4}$. 

Wegen dem [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] ist $\lvert \mathcal{A}_{4} / \mathcal{K}\rvert=\frac{12}{4}=3$ was eine [[Primzahlen|Primzahl]] ist. Dementsprechend ist es [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]], was uns genau zeigt, dass ${1}\trianglelefteq \mathcal{K}\trianglelefteq\mathcal{A}_{4}\trianglelefteq S_{4}$ [[Auflösbare Gruppen#Auflösbarkeit endlicher Gruppen|auflösbar]] ist. 
## $n>4$
Für $n> 4$ ist $S_{n}$ gilt:
1) [[#Wiederholung aus der Linearen Algebra#Signum|$\mathcal{A_{n}}$]]$,\set{1}$ und $S_{n}$ sind die einzigen [[Normalteiler|normale]] Untergruppen von $S_{n}$
2) Jede normale Untergruppe von $\mathcal{A_{n}}$ ist entweder $\mathcal{A_{n}}$ oder $\set 1$
3) $S_{n}$ ist nicht [[Auflösbare Gruppen|auflösbar]]. 
#### Beweis
Wir zeigen zunächst, dass aus 2) und folgern damit 1) und danach damit 3). Dazu gilt nach [[#Wiederholung aus der Linearen Algebra#Beweis|Beobachtung]], dass $\mathcal{A_{n}}$ durch Zykel der Größe 3 erzeugt wird. Außerdem sind die [[#Verhalten unter Konjugation|Konjugationsklassen unter $S_{n}$ genau durch Zykellängen gegeben]]. 
##### 2)
Sei $\set e \neq N \trianglelefteq \mathcal{A_n}$ ein [[Normalteiler]]. Wir wollen zeigen, dass dann $N=\mathcal{A_{n}}$ gilt: 

Zunächst beobachten wir dafür dass es nach der obigen Anmerkung reicht zu zeigen, dass alle 3er-Zykel in $N$ liegen. Wir überlegen uns nun, dass es ausreicht sogar nur einen 3er-Zykel in $N$ zu finden: 

Denn wenn $g=(a, b, c)\in N$ existiert, dann gilt nach Beobachtung über Konjugationsklassen für jedes $h=(k,l,n)$, dass ein $\varphi \in S_{n}$ existiert mit $$\varphi g\varphi^{-1}=h$$Wenn $\varphi\in\mathcal{A}_n$ ist, sind wir fertig, da $N$ ein Normalteiler von $\mathcal{A_{n}}$ ist.
Wenn $\varphi \not\in \mathcal{A_{n}}$ ist, dann ist aber durch Multiplikation mit einer weiteren [[#Transpositionen|Transposition]] $$\tilde\varphi=\varphi\cdot(d,e)\in \mathcal{A_{n}}$$wobei $\set{d,e}\cap \set{a,b,c}=\varnothing$ ($n\geq 5$).
Dann ist aber $\tilde\varphi\cdot g\cdot \tilde\varphi^{-1}=\varphi\cdot(d,e)\cdot g \cdot(d,e)^{-1}\cdot \varphi^{-1}=\varphi g \varphi^{-1}=h\in N$.

Wir wollen also einen Zykel der Länge 3 finden:
###### Beweis der Existenz eines Zykels der Länge 3
Betrachte dazu für ein $g\in N \setminus \set e$ und die Fixpunktmenge$$\text{Fix}(g):=\set{m\mid g(m)=m}$$und betrachte ein $g$ sodass $\lvert \text{Fix}(g)\rvert$ am größten ist bzw. am wenigsten Elemente durch $g$ "bewegt" werden. Wir werden zeigen, dass $g$ ein 3-Zyklus ist.

**Annahme**: $g$ bewegt mindestens 5 Elemente. Dann gilt einer der Fälle (je nach größter Zykluslänge):
1) $g=(a, b, c, d, ...) ...$
2) $g=(a,b,c)(d,e,...)...$
3) $g=(a,b)(c,d)(e,f)...$

Betrachte zunächst den ersten Fall. Dann gilt für jedes $h$ mit den selben Zykellängen existiert ein $\varphi \in S_{n}$ mit $\varphi g \varphi^{-1}=h$. Wir suchen uns jetzt ein $h$, dass quasi die "unnötigen" Zykel von $g$ eliminiert also $g\cdot h$ vereinfacht und transformieren $\varphi$ potentiell danach so, dass es in $\mathcal{A_{n}}$ ist.

Nummeriere die Zykel in $g$ durch also $c_{1}=(a,b,c,d,...)$, $c_{2}=(x_{1},...,x_{k})$, bis $c_{m}$
*Fall:* $m\neq 1$ :
Dann wählen wir$$h=c_{1}\quad c_{2}^{-1}\quad...\quad c_{m}^{-1}$$wobei z.B. $c_{2}^{-1}=(x_{k},...,x_{1})$. 
Dann gilt $g\cdot h =c_{1}\cdot c_{1}$ was insgesamt nur noch die Elemente aus $c_{1}$ bewegt, also weniger als vorher. 

Wenn $\varphi \in \mathcal{A_{n}}$ sind wir also fertig, weil $\lvert \text{Fix}(g\cdot h)\rvert > \lvert \text{Fix}{(g)}\rvert$ was ein **Widerspruch** zur geforderten Maximalität von $\lvert \text{Fix}(g)\rvert$ ist, da dann $h \in N$ (wegen Normalität) und $g\cdot h \in N$. (Außerdem ist $g\cdot h\neq e$, weil z.B. $a$ zu $c$ bewegt wird) 

Wenn $\varphi  \not \in \mathcal{A_{n}}$ betrachten wir $$\tilde\varphi=\varphi\cdot(ab)\in \mathcal{A_{n}}$$Dann bewegt $\tilde g=g\cdot(\tilde\varphi g \tilde\varphi^{-1})=g\cdot(ab)\cdot h\cdot (ab)$, die Elemente außer denen in $c_{1}$ nicht und wir haben wie bei $\varphi \in \mathcal{A_{n}}$ einen **Widerspruch**

*Fall* $m=1$
Also $g=(a_{1},...,a_{k})$ mit $k\geq 5$. Dann finde $h,\varphi\in S_{n}$ mit $$h=\varphi g\varphi^{-1}=(a_{k},...,a_{4},a_{1},a_{2},a_{3})$$Wenn $\varphi \in \mathcal{A}_{n}$ ist $gh=(a_{4}, a_{2})(a_{1}, a_{3})\in N$ und wir haben wie oben einen **Widerspruch**. Wenn $\varphi\not \in \mathcal{A_{n}}$ betrachten wir $\tilde \varphi = \varphi \cdot (a_{1}, a_{2})$ und erhalten $g\cdot \tilde\varphi g \tilde\varphi^{-1}=g\cdot(a_{1},a_{2})\cdot h \cdot (a_{1},a_{2})=(a_{4},a_{3})=g\cdot (a_{k},...,a_{4},a_{2},a_{1},a_{3})=(a_{4}, a_{3},a_{1})$ was wie oben zu einem **Widerspruch** führt.

Für den zweiten Fall $g=(a,b,c)(d,e,...)...$ geht man analog vor wie bei $m\neq 1$ oben. Für den dritten Fall $g=(a,b)(c,d)(e,f)...$ konjugieren wir mit $$\varphi=(a, b, c)\in \mathcal{A_{n}}$$Dann ist $h:=\varphi g \varphi^{-1}=(a, d)(b, c)(e,f)...$ und $g\cdot h =(a, c)(b, d)$ was wieder zu einem **Widerspruch** führt.

Wir wissen also jetzt $\lvert \text{Fix}(g)\rvert \geq n- 4$, wollen aber zeigen $\lvert \text{Fix}(g)\rvert=n-3$. ($2$ kann nicht sein, da sonst $g\not \in \mathcal{A_{n}}$).
**Annahme:** $\lvert \text{Fix}(g)\rvert=n-4$. Dann ist $g=(a,b,c,d)$ oder $g=(a,b)(c,d)$. Den ersten Fall können wir [[#Signum|als 4-Zyklus]] in $\mathcal{A_{n}}$ ausschließen, da 4 gerade ist. Wir wollen also jetzt aus $g=(a,b)(c,d)$ einen 3-Zyklus in $N$ konstruieren:
Sei dazu $f\in \set{1,...,n}\setminus\set{a,b,c,d}$ (hier nutzen wir aus, dass $n\geq 5$ ist) und $$\varphi=(f, b, a)\in \mathcal{A_{n}}$$Dann ist $h=\varphi\cdot g\cdot \varphi^{-1}=(a,f)(c,d)$. Dann ist $h\in N$, weil $N \trianglelefteq \mathcal{A_{n}}$ also ist auch $$g\cdot h=(a, f,b)\in N$$und damit haben wir einen **Widerspruch** und einen 3-Zyklus in $N$ und damit bewiesen, dass die einzigen Normalteiler von $\mathcal{A_{n}}$ genau $\set{1}$ und $\mathcal{A_{n}}$ sind.

##### 1)
Dass $\mathcal{A_{n}}\trianglelefteq S_{n}$ gilt als [[#Signum|Kern vom Signum-Homorphismus]].
Sei $\set{1}\neq U \underset{\neq}\triangleleft S_{n}$. Dann ist $H:=U \cap \mathcal{A_{n}}$ eine [[Gruppen#Untergruppen|Untergruppe]] von $\mathcal{A}_{n}$ und es gilt für alle $g\in \mathcal{A}_{n}:g(U\cap \mathcal{A}_{n})g^{-1}=U\cap\mathcal{A}_{n}=H$ also $H\trianglelefteq \mathcal{A}_{n}$, also muss mit [[#2)]] gelten, dass $U\subseteq(S_{n}\setminus\mathcal{A}_{n})\cup{\{1\}}$ oder $U\supseteq \mathcal{A_{n}}$. Der erste Fall ist aber keine Untergruppe, denn $\text{sgn}(x)=-1\implies \text{sgn}(x\cdot x)=(-1)\cdot(-1)=1$, also $x^{2}\not \in U$. Also muss $U\supseteq \mathcal{A}_{n}$ sein. Da aber wegen [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] $\frac{n!}{2}=\lvert \mathcal{A_{n}}\rvert\leq \lvert U\rvert\mid \lvert S_{n} \rvert=n!$ [[Kommutative Ringe#Teiler|Teiler]] von $n!$ ist, muss $\lvert U\rvert=\frac{n!}2$ also $U=\mathcal{A}_n$ sein.

##### 3)
Es genügt wegen [[#1)]] einzusehen, dass $\mathcal{A}_{n}$[[Gruppenhomomorphismen|$\cong$]] [[Faktorgruppen|$\mathcal{A}_{n}/\set{1}$]] nicht abelsch ist. Es gilt $$\begin{gathered}(1,2,3)\cdot(2,3,4)=(1,2)(4,3)\\(2,3,4)\cdot(1,2,3)=(1,3)(2,4)\end{gathered}$$also kann $S_{n}$ nicht [[Auflösbare Gruppen|auflösbar]] sein.
