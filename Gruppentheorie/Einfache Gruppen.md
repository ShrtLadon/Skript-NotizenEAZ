Eine [[Gruppen|Gruppe]] $G$ heißt **einfach**, wenn $G$ außer $G$ und $\set 1$ keine [[Normalteiler|normalen]] [[Gruppen|Untergruppen]] hat.

### Aufbaueigenschaft
Für jede endliche Gruppe existieren $G_{0},...,G_{n}$ mit $$\set 0 =G_{0}\triangleleft G_{1}\triangleleft ... \triangleleft G_{n}=G$$sodass für alle $i\in \set{0,...,n-1}$ gilt [[Faktorgruppen|$G_{i+1}/G_{i}$]] ist einfach.
##### Beweis
*Fall:* $G$ ist einfach. Dann sind wir fertig mit $G_{0}=\set{0}$ und $G_{1}=G$. 
*Fall:* $G$ ist nicht einfach:
Dann hat $G$ eine normale Untergruppe $\set{0}\neq U \neq G$. Sei diese im Nachfolgenden maximal (also maximale Ordnung unter normalen nichtrivialen Untergruppen).
**Annahme:** $G/U$ ist nicht einfach. 
Dann existiert eine nichttriviale normale Untergruppe $H\triangleleft G/U$, also gilt für alle $gU\in G/U$$$gUHUg^{-1}=H$$Insbesondere gilt aber, dass für die [[Gruppenhomomorphismen|Projektion]] $\pi:G \rightarrow G/U,x\mapsto xG$ $\pi^{-1}(H)$ eine Untergruppe von $G$ ist (leicht zu verifizieren). Sei also $H'=\pi^{-1}(H)$, was insbesondere  Dann gilt für jedes $g\in G$, dass $\pi(gH'g^{-1})=\pi(g)\pi(H')\pi(g)^{-1}=H$ also ist $gH'g^{-1}\subseteq \pi^{-1}(H)$ und damit $H'$ ein nichttrivialer Normalteiler von $G$ und es gilt $U\subsetneq H'$, was ein **Widerspruch** zur Maximalität von $U$ ist. 

Damit ist $G/U$ einfach und wir sind fertig.
### Beispiele
- Es gilt [[Symmetrische Gruppe#$n>4$|$\mathcal{A}_5$]] ist eine einfache Gruppe
- Eine (nicht triviale) [[Gruppen|abelsche Gruppe]] ist genau dann einfach, wenn $\lvert G\rvert$ [[Primzahlen|prim]] ist.

###### Beweis
"$\Rightarrow$"
**Annahme**: $\lvert G\rvert$ ist nicht prim, also $\lvert G\rvert=p\cdot m$ mit $p$ prim aufgrund der [[Kommutative Ringe#Primfaktoren|Primfaktorzerlegung]]. Dann existiert nach [[Gruppen#Theorem von Cauchy|Theorem von Cauchy]] eine [[Gruppen#Zyklische Gruppen|zyklische]] Untergruppe $U$ der [[Gruppen#Ordnung|Ordnung]] $p$. Außerdem ist, da $G$ abelsch ist [[Normalteiler#Äquivalente Formulierungen|auf jeden Fall $U$ normal]], was ein **Widerspruch** ist. 

"$\Leftarrow$"
$G$ hat nach [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] nur Untergruppen der Ordnung $1$ oder $p$. 