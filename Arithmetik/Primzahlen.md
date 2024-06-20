In diesem Abschnitt befassen wir uns nur mit den [[kommutative Ringe#Prim- und irreduzible Elemente|Primelementen]] im Ring $\mathbb{Z}$. 

### Verteilung und Anzahl von Primzahlen
#### Anzahl von Primzahlen
Es gibt unendlich viele Primzahlen

###### Beweis
Annahme: Es gibt nur die Primzahlen $p_{1}, ..., p_{k} \in \mathbb{N}$. Dann gilt $$q=p_{1}\cdot...\cdot p_{k}+1$$ wird von keinem $p_{i}$ geteilt. Also kann $q$ keine [[kommutative Ringe#Primfaktoren|Primfaktorzerlegung]] haben, was ein Widerspruch ist. 

> [!BOOK] In generellen Euklidischen Ringen
> Der Beweis funktioniert nicht generell in Euklidischen Ringen, weil dort $p_1\cdot...\cdot p_k$ eine [[kommutative Ringe#Einheiten|Einheit]] sein kann

#### Abstand
Für jedes $n\in \mathbb{N}$ gibt es ein $k\in \mathbb{N}$, sodass $k, k+1,...,k+n$  nicht prim sind. 

###### Beweis
Betrachte $k = (n+2)! + 2$. Dann ist$$\begin{gathered}k+0=(n+2)!+2 \equiv 0\mod2\\k+1=(n+2)!+3 \equiv 0\mod3\\\vdots\\k+n=(n+2)!+n+2 \equiv 0\mod n+2\end{gathered}$$Also sind $k,...,k+n$ nicht prim.

#### Primzahlsatz / Anteil
Sei $\pi(x)$ die Anzahl der Primzahlen im Intervall $[0,x]$. Dann gilt $$\lim_{x\to \infty}\pi(x)\cdot \frac{\ln(x)}{x}=1$$In anderen Worten gibt es ca. so viele Primzahlen in $[0,x]$ wie $\frac x {\ln(x)}$ 

## Primzahltests / Eigenschaften
#### Satz von Wilson
Sei $n \in \mathbb{N}$. Dann gilt 
- Ist $n > 4$ und $n$ keine Primzahl so gilt $$(n-1)!\equiv0 \mod n$$
- Ist $n$ eine Primzahl, so gilt $$(n-1)!\equiv-1 \mod n$$

###### Beweis
1) Sei $n > 4$ nicht prim. Dann gibt es paarweise verschiedene Primzahlen $p_{1},..., p_{k} \leq n-1$ und $l_{i} \in \mathbb{N}$: $$n=p_{1}^{l_{1}}\cdot ...\cdot p_{k}^{l_{k}}$$ Fall $k \neq1$:
   Dann kommt jedes $p_{i}^{k_{i}}$ in $(n-1)!$ vor und damit teilt $n \mid (n-1)!$ 
   Fall $k = 1$
   Dann ist $n= p^{l}$ und insbesondere weil $n$ nicht prim und keine Einheit (> 4) gilt $l\geq 2$.  Dann sind aber $p^{l-1}$ und $p^{l-1}+ p < n-1$ da $n > 4$. Dann ist aber $p^{l-1}\cdot (p^{l-1}+p) = p^{2l-2}+p^{l}= p^{l}\cdot(p^{l-2}+1)$ Also insbesondere teilt $p^{l}=n\mid (n-1)!$

2) Sei $n$ eine Primzahl. Dann ist $\mathbb{K}:=\mathbb{Z}/n \mathbb{Z}$ ein Körper. Es gilt $(n-1)!=\alpha_{1}\cdot...\cdot\alpha_{n-1}$, wobei $\alpha_{i} \in \mathbb{K}^{*}$ alle [[kommutative Ringe#Einheiten|Einheiten]] sprich alle von 0 verschiedenen Elemente in $\mathbb{K}$ durchläuft. Da gilt, dass $\forall a \in \mathbb{K}^{*}:\exists b \in \mathbb{K}^{*}:ab=1$. Das heißt in $\alpha_{1}\cdot...\cdot \alpha_{n-1}$ kürzen sich alle $a_{i}$ weg bis auf die Selbstinversen, also die $x$ mit $x\cdot x=1$. Allerdings hat das [[Polynomringe|Polynom]] $X^{2}-1$ nur die Nullstellen $1,-1$ und kann auch nicht mehr [[Polynomringe#Teilbarkeit|haben]]. Daraus ergibt sich $(n-1)!=1\cdot (-1)$.

#### Kleiner Satz von Fermat
Sei $p\in \mathbb{N}$ eine Primzahl, $a \in \mathbb{Z}$ beliebig.
1) $a^{p} \equiv a \mod p$
2) Ist $a$ nicht teilbar durch $p$, dann gilt $a^{p-1}\equiv 1 \mod p$

###### Beweis
1)
Ist $a\equiv 0 \mod p$. Dann ist $a^{p}\equiv0 \equiv a \mod p$
Ist $a \not\equiv 0 \mod p$. Dann folgt $a^{p}\equiv a \mod p$ aus 2)

2)
Sei $\mathbb{K} := \mathbb{Z}/p \mathbb{Z}$. Dann ist die Multiplikation mit $\overline a$ definiert als $\mathbb{K}^{*} \rightarrow \mathbb{K}^{*}, \overline b \mapsto  \overline a \cdot \overline b$ eine bijektive Abbildung, denn Multiplikation mit der Inversen $(\overline a) ^{-1}$ ist die Umkehrabbildung.

Insbesondere sind damit $\overline a, \overline a \cdot \overline 2, ..., \overline a \cdot \overline{(p-1)}$ alle Elemente aus $\mathbb{K}^{*}$. Also ist $$(\overline a)^{p-1}(\overline 1 \cdot ... \cdot \overline{(p-1)})=\overline a \cdot \overline a\cdot \overline 2\cdot ...\cdot \overline a \cdot \overline{(p-1)}=\overline 1\cdot ... \cdot \overline{(p-1)}$$ Durch [[kommutative Ringe#Teilbarkeit#Nullteiler und Integritätsbereiche#Eigenschaften|kürzen]] ergibt sich $(\overline a)^{p-1}=\overline 1$. 
