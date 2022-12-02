Col cambiamento di variabile negli integrali doppi si intende solitamente il passaggio alle coordinate polari

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[axis lines = left]
\addplot[domain = -3:3, samples=25]{cos(deg(x))};
\end{axis}
\end{tikzpicture}

\hskip 5pt

\begin{tikzpicture}
\begin{axis}[axis lines = left]
\addplot[domain = -3:3, samples=200]{x};
\end{axis}
\end{tikzpicture}
\end{document}
```

$$\phi(r,t) = \begin{bmatrix}
\phi_{1}(r,\theta) \\
\phi_{2}(r,\theta)
\end{bmatrix} = \begin{bmatrix}
r \cos \theta \\
r \sin \theta
\end{bmatrix} = 
\begin{bmatrix}
x \\
y
\end{bmatrix}$$

$$ \iint_{E} $$
