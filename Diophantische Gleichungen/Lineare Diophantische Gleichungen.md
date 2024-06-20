Seien $a_{1}, ..., a_{k} \in \mathbb{Z}$ und $c \in \mathbb{Z}$. Sei außerdem $t:=$ [[kommutative Ringe#Nullteiler und Integritätsbereiche|$ggT(a_{1},...,a_{k})$]]. 

##### Existenz
Dann existiert eine Lösung $(x_{1},...,x_{k}) \in \mathbb{Z}^{k}$ für $$a_{1}\cdot x_{1}+...+a_{k}\cdot x_{k} = c $$genau dann wenn $t \mid c$. 
###### Beweis und Konstruktion der Lösung
"$\Rightarrow$" Es existieren $c_{1},...,c_{k} \in \mathbb{Z}$, sodass $c_{i}\cdot t = a_{i}$. Dadurch ergibt sich für eine Lösung, dass $t\cdot c_{1} \cdot x_{1}+...+t\cdot c_{k} \cdot x_{k} = t\cdot (c_{1}\cdot x_{1}+....+c_{k}\cdot x_{k})=c$ also insgesamt $t \mid c$. 

"$\Leftarrow$" 
Zunächst überlegt man sich, dass nach Definition der größte gemeinsame Teiler von $u,v,w$ auch den $ggT(u,v)$ und $w$ teilen muss. Der größte Teiler, der dies erfüllt, kann mithilfe des [[Euklidische Ringe#(Erweiterter-) Euklidischer Algorithmus|Erweiterten Euklidischen Algorithmus]] bestimmt werden. Induktiv kann man so also Linearkombinationen für die ggTs bestimmen. Diese kann am Ende mit $\lambda$ multipliziert werden, wobei $\lambda \in \mathbb{Z}$ genauso gewählt, dass $\lambda t = c$.

##### Lösungsmenge
Es gilt für die Lösungsmenge  von $$a_{1}\cdot x_{1}+...+a_{k}\cdot x_{k}=c$$ist gegeben durch eine beliebige Lösung $z_{0}\in \mathbb{Z}^{k}$ als $$\mathcal{L}(c)=z_{0}+\mathcal{L}(0)$$
###### Beweis
"$\subseteq$"
Sei $x\in \mathcal{L}(c)$. Dann ist $x = (x-z_{0})+z_{0}$, aber außerdem wegen der Linearität der Gleichung $(x-z_{0})\in \mathcal{L}(0)$.

"$\supseteq$"
Sei $x_{0} \in \mathcal{L}(0)$. Dann gilt wegen der Linearität $x_{0}+z_{0}\in \mathcal{L}(c)$.  


###### Beispiel k = 2
Für $k=2$ ist $\mathcal{L}(0)=\set{(s\cdot \frac{a_{2}}{t}, s\cdot \frac{a_{1}}{t}):s \in \mathbb{Z}}$ 