Ein [[Kommutative Ringe#Nullteiler und Integritätsbereiche|Integritätsbereich]] $R$ heißt **euklidischer Ring**, wenn es eine Abbildung $N:R \setminus \{0 \} \rightarrow \mathbb{N} \cup \{0 \}$ gibt, mit:
- $a,b \neq 0$ und $a \mid b \implies N(b) \geq N(a)$ 
- Für alle $b \in R$ und $a \neq 0$ existieren $q,r \in R$ mit $$b=qa+r$$ und $r = 0$ oder $N(r)< N(a)$

Das ist im Endeffekt ein Ring, in dem man "mit Rest teilen" kann. 

###### Eigenschaften
- $a,b$ [[Kommutative Ringe#Assoziiertheit|assoziiert]] $\implies N(a) = N(b)$ 
- $a$ [[Kommutative Ringe#Einheit|Einheit]] $\implies N(e) = N(1)$ 
- $\min N(R) = N(1)$ 
- $a \not \in R^{*} \implies N(a) > N(1)$ 
- $a \mid b$ und $a,b$ nicht assoziiert $\implies N(b) > N(a)$ 
- Jeder Euklidische Ring ist [[Kommutative Ringe#faktorielle Ringe|faktoriell]]. 
- Es gilt $a,b$ sind [[Kommutative Ringe#Teilerfremde Elemente|teilerfremd]] $\iff$ $s,t\in R$ existieren mit $s\cdot a + t \cdot b = 1$
	- siehe Abschnitt zu [[#Begründung der Funktionalität|Euklidschem Algorithmus]]

### (Erweiterter-) Euklidischer Algorithmus
In einem euklidischen Ring liefert folgender Algorithmus den [[Kommutative Ringe#Teilbarkeit|größten gemeinsamen Teiler]] von $a,b$.
```pseudo
	\begin{algorithm}
	\caption{ErweiterterEuklidischerAlgorithmus}
	\begin{algorithmic}
		\Procedure{EEA}{a,b}
        
			\State $r_{0}\gets a$
			\State $r_1 \gets$ \Call{BestimmeRest}{a,b}
			\State $i \gets 1$
			\While{$r_i \neq 0$}
				\State $r_{i + 1}\gets$ \Call{BestimmeRest}{$r_{i}$, $r_{i-1}$}
				\State $i\gets i+1$
	        \EndWhile
	    \Return $r_{i - 1}$ \Comment{Eigentlich wird (sofern $a\not\mid b$) $(r_{1},...,r_{i-1})$ zurückgegeben}
        \EndProcedure

		
        \Procedure{BestimmeRest}{a,b}
	        \State Bestimme $q,r \in R$ sodass $b = qa + r$ und $r = 0 \lor N(r)< N(a)$
	        \Return r
        \EndProcedure
	\end{algorithmic}
	\end{algorithm}
```
Mithilfe der Reste (und Teiler $q$) kann man nun durch einsetzen ausgehend von $r_{i-1}$ bis $a$ mit Umstellen eine Linearkombination von $r_{i-1}$ mit $a,b$ finden.

##### Begründung der Funktionalität
In einem euklidischen Ring gilt für die Division mit Rest von $b = q \cdot a + r$ für alle $c \in R$ $$c \mid a \land c \mid b \iff c \mid a  \land c \mid r$$
Sei also $c$ ein gemeinsamer Teiler von $a,b$. Dann ist $c$ in diesem Algorithmus auch immer jeder gemeinsame Teiler von $r_{i-1} = q_{i-1}r_{i} + r_{i+1}$ und $r_{i}$. Für $r_{i+1} = 0$ ist dann aber jeder Teiler von $r_{i-1}$ und $r_{i}$ genau ein Teiler von $q_{i-1} =: ggT(a,b)$ 


### Beweis das Euklidische Ringe faktoriell sind
1) z.Z. [[Kommutative Ringe#Prim- und irreduzible Elemente|$irreduzibel \implies prim$]]

	Sei $p$ irreduzibel.  Betrachte $a,b \in R$ mit $p\mid a \cdot b$ also ein $c \in R$ existiert, sodass $p\cdot c = a\cdot b$
	
	 Falls $p \mid a$ sind wir fertig, deshalb gelte o.B.d.A. $p\not\mid a$. Dann gilt $p \not \sim a$ und da die Teiler von $p$ nur Einheiten oder Assoziierte sind, dass $ggT(a,p) = 1$ ist. D.h. insbesondere, dass $p$ und $a$ teilerfremd sind, also $s,t \in R$ existieren, mit $$s\cdot p+t\cdot a = 1$$ Dann gilt aber für $t\cdot p \cdot c = t \cdot a \cdot b = (1-s \cdot p)\cdot t \cdot b$. Umstellen nach $b$ liefert$$b=t\cdot p \cdot c + s\cdot t \cdot b = p\cdot(tc +sb)$$also $p\mid b$. Insgesamt ist also $p$ prim.

2) z.Z. $0 \neq a \in R$ lässt sich zerlegen in $a = e \cdot p_{1}\cdot ... \cdot p_{k}$ mit $e$ Einheit und $p_{i}$ irreduzibel.

	Mache dazu starke Induktion über $N(a)\in \mathbb{N}_{0}$. 
	**IA: N(a) = N(1)** 
		Dann ist $a$ Einheit, also ist $a = a$ die gewünschte Zerlegung.

	**IS**
		Ist $a$ irreduzibel, dann sind wir fertig. Sonst existieren $b,c\in R$ keine Einheiten und nicht zu $p$ assoziiert mit $a=b\cdot c$ $\implies b \mid a, c \mid a$ $\implies N(b), N(c) < N(a)$. Das liefert uns aber mithilfe der Induktionsvorraussetzung eine Zerlegung für $a$. 

## Beispiele
Das klassische Beispiel für einen euklidischen Ring ist $\mathbb{Z}$ mit $N(a) := \vert a \vert$.

Ein weiteres Beispiel ist jeder [[Körper]] $\mathbb{K}$ mit einer konstanten Funktion als Normfunktion.

Auch die [[Kommutative Ringe#Gaußsche Zahlen|Gaußschen Zahlen]] sind mit der komplexen Betragsfunktion ein euklidischer Ring.
