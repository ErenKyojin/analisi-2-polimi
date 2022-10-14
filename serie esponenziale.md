
# serie esponenziale complessa

[[Raggio di convergenza]] infinito (stessa dimostrazione del caso reale)
definiamo la funzione esponenziale complessa da $\mathbb{C}$ a $\mathbb{C}$ come somma di questa serie:
$$ \sum_{n=0}^\infty  \frac{z^n}{n!} = e^z\qquad \forall z \in \mathbb{C}$$
Prendendo $z$ immaginario puro $(z = ix, x \in \mathbb{R})$

$$ \begin{align}
e^{ix}=\sum_{n=0}^\infty \frac{(ix)^n}{n!} &= 1 + ix + \frac{ix^2}{2!} + \frac{ix^3}{3!} +\frac{ix^4}{4!} + \frac{ix^5}{5!} + \dots \\
&=1 + ix - \frac{x^2}{2!}- \frac{ix^3}{3!}+\frac{x^4}{4!}+\frac{ix^5}{5!}-\frac{x^6}{6!}\dots
\end{align} $$

Raggruppando le parti reali:
$$\begin{align}
&= \left( 1-\frac{x^2}{2!} + \frac{x^4}{4!}  - \frac{x^6}{6!} + \dots\right) + i\left( x-\frac{x^3}{3!}+\frac{x^5}{5!} + \dots \right) =  \\
&=\sum_{n=0}^\infty (-1)^n \frac{x^{2n}}{2n!} + i \sum_{n=0}^\infty \frac{x^{2n+1}}{(2n+1)!} = \\
&=\cos x + i\sin x 
\end{align}$$
Formula di eulero 
$$ \fbox{$e^{ix}=\cos x + i \sin x\qquad \forall x \in \mathbb{R}$} $$


>[!oss]
>$$e^{-ix} = e^{i(-x)} = \cos(x) - i\sin(x)$$
>Notiamo quindi che $e^{ix} + e^{-ix} = 2\cos x$, quindi
>$$ \cos(x) = \frac{e^{ix} + e^{-ix}}{2} $$
>$$\sin(x) = \frac{e^{ix} - e^{-ix}}{2i}$$
