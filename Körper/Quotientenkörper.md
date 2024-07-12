Sei $R$ ein [[Kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereich]]. Dann gibt es einen bis auf [[Ringhomomorphismen|Isomorphie]] eindeutig bestimmten [[Körper]] $Q$ mit $R$ Teilring von $Q$, sodass für jedes $q \in Q$ $r,s \in R$ existieren, sodass $r\cdot q = s$. 
Wir nennen diesen Körper $Q$ den **Quotientenkörper von $R$**. 

### Beispiele
- für $R = \mathbb{Z}$ ist $Q=\mathbb{Q}$. 
- für $R = \mathbb{Z}[i]$ ist $Q=\mathbb{Q}[i]$, denn $\frac{a+bi}{c+di}$ hat rationalen Real und Imaginärteil durch Nachrechnen
- Für $R = \mathbb{K}[X]$ mit [[Kommutative Ringe#Körper|$\mathbb{K}$ Körper]], ist $Q$ der Körper $\mathbb{K}(x)$, der "rationalen Funktionen" auf $\mathbb{K}$, also z.B. $\frac {x+1}{x-1}$. Das ist aber als abstrakter Ausdruck aufzufassen und keine richtige Funktion. Das ist eine [[Körper#einfache Körpererweiterungen|einfache]] und [[Körper#Grad|unendliche Körpererweiterung]]. 

## Polynomringe von faktoriellen Ringen mit Quotientenkörper
Ähnlich wie im Abschnitt [[Polynomringe#Ganzzahlige Polynome]] kann man zeigen:

Sei $R$ ein [[Kommutative Ringe#faktorielle Ringe|faktorieller Ring]] mit Quotientenkörper $Q$. Dann gilt:
1) Ist $p\in R[X]$ irreduzibel und $grad(p)\geq 1$, so ist $p$ [[Kommutative Ringe#Prim- und irreduzible Elemente|irreduzibel]] in $Q[X]$, [[Polynomringe#Primitive Polynome|primitiv]] und prim.
2) Jedes $p\in R[X]$ ist ein Produkt eines Elementes $a \in R$ und irreduzibler, primitiver $p_{i} \in R[X]$
3) $R[X]$ ist faktoriell
4) Die Primelemente von $R[X]$ sind die Primelemente in $R$ und die primitiven Polynome, die in $Q[X]$ irreduzibel sind.

