Wir nennen eine Zahl $a \in \mathbb{R}$ konstruierbar $\iff$ $(0,a) \in \mathbb{R}^2$ ist [[Formalisierung von Konstruktionen mit Zirkel und Lineal#Allgemeine Frage der Konstruierbarkeit|konstruierbar]]. 

Da $(a,b)$ konstruierbar $\iff (0,a), (0,b) \in \mathbb{R}^{2}$ konstruierbar gilt, "verlieren" wir dabei auch keine Punkte.
###### Beweis
"$\Rightarrow$"<iframe scrolling="no" title="Lemma  12.1 - Hinrichtung" src="https://www.geogebra.org/material/iframe/id/vgzdk2vb/width/1911/height/859/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="360px" style="border:0px;"> </iframe>
"$\Leftarrow$"
Die Rückrichtung ist quasi identisch, nur aus umgekehrter Richtung. Der Kreis hat Radius $\lVert (0,0) - (0,a)\rVert$ und wir bilden statt dem jeweiligen Lot die Orthogonale.

# Algebraische Eigenschaften
### Körpereigenschaft
Es gilt $\mathbb{K} := \set{a \in \mathbb{R} : \text{a konstruierbar}}$ ist ein [[kommutative Ringe#Körper|Körper]].
#### Beweis
Wir müssen zeigen, dass $\mathbb{K}$ ein Unterkörper von $\mathbb{R}$ ist. Da $(0,0),(0,1)$ direkt gegeben sind, sind $0,1$ konstruierbar also in $\mathbb{K}$. 

Seien $a,b \in \mathbb{K}$. 
###### $a-b \in \mathbb{K}$
<iframe scrolling="no" title="a-b in K" src="https://www.geogebra.org/material/iframe/id/uxrw9mpr/width/1911/height/859/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="360px" style="border:0px;"> </iframe>

###### Falls $b \neq 0$, $\frac a b \in \mathbb{K}$ 
<iframe scrolling="no" title="a/b ist im Körper" src="https://www.geogebra.org/material/iframe/id/wy99fyqz/width/1911/height/859/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="360px" style="border:0px;"> </iframe>

### Quadratwurzeln
Es gilt, falls $a \in \mathbb{K}$ positiv, dann ist auch $\sqrt a \in \mathbb{K}$. 
#### Beweis
<iframe scrolling="no" title="Konstruktion von Quadratwurzeln" src="https://www.geogebra.org/material/iframe/id/k9gcgdpw/width/1911/height/859/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="360px" style="border:0px;"> </iframe>
## Vollständige Charakterisierung
Es gilt $r \in \mathbb{K}$ genau dann wenn, es endlich viele [[kommutative Ringe#Körper|Körper]] $K_{i}$ gibt mit$$\mathbb{Q}=K_{0}\subset K_{1}\subset ... \subset K_{m}$$und positive Zahlen $d_{i} \in K_{i}$, sodass $r \in K_{m}$ und $$K_{i+1}=K_{i}[\sqrt{d_{i}}]=\set{a+b\cdot\sqrt{d_{i}}:a,b \in K_{i}}$$
#### Beweis
"$\Leftarrow$" ist wegen [[#Algebraische Eigenschaften#Quadratwurzeln|der Konstruierbarkeit von Wurzeln]] und der [[#Körpereigenschaft]] klar.

"$\Rightarrow$" Sei die Menge aller solchen $r$'s gegeben durch $\mathbb{K}'$.

z.Z. Hat eine Menge an Knoten $M$ Koordinaten in $\mathbb{K}'$, dann hat jeder [[Formalisierung von Konstruktionen mit Zirkel und Lineal|konstruierbare]] Knoten Koordinaten in $\mathbb{K}'$, denn $(0,1), (0,0)$ sind insbesondere immer in $\mathbb{K}'$. 
Es genügt zu zeigen, dass die in einem Schritt konstruierbaren Punkte wieder in $\mathbb{K}'$ liegen.
###### Schnitt von zwei Geraden
Eine Gerade $l$ durch Punkte $A,B \in M$ ist gegeben durch $\set{\begin{pmatrix}x \\ y\end{pmatrix} \in \mathbb{R}^{2} : ax+by = c}$ mit $a,b,c \in \mathbb{K}'$. Insbesondere ist für zwei unterschiedliche Geraden entweder die Schnittmenge leer oder eindeutig. Da allerdings die Schnittmenge von zwei Geraden durch ein LGS gegeben ist und dies auch über $\mathbb{K}' \subset \mathbb{R}$ lösbar ist, muss die eindeutige Lösung Koordinaten in $\mathbb{K}'$ haben

###### Schnitt von Kreisen
Sei $(a,b) \in M$ der Mittelpunkt und $r \in \mathbb{K}'$ der Radius eines Kreises $\mathcal{K}$. Dann ist der Kreis gegeben durch $\mathcal{K} = \set{\begin{pmatrix}x \\ y\end{pmatrix} : (x-a)^{2}+ (y-b)^{2} = r^{2}}$. Die Schnittmenge ist gegeben durch die Lösungsmenge des Gleichungssystems in $\mathbb{R}^2$$$\begin{cases}(x-a)^{2}+(y-b)^{2}=r^{2} \\(x-c)^{2}+(y-d)^{2}=r'^{2}\end{cases}$$Wenn man die zweite von der ersten Zeile abzieht, kann man nach $x$ oder $y$ umstellen (potentiell nur nach einem davon) und in die zweite Gleichung einsetzen. Das liefert uns eine quadratische Gleichung die mit pq-Formel die Lösungen (wenn existent)$$\lambda \pm \sqrt{\mu}$$hat, mit $\lambda, \mu \in \mathbb{K}'$. Also sind auch die Koordinaten von dem Schnittpunkt in $\mathbb{K}'$. 

FALSCH potentiell wurzel
###### Schnitt von Kreisen und Gerade
Mit [[#Schnitt von Kreisen]] und [[#Schnitt von zwei Geraden]] wissen wir dass der Schnitt eines Kreises und einer Gerade gegeben ist durch $$\begin{cases}(x-a)^{2}+(y-b)^{2}=r^{2} \\cx+dy=e\end{cases}$$Wenn man die erste Zeile nach $x$ oder $y$ umstellt (je nachdem ob $d = 0$) und in die erste Gleichung einsetzt erhält man mit der pq-Formel, dass die Lösungen (wenn existent) die Form $$\lambda \pm \sqrt{\mu}$$mit $\lambda, \mu \in \mathbb{K}'$ haben. Insbesondere ist aber aufgrund der Beschaffenheit von $\mathbb{K}'$ auch $x \in \mathbb{K}'$ und damit auch $y \in \mathbb{K}'$   