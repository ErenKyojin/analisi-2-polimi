
>[!esempio]
>$$ y'(t) = y(t) $$
>Tre famiglie di soluzioni
>$\color{cyan} ke^{t+c}$
>$\color{yellow}0$
>$\color{red}-ke^{t+c}$
>
>```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[axis lines = center]
\addplot[domain = -3:3, samples=25, color = cyan]{e^x};
\addplot[domain = -3:3, samples=25, color = yellow]{0};
\addplot[domain = -3:3, samples=25, color = red]{-e^x};
\addlegendentry{\(+e^x\)}
\addplot[domain = -3:3, samples=25, color = cyan]{2* e^x};
\addplot[domain = -3:3, samples=25, color = cyan]{3*e^x};
\addplot[domain = -3:3, samples=25, color = red]{-2*e^x};
\addplot[domain = -3:3, samples=25, color = red]{-3*e^x};
\addlegendentry{\(0\)}
\addlegendentry{\(-e^x\)}
\end{axis}
\end{tikzpicture}
\qquad
\begin{tikzpicture}
\draw[->, color = red ] (0,3) -- (0,0);
\draw[->, color = cyan] (0,3) -- (0,6);
\node[color = yellow] at (0,3){o};
\end{tikzpicture}
\end{document}
>```

Le soluzioni non nulle non possono cambiare di segno non potendo attraversare l'asse $t$ che è soluzione (y=0), inoltre possiamo intuire la idrezione delle frecce dal segno di $f$

Una soluzione compresa tra due costanti ha come asintoti entrambe le costanti.