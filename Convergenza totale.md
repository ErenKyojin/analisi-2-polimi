# Convergenza totale di una serie di funzioni

 Partiamo con un esempio
 >[!esempio]
 >$$ \frac{\sin nx}{n^3},\qquad x \in (-1,1) $$
 >```tikz
 >\begin{document}
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

