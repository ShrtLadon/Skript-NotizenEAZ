Eine [[Gruppen|Gruppe]] $G$ heißt **auflösbar**, wenn es [[Gruppen#Untergruppen|Untergruppen]] $G_{1},...,G_{m}$ in $G$ gibt, sodass
- $G_{1}=\set{1}$
- $G_{m}=G$
- Für $1\leq i \leq n-1$ gilt [[Normalteiler|$G_{i}\trianglelefteq G_{i+1}$]] 
- Für $1 \leq i \leq n-1$ ist die [[Faktorgruppen|Faktorgruppe]] $G_{i+1}/G_i$ [[Gruppen|abelsch]]. 

## Eigenschaften
### Vererbung
1) Ist $G$ auflösbar und [[Gruppen#Untergruppen|$H \leq G$]], dann ist auch $H$ auflösbar.
2) Ist $G$ auflösbar und [[Normalteiler|$H \trianglelefteq G$]], so ist [[Faktorgruppen|$G/H$]] auflösbar.
3) Sei $H \trianglelefteq G$. Wenn $H$ und $G/H$ auflösbar, dann ist auch $G$ auflösbar.
##### Beweis
###### 1)
Seien $\set 1=G_{1} \trianglelefteq G_{2} \trianglelefteq ... \trianglelefteq G_{m}=G$ die Untergruppen der Auflösung von $G$. 
Setze $H_{i}:= H \cap G_{i}$ für $1 \leq i \leq m$. Dann gilt $H_{1}=\set 1$ und $H_{m}=H$. Außerdem ist der Schnitt von Untergruppen wieder eine Untergruppe (ÜB6.4) also gilt $$H_{1}\leq...\leq H_m$$*Normalteiler*: Sei $x \in H_{i+1}$ dann ist $xH_{i}x^{-1}=x(H_{i}\cap G)x^{-1}=xH_{i}x^{-1}\cap x H x^{-1}\overset{H_{i} \trianglelefteq H_{i+1}, H\leq G}=H_{i}\cap H=H_{i}$ also ist $H_{i} \trianglelefteq H_{i+1}$.

*abelsch*: Betrachte die [[Gruppenhomomorphismen]] $i:H_{i+1} \rightarrow G_{i+1},x\mapsto x$ und $p:G_{i+1} \rightarrow G_{i+1}/G_{i}, x \mapsto xG_{i}$. Dann ist auch die Komposition $p \circ i$ ein Homomorphismus, damit ist nach [[Faktorgruppen#Isomorphiesatz|Isomorphiesatz]] $H_{i+1}/\ker(p\circ i)\cong \text{Bild}(p\circ i)\leq G_{i+1}/G_{i}$. Da $\ker(p\circ i)=H_{i+1}\cap G_{i}=G_{i+1}\cap H \cap G_{i}\overset{G_{i}\subseteq G_{i+1}}=G_{i}\cap H=H_{i}$. Also ist $H_{i+1}/H_{i}$ isomorph zu einer Untergruppe einer abelschen Gruppe, also abelsch.
###### 2)
Seien $\set 1=G_{1} \trianglelefteq G_{2} \trianglelefteq ... \trianglelefteq G_{m}=G$ die Untergruppen der Auflösung von $G$.
Betrachte $p:G \rightarrow G/H, x \mapsto xH$ und setze $$N_{i}:=p(G_{i})\subset G/H$$Offensichtlich gilt $\set{e_{G/H}}=N_{1}\subset ... \subset N_{m}=G/H$ und als Bild eines [[Gruppenhomomorphismen#Eigenschaften|Gruppenhomomorphismus]] ist jedes $N_{i}$ eine Untergruppe von $G/H$ also wie man sich schnell an der Definition überlegt $N_{i}$ eine Untergruppe von $N_{i+1}$. 
*Normalteiler*: Sei $xG \in N_{i+1}$, also $x \in G_{i+1}$. Dann ist $$xG\cdot N_i\cdot(xG)^{-1}=\set{xnx^{-1}G\mid n \in G_i}\overset{G_{i} \trianglelefteq G_{i+1}\ni x}=p(G_{i})=N_{i}$$
*abelsch*: TODO mit isomorphiesatz, wenn der drankommt.

###### 3)
Seien $\set 1=H_{1} \trianglelefteq H_{2} \trianglelefteq ... \trianglelefteq H_{m}=H$ die Untergruppen der Auflösung von $H$ und seien $\set 1=N_{1} \trianglelefteq N_{2} \trianglelefteq ... \trianglelefteq N_{m}=G/H$ die Untergruppen der Auflösung von $G/H$. Dann setze $$G_i:=\begin{cases}H_{i} & i\leq m \\p^{-1}(N_{i-m}) & i>m\end{cases}$$wobei $p$ die Abbildung aus [[#2)]] ist.

TODO möglich mit isomorphiesatz, hatten wir aber noch nicht.

## Auflösbarkeit endlicher Gruppen
Sei $G$ eine endliche [[Gruppen|Gruppe]]. Dann ist $G$ auflösbar genau dann wenn es Untergruppen gibt $$\set 1 =G_{1} \trianglelefteq G_{2} \trianglelefteq ... \trianglelefteq G_{m}=G$$so dass $G_{i}/G_{i-1}$ [[Gruppen#Zyklische Gruppen|zyklisch]] sind und $\lvert G_{i}/G_{i-1}\rvert$ [[Primzahlen|prim]]
#### Beweis
##### "$\Rightarrow$"
Führe (starke) Induktion nach $\lvert G\rvert$.
*IA*: $\lvert G\rvert =1$. Dann setze $G_{1}=G_{m}=G$. Dann gilt jede Aussage für alle $G_{i}/G_{i-1}$ für $1\leq i \leq 1-1=0$, da kein solches $i$ existiert.

*IS*: 
Nach Annahme ist $G$ auflösbar also gibt es $$\set 1 =G_{1} \trianglelefteq G_{2} \trianglelefteq ... \trianglelefteq G_{m}=G$$die $G$ auflösen.
Insbesondere kann man o.B.d.A fordern, dass $G_{m-1}\subsetneq G_m$ ist (sonst streiche die gleichen Elemente). D.h. es gilt $\lvert G_{m-1}\rvert < \lvert G_m\rvert$ und mit Induktionsvoraussetzung gibt es$$\set 1 =H_{1} \trianglelefteq H_{2} \trianglelefteq ... \trianglelefteq H_{k}=G_{m-1}$$die $G_{m-1}$ auflösen und für die $\lvert H_{i}/H_{i-1}\rvert$ prim ist. 
Außerdem ist wenn $G_{m-1}\subsetneq G_m$ auch $\lvert G_{m}/G_{m-1}\rvert < \lvert G\rvert$ wegen dem [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]]. Also gibt es nach Induktionsvoraussetzung$$\set {1_{G_{m}/G_{m-1}}} =N_{1} \trianglelefteq N_{2} \trianglelefteq ... \trianglelefteq N_{l}=G_{m}/G_{m-1}$$die $G_{m}/G_{m-1}$ auflösen und für die $\lvert N_{i}/N_{i-1}\rvert$ prim ist. 
Definiere für $2 \leq j \leq l$ $$H_{k+j}:=p^{-1}(N_{j})=\dot\bigcup_{x\in N_{j}}x$$wobei $p:G_{m} \rightarrow G_{m}/G_{m-1},x\mapsto xG_{m-1}$ ist. Die rechte Seite überlegt man sich schnell weil die $x$ genau die Mengen sind die von $p$ auf die selbe Menge geworfen werden. 
Anmerkung: Die 2 ist korrekt, weil $H_{k}=G_{m-1}=p^{-1}(\set 1)=p^{-1}(N_{1})$.
###### Beweis der geforderten Eigenschaften von $H_{n}$
Anmerkung wir müssen nirgendwo $H_{k}$ und $H_{k+1}$ gesondert betrachten, weil $H_{k}=p^{-1}(N_{1})$

Es gilt $H_{k} =G_{m-1}\subseteq H_{k+1}\subseteq...\subseteq H_{k+l}$ und für $a,b \in H_{k+j}$, dass $aG_{m-1}\cdot b^{-1}G_{m-1}\in N_{j}$, denn $N_{j} \leq G_m/G_{m-1}$. Dann ist aber auch $a\cdot b^{-1}\in H_{k+j}$. Außerdem ist $N_{j}\neq \varnothing$ und also da $p$ surjektiv $H_{k+j}\neq \varnothing$ also $H_{k+j}$ nach [[Gruppen#Untergruppenkriterium|Untergruppenkriterium]] eine Untergruppe. 

Sei $x \in H_{k+j+1}$. Dann gilt $xH_{k+j}x^{-1}=\bigcup_{n\in N_j}(xG_{m-1}n x^{-1}G_{m-1})$ wobei aber die vereinigten Mengen jeweils in $N_{j}$ liegen, da $N_{j} \trianglelefteq N_{j+1}$.

TODO: Mit Isomorphiesatz ist $H_{k+j+1}/H_{k+j}\cong H_{k+j+1}/G_{m-1}/H_{k+j}/G_{m-1}=N_{k+j+1}/N_{k+j}$ den hatten wir aber noch(?) nicht. Alternativ kann man sich die Kardinalitäten "manuell" mit Satz von Lagrange überlegen und dann benutzen dass Gruppen primer Ordnung zyklisch sind.
##### "$\Leftarrow$" 
Dann gilt $G_{i+1}/G_{i}$ ist [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] also insbesondere nach ÜB6.2.3 isomorph zu $\mathbb{Z}_n$ also abelsch und damit ist $G$ auflösbar. 

### Auflösbarkeit von Gruppen der Ordnung $p^{m}$
Sei $p$ eine [[Primzahlen|Primzahl]] und $G$ eine [[Gruppen|Gruppe]] mit $\lvert G\rvert=p^{m}$. Dann ist $G$ auflösbar und es gibt eine Kette $$\set 1=G_{1} \triangleleft G_{2}\triangleleft ...\triangleleft G_{m+1}=G$$sodass $G_{i}/G_{i-1}$ zyklisch von Ordnung $p$ ist.
##### Beweis
Führe Induktion nach $m=\log_p(\lvert G\rvert)$ 
*IA* $m=1$. Dann ist $G$ [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] also folgt direkt die Behauptung.

*IS* Für $m > 1$ gilt [[Operation durch Konjugation#Konjugationsklassen, Zentralisator und Kern|$Z(G)$]] ist als Kern eines [[Gruppenhomomorphismen|Homomorphismus]] ein [[Normalteiler]] von $G$. Wenn $Z(G)=G$ (bzw. $G$ abelsch), dann sind wir fertig mit $G_{2}=G$ und $G_{1}={1}$.
Wenn $Z(G) \subsetneq G$, dann ist $\lvert G/Z(G)\rvert= p^{k}$ nach [[Operation durch Konjugation#Konjugationsklassen, Zentralisator und Kern#Beweis|Beweis dieses Lemmas]]. 

Dann ist aber nach Induktionsvoraussetzung $G/Z(G)$ auflösbar mit der passenden "Auflösung". Da $Z(G)$ und $G/Z(G)$ auflösbar sind, ist auch $G$ auflösbar mit einer Kette$$\set 1=G_{1} \triangleleft G_{2}\triangleleft ...\triangleleft G_{m+1}=G$$die nach [[#Auflösbarkeit endlicher Gruppen]] alle zyklisch sind und $G_{i+1}/G_{i}$ prim viele Elemente haben. Außerdem gilt wegen [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] $\lvert G_{1}/G_{2}\rvert, \lvert G_{2}/G_{3}\rvert,... \lvert G_{m}/G_{m+1}\rvert\mid \lvert G\rvert$ also sind $\lvert G_{i+1}/G_{i} \rvert =p$. 
# Beispiele
- jede abelsche Gruppe ist auflösbar mit $G_{1}=\set{1}$ und $G_{2}=G$. 
- Wenn $\lvert G\rvert$ [[kommutative Ringe#Prim- und irreduzible Elemente|prim]], so ist $G$ [[Gruppen#Zyklische Gruppen#Eigenschaften|zyklisch]] also nach ÜB6.3.3 [[Gruppenhomomorphismen|isomorph]] zur abelschen Gruppe $\mathbb{Z}_{p}$ also auflösbar

### Diedergruppe
Die [[Gruppen#Diedergruppe|Diedergruppe]] $D_{2n}$ ist auflösbar, auch wenn z.B. $D_{6}\cong S_{3}$ zur [[Gruppen#symmetrische Gruppe|symmetrischen Gruppe]] nicht abelsch ist.
###### Beweis
Betrachte $G_{2}=\langle r\rangle$ die Menge der Drehungen. Das ist ein [[Normalteiler#Diedergruppe|Normalteiler von $D_{2n}$]]. Setze noch $G_{1}=\set{1}$ und $G_{3}=G$. Dann ist $G_{2}/G_{1}=G_{2}$ als zyklische Gruppe [[Gruppenhomomorphismen|isomorph]] nach ÜB6.3.3 zur abelschen Gruppe $\mathbb{Z}_{n}$ also abelsch. Auf ÜB7.1 wurde nachgerechnet, dass $\#G_{3}/G_{2}=2$. Die Gruppe mit 2 Elementen ist aber eindeutig (Verknüpfung mit 0 fest und das andere Element muss selbst-invers sein) als $\mathbb{Z}_2$ also abelsch.

