1. $D$ $y$-semplice $D = \{x \subseteq [a,b], g_{1}(x) \leq y \leq g_{2}(x)\}$, $f : D \to \mathbb{R}$ continua in $D$

$$ \int\! \int_{D} \!  f(x,y)\, \mathrm{d}x  \! \, \mathrm{d}y = \int_{a}^b \! \left( \int_{g_{1}(x)}^{g_{2}(x)} f(x,y)\! \, \mathrm{d}y  \right) \, \mathrm{d}x   $$
Integriamo prima in $\mathrm{d}y$ perchè D è $y$-semplice, se fosse $x$-semplice

2. $D$ $x$-semplice $D = \{y \subseteq [c,d], h_{1}(y) \leq x \leq h_{2}(y)\}$
$$ \int\!\int_{D} \! f(x,y) \, \mathrm{d}x  \! \, \mathrm{d}y =  \int_{c}^d \left( \int_{h_{1}(y)}^{h_{2}(y)} \! f(x,y)\, \mathrm{d}x  \right)\! \, \mathrm{d}y $$

>[!esempio]
>$T$ triangolo di vertici $(0,0), (1,0), (1,1)$ 
>$$ T = \{x \in [0,1], 0 \leq y \leq x\} $$


>[!oss]
>Le formule di riduzione trasformano un integrale doppio in due variabile a due integrali di una variabile l'uno dentro l'altro