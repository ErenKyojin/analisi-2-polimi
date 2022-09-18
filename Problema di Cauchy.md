# Problema di Cauchy
Possiamo introdurre il problema di Cauchy pensando al come trovare la soluzione che passa per un determinato punto del piano, più precisamente:

>[!def]
>Data una generica [[EDO]] del $1°$ ordine
>$$y'(t) = f(t,y(t))$$
>E dato $(t_0, y_0) \in$ dominio di definizione di $f$.
>Si chiama problema di Cauchy il problema di determinare $y : I \subset \mathbb{R}$ che soddisfa
>$$\begin{cases}
>y'(t) = f(t,y(t)) \\
>\fbox{$y(t_{0}) = y_{0}$} \rightarrow \text{1 condizione in quanto del primo ordine}
>\end{cases}
>$$
 >Per un qualche $I$ con $t_0 \in I$

# risolvere il problema di cauchy
1. determinare l'integrale generale, $\infty^1$ soluzioni con un solo parametro $C$
2. impongo $y(t_{0}) = y_{0}$ e determino $C$
3. Sostituisco $C$ nell' integrale generale

>[!esempio]
>data $$y'(t) = ty(t)^3$$
>quindi $f(t,y) = ty^3$ definita in tutto $\mathbb{R}^2$ (il che significa che posso impostare il problema di Cauchy $\forall (t_{0},y_{0}) \in \mathbb{R}$)
>
>L'integrale generale di questa equazione è:
>$$y(t) = \pm \sqrt{ \frac{1}{-t^2+C} }$$
>Mentre la soluzione costante è $y(t) = 0$
>
>
>Prendiamo in considerazione 3 casi:
>1. $$\begin{align}
>&\begin{cases}
>y'=ty^3  \\
>y(0) = 1
>\end{cases} \\
>\Longrightarrow &1 = +\sqrt{ \frac{1}{0+C} } \Rightarrow 1 = \sqrt{ \frac{1}{C} } \Rightarrow C=1
>\end{align}
>$$
>
>```tikz
>\begin{document}
>\end{document}
>```
>