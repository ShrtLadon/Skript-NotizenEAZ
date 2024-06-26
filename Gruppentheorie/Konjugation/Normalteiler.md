Ein **Normalteiler** ist eine [[Gruppen#Untergruppen|Untergruppe]] $N \leq G$ einer, die *nur* zu sich selbst [[Operation durch Konjugation|konjugiert]] ist, d.h. $$\forall g\in G:gNg^{-1}=N$$Wir schreiben dann $N\trianglelefteq G$.

## Äquivalente Formulierungen
- $\forall g \in G\forall n \in N:gng^{-1}\in N$
- $N \trianglelefteq G \iff \forall g\in G:$ [[Gruppenwirkung#Rechts und Linksnebenklassen|$gH=Hg$]] 

###### Beweis
- Es genügt zu zeigen, dass daraus folgt $gNg^{-1}=N$ bzw. dass die Funktion $n\mapsto gng^{-1}$ surjektiv nach $N$ abbildet. Sei dazu $x\in N$. Dann gilt $g(g^{-1}xg)g^{-1}=x$ und $g^{-1}xg=g^{-1}x(g^{-1})^{-1}\in N$. Also ist $gNg^{-1}=N$.
- ÜB7.3

## Eigenschaften
- [[Gruppen#Untergruppen|$H \leq G$]] und [[Gruppenwirkung#Index|Index]] von 2 impliziert $H \trianglelefteq G$.

###### Beweis
- ÜB7.3.2

## Motivation
Die Motivation für die Definition von Normalteilern sind [[Faktorgruppen]]. Denn für $H \leq G$ eine [[Gruppen#Untergruppen|Untergruppe]] gilt [[Gruppenwirkung#Rechts und Linksnebenklassen|$G/H$]] ist eine Menge, die wir gerne mit einer (einfachen) Verknüpfung zu einer Gruppe machen würden. Der naheliegenste Versuch wäre es die Verknüpfung als $$(g_{1}H)\cdot(g_{2}H):=g_{1}g_{2}H$$zu definieren und zu untersuchen, wann diese wohldefiniert ist:
Seien also $g_1 H=g_1'H$ und $g_{2}H=g'_{2}H$. Dann existieren $h_{1},h_{2}$ mit $g_1'=g_1h_1$ und $g_2'=g_2'h_2$ also wenn man das in die Verknüpfung einsetzt $$g_1'g_2'H=g_1h_1g_2h_2H\overset{h_1H=H}=g_1h_{1}g_2H=g_1g_2g_{2}^{-1}h_1g_2$$Das ist also genau dann gleich $g_{1}g_{2}H$, wenn $g_{2}^{-1}h_{1}g_{2}\in H$ bzw. wohldefiniert, wenn das für alle $g\in G$ und $h\in H$ gilt, also genau $H \trianglelefteq G$ gilt.
# Beispiele
- $\set e, G \trianglelefteq G$ 
- Für einen [[Gruppenhomomorphismen|Homomorphismus]] $\Phi:H \rightarrow G$ gilt $\ker \Phi \trianglelefteq G$
	-> $\Phi(hxh^{-1})=\Phi(h)\Phi(x)\Phi(x)^{-1}\overset{x\in \ker \Phi}=\Phi(h)e \Phi(h)^{-1}=e$ also $hxh^{-1}\in \ker \Phi$
	
##### Diedergruppe
Betrachte die [[Gruppen#Diedergruppe|Diedergruppe]] $D_{2n}$. Dann gilt das [[Gruppen#Erzeugnis|Erzeugnis]] $\langle r\rangle=\set{Id,r,...,r^{n-1}}$ ist ein Normalteiler von $D_{2n}$, aber $\langle s \rangle = \set{Id, s}$ ist kein Normalteiler.
Beweis auf ÜB 7.

