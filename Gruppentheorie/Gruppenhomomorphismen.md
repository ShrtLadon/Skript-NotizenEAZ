Seien $(G,*_{G}), (H,*_H)$ [[Gruppen]]. Eine Abbildung $\phi:H \rightarrow G$ heißt **Gruppenhomomorphismus**, wenn gilt $$\forall a,b\in H: \phi (a*_{H}b)=\phi(a)*_{G}\phi(b)$$Wenn $\phi$ bijektiv ist, nennen wir $\phi$ auch **Isomorphismus**, $G,H$ **isomorph** und schreiben $G \cong H$.

### Eigenschaften
Sei $\phi:H \rightarrow G$ ein Homomorphismus. Dann gilt:
- $\phi(e_{H})=e_{G}$
- $\forall a \in H : \phi(a^{-1})= \phi(a)^{-1}$
- $\text{Bild}(\phi) \leq G$ ist [[Gruppen#Untergruppen|Untergruppe]]
- $\ker \phi = \set{x \in H : \phi(x)=e_{G}}\leq H$ ist Untergruppe
- $\ker \phi = \set{e_{H}}\iff \phi$ injektiv. (Anmerkung das haben wir nicht in der VL gehabt, aber wurde in einem Beweis verwendet.)

### Beispiele
- $\phi:H \rightarrow G, x \mapsto e_G$ ist immer ein Homomorphismus.
- Für [[Gruppen#Untergruppen|$H \leq G$]] ist die Inklusion $i:H \rightarrow G, x\mapsto x$ immer ein Homomorphismus
- $\exp:(\mathbb{R}, +) \rightarrow (\mathbb{R}_{>0},\cdot), x\mapsto e^{x}$ ist ein Isomorphismus. 