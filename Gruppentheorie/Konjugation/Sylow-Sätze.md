Sei $G$ eine endliche [[Gruppen|Gruppe]], $p$ eine [[Primzahlen|Primzahl]] und $p^{a}$ [[Kommutative Ringe#Teiler|Teiler]] $\lvert G\rvert$ mit maximalem $a$. d.h. $p^{a}\cdot m = \lvert G\rvert$ und $p\not\mid m$. Dann gilt:
1) Es gibt $U < G$ [[Gruppen#Untergruppen|Untergruppe]] mit $\lvert U\rvert=p^{a}$.
2) Je zwei Untergruppen $U_{1},U_{2}$ der [[Gruppen#Ordnung|Ordnung]] $p^{a}$ sind [[Operation durch Konjugation#Konjugation zueinander|konjugiert zueinander]].
3) $\lvert \text{Syl}_{p}(G)\rvert =:n_{p}$ ist gleich [[Normalisator|$\lvert G:N_{G}(U)\rvert$]] und kongruent zu $1$ modulo $p$.

Für $a \geq 1$  definieren wir $\text{Syl}_{p}(G)=\set{U<G \mid \lvert U\rvert=p^{a}}$ und $U\in \text{Syl}_{p}(G)$ eine **p-Sylow Untergruppe**.
#### Beweis
Den Fall $a=0$ werden wir teilweise ignorieren, weil er klar ist (gerade bei Randfällen).
###### 1)
Wir machen starke Induktion nach $n=\lvert G\rvert=p^{a}\cdot m$.
*Induktionsanfang:* $n=1$. Dann ist $U=G=\set{e}$ und $\lvert {e}\rvert=p^{0}$.  

*Induktionsschluss:* Sei die Aussage für kleinere $n$ richtig. 

*Fall* [[Operation durch Konjugation#Konjugationsklassen, Zentralisator und Kern|$\lvert Z(G)\rvert$]] ist [[Kommutative Ringe#Teiler|teilbar]] durch $p$:
Nach [[Gruppen#Theorem von Cauchy|Theorem von Cauchy]] gilt es existiert ein $x \in Z(G)$ mit $\text{ord}(g)=p$. Sei $K:=\langle g\rangle$ die erzeugte  [[Gruppen#Zyklische Gruppen|zyklische Untergruppe]] von $G$ von [[Gruppen#Ordnung|Ordnung]] $p$.  Dann gilt $K\subseteq Z(G)$ kommutiert $K$ mit allen Elementen aus $G$. Insbesondere ist dann auch [[Gruppenwirkung#Rechts und Linksnebenklassen|$gK=Kg$]] für jedes $g\in G$ und damit [[Normalteiler#Äquivalente Formulierungen|$K \trianglelefteq G$]]. Außerdem gilt nach [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]], dass
$\lvert$[[Faktorgruppen|$G/K$]]$\rvert=p^{a-1}\cdot m$, also existiert nach Induktionsannahme ein $U < G/K$ mit $\lvert U\rvert=p^{a-1}$. 

Betrachte $$\pi:G \rightarrow G/K,x\mapsto xK$$den kanonischen [[Gruppenhomomorphismen|Homomorphismus]]. Betrachte nun $V:=\pi^{-1}(U)$. Es gilt $\pi(e)=eG\in U$ also $e\in V$ und für $a,b\in V$, dass $\pi(a\cdot b^{-1})=\pi(a)\cdot \pi(b)^{-1}\in U$, da $U$ Untergruppe. Also ist nach [[Gruppen#Untergruppenkriterium|Untergruppenkriterium]] $V$ eine Untergruppe von $G$. 
Außerdem gilt die Einschränkung $\pi\lvert_{V}^U$ hat immer noch $\ker \pi\lvert_{V}^{U}=\ker\pi=K$ und es gilt mit [[Faktorgruppen#Isomorphiesatz|Isomorphiesatz]] und Satz von Lagrange:$$\lvert V\rvert=\lvert K\rvert\cdot  \lvert U\rvert=p^{a-1}\cdot p=p^{a}$$und wir haben die gesuchte Untergruppe.

*Fall* $\lvert Z(G)\rvert$ ist nicht durch $p$ teilbar.
Dann gilt mit der [[Operation durch Konjugation#Klassengleichung|Klassengleichung]] - da $p \mid G\rvert$ - dass $p\not\mid \sum\limits_{x\in X, \lvert G:Z_G(x)\rvert \neq 1}\lvert G:Z_G(x)$. Also muss es ein $g\in G$ geben, sodass $p \not \mid \lvert G:Z_{G}(g)\rvert\neq 1$. (Es kann keine leere Summe sein, sonst ist $\lvert Z(G)\rvert=\lvert G\rvert=p^{a}m$). Dann gilt mit Satz von Lagrange $$\lvert Z_G(g)\rvert=\frac{\lvert G\rvert}{\lvert G:Z_G(g)\rvert}=p^{a}\cdot m'<\lvert G\rvert$$ Mit Induktionsannahme existiert also ein $U<Z_G(g)<G$ mit $\lvert U\rvert=p^a$. 

###### 2)
Seien $H_{1},H_{2}\in \text{Syl}_{p}(G)$. Betrachte die [[Gruppenwirkung#Rechts und Linksnebenklassen|Linksnebenklassen]] $$G/H_{1}=\set{gH_{1}\mid g\in G}=: M$$
Es [[Gruppenwirkung|wirkt]] $G$ auf $M$ durch $$h*gH_{1}=hgH_{1}$$Also wirkt auch $H_{2}< G$ auf $M$ und der [[Gruppenwirkung#Bahn und Stabilisator|Bahnenraum]] $H_{2}/M$ partitioniert $M$. Außerdem hat jede Bahn wegen [[Gruppenwirkung#Bahnenformel|der Bahnenformel]] als [[Gruppen#Ordnung|Ordnung]] einen [[Kommutative Ringe#Teiler|Teiler]] von $\lvert H_2\rvert$ also $1$ oder $p^{k},k\geq 1$.  

Es gilt $p\not\mid \lvert M\rvert$, wegen Lagrange, also insbesondere weil $H_{2}/M$ eine Partition von $M$ ist, dass es eine Bahn mit genau einem Element geben muss. Das bedeutet es existiert ein $gH_{1}\in M$, sodass für alle $h_{2}\in H_{2}$ gilt $$h_{2}gH_{1}=gH_{1}\iff g^{-1}h_{2}gH_{1}=H_{1}$$D.h. insbesondere $g^{-1}h_{2}g\cdot e=g^{-1}h_{2}g\in H_{1}$ und damit gilt $g^{-1}H_{2}g\subseteq H_{1}$.
Wegen der [[Operation durch Konjugation#Isomorphieeigenschaft|Isomorphieeigenschaft der Konjugation]] und weil wir uns endliche Gruppen anschauen muss gelten $\lvert g^{-1}H_{2}g\rvert=\lvert H_{2}\rvert=\lvert H_1\rvert$ und damit $g^{-1}H_{2}g=H_{1}$ also $H_{1},H_{2}$ konjugiert zueinander. 

###### 3)
noch nicht behandelt.

#### Weitere Eigenschaften von $n_{p}$
- $n_{p} =1 \iff$ Es existiert eine [[Normalteiler|normale]] p-Sylow Untergruppe. Diese ist dann auch eindeutig und wir bezeichnen sie mit $U_{p}$.
- $n_{p}$ ist ein [[Kommutative Ringe#Teiler|Teiler]] von $\frac{\lvert G\rvert}{p^{a}}\in \mathbb{Z}$. 

###### Beweis
Sei $n_{p}=\lvert \text{Syl}_{p}(G)\rvert$. Dann gilt mit dem zweiten Punkt der Sylow-Sätze und der [[Operation durch Konjugation#Isomorphieeigenschaft|Isomorphieeigenschaft]] insbesondere, dass $\text{Syl}_{p}(G)$ genau die zu $U_p$ konjugierten Untergruppen sind. Daraus folgt auch [[Normalisator#Wichtige Eigenschaften|direkt]], dass genau für $n_{p}=1$ die p-Sylow Gruppe eindeutig ist.

Außerdem gilt [[Normalisator#Wichtige Eigenschaften|$n_{p}=\lvert G: N_{G}(U_p)\rvert$]]. Da [[Normalisator#Wichtige Eigenschaften|$U < N_G(U_p)$]] und wegen Anwendung des [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] auch, dass $\lvert U_p\rvert \cdot \lvert N_{G}(U_p) : U_p\rvert= \lvert N_{G}(U_p)\rvert$ (wir beziehen uns hier wirklich auf $U_p < N_{G}(U_p)$). Da wegen Satz von Lagrange aber ebenfalls gilt $n_{p}=\frac{\lvert G\rvert}{\lvert N_{G}(U_p\rvert}=\frac{\lvert G\rvert}{\frac{\lvert N_G(U_p) \rvert \cdot \lvert U_p\rvert}{\lvert U_p\rvert}}=\frac{\lvert G\rvert}{\lvert N_{G}(U_p) : U_p\rvert \cdot \lvert U_p\rvert}$. Daraus folgt $n_{p}\cdot \lvert N_{G}(U_p):U_p\rvert=\frac{\lvert G\rvert}{\lvert U_p\rvert}$ also ist $n_{p}$ ein [[Kommutative Ringe#Teiler|Teiler]] von $\frac{\lvert G\rvert}{p^{a}}$.   

#### Schnitt von p-Sylow Untergruppen
 Seien $U\neq H \in \text{Syl}_{q}(G)$ und $\lvert U\rvert=\lvert H\rvert=q$. Dann gilt $U \cap H\lneq U$ und nach [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] also, dass $\lvert U\cap H\rvert \mid \lvert U\rvert$ und damit $U\cap H=\set{e}$, da $\lvert U\rvert=q$ prim. 

# Folgerungen
##### $\lvert G\rvert=m\cdot p^{a}$ mit $m < p$.
Es gilt $n_{p}=1$ und wenn $m$ eine [[Primzahlen|Primzahl]] ist, dass $G$ [[Auflösbare Gruppen|auflösbar]] ist.

###### Beweis
Denn es gilt $n_{p} \equiv 1 \mod p$ und $n_{p} \mid m< p$. Daraus folgt $n_{p}=1$ und [[#Weitere Eigenschaften von $n_{p}$|damit]] ist die(!) p-Sylow Untergruppe [[Normalteiler|normal]]. Sei also $U\in \text{Syl}_{p}(G)$ die normale p-Sylow Gruppe. Wenn $m$ eine [[Primzahlen|Primzahl]] ist, dann ist mit [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] $\lvert G/U\rvert=\frac{\lvert G\rvert}{\lvert U_p\rvert}=m$ also [[Faktorgruppen|$G/U_p$]] [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] und damit [[Auflösbare Gruppen#Beispiele|nach dieser Bemerkung]] auflösbar. Außerdem gilt $U_p$ ist als [[Auflösbare Gruppen#Auflösbarkeit von Gruppen der Ordnung $p {m}$|p-Gruppe]] auflösbar. Da sich [[Auflösbare Gruppen#Vererbung|Auflösbarkeit "vererbt"]] ist auch $G$ auflösbar.
 
##### $\lvert G\rvert=pq$ mit $p\neq q$ Primzahlen
Dann gilt $n_{q}=1$ oder $n_{p}=1$ und $G$ ist [[Auflösbare Gruppen|auflösbar]].
###### Beweis
o.B.d.A. ist $q < p$ 
Dann gilt nach [[#Folgerungen#$ lvert G rvert=m cdot p {a}$ mit $m < p$.|obigem Satz]], dass $n_{p}=1$ und $G$ auflösbar. 

##### $\lvert G\rvert= p^{2}q$ mit $p\neq q$ Primzahlen
Dann ist $n_{q}=1$ oder $n_{p}=1$ und $G$ auflösbar
###### Beweis
Wenn $q < p$ gilt mit [[#$ lvert G rvert=m cdot p {a}$ mit $m < p$.|dem ersten Lemma]] $n_{p}=1$ und da $q$ [[Primzahlen|Primzahl]] auch, dass $G$ auflösbar ist. 
Sei also $q >p$
*Fall:* $n_{p}=1$. Dann ist $G/U_{p}$ als [[Auflösbare Gruppen#Auflösbarkeit von Gruppen der Ordnung $p {m}$|q-Gruppe auflösbar]] und $U_{p}$ als p-Gruppe. Damit ist auch $G$ auflösbar.
*Fall* $n_{p} > 1$.
Es gilt $n_{q} \in \set{1,p,p^{2}}$ als Teiler von $p^{2}$. Da $n_{q}\equiv 1 \mod q$ und $p<q$ ist $n_{q}\neq p$.
Wenn $n_{q}=1$ ist, ist $G/U_{q}$ als p-Gruppe auflösbar und $U_{q}$ als zyklische Gruppe also auch $G$ auflösbar.

**Annahme**: $n_{q}>1$:
Dann gibt es $p^2$ [[Gruppen#Untergruppen|Untergruppen]] der [[Gruppen#Ordnung|Ordnung]] $q$.
Da alle $U\in \text{Syl}_{q}(G)$ genau $q$ Elemente haben, ist jedes $U$ [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] und wird von jedem Element außer $e$ erzeugt. D.h. $\forall x\in U\setminus\set{e}: \text{ord}(x)=q$. 

Wegen der oben bewiesenen [[#Schnitt von p-Sylow Untergruppen|"Fast Disjunktheit"]] gilt $\lvert \dot\bigcap_{H\in \text{Syl}_{q}}H\setminus\set e\rvert=p^{2}(q-1)$ also, dass es höchstens $p^{2}q-p^{2}(q-1)=p^{2}$ Elemente der Ordnung $\neq q$ gibt.
Insbesondere müssen [[Gruppen#Ordnung#Eigenschaften|da $\forall g\in G:\text{ord}(g) \mid \lvert G \rvert$]] alle Elemente $x\in U \in \text{Syl}_{p}$ Ordnung $p^{2}, p, 1$ haben müssen und $\lvert U\rvert=p^2$, dass $U=G\setminus \dot\bigcap_{H\in \text{Syl}_{q}}H\setminus\set e$ und damit $n_{p}=1$, was ein **Widerspruch** ist.


