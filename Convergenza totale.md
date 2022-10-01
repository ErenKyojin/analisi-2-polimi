# Convergenza totale di una serie di funzioni

 Partiamo con un esempio
 >[!esempio]
 >$$ \frac{\sin nx}{n^3},\qquad x \in (-1,1) $$
 >```tikz
 >\begin{document}
 >\begin{tikzpicture}[domain=-1:1]
 >\draw[thin, color=gray] (-1.5,-1.5) grid (1.5,1.5);
 >\draw[->] (-1.5,0) -- (1.5,0) node[right] {$x$};
 >\draw[->] (0,-1.5) -- (0,1.5) node[above] {$f(x)$};
 >\draw[color=orange] plot (\x,{sin(\x r)}) node[below right,color=orange] {$S_{1}(n)$};
 >\draw[color=red] plot (\x, {sin(\x r) + sin(2\x r)/8}) node[above,color=red]{$S_{2}(n)$};
 >\draw[color=cyan] plot (\x, {sin(\x r) + sin(2\x r)/8 + sin(3\x r)/27} ) node[left,color=cyan]{$S_{3}(n)$};
 >\end{tikzpicture}
 >\end{document}
>```
>
>----
>
>
>Serie geometrica:
>$$ x^n, x \in \left( -1, -\frac{1}{2} \right) $$
>
>```tikz
>\begin{document}
>\begin{tikzpicture}[domain=-1:-0.5]
>\draw[->] (-2.5,0) -- (2.5,0) node[right]{$x$};
>\draw[->] (0,-2.5) -- (0,2.5) node[above]{$f(x)$};
>\draw[color=red] plot (\x, {\x^0});
>\draw[color=orange] plot (\x, {\x^0+\x^1});
>\draw[color = cyan] plot (\x, {\x^0 + \x^1 + \x^2});
>\end{tikzpicture}
>\end{document}
>```


>[!def] Definizione importante
>La serie di termini generali $f_{n}(x), x \in J$, converge, totalmente nell'intervallo non vuoto $I \subseteq J$ se esiste una successione numerica $a_{n} \geq 0$ tale che:
>1. $|f_{n}(x)| \leq a_{n}\qquad \forall x \in I, \forall n = 0,1,2,3,\dots$
>2. $\sum_{n=0}^\infty a_{n} < +\infty$ 

>[!oss]
>Si parla di convergenza totale nel riguardo di un intervallo, non di un punto (motivo per cui non è un criterio presente nelle serie numeriche)

>[!oss]
>La convergenza totale in $I$ implica la [[Convergenza assoluta]] e quindi [[convergenza semplice]].
>
>>[!error]
>>non vale il viceversa, se una serie converge assolutamente in ogni punto di $I$ non è detto che converga totalmente in $I$, basti pensare alla serie geometrica in $E=(-1,1)$

