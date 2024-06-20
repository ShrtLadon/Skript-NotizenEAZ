Die symmetrische Gruppe ist für eine Menge $X$ gegeben durch $$S_{(X)}=(\set{f:X \rightarrow X \quad:\quad \text{f ist bijektiv}},\circ)$$für $X=\set{1,...,n}$ mit $n \in \mathbb{N}$ nennt man $S_{(X)}$ auch $S_{(n)}$  

# Wiederholung aus der Linearen Algebra
Das nachfolgende wird größtenteils ohne Beweis eingeführt, dafür ist ein ein LA-Skript zu schauen:

- Es gilt $\lvert S_{n}\rvert=n!$
- Für $n>2$ ist $S_{n}$ nicht abelsch.

### Schreibweisen
Für eine $g\in S_{n}$ kann man $g$ schreiben als $\begin{pmatrix}1 & 2 & ... & n\\g(1) & g(2) & ... & g(n)\end{pmatrix}$. Alternativ gibt es noch die Zyklenschreibweise bestehend aus Tupeln $(x, g(x),...,g^i(x))$ mit paarweise unterschiedlichen Einträgen, sodass $g^{i+1}(x)=x$, wobei man oft noch Tupel der Länge 1 weglässt.
Ein Beispiel ist $g=\begin{pmatrix}1 & 2 & 3 & 4 & 5 & 6\\3 & 4 & 1 & 5 & 2& 6\end{pmatrix}=\begin{pmatrix}1 & 2\end{pmatrix} \begin{pmatrix}2 & 4 & 5\end{pmatrix}$. 
### Transpositionen
Eine Transposition ist ein $\begin{pmatrix}i & j\end{pmatrix}\in S_{n}$, die genau zwei Elemente vertauscht. Wir können jedes $g\in S_{n}$ als ein Produkt von Transpositionen schreiben. Dabei ist das Produkt nicht eindeutig, aber ob die Anzahl der Transpositionen gerade oder ungerade ist schon.

### Signum
Das Signum $\text{sgn}:S_{n} \rightarrow \set{1, -1}, x \mapsto \begin{cases}1 & \text{g besteht in Darstellung aus gerader Anzahl an Transpositionen}\\-1 & \text{sonst}\end{cases}$  ist ein [[Gruppenhomomorphismen|Gruppenhomomorphismus]], wobei $\set{1,-1}$ mit der eindeutigen Gruppenstruktur isomorph zu $\mathbb{Z}/2\mathbb{Z}$ ist.

Wir bezeichnen dabei $\ker \text{sgn}=\mathcal{A_{n}}=\set{g\in S_{n}\mid \text{sgn}(g)=1}$ als *alternierende Gruppe*. Da [[Normalteiler#Beispiele|$\mathcal{A_{n}} \trianglelefteq S_{n}$]] ist $S_{n}/A_{n}\cong \set{-1, 1}$ nach [[Faktorgruppen#Isomorphiesatz|Isomorphiesatz]] (zumindest für $n>1$) und $\lvert \mathcal{A}_{n}\rvert=\frac{n!}{2}$ für $n>1$.  


# Satz von Cayley
Es gilt jede Gruppe ist [[Gruppenhomomorphismen|isomorph]] zu einer Untergruppe einer symmetrischen Gruppe.

###### Beweis
Sei $G$ eine Gruppe und $*:G\times G \rightarrow G$ die [[Gruppenwirkung]] von $G$ auf sich selbst. Dann kann man dem einen [[Gruppenhomomorphismen|Gruppenhomomorphismus]] $\rho:G \rightarrow S_{(G})$ [[Gruppenwirkung#Zusammenhang zu symmetrischer Gruppe|zuordnen]]. 

Sei $g \in \ker \rho$. Dann ist $\rho(g)=Id$, also $g*x=g\cdot x=x$ für alle $x \in G$. Damit ist aber $g=e$ wegen [[#Eigenschaften|der Eindeutigkeit des neutralen Elements]]. Also ist $\ker \rho =\set{e}$ und [[Gruppenhomomorphismen#Eigenschaften|damit]] $\rho$ injektiv. 
Dann ist allerdings $\rho: G \rightarrow \text{Bild}(\rho) \leq S_{(X)}$ ein Isomorphismus auf eine Untergruppe von $S_{(X)}$.

# Verhalten unter Konjugation
Für $g \in S_{n}$ und $h=(x_{1,1}, x_{1,2},...,x_{1,l_{1}}),...,(x_{k,1},...,x_{k,l_{k}})$ in [[#Schreibweisen|Zykelnotation]] gilt die [[Operation durch Konjugation|Konjugation]] ist $$ghg^{-1}=(g(x_{1,1}), g(x_{1,2}),...,g(x_{1,l_{1}})),...,(g(x_{k,1}),...,g(x_{k,l_{k}}))$$Insbesondere sind also die [[Operation durch Konjugation#Konjugationsklassen, Zentralisator und Kern|Konjugationklassen]] genau die Elemente mit der selben Anzahl der jeweiligen selben Zyklenlängen.

##### Beweis/Begründung
Für einen Zyklus $(x_{1},...,x_{k})$ betrachten wir den Zyklus von $ghg^{-1}$ der bei $g(x_{1})$ startet. Dann erhält man genau $(g(x_{1}), g(x_{2}),...,g(x_{k}))$, denn für ein $x_{i}$ gilt $h(x_{i})=x_{i+1}$ (bzw. $x_1$ für $i=k$, da aber analog). Dann ist $(ghg^{-1})(g(x_{i}))=(gh)(x_{i})=g(x_{i+1})$

# Auflösbarkeit
### $n\leq 4$
Für $n\leq 4$ ist $S_{n}$ [[Auflösbare Gruppen|auflösbar]]. 
##### Beweis
Für $S_{1},S_{2}$ sind die [[Gruppen|Gruppen abelsch]], also [[Auflösbare Gruppen#Beispiele|auflösbar]]. Für $S_{3}$ gilt $S_{3}\cong D_{6}$ zur [[Gruppen#Diedergruppe|Diedergruppe]], die nach dem [[Auflösbare Gruppen#Diedergruppe#Beweis|Beweis]] auflösbar ist. Es verbleibt also zu zeigen, dass $S_{4}$ auflösbar ist.

Dazu gilt die [[#Signum|alternierende Gruppe]] $\mathcal{A}_{4}$ ist ein [[Normalteiler]] von $S_{4}$ und $\lvert A_{4}\rvert=12$. Außerdem gilt für einen Zyklus $(i, j, k, l)$ dass $(i,j,k,l)=(i, j)\cdot (j, k)\cdot (k,l)$ also sind Zyklen der Länge 4 nicht in $A_{n}$, aber $(i, j)(k,l)=(i, j)(k,l)$ wenn $i, j, k$ und $l$ alle paarweise verschieden sind. Wenn $(i,j)=(k,l)$, dann ist das Produkt die Identität (hier ist mit = Gleichheit der Funktionen gemeint!) und wenn o.B.d.A $j=k$ dann ist das Produkt $(i,j,l)$. 

Das heißt $\mathcal{A}_4$ besteht genau aus $(i,j)(k,l)$ und $(i,j,l)$ und natürlich der Identität.
Betrachte nun $\mathcal{K}=\set{(1,2)(3,4), (1,3)(2,4),(1,4)(2,3),1}$ also genau $\mathcal{K}=\mathcal{A}_{4}\setminus\set{(i,j,k)\in \mathcal{A}_{4}}$. Man rechnet leicht (einfach für alle Elemente durchprobieren) nach, dass $\mathcal{K}$ eine [[Gruppen#Untergruppen|Untergruppe]] ist. Da nach [[#Verhalten unter Konjugation]] die Zykellängen erhalten bleiben, ist $g\mathcal{K}g^{-1}=\mathcal{K}$ ein [[Normalteiler]] von $\mathcal{A}_{4}$. 

Wegen dem [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] ist $\lvert \mathcal{A}_{4} / \mathcal{K}\rvert=\frac{12}{4}=3$ was eine [[Primzahlen|Primzahl]] ist. Dementsprechend ist es [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]], was uns genau zeigt, dass ${1}\trianglelefteq \mathcal{K}\trianglelefteq\mathcal{A}_{4}\trianglelefteq S_{4}$ [[Auflösbare Gruppen#Auflösbarkeit endlicher Gruppen|auflösbar]] ist. 
### $n>4$
