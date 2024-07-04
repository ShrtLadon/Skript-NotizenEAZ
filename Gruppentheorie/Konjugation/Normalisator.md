Sei $U < G$ eine [[Gruppen#Untergruppen|Untergruppe]]. Dann ist der **Normalisator** definiert als $$N_G(U):=\set{g\in G\mid g^{-1}\cdot U \cdot g=U}$$Das ist eine [[Gruppenwirkung|Operation]] von $G$ auf $\set{U \mid U \leq G}$, denn [[Operation durch Konjugation|$c_{g}$]] ist ein [[Gruppenhomomorphismen|Homomorphismus]] also unter Untergruppen abgeschlossen.
#### Wichtige Eigenschaften
- $N_{G}(U)$ ist eine [[Gruppen#Untergruppen|Untergruppe]] von $G$ und es gilt [[Normalteiler|$U \trianglelefteq N_{G}(U)$]].
- $N_{G}(U)$ ist die größte Untergruppe von $G$ in der $U$ normal ist.
- [[Gruppenwirkung#Index|$\lvert G:N_{G}(U)\rvert$]] ist die Anzahl der zu $U$ konjugierten Untergruppen (falls G endlich)
- [[Gruppenwirkung#Index|$\lvert G:N_{G}(U)\rvert$]] $=1 \iff N_G(U)=G$
###### Beweis
Es gilt $1 \in N_G(U)$ und für $a,b \in N_{G}(U)$, dass $a^{-1}\in N_{G}(U)$, da [[Operation durch Konjugation|$c_{a}^{-1}$]] genau durch $c_{a^{-1}}$ gegeben ist und $c_{a}(U)=U$ und damit $c_{a^{-1}}(c_a(U))=U$. Außerdem gilt $a\cdot b U b^{-1}a^{-1}=U$ also $a\cdot b\in N_G(U)$ und damit ist es eine Untergruppe. Offensichtlich gilt $U \subseteq N_{G}(U)$, also ist $U$ eine Untergruppe von $N_G(U)$. Dass $U\trianglelefteq N_G(U)$ folgt direkt mit der Definition und auch, dass es die größte Untergruppe ist, die das erfüllt.

Mit dem Kommentar in der Definition merken wir, dass bezüglich dieser Operation gilt: $N_G(U)=$[[Gruppenwirkung#Bahn und Stabilisator|$\text{Stab}_{\set{U \mid U \leq G}}(U)$]]. Wegen dem [[Gruppenwirkung#Orbit-Stabilisator-Theorem|Orbit-Stabilisator-Theorem]] gilt also $\lvert N_{G}(U)\rvert=\lvert G\cdot U\rvert$, wobei $G\cdot U$ auch bezüglich dieser Operation gemeint ist also $$G\cdot U=\set{gUg^{-1} \mid g\in G}$$also genau die zu $U$ konjugierten Elemente. 


 
