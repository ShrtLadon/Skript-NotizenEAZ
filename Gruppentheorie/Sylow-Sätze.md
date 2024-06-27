Sei $G$ eine endliche [[Gruppen|Gruppe]], $p$ eine [[Primzahlen|Primzahl]] und $p^{a}$ [[kommutative Ringe#Teiler|Teiler]] $\lvert G\rvert$ mit maximalem $a$. d.h. $p^{a}\cdot m = \lvert G\rvert$ und $p\not\mid m$. Dann gilt:
- Es gibt $U < G$ [[Gruppen#Untergruppen|Untergruppe]] mit $\lvert U\rvert=p^{a}$.
- Je zwei Untergruppen $U_{1},U_{2}$ der [[Gruppen#Ordnung|Ordnung]] $p^{a}$ sind [[Operation durch Konjugation#Konjugation zueinander|konjugiert zueinander]].
- $\lvert \text{Syl}_{p}(G)\rvert =:n_{p}$ ist gleich [[Normalisator|$\lvert G:N_{G}(U)\rvert$]] und kongruent zu $1$ modulo $p$.

Für $a \geq 1$  definieren wir $\text{Syl}_{p}(G)=\set{U<G \mid \lvert U\rvert=p^{a}}$ und $U\in \text{Syl}_{p}(G)$ eine **p-Sylow Untergruppe**.
### Beweis
Noch nicht behandelt.

## Weitere Eigenschaften von $n_{p}$
- $n_{p} =1 \iff$ Es existiert eine [[Normalteiler|normale]] p-Sylow Untergruppe. Diese ist dann auch eindeutig.
- $n_{p}$ ist ein [[kommutative Ringe#Teiler|Teiler]] von $\frac{\lvert G\rvert}{p^{a}}\in \mathbb{Z}$. 

##### Beweis
Sei $n_{p}=\lvert \text{Syl}_{p}(G)\rvert$. Dann gilt mit dem zweiten Punkt der Sylow-Sätze und der [[Operation durch Konjugation#Isomorphieeigenschaft|Isomorphieeigenschaft]] insbesondere, dass $\text{Syl}_{p}(G)$ genau die zu $U$ konjugierten Untergruppen sind. Daraus folgt auch [[Normalisator#Wichtige Eigenschaften|direkt]], dass genau für $n_{p}=1$ die p-Sylow Gruppe eindeutig ist.

Außerdem gilt [[Normalisator#Wichtige Eigenschaften|$n_{p}=\lvert G: N_{G}(U)\rvert$]]. Da [[Normalisator#Wichtige Eigenschaften|$U < N_G(U)$]] und wegen Anwendung des [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] auch, dass $\lvert U\rvert \cdot \lvert N_{G}(U) : U\rvert= \lvert N_{G}(U)\rvert$ (wir beziehen uns hier wirklich auf $U < N_{G}(U)$). Da wegen Satz von Lagrange aber ebenfalls gilt $n_{p}=\frac{\lvert G\rvert}{\lvert N_{G}(U)\rvert}=\frac{\lvert G\rvert}{\frac{\lvert N_G(U) \rvert \cdot \lvert U\rvert}{\lvert U\rvert}}=\frac{\lvert G\rvert}{\lvert N_{G}(U) : U\rvert \cdot \lvert U\rvert}$. Daraus folgt $n_{p}\cdot \lvert N_{G}(U):U\rvert=\frac{\lvert G\rvert}{\lvert U\rvert}$ also ist $n_{p}$ ein [[kommutative Ringe#Teiler|Teiler]] von $\frac{\lvert G\rvert}{p^{a}}$.   

# Folgerungen
##### $\lvert G\rvert=m\cdot p^{a}$ mit $m < p$.
Es gilt $n_{p}=1$ und wenn $m$ eine [[Primzahlen|Primzahl]] ist, dass $G$ [[Auflösbare Gruppen|auflösbar]] ist.

###### Beweis
Denn es gilt $n_{p} \equiv 1 \mod p$ und $n_{p} \mid m< p$. Daraus folgt $n_{p}=1$ und [[#Weitere Eigenschaften von $n_{p}$|damit]] ist die(!) p-Sylow Untergruppe [[Normalteiler|normal]]. Sei also $U\in \text{Syl}_{p}(G)$ die normale p-Sylow Gruppe. Wenn $m$ eine [[Primzahlen|Primzahl]] ist, dann ist mit [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] $\lvert G/U\rvert=\frac{\lvert G\rvert}{\lvert U\rvert}=m$ also [[Faktorgruppen|$G/U$]] [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] und damit abelsch. Also ist $G$ auflösbar. 

##### $\lvert G\rvert=pq$ mit $p\neq q$ Primzahlen
Dann gilt $n_{q}=1$ oder $n_{p}=1$ und $G$ ist [[Auflösbare Gruppen|auflösbar]].
###### Beweis
o.B.d.A. ist $q < p$ 
Dann gilt nach [[#Folgerungen#$ lvert G rvert=m cdot p {a}$ mit $m < p$.|obigem Satz]], dass $n_{p}=1$ und $G$ auflösbar. 