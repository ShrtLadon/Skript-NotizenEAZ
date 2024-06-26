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
Sei $n_{p}=\lvert \text{Syl}_{p}(G)\rvert$. Dann gilt mit dem zweiten Punkt der Sylow-Sätze und der [[Operation durch Konjugation#Isomorphieeigenschaft|Isomorphieeigenschaft]] insbesondere, dass $\text{Syl}_{p}(G)$ genau die zu $U$ konjugierten Untergruppen sind. Also gilt [[Normalisator#Wichtige Eigenschaften|$n_{p}=\lvert G: N_{G}(U)\rvert$]]. Da [[Normalisator#Wichtige Eigenschaften|$U < N_G(U)$]] gilt wegen Anwendung des [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] auch, dass $\lvert U\rvert \cdot \lvert N_{G}(U) : U\rvert= \lvert N_{G}(U)\rvert$ (wir beziehen uns hier wirklich auf $U < N_{G}(U)$). Da wegen Satz von Lagrange aber ebenfalls $\lvert N_G(U)\rvert \mid  \lvert G\rvert$ Teiler ist und $\lvert U\rvert=p^a$ folgt (TODO). 

# Folgerungen
##### $\lvert G\rvert=m\cdot p^{a}$ mit $m < p$.
Es gilt $n_{p} \equiv 1 \mod p$ und $n_{p} \mid m< p$. Daraus folgt $n_{p}=1$ und [[#Weitere Eigenschaften von $n_{p}$|damit]] ist die(!) p-Sylow Untergruppe [[Normalteiler|normal]]. Wenn $m$ eine [[Primzahlen|Primzahl]] ist

######