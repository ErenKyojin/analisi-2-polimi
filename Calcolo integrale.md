$$ A \subseteq \mathbb{R}^3 \int\!\int\!\int_{A} \! f(x,y,z)\, \mathrm{d}x  \! \, \mathrm{d}y  \! \, \mathrm{d}z  $$


# Integrali doppi

## Regioni semplici
>[!def] 
>$D \subseteq \mathbb{R}^2$ è detta regione-$y$ semplice se $$D = \{(x,y) \in \mathbb{R}^2 : x \in [a,b], g_{1}(x) \leq y \leq g_{2}(x)\}$$
> con $[a,b]$ limitato $g_{1} \leq g_{2}$ continue in $[a,b]$

>[!def]
>$D \subseteq \mathbb{R}^2$ è detta regione $x$-semplice se
> $$ D = \{(x,y) \in \mathbb{R}^2 : y \in [c,d], h_{1}(y) \leq x \leq h_{2}(y)\} $$
> Con $[c,d]$ limitato e $h_{1} \leq h_{2}$ continue in $[c,d]$

---


Significato geometrico dell'integrale doppio è il volume con segno sottostante alla curva, oppure la massa di una superficie 2d

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[axis lines = center]
\addplot[domain = -3:3, samples=100]{-sqrt(1 - x^2)};
\addplot[domain = -3:3, samples=100]{sqrt(1-x^2)};
\end{axis}
\end{tikzpicture}
\end{document}
```