Particolari serie dove abbiamo gli $x^n$ moltiplicati per coefficienti

>[!def]
>Una serie di potenze è una serie di funzioni della forma
>$$ \sum_{n=0}^\infty  a_{n} (x - x_{0})^n = a_{0}+a_{1}(x-x_{0})+a_{2}(x-x_{0})^2+\dots + a_{n}(x-x_{0})^n+\dots$$
>È una serie centrata in $x_{0}$ con $a_{n} \in \mathbb{R}$ detti coefficienti.


Se $x=x_{0}$
$$ \sum a_{n}(x-x_{0})  = a_{0}+ a_{1}\underbrace{ (x_{0}-x_{0})^1 }_{ 0 } + a_{2}\underbrace{ (x_{0}-x_{0})^2 }_{ 0 } = a_{0}$$
Vogliamo cconoscere l'insieme di [[convergenza]] della generica
$$ \sum_{n=0}^\infty a_{n}(x-x_{0})^n$$
>[!oss]
>se $a_{n} = 1 \forall n$ l'insieme di convergenza semplice è $(x_{0}-1, x_{0}+1)$
>Si tratta infatti di una traslata della [[serie geometrica]]


Posso determinare l'insieme di convergenza della  generica serie di potenze senza avere informazioni sugli $a_{n}$?
L'insieme di convergenza dipende dalla rapidità di convergenza di $\sum a_{n}$

>[!esempio]
>Consideriamo la [[serie esponenziale]]
>$e^x = \sum \frac{x^n}{n!}$ abbiamo che $a_{n} = \frac{1}{n!}$ che converge molto rapidamente come si vede usando il [[criterio del rapporto]]
>$$ l = \lim_{ n \to \infty } \frac{a_{n+1}}{a_{n}} = \frac{1}{(n+n!)}=\lim_{ n \to \infty } \frac{1}{n+1} = 0 < 1 $$

Vogliamo quindi determinare il [[raggio di convergenza]]


## Integrabilità termine a termine per una serie di potenze reali

Data una serie di potenze $\sum a_{n}(x-x_{0})^n$ avente raggio di convergenza $0 < R \leq +\infty$ per ogni $x \in (x_{0}-R,x_{0}+R)$ finito, vale la formula di integrazione termine a termine:

$$ \begin{align}
\int_{x_{0}}^x \! \sum_{n=0}^\infty a_{n}(t-x_{0})^n \, \mathrm{d}t  &=  \sum a_{n}\int_{x_{0}}^x \! (t-x_{0})^n\, \mathrm{d}t  \\
&=\sum a_{n} \frac{(x-x_{0})^{n+1}}{n+1}
\end{align}$$
Che ha raggio di convergenza ancora $R$ infatti:
$$ \lim_{ n \to \infty }  \left| \frac{b_{n}}{b_{n+1}} \right| = \lim_{ n \to \infty } \left| \frac{a_{n}}{a_{n+1}} \cdot \frac{n+2}{n+1} \right| = \lim_{ n \to \infty }  \left( \frac{a_{n}}{a_{n+1}} \right) = R  $$
## Derivabilità termine a termine per una serie di potenze
Data una serie di potenze $\sum a_{n}(x-x_{0})^n$ avente raggio di convergenza $0 < R \leq +\infty$ per ogni $x \in (x_{0}-R, x_{0}+R)$ vale la formula di derivazione termine a termine:
$$ \left( \sum_{n=0}^\infty a_{n}(x-x_{0})^n \right)' = \sum_{\color{red}n=1\color{white}}a_{n}n(x-x_{0})^{n-1} $$
E la serie di potenze derivata ha raggio di convergenza ancora R. È ovvio che si può reiterare per derivate di ogni ordine:


>[!conseguenze]
La somma di una serie di potenze è derivabile ad ogni ordine:



# serie di potenze complesse
>[!def]
> si dice serie di potenze complesse una serie del tipo:
> $$ \sum_{n=0}^\infty a_{n}(z-z_{0})^n = a_{0} + a_{1}(z-z_{0})+a_{2}(z-z_{0})^2+\dots$$
> 
> Con:
> - $a_{n} \in \mathbb{C}$ anche se solitamente è in $\mathbb{R}$
> - $z \in \mathbb{C}$
> - $z_{0} \in \mathbb{C}$

>[!teorema]
>
>
>```tikz
>\begin{document}
>\tikz{
>\draw[->] (-1.5,-2) -- (-1.5,4);
>\draw[->](-2,-1.5) -- (7, -1.5);
>\node[circle,draw,scale=6] (c) at (0,0){};
>\node(c) at (0,0){$z_{0}$}
>}
>\end{document}
>```
>All'interno del raggio la serie converge, all'esterno non converge, e sul bordo del cerchio va studiato caso per caso.


Le formule per il calcolo di $R$ rimangono valide.

[[serie esponenziale#serie esponenziale complessa]]

