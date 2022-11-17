>[!def]
>$A \subseteq \mathbb{R}^2$ aperto, $f : A \to \mathbb{R}$ derivabile
>Se le derivate parziali
>$$ \frac{ \partial f }{ \partial x } (x,y)\qquad\frac{ \partial f }{ \partial y } (x,y) $$
>sono a loro volta derivabili in $A$ definiamo le derivate seconde:
> $$ \begin{align}
> &\frac{ \partial^2 f  }{ \partial x^2 } = \frac{ \partial  }{ \partial x }\left( \frac{ \partial f }{ \partial x } (x,y) \right)\quad&\frac{ \partial^2 y }{ \partial x \partial y  } (x,y)  \frac{ \partial  }{ \partial y }\left( \frac{ \partial f }{ \partial x }  \right) (x,y) \\
>&\frac{ \partial^2 f}{ \partial x \partial y } = \frac{ \partial  }{ \partial x } \left( \frac{ \partial f }{ \partial y } (x,y) \right)\ &\frac{ \partial^2 f }{ \partial y^2 }(x,y) = \frac{ \partial  }{ \partial y }\left( \frac{ \partial f }{ \partial y } (x,y) \right)       
>\end{align} $$


Possiamo arrangiare le derivate parziali nella [[matrice hessiana]]




>[!def]
>Se $f$ è derviabile due volte in $A$ e tutte le derivate parziali seconde sono continue in $A$ diciamo che $f$ è di [[classe C]]$^2$ in $A : f \in C^2(a)$

>[!oss]
>In teoria se $f$ è definita per casi o se compare $t^\alpha$ con $\alpha \in (0,2)$ bisognerebbe verificare a mano la classe di appartenenza di $f$


>[!teorema di schwarz]
>$A \subseteq \mathbb{R}^2$ aperto, $f \in C^2(A)$ allora
> $$ \frac{ \partial^2 f }{ \partial x\partial y } (x,y) = \frac{ \partial^2 f }{ \partial y\partial x }(x,y)\quad \forall (x,y) \in A   $$
> Cioè $A\dots ?$

