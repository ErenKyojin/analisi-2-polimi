>[!def]
>Sia $A \subseteq \mathbb{R}^2$ aperto
>$f : A \to \mathbb{R}$ derivabile in $(X_{0},y_{0}) \in A$
>Se $\nabla f (x_{0},y_{0}) = \begin{bmatrix}0 & 0\end{bmatrix}^T$ allora $(x_{0},y_{0})$ è detto punto critico o punto stazionario

>[!def]
>Un punto critico di $f$ che non è punto estremale di $f$ è detto punto di sella


```tikz
\usepackage{pgfplots}
\begin{document}
\begin{tikzpicture}[colormap/virdis]
\addplot[
	surf,
	samples=18,
	domain= -3:3
]
x*sin(y)

\end{tikzpicture}
\end{document}
```