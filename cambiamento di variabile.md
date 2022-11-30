Col cambiamento di variabile negli integrali doppi si intende solitamente il passaggio alle coordinate polari
```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[axis lines = left]
\addplot[domain = -3:3, samples=25]{cos(deg(x))};
\end{axis}
\begin{axis}
\addplot{x};
\end{axis}
\end{tikzpicture}
\end{document}
```