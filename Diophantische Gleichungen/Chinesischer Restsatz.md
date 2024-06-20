Der chinesische Restsatz ermöglicht es (mithilfe von [[Diophantische Gleichungssysteme#Kongruenzen|Kongruenzeigenschaften]]) [[Diophantische Gleichungssysteme]] zu lösen.

# Aussage
Sei $k\in \mathbb{N}$ und $m_{1},...,m_{k}\in \mathbb{N}$ paarweise [[kommutative Ringe#Teilerfremde Elemente|teilerfremd]] in $\mathbb{Z}$. Seien $a_1,...,a_{k}\in \mathbb{Z}$. Dann ist $$x\equiv a_{i}\mod m_{i}, \quad i=1,...,k$$lösbar in $\mathbb{Z}$ und die Lösungsmenge ist eine Restklasse modulo $m_{1}\cdot ... \cdot m_{k}$.

#### Beweis / Lösungsmethode
Induktion nach $k$
**Induktionsanfang** $k=1$: Dann ist die Lösungsmenge genau die Restklasse $\overline{a_{1}}$ modulo $m_{1}$.

**Induktionsvorraussetzung**: Sei $k-1 \in \mathbb{N}$ und beide Aussagen dafür bewiesen

**Induktionsschluss**: Dann gibt es ein $y$ s.d. $y \equiv a_{i} \mod m_{i}$ für $i=1,...,k-1$ nach Induktionsvorraussetzung und $x\equiv a_{i}\mod m_{i}$ für $i=1,...,k-1$ äquivalent  zu $x\equiv \mod m_{1}\cdot...\cdot m_{k-1}=: l$. 

Dann ist $l$ teilerfremd zu $m_{k}$.  Suche also die Lösungsmenge von $$\begin{gathered}x \equiv y \mod l\\x \equiv a_{k}\mod m_{k}\end{gathered}$$was äquvalent dazu ist, $x,r,s \in \mathbb{Z}$ zu suchen, sodass $$(**)\begin{cases}s\cdot l + x = y \\r\cdot m_{k}+x = a_{k}\end{cases}$$subtrahieren der beiden Zeilen liefert $s\cdot l - r \cdot m_{k}=y-a_{k}$. Dazu löse (da $l,m_{k}$ teilerfremd) $\tilde{s}\cdot l + \tilde r\cdot m_{k}=1$ mithilfe des [[Euklidische Ringe#(Erweiterter-) Euklidischer Algorithmus|Erweiterten Euklidischen Algorithmus]]. Dann ist $s=(y-a_{k})\cdot \tilde{s}$ und $r = - (y-a_{k})\cdot \tilde r$ die gesuchte Lösung, was mit wieder einsetzen eine Lösung $x_{0}$ liefert.

**Lösungsmenge**: Es gilt $(**)\iff \begin{cases}x\equiv x_{0} \mod l \\x \equiv x_{0} \mod m_{k}\end{cases}$ wobei $x_{0}$ eine Lösung von $(**)$ ist.
Das ist äquivalent zu $x-x_{0}$ teilbar durch $l$ und $m_{k}$ $\overset{\text{teilerfremd}}\iff l\cdot m_{k}=m\mid x-x_{0}$. Also ist die Lösungsmenge genau eine Restklasse modulo $m$.

> [!Book] Allgemeinheit
> Die Aussagen gelten in jedem [[Hauptidealringe|Hauptidealring]]. 

### Interpretation in der Ringtheorie
Seien $k\in \mathbb{N}, m_{1},...,m_{k}\in \mathbb{Z}$ paarweise teilerfremd und $m := m_{1}\cdot...\cdot m_{k}$.  Dann existiert eine kanonische Bijektion $$\Phi:(\mathbb{Z}/ m \mathbb{Z}) \rightarrow (\mathbb{Z}/m_{1}\mathbb{Z})\times\dots\times (\mathbb{Z}/m_{k}\mathbb{Z}), \overline x \mapsto (\overline x, ..., \overline x)$$Wenn man Addition und Multiplikation komponentenweise definiert ist das sogar ein [[Ringhomomorphismen|Ringisomorphismus]]. 
