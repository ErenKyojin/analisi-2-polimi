# EQUAZIONI DI BERNOULLI

>[!def]
>Si chiamano equazioni di Bernoulli le [[EDO]] del 1° ordine non lineari del tipo:
> $$ y'(t) = k(t)y(t) + h(t)y(t)^\alpha\qquad \left(\alpha \in \mathbb{R}, \qquad\begin{align}
>\alpha \neq 1  \\
>\alpha \neq 0
>\end{align}\right) $$
>$h,k : J \to \mathbb{R}$ continue

### premesse
1. ci occupiamo solo di soluzioni $y \geq 0$
2. Nel caso $\alpha < 1$ accadono "fenomeni strani", la tecnica di risoluzione è valida non di meno.


## Procedimento

1. Cerchiamo le soluzioni costanti (sempre almeno quella nulla)
2. Divido per $y^\alpha$
$$
\begin{align}
\frac{y'(t)}{y^\alpha} &= \frac{k(t)h(t)}{y^\alpha(t)} + \frac{h(t)\cancel{y^\alpha(t)}}{\cancel {y^\alpha(t)}}  \\
\frac{y'(t)}{y(t)^\alpha} &= k(t)y(t)^{1-\alpha} + h
\end{align}$$
3. Pongo $Z(t) = y(t)^{1 - \alpha}$
Qual è l'equazione soddisfatta da $Z$?
$$\begin{align}
&Z'(t) = (1-\alpha)y^{-\alpha}y'(t) \Rightarrow Z'(t) = (1-\alpha)[k(t)y(t)^{1-\alpha} + h]  \\
&\Rightarrow Z'(t) = (1-\alpha)[k(t)z(t)+h]
\end{align}$$
Che è un equazione lineare, infatti:
$$ Z'(t) = \underbrace{ (1-\alpha)k(t) }_{ a(t) }z(t) + \underbrace{ (1-\alpha)h(t) }_{ b(t) } $$
4. risolvo l'equazione lineare in $Z$
5. Torno alla variabile $y = Z(t)^{\frac{1}{1-\alpha}}$