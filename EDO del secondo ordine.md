# [[EDO]] del secondo ordine


Prendiamo un esempio dalla fisica, presa una particella e definita la sua posizione $y(t)$, allora la sua velocità è $y'(t)$ e l'accelerazione è $y''(t)$.
Data poi la legge fondamentale della dinamica
$$ F = ma \Longrightarrow F = mf'' $$
Allora $$ my'' = F(t,y,y') $$
Che è una equazione differenziale ordinaria, di secondo ordine in quanto la derivata di ordine maggiore è la seconda.

In altri campi della fisica come termodinamica e fluidodinamica, si utilizzano [[EDO alle derivate parziali]]







# EDO del secondo ordine lineari

Hanno forma
$$ a(t)y''(t) + b(t)y'(t) + c(t)y(t) = f(t) $$
$a \neq 0, f$ definito forzante.

>[!esempio]
>```tikz
>\usepackage{circuitikz}
>\begin{document}
>\begin{circuitikz}[american, voltage shift=0.5]
>\draw (0,6)
>to[vsource, v=E] (0,0)
>to[short] (0,6) -- (2,6)
>to[R=R] (2,4)
>to[L=L] (2,2)
>to[C=C] (2,0)
>(2,0) -- (0,0);
>\end{circuitikz}
>\end{document}
>```
>
>Circuito RLC in serie, vogliamo determinare la carica $q(t)$ e la corrente $i(t) = q'(t)$.
>$$ \begin{align}
>&Li'(t) + Ri(t) + \frac{q(t)}{C} = E(t) \\
>&Lq''(t)+Rq'(t)+\frac{1}{C}q(t)=E(t) \\
>&Li''(t) + Ri'(t) + \frac{1}{C}i(t) = E'(t)
\end{align}$$


# Soluzioni di una EDO del secondo ordine

Partiamo da un esempio
>[!esempio]
>$$ y'' = 0 $$
>Che ha come soluzione ogni equazione lineare $y = c_{1}t+c_{2}$ per ogni $c_{1},c_{2} \in \mathbb{R}$
>Ed, abbiamo quindi infinite soluzioni.

Per la precisione abbiamo $\infty^2$ soluzioni, per cercarne una specifica dobbiamo risolvere il [[Problema di Cauchy]] del tipo:
$$ 
\begin{cases}
a(t)y''+b(t)y' + c(t)y = f(t) \\
y'(t_{0}) = v_{0} \\
y (t_{0}) = y_{0}
\end{cases}
$$