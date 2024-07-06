Sei $R$ ein [[Kommutative Ringe|kommutativer Ring]]. Dann heißt $I \subset R$ **Ideal**, wenn 
- $(I,+)$ eine Untergruppe von $(R,+)$ ist und
- $\forall r \in R, a \in I: r \cdot a \in I$. 

#### Eigenschaften
- $1 \in I \iff I = R \iff I \cap R^{*}\neq \varnothing$
- $I,I'$ Ideal $\implies I \cap I'$ Ideal. 
- Für $I_{1} \subset I_{2} \subset ...$ Ideal ist $\bigcup_{i=1}^{\infty}I_{i}$ ein Ideal


#### Erzeugte Ideale
Für $S \subset R$ ist das von $S$ **erzeugte Ideal** $$(S) := \bigcap_{S\subseteq I, I \text{ Ideal}}I$$ Es gilt $$(S) = \{\sum\limits_{i=1}^{m}r_{i}s_{i}: r_{i}\in R, s_{i} \in S, m \in \mathbb{N}_{0}\}$$
##### Hauptideale 
Für jeden Ring $R$ und jedes $a \in R$ ist $$aR :=(a):=\{ab:b\in R\}$$ein Ideal. Wir nennen so ein Ideal ein **Hauptideal**, welches aus den Vielfachen von $a$ besteht.


###### Eigenschaften
- $a \mid b \iff b \in (a) \iff (b)\subset (a)$
	- $a\sim b \iff (a) = (b)$

### Prim- und maximale Ideale
Ein Ideal $I\subsetneq R$ heißt
- **Primideal**, wenn $ab\in I \implies a\in I$ oder $b\in I$ 
- **maximal**, wenn es kein Ideal $I \subsetneq J \neq R$ gibt. Also kein Ideal "zwischen" $I$ und $R$ existiert.

#### Eigenschaften
- $\{0\}$ Primideal $\iff R$ [[Kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereiche]].
- Hauptideal $(p), p\neq 0$ ist Primideal $\iff$ p [[Kommutative Ringe#Prim- und irreduzible Elemente|prim]].
- Ideal $I$ ist ein Primideal $\iff$ [[Faktorringe|$R/I$]] [[Kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereich]] 
- Ideal $I$ maximal $\iff$ $R / I$ [[Kommutative Ringe#Körper|Körper]]
- In einem Hauptidealring ist $I$ maximal $\iff I \neq \{0\}$ und $I$ ein Primideal.
	- Generell gilt jedes maximale Ideal ist prim.

## Beispiele
- $\{0\}, R$ sind immer Ideale
- Für $R = \mathbb{Z}$ ist $I = 2\mathbb{Z}$ ein Ideal. 
- $R \neq \{0\}$ und $\{0\}$ sind die einzigen Ideale $\iff R$ ist ein [[Kommutative Ringe#Körper|Körper]]. 


- in $\mathbb{Z}[x]$ ist $(X,2)$ kein Hauptideal, insbesondere also auch kein [[Hauptidealringe|Hauptidealring]], aber maximal.
###### Beweis
$(X,2)$ sind genau die Polynome mit gerader Konstanten. Wäre $I = (a)$ dann würde gelten $a \mid 2$. In $\mathbb{Z}[x]$ folgt daraus $a \sim 2$ oder $a \sim 1$. Allerdings impliziert $a\sim 2$, dass $(a) = (2) \not\ni X$ und $a\sim 1$, dass $I=(1)=R$ was beides nicht gilt.

Es ist maximal, denn für jedes Ideal $J \supsetneq I$ mit $p = \sum\limits_{i=0}^{n}a_{l}X^{l} = a_{0} + X(...) \in J \setminus I$ ist $a_{0} \in J$ und ungerade, denn $X(...)$ also insb. $-X(...)\in I$. Wähle also einfach die betragsmäßig nächstkleinere gerade Zahl $b_{0} \in I$. Dann gilt $a_{0}-b_{0} = 1\in J$ also $J = R$ 
