>[!def] 
>Data una funzione $f$ definita su $A$ si dice che $f$ è di calsse $C^k$ se in $A$ esistono tutte le derivate fino al $k-$esimo ordine e la $k-$esima è continua
```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[axis lines = left]
\addplot[domain = -3:3, samples=25]{cos(deg(x))};
\end{axis}
\end{tikzpicture}
\end{document}
```