worlds 20# formula risolutiva EDO del 1° ordine
>[!teorema] teorema
>$a,b : J \subseteq \mathbb{R} \to \mathbb{R}\qquad y'(t) = a(t)y(t)+b(t)$
>L'integrale generale è dato dalla formula:
> $$ y(t) = e^{A(t)}\left(\int \! e^{-A(t)}b(x) \, \mathrm{d}x + C\right)\qquad C \in \mathbb{R} $$
con $A(t)$ primitiva di $a$
>
>>[!dim]
>>1. portiamo $ay$ sulla sinistra
>>$$y' - ay = b$$
>>2. moltiplichi per $e^{-A}$
>> $$ y'e^{-A} - aye^{-A} = be^{-A} $$
>>3. riconosco $y(t)'e^{-A(t)}-a(t)y(t)e^{-A(t)} = [y(t)e^{-A}]'$
>> $$ \begin{align}
>>[ye^{-A}]' &= be^{-A}  \\
>>y &= e^A\left( \int \! be^{-A} \, \mathrm{d}t  \right) \qquad\blacksquare
\end{align}$$



>[!esempio]
>$y'(t) + y(t) + \sin(t) = 0$
> $$ \begin{align}
> &e^t[y'(t) + y(t)] = -\sin(t)e^t \\
> &e^t y(t) = \int \! -e^t \sin(t) \, \mathrm{d}t + C  \\
>&e^ty(t) = \int -e^t \sin t \, \mathrm{d}t  \\
>&y(t) = e^{-t}\left[ \int \! -e^t \sin(t) + C \, \mathrm{d}t  \right]
>\end{align} $$

