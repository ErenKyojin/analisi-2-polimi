/# Convergenza totale di una serie di funzioni

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
>\begin{tikzpicture}[domain=-1.1:-0.4]
>\draw[->] (-2.5,0) -- (2.5,0) node[right]{$x$};
>\draw[->] (0,-2.5) -- (0,2.5) node[above]{$f(x)$};
>\draw[color=red,samples=200] plot (\x, {1});
>\draw[color=orange,samples=200] plot (\x, {1+\x^1});
>\draw[color = cyan,samples=200 ] plot (\x, {1 + \x^1 + \x^2});
>\draw[color = blue,samples=200] plot (\x, {1 + \x^1 + \x^2 + \x^3});
>\draw[color = teal, samples=200] plot (\x, {1 + \x^1 + \x^2 + \x^3 + \x^4});
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



## Convergenza totale per le [[serie di potenze]] reali

Data una serie di potenza avente raggio di convergenza $0 \leq R \leq +\infty$ si ha:
1. Se $R = +\infty$ la serie converge totalmente in ogni intervallo chiuso e limitato $[c,d]$
2. Se $0 < R < +\infty$ la serie converge totalmente in ogni intervallo chiuso $[c,d] \subset (x_{0} - R, x_{0}+R)$


Allora
>[!important] importante
>Non è necessario studiare la convergenza totale per una serie di potenze!

>[!oss]
>Nel primo caso la serie potrebbe non convergetre totalmente su $\mathbb{R}$
>
>>[!esempio]
>>$$ \begin{align}
>> &\sum \frac{\sin(nx)}{n^3} \quad\text{converge totalmente su }\mathbb{R} \\
>> e^x = &\sum \frac{x^n}{n!} \quad\text{converge totalmente su ogni insieme }[c,d], \text{non su }\mathbb{R}
>>\end{align} $$

## convergenza totale della serie trigonometrica
Data la serie trigonometrica
$$ a_{0} + \sum_{n=1}^\infty (a_{n} \cos(nx) + b_{n}\sin(nx))$$
1. Se $\sum (|a_{n}| + |b_{n}|) < \infty$
Allora la serie trigonometrica converge totalmente in $\mathbb{R}$, in particolare la funzione somma è continua in $\mathbb{R}$ e posso integrare termine a termine in ogni sottoinsieme limitato

2. Se $\sum n(|a_{n}| + |b_{n}|) < \infty$ allora la funzione somma è derivabile in $\mathbb{R}$ e posso derivare termine a termine

Iterando la seconda II:
se $n^2(|a_{n}|+|b_{n}|)< +\infty$ allora la $f$ somma è derivabile termine a termine 2 volte.