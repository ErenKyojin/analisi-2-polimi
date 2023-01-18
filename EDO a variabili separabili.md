# EDO a variabili separabili

>[!def]
>Una EDO del $1°$ ordine si dice a variabili separabili se
>$$y'(t) = h(t) = g(y(t))$$
>Con $h : J \subseteq \mathbb{R} \to \mathbb{R}, g : J \subseteq \mathbb{R} \to \mathbb{R}$
>Cioè $f(t,y) = h(t) \cdot g(y)$
>
>Inoltre possiamo vedere come il dominio delle due funzioni, se ristretto, delimiti un area limitata, ad esempio:
>```tikz
>\begin{document}
>\begin{tikzpicture}
>\draw[->] (-0.1,0) -- (6,0) node[above] {$x$};
>\draw[->] (0,-0.1) -- (0,5) node[right] {$y$};
>\draw[dashed] (0,3) -- (5,3);
>\draw[dashed] (0,1) -- (5,1);
>\draw[dashed] (2,0) -- (2,3) node[pos = 0.1, left] {$J_{1}$} node[above left] {$J_{2}$};
>\draw[dashed] (5,0) -- (5,3);
>\end{tikzpicture}
>\end{document}
>```


>[!esempio]
>$$y'(t) = \frac{1}{t}\qquad h(t) = \frac{1}{t} \qquad g(y) = 1$$ 
>$f$ è definita
>$(\mathbb{R} \setminus \{0\}) \times \mathbb{R}$

## [[Soluzioni]] costanti costanti della EDo a variabili separabili
$$y'(t) = h(t)g(y(t))$$
Ha come soluzioni costanti $y(t) = C\qquad \forall t : f(t,c) = 0 \forall t \in J_{1}$

$\Rightarrow h(t)g(c) = 0 \forall t\Rightarrow g(C) = 0$