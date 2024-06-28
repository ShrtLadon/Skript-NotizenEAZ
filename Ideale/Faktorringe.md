Sei $R$ ein [[kommutative Ringe|kommutativer Ring]]. 

# Modulo
Sei $I\subseteq R$ [[Ideale|Ideal]] und $a,b \in R$ ist $a\equiv_{I}b$ bzw. $a$ und $b$ **kongruent modulo I**, wenn$$a-b\in I$$Das ist eine Äquivalenzrelation. Wir bezeichnen die Äquivalenzklasse von $a$ als **Restklasse** von $a$ und schreiben $\bar{a}$ oder $a+I$ 
### Eigenschaften
- Für $a \equiv_{I} b$ und $c \equiv_{I} d$ gilt $a+c \equiv_{I} b+d$ und $a\cdot c \equiv_{I} b \cdot d$ 


# Faktorringe
Sei $I\subseteq R$ Ideal. Dann ist der **Faktorring modulo I** die Menge der Restklassen$$R/I:=\{\bar{a}:a\in R\}$$ mit der Addition $\bar{a} + \bar{b} := \bar{a+b}$ und Multiplikation $\bar{a}\cdot\bar{b}:= \overline{a\cdot b}$.

Das ist ein kommutativer Ring mit $\bar 0$ als Nullelement und $\bar 1$ als Einselement.

### Beispiele
- $R / \{0\}=R$ und $R/R$ der Nullring
- Für $R = \mathbb{Z}, I = n \mathbb{Z}$ ist $R/I= \mathbb{Z}/n\mathbb{Z}$ 