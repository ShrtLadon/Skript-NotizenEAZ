Eine [[Gruppen|Gruppe]] $G$ heißt **auflösbar**, wenn es [[Gruppen#Untergruppen|Untergruppen]] $G_{1},...,G_{m}$ in $G$ gibt, sodass
- $G_{1}=\set{1}$
- $G_{m}=G$
- Für $1\leq i \leq n-1$ gilt [[Normalteiler|$G_{i}\trianglelefteq G_{i+1}$]] 
- Für $1 \leq i \leq n-1$ ist die [[Faktorgruppen|Faktorgruppe]] $G_{i+1}/G_i$ [[abelsche Gruppen|abelsch]]. 

## Eigenschaften
### Vererbung
1) Ist $G$ auflösbar und [[Gruppen#Untergruppen|$H \leq G$]], dann ist auch $H$ auflösbar.
2) Ist $G$ auflösbar und [[Normalteiler|$H \trianglelefteq G$]], so ist [[Faktorgruppen|$G/H$]] auflösbar.
3) Sei $H \trianglelefteq G$. Wenn $H$ und $G/H$ auflösbar, dann ist auch $G$ auflösbar.
##### Beweis
###### 1)
Seien $\set 1=G_{1} \trianglelefteq G_{2} \trianglelefteq ... \trianglelefteq G_{m}=G$ die Untergruppen der Auflösung von $G$. 
Setze $H_{i}:= H \cap G_{i}$ für $1 \leq i \leq m$. Dann gilt $H_{1}=\set 1$ und $H_{m}=H$. Außerdem ist der Schnitt von Untergruppen wieder eine Untergruppe (ÜB6.4) also gilt $$H_{1}\leq...\leq H_m$$*Normalteiler*: Sei $x \in H_{i+1}$ dann ist $xH_{i}x^{-1}=x(H_{i}\cap G)x^{-1}=xG_{i}x^{-1}\cap x H x^{-1}\overset{G_{i} \trianglelefteq G_{i+1}, H_{i+1}\leq H}=G_{i}\cap H=H_{i}$ also ist $H_{i} \trianglelefteq H_{i+1}$.

*abelsch*: Betrachte die [[Gruppenhomomorphismen]] $i:H_{i+1} \rightarrow G_{i+1},x\mapsto x$ und $p:G_{i+1} \rightarrow G_{i+1}/G_{i}, x \mapsto xG_{i}$. Dann ist auch die Komposition $p \circ i$ ein Homomorphismus, damit ist nach [[Faktorgruppen#Isomorphiesatz|Isomorphiesatz]] $H_{i+1}/\ker(p\circ i)\cong \text{Bild}(p\circ i)\leq G_{i+1}/G_{i}$. Da $\ker(p\circ i)=H_{i+1}\cap G_{i}=G_{i+1}\cap H \cap G_{i}\overset{G_{i}\subseteq G_{i+1}}=G_{i}\cap H=H_{i}$. Also ist $H_{i+1}/H_{i}$ isomorph zu einer Untergruppe einer abelschen Gruppe, also abelsch.
###### 2)
Seien $\set 1=G_{1} \trianglelefteq G_{2} \trianglelefteq ... \trianglelefteq G_{m}=G$ die Untergruppen der Auflösung von $G$.
Betrachte $p:G \rightarrow G/H, x \mapsto xH$ und setze $$N_{i}:=p(G_{i})\subset G/H$$Offensichtlich gilt $\set{e_{G/H}}=N_{1}\subset ... \subset N_{m}=G/H$ und als Bild eines [[Gruppenhomomorphismen#Eigenschaften|Gruppenhomomorphismus]] ist jedes $N_{i}$ eine Untergruppe von $G/H$ also wie man sich schnell an der Definition überlegt $N_{i}$ eine Untergruppe von $N_{i+1}$. 
*Normalteiler*: Sei $xG \in N_{i+1}$, also $x \in G_{i+1}$. Dann ist $$xG\cdot N_i\cdot(xG)^{-1}=\set{xnx^{-1}G\mid n \in G_i}\overset{G_{i} \trianglelefteq G_{i+1}\ni x}=p(G_{i})=N_{i}$$
*abelsch*: Ist mit einem Isomorphiesatz möglich, wurde in der VL nicht gezeigt.

###### 3)
Seien $\set 1=H_{1} \trianglelefteq H_{2} \trianglelefteq ... \trianglelefteq H_{m}=H$ die Untergruppen der Auflösung von $H$ und seien $\set 1=N_{1} \trianglelefteq N_{2} \trianglelefteq ... \trianglelefteq N_{m}=G/H$ die Untergruppen der Auflösung von $G/H$. Dann setze $$G_i:=\begin{cases}H_{i} & i\leq m \\p^{-1}(N_{i-m}) & i>m\end{cases}$$wobei $p$ die Abbildung aus [[#2)]] ist.

## Auflösbarkeit endlicher Gruppen
Sei $G$ eine endliche [[Gruppen|Gruppe]]. Dann ist $G$ auflösbar genau dann wenn es Untergruppen gibt $$\set 1 =G_{1} \trianglelefteq G_{2} \trianglelefteq ... \trianglelefteq G_{m}=G$$so dass $G_{i}/G_{i-1}$ [[Gruppen#Zyklische Gruppen|zyklisch]] sind und $\lvert G_{i}/G_{i-1}\rvert$ [[Primzahlen|prim]]
#### Beweis
##### "$\Rightarrow$"
Führe (starke) Induktion nach $\lvert G\rvert$.
*IA*: $\lvert G\rvert =1$. Dann setze $G_{1}=G_{m}=G$. Dann gilt jede Aussage für alle $G_{i}/G_{i-1}$ für $1\leq i \leq 1-1=0$, da kein solches $i$ existiert.

*IS*: 
Nach Annahme ist $G$ auflösbar also gibt es $$\set 1 =G_{1} \trianglelefteq G_{2} \trianglelefteq ... \trianglelefteq G_{m}=G$$die $G$ auflösen.
Insbesondere kann man o.B.d.A fordern, dass $G_{m-1}\subsetneq G_m$ ist (sonst streiche die gleichen Elemente). D.h. es gilt $\lvert G_{m-1}\rvert < \lvert G_m\rvert$ und mit Induktionsvoraussetzung gibt es$$\set 1 =H_{1} \trianglelefteq H_{2} \trianglelefteq ... \trianglelefteq H_{k}=G_{m-1}$$die $G_{m-1}$ auflösen und für die $\lvert H_{i}/H_{i-1}\rvert$ prim ist.
*Fall* $G_{m-1}=\set{1}$ ist $G/G_{m-1}\cong G$ [[abelsche Gruppen|abelsch]]. Wenn $\lvert G\rvert$ prim (oder 1) ist, sind wir fertig. Sei also $G$ nicht prim, dann existiert mit [[Gruppen#Theorem von Cauchy|Theorem von Cauchy]] ein nicht-triviale Untergruppe $\set{1}<U<G$. Da $G$ abelsch ist, ist jede Untergruppe ein Normalteiler von $G$ und $G/U$ auch abelsch. Wir können also o.B.d.A. vom folgenden Fall ausgehen:

*Fall* $G_{m-1}\neq\set 1$:
Nun ist wenn $G_{m-1}\subsetneq G_m$ auch $\lvert G_{m}/G_{m-1}\rvert < \lvert G\rvert$ wegen dem [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]]. 
Also gibt es nach Induktionsvoraussetzung$$\set {1_{G_{m}/G_{m-1}}} =N_{1} \trianglelefteq N_{2} \trianglelefteq ... \trianglelefteq N_{l}=G_{m}/G_{m-1}$$die $G_{m}/G_{m-1}$ auflösen und für die $\lvert N_{i}/N_{i-1}\rvert$ prim ist. 
Definiere für $2 \leq j \leq l$ $$H_{k+j}:=p^{-1}(N_{j})=\dot\bigcup_{x\in N_{j}}x$$wobei $p:G_{m} \rightarrow G_{m}/G_{m-1},x\mapsto xG_{m-1}$ ist. Die rechte Seite überlegt man sich schnell weil die $x$ genau die Mengen sind die von $p$ auf die selbe Menge geworfen werden. 
Anmerkung: Die 2 ist korrekt, weil $H_{k}=G_{m-1}=p^{-1}(\set 1)=p^{-1}(N_{1})$.
###### Beweis der geforderten Eigenschaften von $H_{n}$
Anmerkung wir müssen nirgendwo $H_{k}$ und $H_{k+1}$ gesondert betrachten, weil $H_{k}=p^{-1}(N_{1})$

Es gilt $H_{k} =G_{m-1}\subseteq H_{k+1}\subseteq...\subseteq H_{k+l}$ und für $a,b \in H_{k+j}$, dass $aG_{m-1}\cdot b^{-1}G_{m-1}\in N_{j}$, denn $N_{j} \leq G_m/G_{m-1}$. Dann ist aber auch $a\cdot b^{-1}\in H_{k+j}$. Außerdem ist $N_{j}\neq \varnothing$ und also da $p$ surjektiv $H_{k+j}\neq \varnothing$ also $H_{k+j}$ nach [[Gruppen#Untergruppenkriterium|Untergruppenkriterium]] eine Untergruppe. 

Sei $x \in H_{k+j+1}$. Dann gilt $xH_{k+j}x^{-1}=\bigcup_{n\in N_j}(xG_{m-1}n x^{-1}G_{m-1})$ wobei aber die vereinigten Mengen jeweils in $N_{j}$ liegen, da $N_{j} \trianglelefteq N_{j+1}$.

Mit Isomorphiesatz ist $H_{k+j+1}/H_{k+j}\cong H_{k+j+1}/G_{m-1}/H_{k+j}/G_{m-1}=N_{k+j+1}/N_{k+j}$ den hatten wir aber nicht. Alternativ kann man sich die Kardinalitäten "manuell" mit Satz von Lagrange überlegen und dann benutzen dass Gruppen primer Ordnung zyklisch sind.
##### "$\Leftarrow$" 
Dann gilt $G_{i+1}/G_{i}$ ist [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] also insbesondere nach ÜB6.2.3 isomorph zu $\mathbb{Z}_n$ also abelsch und damit ist $G$ auflösbar. 

### Auflösbarkeit von Gruppen der Ordnung $p^{m}$
Sei $p$ eine [[Primzahlen|Primzahl]] und $G$ eine [[Gruppen|Gruppe]] mit $\lvert G\rvert=p^{m}$. Dann ist $G$ auflösbar und es gibt eine Kette $$\set 1=G_{1} \triangleleft G_{2}\triangleleft ...\triangleleft G_{m+1}=G$$sodass $G_{i}/G_{i-1}$ zyklisch von Ordnung $p$ ist.
##### Beweis
Führe Induktion nach $m=\log_p(\lvert G\rvert)$ 
*IA* $m=1$. Dann ist $G$ [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] also folgt direkt die Behauptung.

*IS* Für $m > 1$ gilt [[Operation durch Konjugation#Konjugationsklassen, Zentralisator und Kern|$Z(G)$]] ist als Kern eines [[Gruppenhomomorphismen|Homomorphismus]] ein [[Normalteiler]] von $G$. Wenn $Z(G)=G$ (bzw. $G$ abelsch), dann sind wir fertig mit $G_{2}=G$ und $G_{1}=\set{1}$.
Wenn $Z(G) \subsetneq G$, dann ist $\lvert G/Z(G)\rvert= p^{k}$ nach [[Operation durch Konjugation#Konjugationsklassen, Zentralisator und Kern#Beweis|Beweis dieses Lemmas]]. 

Dann ist aber nach Induktionsvoraussetzung $G/Z(G)$ auflösbar mit der passenden "Auflösung". Da $Z(G)$ (weil abelsch) und $G/Z(G)$ auflösbar sind, ist auch $G$ auflösbar mit einer Kette$$\set 1=G_{1} \triangleleft G_{2}\triangleleft ...\triangleleft G_{m+1}=G$$die nach [[#Auflösbarkeit endlicher Gruppen]] alle zyklisch sind und $G_{i+1}/G_{i}$ prim viele Elemente haben. Außerdem gilt wegen [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] $\lvert G_{1}/G_{2}\rvert, \lvert G_{2}/G_{3}\rvert,... \lvert G_{m}/G_{m+1}\rvert\mid \lvert G\rvert$ also sind $\lvert G_{i+1}/G_{i} \rvert =p$. 
# Beispiele
- jede abelsche Gruppe ist auflösbar mit $G_{1}=\set{1}$ und $G_{2}=G$. 
- Wenn $\lvert G\rvert$ [[Kommutative Ringe#Prim- und irreduzible Elemente|prim]], so ist $G$ [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] also nach ÜB6.3.3 [[Gruppenhomomorphismen|isomorph]] zur abelschen Gruppe $\mathbb{Z}_{p}$ also auflösbar

### Diedergruppe
Die [[Gruppen#Diedergruppe|Diedergruppe]] $D_{2n}$ ist auflösbar, auch wenn z.B. $D_{6}\cong S_{3}$ zur [[Gruppen#symmetrische Gruppe|symmetrischen Gruppe]] nicht abelsch ist.
###### Beweis
Betrachte $G_{2}=\langle r\rangle$ die Menge der Drehungen. Das ist ein [[Normalteiler#Diedergruppe|Normalteiler von $D_{2n}$]]. Setze noch $G_{1}=\set{1}$ und $G_{3}=G$. Dann ist $G_{2}/G_{1}=G_{2}$ als zyklische Gruppe [[Gruppenhomomorphismen|isomorph]] nach ÜB6.3.3 zur abelschen Gruppe $\mathbb{Z}_{n}$ also abelsch. Auf ÜB7.1 wurde nachgerechnet, dass $\#G_{3}/G_{2}=2$. Die Gruppe mit 2 Elementen ist aber eindeutig (Verknüpfung mit 0 fest und das andere Element muss selbst-invers sein) als $\mathbb{Z}_2$ also abelsch.
### Gruppen der Ordnung < 60
Es gilt jede Gruppe der [[Gruppen#ordnung|Ordnung]] kleiner 60 ist auflösbar.

>[!Note]
>[[Symmetrische Gruppe|$\lvert S_{5}\rvert$]]$=5!=60$ und $S_{5}$ ist [[Symmetrische Gruppe#$n>4$|nicht auflösbar]]. 
##### Beweis
Sei $G$ eine Gruppe und $n=\lvert G\rvert$. 
Zum Beweis bedienen wir uns massiv bei der Eigenschaft, dass 
a) [[#Auflösbarkeit von Gruppen der Ordnung $p {m}$|p-Gruppen]] (insbesondere [[#Beispiele|für $n$ prim]]) 
b) [[Sylow-Sätze#$ lvert G rvert= p {2}q$ mit $q neq p$ Primzahlen|$ \lvert G \rvert= p^{2}q$ mit $p \neq q$ Primzahlen]] 
c) [[Sylow-Sätze#$ lvert G rvert=pq$ mit $p neq q$ Primzahlen|$ \lvert G \rvert=pq$ mit $p \neq q$ Primzahlen]]
d) [[Sylow-Sätze#$ lvert G rvert=m cdot p {a}$ mit $m < p$.|$\lvert G \rvert=m \cdot p^{a}$ mit $m < p$ prim]]

auflösbar sind. Für einzelne $n$ müssen wir separat beweisen, dass $G$ auflösbar ist. Dazu werden wir uns jedes einzelne $n\in \set{1,...,60}$ anschauen, hier der Übersichtlichkeit halber in mehreren Spalten:


|       n        |    Bew.     |        n        |       Bew.        |        n        |       Bew.        |
| :------------: | :---------: | :-------------: | :---------------: | :-------------: | :---------------: |
|      $1$       | $G=\set{1}$ |  $21=7\cdot3$   |        c)         |      $41$       |        a)         |
|      $2$       |     a)      | $22=2\cdot 11$  |        c)         |  $42=6\cdot 7$  | [[#Lemma $n=42$]] |
|      $3$       |     a)      |      $23$       |        a)         |      $43$       |        a)         |
|    $4=2^2$     |     a)      |      $24$       | [[#Lemma $n=24$]] | $44=2^2\cdot11$ |        b)         |
|      $5$       |     a)      |    $25=5^2$     |        a)         | $45=3^2\cdot5$  |        b)         |
|  $6=2\cdot 3$  |     c)      |  $26=2\cdot13$  |        c)         | $46=2\cdot 23$  |        c)         |
|      $7$       |     a)      |    $27=3^3$     |        a)         |      $47$       |        a)         |
|    $8=2^3$     |     a)      | $28=7\cdot 2^2$ |        b)         |      $48$       | [[#Lemma $n=48$]] |
|    $9=3^3$     |     a)      |      $29$       |        a)         |    $49=7^2$     |        a)         |
| $10=5\cdot 2$  |     c)      |      $30$       | [[#Lemma $n=30$]] | $50=5^2\cdot2$  |        b)         |
|      $11$      |     a)      |      $31$       |        a)         | $51=3\cdot 17$  |        c)         |
| $12=2^2\cdot3$ |     b)      |    $32=2^5$     |        a)         | $52=2^2\cdot13$ |        b)         |
|      $13$      |     a)      |  $33=3\cdot11$  |        c)         |      $53$       |        a)         |
|  $14=7\cdot2$  |     c)      | $34=17\cdot 2$  |        c)         | $54=3^3\cdot2$  |        d)         |
|  $15=5\cdot3$  |     c)      |  $35=5\cdot 7$  |        c)         |  $55=5\cdot11$  |        c)         |
|    $16=2^4$    |     a)      |      $36$       | [[#Lemma $n=36$]] |      $56$       | [[#Lemma $n=56$]] |
|      $17$      |     a)      |      $37$       |        a)         |  $57=3\cdot19$  |        c)         |
| $18=3^2\cdot2$ |     b)      | $38=2\cdot 19$  |        c)         |  $58=2\cdot29$  |        c)         |
|      $19$      |     a)      | $39=3\cdot 13$  |        c)         |      $59$       |        a)         |
| $20=5\cdot2^2$ |     b)      |      $40$       | [[#Lemma $n=40$]] |        -        |         -         |
Für die einzelnen Beweise werden wir uns viel auf die [[Sylow-Sätze]] und insbesondere [[Sylow-Sätze#Weitere Eigenschaften von $n_{p}$|Eigenschaften von $n_p$]] beziehen. Außerdem werden wir hin und wieder den [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] verwenden, also $\lvert G/H\rvert=\frac{\lvert G\rvert}{\lvert H\rvert}$.
Zusätzlich werden wir verwenden, dass [[Normalteiler#Beispiele|der Kern von Homomorphismen]] ein [[Normalteiler]] ist und nach [[#Vererbung|oben]] $G$ auflösbar $\iff H \trianglelefteq G,G/H$ auflösbar.

###### Vorüberlegung / Funktionsdefinition
Betrachte außerdem für ein $p$ [[Primzahlen|Primzahl]] die Abbildung $$\varphi_p:G \rightarrow \text{Abb}(\text{Syl}_{p}(G),\text{Syl}_{p}(G)), g\mapsto c_{g}$$ wobei $c_{g}(U)=g^{-1}Ug$ die Bilder der [[Operation durch Konjugation]].
Wir bemerken zunächst, dass $$gUg^{-1}=gU'g^{-1}\implies U=g^{-1}gUg^{-1}g=g^{-1}gU'g^{-1}g=U'$$ $c_{g}$ injektiv ist. Da es eine endliche Menge auf sich selbst abbildet, ist es auch bijektiv und damit bildet $\varphi_{p}$ sogar in [[Symmetrische Gruppe|$S_{(\text{Syl}_{p}(G))}$]] ab, was [[Gruppenhomomorphismen|isomorph]] zu $S_{n_p}$ ist. Man rechnet leicht nach, dass $\varphi_{p}$ ein [[Gruppenhomomorphismen|Homomorphismus]] ist.
Wenn $n_p>1$, gilt weil alle $U_{1},U_{2}\in \text{Syl}_{p}(G)$ [[Sylow-Sätze|zueinander konjugiert]] sind, dass $\text{Bild}(\varphi_p)\supsetneq \set 1$ und damit auch $\ker(\varphi_{p})\neq G$.
###### Lemma: $n=24$ 
Es gilt $24=2^{3}\cdot 3$. 
*Fall*: $n_{2}=1$
Dann ist $U_{2}\trianglelefteq G$ und $\lvert G/U_{2}\rvert=\frac{24}{2^3}=3$. Also sind $G/U_{2}$, $U_{2}$ nach obiger Tabelle auflösbar und damit auch $G$.
*Fall* $n_{2}\neq 1$. Dann ist $n_{2}=3$, also $\lvert \text{Syl}_{2}(G)\rvert=3$. Es gilt für die [[#Vorüberlegung / Funktionsdefinition]] dass $\ker\varphi_{3}\neq G$. Außerdem ist $\varphi_{3}$ nicht injektiv, da $24 = \lvert G\rvert>\lvert S_{2}\rvert=2$. Also ist $\ker \varphi_{3}\neq \set{e}$. Wir wissen außerdem, dass $\ker \varphi_{3}\trianglelefteq G$. Da $\lvert \ker \varphi_{3}\rvert, \lvert G/\ker\varphi_3\rvert<24$ wissen wir nach der Tabelle oben schon, dass $\ker \varphi_{3}, G/\ker\varphi_{3}$ auflösbar sind und damit $G$ auch.

###### Lemma $n=30$
Es gilt $30=2\cdot3\cdot5$.
Dann ist $n_{3}\in\set{1,2,5,10}$.  Wenn $n_{3}=1$ gehen wir wie bei [[#Lemma $n=24$]] vor und $G$ ist auflösbar.
Wenn $n_{3}\neq 1$ ist $2,5 \not\equiv 1 \mod 3$, also muss $n_{3}=10$ sein. Da der [[Sylow-Sätze#Schnitt von p-Sylow Untergruppen|Schnitt von p-Sylow Untergruppen trivial]] also $\set{e}$ ist, gilt $\lvert \dot\bigcup_{H\in \text{Syl}_{3}(G)}(H\setminus \set e)\rvert=(3-1)\cdot 10 =20$.

Da alle $U\in \text{Syl}_{3}(G)$ genau $3$ Elemente haben, ist jedes $U$ [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] und wird von jedem Element außer $e$ [[Gruppen#Erzeugnis|erzeugt]]. D.h. $\forall x\in U\setminus\set{e}: \text{ord}(x)=3$ und wir wissen es gibt mindestens 20 Elemente der [[Gruppen#Ordnung|Ordnung]] 3.

Nun gilt $n_{5}\in \set{1,2,3,6}$. Da $2,3\not\equiv 1 \mod 5$ ist $n_{5}\in \set{1,6}$.
**Annahme**: $n_{5}=6$ 
Wir sehen wie oben $\lvert \dot\bigcup_{H\in \text{Syl}_{5}(G)}(H\setminus \set e)\rvert=(5-1)\cdot 6 =24$. Also gibt es mindestens 24 Elemente der Ordnung 5. Da aber $20+25 > 30$ haben wir einen **Widerspruch**.
Also ist $n_{5}=1$ und wie in [[#Lemma $n=24$]] gilt $G$ auflösbar.

###### Lemma $n=36$
Es gilt $36=2^{2}\cdot3^{2}$. Also ist $n_{3}\in \set{1,2,4}$. Da $2\not\equiv 1 \mod 3$ ist $n_{3}\in \set{1,4}$. 
Für $n_{3}=1$ ist $G$ wie vorher auflösbar.
Sei $n_{3}=4$. Dann ist $\varphi_{3}$ nicht injektiv, denn $\lvert G\rvert=36>24=\lvert S_{4}\rvert$, also ist $\ker \varphi_{3}\neq \set{e}, G$ wie in [[#Lemma $n=24$]] ist $G$ auflösbar. 
###### Lemma $n=40$
Es gilt $40=5\cdot2^{3}$, also ist $n_{5}\in \set{1,2,4,8}$ und $2,4,8 \not\equiv 1 \mod 5$.  D.h. $n_{5}=1$ und wie oben sehen wir $G$ ist auflösbar.
###### Lemma $n = 42$
Nach [[Sylow-Sätze#$ lvert G rvert=m cdot p {a}$ mit $m < p$.|diesem Lemma]] gilt, dass $n_{7} = 1$. Damit ist $U_{7}$ Normalteiler und auflösbar und $G/U_7$ eine Gruppe der Ordnung 6 und damit auflösbar. Mit der [[#Vererbung]] folgt, dass $G$ auflösbar ist.
###### Lemma $n=48$
Es gilt $48=2^{4}\cdot 3$. Also ist $n_{2}\in \set{1,3}$. Für $n_{2}=1$ sind wie vorher fertig. Für $n_{2}=3$ gilt $\set{e}\neq \ker \varphi_{2}\neq G$, denn $\lvert G\rvert=48 > 6 =\lvert S_{3}\rvert$ und damit wie in [[#Lemma $n=24$]] $G$ auflösbar. 
###### Lemma $n=56$
Es gilt $56=7\cdot 2^{3}$. Also ist $n_{7}\in \set{1,2,4,8}$, aber da $2,4\not\equiv 1 \mod 7$ ist $n_{7}\in\set{1,8}$. Für $n_{7}=1$ sind wir wie oben fertig.
Sei also $n_{7}=8$. Dann gilt wie in [[#Lemma $n=30$]], dass es $8\cdot (7-1)$ Elemente der Ordnung 7 gibt. Die restlichen $2^{3}=8$ Elemente müssen also die einzige 2-Sylowuntergruppe bilden, also gilt $n_{2}=1$ und wie vorher sind wir fertig.
