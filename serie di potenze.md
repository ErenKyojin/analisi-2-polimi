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
>$e^x = \s