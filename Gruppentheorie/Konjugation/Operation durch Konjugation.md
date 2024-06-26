Sei $G$ eine [[Gruppen|Gruppe]], dann [[Gruppenwirkung|operiert]] $G$ mit $$c_{g}(h):=g*h:=ghg^{-1}$$auf sich selbst von links. Diese Operation heißt auch **Konjugationsoperation**. Man kann leicht nachrechnen, dass das ein [[Gruppenhomomorphismen|Gruppenhomomorphismus]] ist.

###### Beweis der Operationseigenschaft
- (A1) $g*(g'*h)=g*(g'hg'^{-1})=gg'hg'^{-1}g^{-1}\overset{(gg')^{-1}=g'^{-1}g^{-1}}=(gg')*h$ 
- (A2) $e*h=ehe^{-1}=h$ 

## Konjugationsklassen, Zentralisator und Kern
- Die [[Gruppenwirkung#Bahn und Stabilisator|Bahnen]] der Konjugationsoperation$$\text{ccl}(h)=G\cdot h=\set{ghg^{-1}|g\in G}, \quad h \in G$$ heißen **Konjugationsklassen**.
- Der **Zentralisator** von $h \in G$ ist $$Z_G(h)=G_{h}=\set{g\in G:ghg^{-1}=h}=\set{gh=hg}$$der [[Gruppenwirkung#Bahn und Stabilisator|Stabilsator]] der Konjugationsoperation.
- Den [[Gruppenwirkung#Bahn und Stabilisator|Kern]] dieser Operation nennt man **Zentrum**$$Z(G):=\ker=\bigcap_{h\in G}Z_G(h)=\set{g\in G\mid\forall x \in G :gx=xg }$$was genau die mit ganz $G$ kommutativen Elemente sind. Es gilt $e \in Z(G)$ 

### Eigenschaften
- Sei $p$ eine [[Primzahlen|Primzahl]] und $G$ eine [[Gruppen|Gruppe]] mit $\lvert G\rvert =p^{m}$ für ein $m \geq 1$. Dann ist $Z(G)\supsetneq \set e$ und sogar ein Vielfaches von $p$ groß.

###### Beweis
Dann gilt wegen der [[#Klassengleichung]], dass $p^{m}=\lvert Z(G)\rvert +\sum\limits_{x\in X, \lvert G:Z_G(x)\rvert \neq 1}\lvert G:Z_G(x)\rvert$, aber außerdem $\forall x \in G\setminus Z(G)$, dass wegen dem [[Gruppenwirkung#Satz von Lagrange|Satz von Lagrange]] $$p^{m}=\lvert Z_G(x)\rvert \cdot \lvert G:Z_G(x)\rvert$$und da $\lvert G:Z_G(x)\rvert \neq 1$, dass $Z_{G}(x)\neq G$. Daraus folgt $\lvert G:Z_G(x)\rvert =p^{t_{x}}$ mit $t_{x} \geq 1$.

Dadurch erhalten wir, dass [[kommutative Ringe#Teilbarkeit|$p \mid \lvert Z(G)\rvert$]]. Da $e \in Z(G)$ ist, ist $\lvert Z(G)\rvert \neq 0$ also mindestens $p$. Daraus folgt die Behauptung. 
#### Klassengleichung
Sei $G$ eine endliche [[Gruppen|Gruppe]] und $X$ ein Repräsentantensystem der Konjugationsklassen (also eine Auswahl von je einem Element aus jeder Konjugationsklasse). Dann gilt $$\lvert G\rvert =\sum\limits_{x\in X}\frac{\lvert G\rvert}{\lvert Z_G(x)\rvert}=\lvert Z(G)\rvert +\sum\limits_{x\in X, \lvert G:Z_G(x)\rvert \neq 1}\lvert G:Z_G(x)\rvert$$
###### Beweis
Es gilt die Konjugationsklassen [[Gruppenwirkung#Bahn und Stabilisator#Eigenschaften|partitionieren]] $G$. D.h $$\lvert G\rvert =\sum\limits_{x\in X}\lvert \text{ccl}_{G}(x)\rvert$$Wegen der [[Gruppenwirkung#Bahnenformel|Bahnenformel]] gilt $\lvert G\rvert=\lvert ccl_{G}(h)\rvert \cdot \lvert Z_G(h)\rvert$. Daraus folgt die Behauptung 1 (da mindestens $e \in Z_G(h)$). Da wegen dem [[Gruppenwirkung#Orbit-Stabilisator-Theorem|Orbit-Stabilisator-Theorem]] $\lvert \text{ccl}_{G}(x)\rvert = \lvert G:Z_G(x)\rvert$ dem [[Gruppenwirkung#Index|Index]] ist $\lvert G\rvert =\sum\limits_{x\in X, \lvert \text{ccl}_G(x)\rvert = 1}\lvert \text{ccl}_{G}(x)\rvert+\sum\limits_{x\in X, \lvert G:Z_G(x)\rvert \neq 1}\lvert G:Z_G(x)\rvert$.

Es gilt immer $x \in \text{ccl}_G(x)$. Also ist $\#\text{ccl}_G(x)=1$ genau dann wenn $\forall g \in G: gxg^{-1}=x$ also $gx=xg$ also $x\in Z(G)$. Daraus folgt die Behauptung. 

## Konjugation zueinander

### "Grundeigenschaft"
Sei $H\leq G$ eine [[Gruppen#Untergruppen|Untergruppe]] und $g \in G$. Dann ist $$gHg^{-1}:=\set{ghg^{-1}|h\in H}$$eine Untergruppe von $G$. 
###### Beweis
Es gilt $geg^{-1}=e \in gHg^{-1}$ also $gHg^{-1}\neq \varnothing$.
Seien $gh_{1}g^{-1}, gh_{2}g^{-1}\in gHg^{-1}$. Dann gilt $$(gh_{1}g^{-1})(gh_{2}g^{-1})^{-1}=gh_{1}g^{-1}gh_{2}^{-1}g^{-1}=gh_{1}h_{2}^{-1}g^{-1}\in gHg^-1$$wobei genutzt wird, dass $h_{1}h_{2}^{-1}\in H$ weil $H$ eine Untergruppe ist. Wegen dem [[Gruppen#Untergruppenkriterium|Untergruppenkriterium]] ist $gHg^{-1}$ also eine Gruppe.

### Definition
Seien $U,V \leq G$ zwei [[Gruppen#Untergruppen|Untergruppen]]. Wir nennen $U,V$ **konjugiert zueinander**, falls$$\exists g\in G:U=gVg^{-1}$$Insbesondere ist das eine Äquivalenzrelation.

#### Isomorphieeigenschaft
Seien $U,V$ zueinander konjugiert. Dann gilt [[Gruppenhomomorphismen|$U \cong V$]] 
###### Beweis
Dann existiert ein $g \in G$, sodass $U=gVg^ {-1}$ . Betrachte $\Phi :V \rightarrow U,h\mapsto ghg^ {-1}$. Wir zeigen, dass $\varphi$ ein [[Gruppenhomomorphismen|Isomorphismus]] ist:

Seien $x,y \in V$ dann gilt $\Phi(x\cdot y)=gxyg^{-1}=gx(g^{-1}g)yg=\Phi(x)\Phi(y)$ also ist $\Phi$ ein [[Gruppenhomomorphismen|Homomorphismus]].
*injektiv*: Sei $\Phi(x)=e$ Dann gilt $gxg^{-1}=e$. Aber dann ist $g^{-1}=xg^{-1}$. Dann muss aber $x=e$ sein. Also ist $\ker \Phi = \set{e}$ und damit $\Phi$ [[Gruppenhomomorphismen#Eigenschaften|injektiv]]. 
*surjektiv*: Das ist per Voraussetzung, dass $U=gVg^{-1}$ ist, gegeben. 