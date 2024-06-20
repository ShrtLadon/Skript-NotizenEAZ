Sei $G$ eine [[Gruppen|Gruppe]] und $H \trianglelefteq G$ ein [[Normalteiler]]. Dann ist [[Gruppenwirkung#Rechts und Linksnebenklassen|$G/H$]] eine Gruppe mit der Verknüpfung$$\cdot:G/H \times G/H\rightarrow G/H, (g_{1}H)\cdot(g_{2}H):=g_1g_2H$$
##### Beweis
Der Beweis dafür, dass diese Abbildung wohldefiniert ist, liefert [[Normalteiler#Motivation|die Motivation für Normalteiler]] z.Z. ist also dass $(G/H,\cdot)$ eine [[Gruppen|Gruppe]].

- $(aH)\cdot((bH)\cdot(cH)) = aH\cdot(bcH)\overset{\text{G assoziativ}}=((ab)cH)=(aH \cdot bH)\cdot cH$ 
- Es gilt $eH \cdot aH=eaH=aH$ 
- $(gH)\cdot(g^{-1}H)=eH$


# Isomorphiesatz
Sei $\Phi:G \rightarrow H$ ein [[Gruppenhomomorphismen|Gruppenhomomorphismus]], dann ist $$\tilde \Phi:G/\ker \Phi \rightarrow \text{Bild}(\Phi), g\ker \Phi\mapsto \Phi(g)$$ein wohldefinierter [[Gruppenhomomorphismen|Isomorphismus]].