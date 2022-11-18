>[!def]
>Sia $A \subseteq \mathbb{R}^2$ aperto
>$f : A \to \mathbb{R}$ derivabile in $(X_{0},y_{0}) \in A$
>Se $\nabla f (x_{0},y_{0}) = \begin{bmatrix}0 & 0\end{bmatrix}^T$ allora $(x_{0},y_{0})$ è detto punto critico o punto stazionario

>[!def]
>Un punto critico di $f$ che non è punto estremale di $f$ è detto punto di sella


```tikz
\usepackage{pgfplots}
\begin{document}
\begin{tikzpicture}
\begin{axis}[colormap/viridis]
\addplot3[
	surf,
	samples=18,
	domain= -5:5
]
{x*sin(y)};

\end{axis}

\end{tikzpicture}
\end{document}
```

In pratica se cerco i punti estremavi di una funzione $f$ in un insieme $A$ aperto
- Se $f$ è derivabile in tutto A: determino i punti critici di $f$ in $A$ e poi stabilisco quali sono massimo minimo e selle.
- Se $f$ ha punti di non derivabilità li includo tra i candidati

>[!oss]
> Se $f$ è anche differenziabile li includo tra i candidati
> 1. Il piano tangente al grafico di $f$ in $(x_{0},y_{0},f(x_{0},y_{0}))$ è orizzontale
> 	$$ z = f(x_{0},y_{0}) + \underbrace{ \langle \nabla f(x_{0},y_{0}), \begin{bmatrix}
>x-x_{0} \\
y-y_{0}
\end{bmatrix}\rangle }_{ = 0 } $$
>
>2. $\forall \mathbf{v} \subseteq \mathbb{R}^2\quad ||\mathbf{v}|| = 1$ si ha 
> $$ \frac{ \partial f }{ \partial \mathbf{v} } (x_{0},y_{0}) = \langle \nabla f(x_{0},y_{0}), \mathbf{v}\rangle = 0 $$


>[!esempio]
>Determinare tutti i punti critici di
>
$$ f(x,y) = 3x^2 + y^2 - x^3y $$
>
>
>```tikz
>\usepackage{pgfplots}
>\begin{document}
>\begin{tikzpicture}
>\begin{axis}[colormap/viridis]
>\addplot3[
>	surf,
>	samples=16,
>	domain = -5:5
>	]
>{3*x^2 + y^2 - x^3 *y};
>\end{axis}
>\end{tikzpicture}
>\end{document}
>```
>
>Ricaviamo il sistema in generale non lineare:
>$$ 
>\begin{cases}
>6x - 3x^2y = 0 \\
>2y - x^3 = 0
>\end{cases}
>$$
>ad occhio $(0,0)$ è soluzione:
>$$ \begin{align}
>&\begin{cases}
>3x(2-xy) = 0 \\
>y = \frac{x^3}{2}
>\end{cases} \\
>&\begin{cases}
>y= \frac{2}{x} \\
>y =\frac{x^3}{2} 
>\end{cases} \implies \begin{cases}
>y = \frac{2}{x} \\
>x^4 = 4
>\end{cases} \\
>&\begin{cases}
>x = \pm \sqrt{ 2 } \\
>y = \frac{2}{x}
>\end{cases}
>\end{align}$$
>
>Quindi grazie al teorema di fermat ci ricond
