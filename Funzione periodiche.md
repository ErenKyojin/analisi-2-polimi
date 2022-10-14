$f : \mathbb{R} \to \mathbb{R}$ è periodica di periodo $T$ se:
$$ f(x+T) = f(x) \qquad \forall x \in \mathbb{R}$$

>[!oss]
>non ci sono ipotesi di regolarità
>Se $f$ periodica di periodot $T$ è anche periodica di periodo $nT$

Se $f$ è periodica di periodo $T$ pari (dispari) in $\left[ -\frac{T}{2}, \frac{T}{2} \right]$ resta pari (dispari) su tutto $\mathbb{R}$


>[!def]
>Chiamiamo armonica $n$-esime le funzioni
> $$ \cos(nx), \sin(nx)\qquad x \in \mathbb{R} $$
>
>```tikz
>\begin{document}
>\tikz{
>\draw[-stealth] (-5,0) -- (5,0);
>\draw[-stealth] (0,-2.5) -- (0,2.5);
>\draw[samples=200,red] plot (\x,  {sin (\x r)}) node[right]{$\sin x$};
>\draw[samples=200,color=blue] plot(\x, {sin (2*\x r)}) node[right]{$\sin 2x$};
>\draw[samples=200,color=green] plot(\x, {sin (3*\x r)}) node[right]{$\sin 3x$};
>}
>\end{document}
>```

ogni armonica $n$-esima è periodica di periodo $\frac{2\pi}{n}$, e quindi anche di periodo $2\pi$, il caso limite è $h=0 \implies f=1$


