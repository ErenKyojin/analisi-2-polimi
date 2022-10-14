
>[!def]
>Una serie trigonometrice è
> $$ a_{0} + \sum_{n=1}^\infty (a_{n} \cos(nx) + b_{n} \sin(nx)) $$
> con $a_{0},a_{n},b_{n} \in \mathbb{R}$

Ogni polinomio trigonometrico è [[Funzione periodiche|periodico]] di periodo $2\pi$, allora la somma di una serie trigonometrica è anchessa $2\pi$ periodica. Per questo motivo supponiamo sempre che la funzione che vogliamo decomporre sia $2\pi$ periodica.


>[!error]
>Le serie trigonometrice, a differenza delle [[Serie di potenze]], possono perdere regolarità dentro il [[raggio di convergenza]]



## Convergenza di una serie trigonometrica

Vogliamo una condizione che ci assicuri una serie trigonometrica converga totalmente in R:
$$ \begin{align}
|f(x)| &= |a_{n} \cos(nx) + b_{n}\sin(nx)| \\
&\leq|a_{n} \cos (nx)| + |b_{n} \sin(nx)| \\
&= |a_{n}| \cdot | \cos(nx)| + |b_{n}| |\sin(nx)| \\
&\leq |a_{n}| + |b_{n}| \\
\end{align} $$

Quando è derivabile termine a termine?
$$\begin{align}
|f_{n}'(x)| &= |-a_{n} n \sin(nx) + b_{n} n \cos(nx)| \\
&\vdots \\
&\leq n(|a_{n}|+|b_{n}|)
\end{align}$$


[[Convergenza totale]]
