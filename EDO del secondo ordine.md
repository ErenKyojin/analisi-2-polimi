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
>Lq''
\end{align}$$
>