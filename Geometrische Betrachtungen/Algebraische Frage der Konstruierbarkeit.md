Wir nennen eine Zahl $a \in \mathbb{R}$ konstruierbar $\iff$ $(0,a) \in \mathbb{R}^2$ ist [[Formalisierung von Konstruktionen mit Zirkel und Lineal#Allgemeine Frage der Konstruierbarkeit|konstruierbar]]. 

Da $(a,b)$ konstruierbar $\iff (0,a), (0,b) \in \mathbb{R}^{2}$ konstruierbar gilt, "verlieren" wir dabei auch keine Punkte.
###### Beweis
"$\Rightarrow$"<iframe scrolling="no" title="Lemma  12.1 - Hinrichtung" src="https://www.geogebra.org/material/iframe/id/vgzdk2vb/width/1911/height/859/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="360px" style="border:0px;"> </iframe>
"$\Leftarrow$"
Die Rückrichtung ist quasi identisch, nur aus umgekehrter Richtung. Der Kreis hat Radius $\lVert (0,0) - (0,a)\rVert$ und wir bilden statt dem jeweiligen Lot die Orthogonale.

# Algebraische Eigenschaften
### Körpereigenschaft
Es gilt $\mathbb{K} := \set{a \in \mathbb{R} : \text{a konstruierbar}}$ ist ein [[Kommutative Ringe#Körper|Körper]].
#### Beweis
Wir müssen zeigen, dass $\mathbb{K}$ ein [[Körper#Teilkörper|Teilkörper]] von $\mathbb{R}$ ist. Da $(0,0),(0,1)$ direkt gegeben sind, sind $0,1$ konstruierbar also in $\mathbb{K}$. 

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
Es gilt $r \in \mathbb{K}$ genau dann wenn, es endlich viele [[Körper]] $K_{i}$ gibt mit$$\mathbb{Q}=K_{0}\subset K_{1}\subset ... \subset K_{m}$$und positive Zahlen $d_{i} \in K_{i}$, sodass $r \in K_{m}$ und $$K_{i+1}=K_{i}[\sqrt{d_{i}}]=\set{a+b\cdot\sqrt{d_{i}}:a,b \in K_{i}}$$
#### Beweis
"$\Leftarrow$" ist wegen [[#Algebraische Eigenschaften#Quadratwurzeln|der Konstruierbarkeit von Wurzeln]] und der [[#Körpereigenschaft]] klar.

"$\Rightarrow$" Sei die Menge aller solchen $r$'s gegeben durch $\mathbb{K}'$.

z.Z. Hat eine Menge an Knoten $M$ Koordinaten in $\mathbb{K}'$, dann hat jeder [[Formalisierung von Konstruktionen mit Zirkel und Lineal|konstruierbare]] Knoten Koordinaten in $\mathbb{K}'$, denn $(0,1), (0,0)$ sind insbesondere immer in $\mathbb{K}'$. 
Es genügt zu zeigen, dass die in einem Schritt konstruierbaren Punkte wieder in $\mathbb{K}'$ liegen.
###### Schnitt von zwei Geraden
Eine Gerade $l$ durch Punkte $A,B \in M$ ist gegeben durch $\set{\begin{pmatrix}x \\ y\end{pmatrix} \in \mathbb{R}^{2} : ax+by = c}$ mit $a,b,c \in \mathbb{K}'$. Insbesondere ist für zwei unterschiedliche Geraden entweder die Schnittmenge leer oder eindeutig. Da allerdings die Schnittmenge von zwei Geraden durch ein LGS gegeben ist und dies auch über $\mathbb{K}' \subset \mathbb{R}$ lösbar ist, muss die eindeutige Lösung Koordinaten in $\mathbb{K}'$ haben

###### Schnitt von Kreisen
Sei $(a,b) \in M$ der Mittelpunkt und $r \in \mathbb{K}'$ der Radius eines Kreises $\mathcal{K}$. Dann ist der Kreis gegeben durch $\mathcal{K} = \set{\begin{pmatrix}x \\ y\end{pmatrix} : (x-a)^{2}+ (y-b)^{2} = r^{2}}$. Die Schnittmenge ist gegeben durch die Lösungsmenge des Gleichungssystems in $\mathbb{R}^2$$$\begin{cases}(x-a)^{2}+(y-b)^{2}=r^{2} \\(x-c)^{2}+(y-d)^{2}=r'^{2}\end{cases}$$Wenn man die zweite von der ersten Zeile abzieht, kann man nach $x$ oder $y$ umstellen (potentiell nur nach einem davon) und in die zweite Gleichung einsetzen. Das liefert uns eine quadratische Gleichung die mit pq-Formel die Lösungen (wenn existent)$$\lambda \pm \sqrt{\mu}$$hat, mit $\lambda, \mu \in \mathbb{K}'$. Also sind auch die Koordinaten von dem Schnittpunkt in $\mathbb{K}'$. 
###### Schnitt von Kreisen und Gerade
Mit [[#Schnitt von Kreisen]] und [[#Schnitt von zwei Geraden]] wissen wir dass der Schnitt eines Kreises und einer Gerade gegeben ist durch $$\begin{cases}(x-a)^{2}+(y-b)^{2}=r^{2} \\cx+dy=e\end{cases}$$Wenn man die erste Zeile nach $x$ oder $y$ umstellt (je nachdem ob $d = 0$) und in die erste Gleichung einsetzt erhält man mit der pq-Formel, dass die Lösungen (wenn existent) die Form $$\lambda \pm \sqrt{\mu}$$mit $\lambda, \mu \in \mathbb{K}'$ haben. Insbesondere ist aber aufgrund der Beschaffenheit von $\mathbb{K}'$ auch $x \in \mathbb{K}'$ und damit auch $y \in \mathbb{K}'$   


### Zusammenhang zu Körpererweiterungen
Sei $a \in \mathbb{R}$ konstruierbar. Dann gibt es ein $m\in \mathbb{N}_{0}$ und einen [[Körper]] $K\subset \mathbb{R}$ mit $a\in K$ und [[Körpererweiterungen#Grad|$[K:\mathbb{Q}]$]]$=2^{m}$. 
Insbesondere bedeutet das $a$ ist [[Körpererweiterungen#algebraische und transzendente Elemente|algebraisch]] über $\mathbb{Q}$ und $\mathbb{Q}(a)=\mathbb{Q}=2^{l}$.
###### Beweis
Nach obiger [[#Körpereigenschaft|Charakterisierung]] existieren $$\mathbb{Q}=K_{0}\subset K_{1}\subset ... \subset K_{m}\ni a$$und positive Zahlen $d_{i} \in K_{i}$ mit $K_{i}[\sqrt{d_{i}}]=K_{i+1}$.
Außerdem gilt $K_{i}[\sqrt{d_{i}}]=$[[Körpererweiterungen#einfache Körpererweiterungen|$K_{i}(\sqrt{d_{i}})$]] und $[K_{i+1}:K_{i}]\leq 2$ (1 ist auch möglich, wenn $\sqrt{d_{i}} \in K_{i}$). Wegen [[Körpererweiterungen#Gradsatz|Gradsatz]] existiert also ein $m'\in \mathbb{N}_{0}$ mit $$[K_{m}:\mathbb{Q}]=[K_{m}:K_{m-1}]\cdot...\cdot[K_{1}: \mathbb{Q}]=2^{m'}$$Wegen dem Gradsatz ist außerdem $[\mathbb{Q}(a):\mathbb{Q}]$ ein [[Kommutative Ringe#Teiler|Teiler]] von $[K_{m}:\mathbb{Q}]$ also existiert ein $l'\in \mathbb{N}_{0}$, sodass $[\mathbb{Q}(a):\mathbb{Q}]=2^{l}$. 

# nicht konstruierbare Knoten
### Quadratur des Kreises
Die Frage nach der Quadratur des Kreises, ist ob man ausgehend von einem Kreis ein Quadrat mit dem selben Flächeninhalt [[Formalisierung von Konstruktionen mit Zirkel und Lineal|konstruieren]] kann. Also:
<iframe scrolling="no" title="Quadratur des Kreises" src="https://www.geogebra.org/material/iframe/id/gp5bcauw/width/1911/height/859/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="360px" style="border:0px;"> </iframe>Es gilt ein solches Quadrat müsste die Seitenlänge $\sqrt{\pi}\cdot r$ haben, wobei $r$ der Radius vom Kreis ist. Wegen der Abgeschlossenheit unter Multiplikation ([[#Körpereigenschaft]]) ist es ausreichend zu zeigen, dass $\sqrt \pi$ nicht konstruierbar ist.

Es gilt nach [[Körpererweiterungen#algebraische und transzendente Elemente#Beispiele|Satz von Lindemann]], dass $\pi$ nicht algebraisch ist. Wenn $\sqrt \pi$ algebraisch wäre, so wäre [[Körpererweiterungen#algebraische Teilkörper und Verknüpfungen von algebraischen Elementen|$\sqrt \pi \cdot \sqrt\pi$]]$=\pi$ auch algebraisch, was ein Widerspruch ist. Also ist wegen dem [[#Zusammenhang zu Körpererweiterungen]] $\sqrt \pi$ nicht konstruierbar.

### Verdopplung des Würfels
Die Verdopplung des Würfels ist die Frage ob man für eine Seitenlänge $a$ eine Seitenlänge $b$ konstruieren kann, sodass das Volumen des Würfels mit Seitenlänge $b$ doppelt so groß ist, wie das Volumen des Würfels mit Seitenlänge $a$. Also $b^{3}=2a^{3}$.
<iframe scrolling="no" title="Verdopplung des Würfels" src="https://www.geogebra.org/material/iframe/id/cstc8db3/width/1922/height/879/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="360px" style="border:0px;"> </iframe>

Wie bei der [[#Quadratur des Kreises]] kann man das auf die algebraische Frage zurückführen, ob $\sqrt[3]{2}$ konstruierbar ist. Da [[Körpererweiterungen#Erzeugte Körper|$[\mathbb{Q}(\sqrt[3]{2}):\mathbb{Q}]=3$]] folgt mit der obigen [[#Zusammenhang zu Körpererweiterungen|Bemerkung]], dass $\sqrt[3]{2}$ nicht konstruierbar ist, also die Verdopplung des Würfels nicht konstruierbar ist.

## Konstruktion regelmäßiger n-Ecke
Sei $n \geq 2$, dann ist äquivalent:
1) ein regelmäßiges $n$-Eck ist konstruierbar (d.h.) alle Seiten eines n-Ecks sind gleich lang.
2) $(\cos(\frac{2\pi}{n}), \sin(\frac{2\pi}n))$ ist als Knoten konstruierbar
3) $\cos(\frac{2\pi}n)$ ist eine konstruierbare Zahl
4) Ist $\alpha_{n}\in \mathbb{C}$ die primitive $n$-te Einheitswurzel (also $\alpha_{n}=e^{\frac{2\pi i}n}$), so gibt es eine Folge an $$\mathbb{Q} \subset K_{1} \subset...\subset K_{m}\ni \alpha_{n}$$[[Körpererweiterungen]] vom jeweiligen [[Körpererweiterungen#Grad|Grad]] 2.

###### Beweis
Durch Skalierung - wir können durch die Länge des Radius, des n-Ecks teilen, weil wir die [[#Quadratwurzeln]] berechnen können - ist o.B.d.A. der Radius des n-Ecks $1$.
$1)\implies 2)$
Für $n=2$ klar, für den Rest folgt wegen Seite-Seite-Seite, dass alle Winkel im $n$-Eck gleich groß sein müssen. Damit ist der "erste" Punkt auf dem n-Eck im Uhrzeigersinn ausgehend von $(1,0)$ konstruierbar und genau $(\cos(\frac{2\pi}n), \sin(\frac{2\pi}n))$.
<iframe scrolling="no" title="cos(2pi/n,sin(2pi/n)) konstruierbar" src="https://www.geogebra.org/material/iframe/id/mrja7efv/width/1911/height/859/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="360px" style="border:0px;"> </iframe>
$2) \implies 1)$
Für $n=2$ klar, sonst können wir iterativ Kreise um die Eckpunkte (startend bei $(\cos(\frac{2\pi}n),\sin(\frac{2\pi}n)$) mit Radius $\lVert (1,0)-(\cos(\frac{2\pi}n),\sin(\frac{2\pi}n))\rVert$ und dessen Schnittpunkte mit dem Einheitskreis betrachten:
<iframe scrolling="no" title="n-Eck aus cos,sin konstruieren" src="https://www.geogebra.org/material/iframe/id/tbjkh2ee/width/1911/height/859/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="360px" style="border:0px;"> </iframe>

$3) \implies 2)$ Das ist nach Schulwissen genau der Schnittpunkt vom Einheitskreis und der Senkrechte durch $(\cos(\frac{2\pi}n),0)$ - d.h. die Gerade durch $(\cos(\frac{2\pi}n,2$) und diesen Punkt), wobei $(\cos(\frac{2\pi}n,2$) wegen der [[#Körpereigenschaft]] immer konstruierbar ist.
<iframe scrolling="no" title="nEck-3->2" src="https://www.geogebra.org/material/iframe/id/z4smgh37/width/1911/height/859/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="360px" style="border:0px;"> </iframe>
$2) \implies 4)$:
Dann existieren $K_{1},...,K_{m},...,K_l$ nach der [[#Vollständige Charakterisierung|Vollständigen Charakterisierung]] mit $\cos\left(\frac{2\pi}n\right)\in K_{m}$, $\sin(\frac{2\pi}n)\in K_{l}$ und $$\mathbb{Q}\subset K_{1}\subset...\subset K_{m}\subset ... \subset K_{l} \subsetneq \mathbb{R}$$ wobei $[K_{i+1}:K_{i}]=2$. Insbesondere ist dann $\alpha_{n}= \cos(2π / n)+ i\cdot \sin(2π / n) \in K_{l}(i)$ und $[K_{l}(i):K_{l}]=2$, [[Körpererweiterungen#Charakterisierung von einfachen Körpererweiterungen|denn $i$ ist eine Nullstelle von $X^{2}+1\in K_{l}[X]$]].

$4) \implies 3)$ Dann ist in jedem Schritt $K_{i+1}=K_{i}(\sqrt{d})$ für ein $d \in K_{i}$, nach [[Körpererweiterungen#Erweiterungen von Grad 1 und 2|diesem Satz]]. Insbesondere bedeutet das, dass wir die Nullstellen vom Polynom $X^{2}-d \in K_{i}[X]$ hinzufügen. Da gilt $\sqrt{d}=\sqrt{\frac{\lvert d\rvert + Re(d)}2} + i\cdot \text{sgn}^{+}(Im(d)) \cdot\sqrt{\frac{\lvert d\rvert - Re(d)}2}$  siehe [Wikipedia](https://de.wikipedia.org/wiki/Quadratwurzel#Definition). Insbesondere können wir die einzelnen Komponenten jeweils aus den Real und Imaginärteil und Quadratwurzeln konstruieren ($\lvert d\rvert=\sqrt{Re(d)^{2}+Im(d)^2}$), d.h. wir können induktiv die Körpererweiterungen ersetzen, sodass am Ende die Kette in $\mathbb{R}$ bleibt, aber $Re(\alpha_n)=\cos(\frac{2\pi}n)$ in $K'_m$ ist.

#### Konstruierbarkeit von regelmäßigen Teiler-Ecken
Sei $n=m_{1}\cdot m_{2}$. Dann gilt:
1) Ist ein regelmäßiges $n$-Eck konstruierbar, so ist auch ein regelmäßiges $m_{1}$ Eck konstruierbar
2) Ist ein regelmäßiges $n$-Eck konstruierbar, so ist auch ein regelmäßiges $2n$-Eck konstruierbar
3) Sind $m_{1},m_{2}$ [[Kommutative Ringe#Teilerfremde Elemente|teilerfremd]] und regelmäßige $m_{1}$- bzw. $m_2$-Ecke konstruierbar, dann ist auch ein $n$-Eck konstruierbar.

###### Beweis
1) Wähle jeden $m_2$-ten Knoten. Daraus folgt direkt die Behauptung, weil wir jeweils den Winkel dazwischen ver$m_2$fachen. 
2) Es gilt [[Formalisierung von Konstruktionen mit Zirkel und Lineal#Konstruktion einer Winkelhalbierenden|Winkelhalbierende]] sind konstruierbar. Insbesondere können wir damit ein $2n$-Eck konstruieren, indem wir jeden Winkel halbieren und den Schnittpunkt mit dem Einheitskreis betrachten
3) Es gilt in [[Euklidische Ringe#(Erweiterter-) Euklidischer Algorithmus|$\mathbb{Z}$]] dass $k_{1},k_{2}\in \mathbb{Z}$ existieren, sodass $k_{1}\cdot m_{1} + k_{2}\cdot m_{2}=1$. Insbesondere gilt also $k_{2}\cdot \frac{2\pi}{m_{1}}+ k_{1}\cdot \frac{2\pi}{m_{2}}=\frac{2\pi\cdot(k_{2}m_{2}+k_{1}m_{1})}{m_{1}\cdot m_{2}}=\frac{2\pi}n$. Das liefert uns ein Abtragen von Winkeln, die wir konstruieren können und damit können wir $\cos(\frac{2\pi}n)$ konstruieren (alternativ Additionstheoreme verwenden)

#### Prim-Ecke
Sei $p$ eine [[Primzahlen|Primzahl]] und $\alpha_{p}\neq 1$ eine $p$-te Einheitswurzel. 
1) Dann gilt [[Körpererweiterungen#Grad|$[\mathbb{Q}(\alpha):\mathbb{Q}]$]]$=p-1$.
2) Ist ein regelmäßiges $p$-Eck konstruierbar, so ist $p-1$ eine Zweierpotenz
3) In diesem Fall hat $p$ die Form $2^{2^{n}}+1$ mit $n\in \mathbb{N}_{0}$

###### Beweis
1) Betrachte $(X^p-1)=(X-1)(X^{p-1}+X^{p-2}+...+1)$. Wir haben bereits [[Polynomringe#Kriterium von Eisenstein#Beispiel|gezeigt]], dass $(X^{p-1}+...+1)$ irreduzibel in $\mathbb{\mathbb{Q}}[X]$ ist. Insbesondere ist $\alpha$ eine Nullstelle von diesem Polynom also gilt nach [[Körpererweiterungen#Charakterisierung von einfachen Körpererweiterungen|Charakterisierung von einfachen Körpererweiterungen]], dass $[\mathbb{Q}(\alpha):\mathbb{Q}]=p-1$.
2) Das folgt direkt aus den äquivalenten Formulierungen für die [[#Konstruktion regelmäßiger n-Ecke]] und dem [[Körpererweiterungen#Gradsatz|Gradsatz]].
3) Mit 2) gilt $p-1=2^{k}$. Annahme: $k$ ist keine Zweierpotenz, also $k=2^{l}\cdot m$ mit $2\not\mid m$ und $l\in \mathbb{N}_{0}$. Dann ist $p=2^{k}+1=2^{m\cdot 2 ^{l}}+1=(2^{2^{l}})^{m}+1$.
	Wir werden zeigen, dass $x^{m}+y^{m}$ durch $x+y$ teilbar ist, woraus direkt ein Widerspruch folgt, denn $p$ ist prim. Dazu beginnen wir mit einer wahren Aussage und folgern:$$\begin{align}&x+y \equiv0 &\mod x+y\\\implies&x\equiv -y &\mod x+y\\\implies&x^{m}\equiv(-y)^{m}&\mod x+y\\\overset{2 \not\mid m}\implies&x^{m}=-y^{m}&\mod x+y\\\implies&(x+y)\mid x^{m}-y^{m}\end{align}$$
#### $p^{2}$-Ecken bei ungeraden Primzahlen
Sei $p$ eine ungerade [[Primzahlen|Primzahl]] und $\alpha_{p}$ eine primitive $p^{2}$-te Einheitswurzel. Dann gilt:
1) Das Polynom $g_{p}:=(X^{p^{2}}-1)/X^{p}-1=((X^{p})^{p-1}+...+X^{p}+1)$ ist irreduzibel in $\mathbb{Q}[X]$
2) $[\mathbb{Q}(\alpha_{p}):\mathbb{Q}]=p^{2}-p$.
3) $\alpha_{p}$ ist nicht konstruierbar (als Polarkoordinaten interpretiert)
4) Regelmäßige $p^{2}$-Ecke sind nicht konstruierbar
5) Regelmäßige $p^{l}$-Ecke sind nicht konstruierbar für $l\geq 2$

###### Beweis
1) Man geht hier analog vor wie in [[Polynomringe#Kriterium von Eisenstein#Beispiel#Beweis|dem Beispiel]], indem man $X^{p^{2}}-1$ passend verschiebt
2)  Insbesondere ist $\alpha_{p}$ eine Nullstelle von $g_{p}$ also gilt nach [[Körpererweiterungen#Charakterisierung von einfachen Körpererweiterungen|Charakterisierung von einfachen Körpererweiterungen]], dass $[\mathbb{Q}(\alpha):\mathbb{Q}]=p(p-1)=p^2-p$.
3) $p^{2}-p$ ist ungerade also keine Zweierpotenz, was es nach [[#Konstruktion regelmäßiger n-Ecke]] sein müsste.
4) folgt direkt aus 3) mit obiger Charakterisierung von Konstruierbarkeit von $n$-Ecken
5) sonst wäre als Teiler ein $p^{2}$-Eck konstruierbar wegen der [[#Konstruierbarkeit von regelmäßigen Teiler-Ecken]].

### Satz von Gauß-Watzel
Genau dann ist ein regelmäßiges $n$-Eck konstruierbar, wenn $n$ die Form $$n=2^{s}\cdot p_{1}\cdot...\cdot p_{k}$$ hat, mit $s\geq 0$ und paarweise verschiedenen Primzahlen $p_{1},...,p_{k}$.

###### Beweis / Bemerkung
Wir haben hier mit den obigen Sätzen und Bemerkungen die eine Richtung also die Notwendigkeit dieser Form gezeigt. Die andere Richtung werden wir hier nicht beweisen, funktioniert aber mit [[Galois-Theorie]].