Seien $(R_{1}, +_{1}, \cdot_{1}), (R_{2}, +_{2}, \cdot_{2})$ zwei [[Kommutative Ringe]]. Eine Abbildung $\varphi:R_{1} \rightarrow R_{2}$  heißt **Ring-Homomorphismus**, wenn für alle $a,b\in R_{1}$ gilt, dass
- $\varphi(a\cdot_{1}b) = \varphi(a)\cdot_{2}\varphi(b)$ 
- $\varphi(a+_{1}b)=\varphi(a)+_{2}\varphi(b)$ 

Falls $\varphi$ bijektiv, so heißt $\varphi$ **Isomorphismus**.
Insbesondere ist jeder Ringhomomorphismus ein [[Gruppenhomomorphismen|Gruppenhomomorphismus bezüglich der Addition]]. 

Wenn $R_{1},R_{2}$ [[Körper]] sind heißt $\varphi$ **Körperhomomorphismus** bzw. **-isomorphismus**.
##### Eigenschaften
- Die Komposition von Ringhomomorphismen ist wieder ein Ringhomomorphismus.
- $\varphi(0)=0$
- Für $\varphi \neq 0$ und $R_{2}$ [[Kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereich]] gilt $\varphi(1)=1$
- $a\mid b \implies \varphi(a)\mid \varphi (b)$ 
##### Beispiele
- $x \mapsto 0$
- die kanonische Einbettung eines Teilrings
- Die Projektion $R \rightarrow R/I,a\mapsto\bar{a}$ 

# Kern
Für einen Ringhomomorphismus $\varphi:R_{1} \rightarrow R_{2}$ ist der **Kern** von $\varphi$ definiert als $$Ker(\varphi):=\varphi^{-1}(\{0\})$$
### Eigenschaften
- Der Kern ist ein [[Ideale|Ideal]]
- $\varphi$ injektiv $\iff Ker(\varphi) = \{0\}$
- Ist $R_{1}$ ein [[Körper]] so ist $\varphi = 0$ oder injektiv.