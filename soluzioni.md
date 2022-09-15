# Soluzioni
>[!def]
>Si chiama **integrale generale** l'insieme di tutte le soluzioni.
>Si chiama **soluzione particolare** una specifica soluzione.


Equazione differenziale | Soluzioni | costanti
---|---|---
1° ordine | $\infty^1$ | 1 costante
2° ordine | $\infty^2$ | 2 costanti

>[!esempio]
>$$y'(t) = y(t)$$
>Integrale generale: $Ce^t$
>Alcune soluzioni particolare: $e^t,\sqrt{ 2 }e^t,-10e^t$
>
>
>$$\begin{align}
>&Z(t) = -1 + \arctan(t) \\ \\
>&Z'(t) =\frac{1}{t^2+1}
>\end{align}$$

>[!oss]
>L'EDO $y'(t) = f(t,y(t))$ è definita sul dominio di definizione della $f$.

Vediamo il procedimento formale, ricordando il [[teorema fondamentale del calcolo integrale]], con un esempio:

>[!esempio]
>$$ \int_{t_{0}}^t \! \frac{1}{x}\, \mathrm{d}x = [\ln]_{t_{0}}^t=\ln(t)-\ln(t_{0}) $$
>Ma allora
>$$ \begin{align}
> &y(t) - y(t_{0}) = \ln(t) - \ln(t_{0}) \\ \\
> &y(t) = \ln(t) - \fbox{$\ln(t_{0}) + y(t_{0})$}\to C
>\end{align} $$
>
>

```tikz
\usetikzlibrary{calc}
\usetikzlibrary{patterns,arrows.meta}
\begin{document}
\begin{tikzpicture}[domain=0.3:4]
\draw[-Stealth] (0,0) -- (0,3);
\draw[-Stealth] (0,0) -- (3,0);
\draw[color=purple] plot (\x,{ln(\x)}) node[right] {$f(x) = \ln x$};
\draw[color=purple] plot (\x,{ln(\x)-1}) node[right] {$f(x) = \ln x - 1$};
\draw[color=purple] plot (\x,{ln(\x)+1}) node[right] {$f(x) = \ln x + 1$};
\end{tikzpicture}
\end{document}
```
I grafici delle soluzioni riempiono il piano.


# soluzioni costanti di EDO del 1° ordine
>[!def]
>Data $$y'(t) = f(t, y(t))$$
>Una soluzione costante è una funzione $y(t) = C,\quad\forall t$ che sia soluzione. 
>
>
>



Ma quando $y(t)=C$ è soluzione?
Sostituisco $C$ al posto di $y$:

$$
\begin{align}
&y'(t) - &&f(t,y(t))\\ 
&\uparrow &&\uparrow \\
C'&=0 &&f(t,C) \\
 \end{align}
$$
$\Rightarrow \text{le soluzioni costanti sono } y(t')=C \forall t$ con $C : f(t,c = 0) \forall t$ 

>[!esempio] equazione logistica
> $$\begin{align}
>&y'(t) = ky(t) - hy^2(t)  \\
>&f(t,y) = ky - hy^2  \\
>&f(t,c) = 0 \forall \\
>&ky-hy^2 = 0 \\
>&\Longrightarrow y = 0 \cap y = \frac{k}{h}
>\end{align}$$

>[!esempio]
>$$\begin{align}
>y'(t) &= te^{y(t)}\quad \Longrightarrow \quad te^y = 0 \quad \forall t \\
>&\Longrightarrow\quad e^y \quad\text{non si annulla, quindi non ha soluzioni costanti}
>\end{align}$$
