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
>1. 
>$$\begin{align}
>&\begin{cases}
>y'=ty^3  \\
>y(0) = 1
>\end{cases} \\
>\Longrightarrow &1 = +\sqrt{ \frac{1}{0+C} } \Rightarrow 1 = \sqrt{ \frac{1}{C} } \Rightarrow C=1 \\
>\Longrightarrow&\text{soluzione } = y(t) +\sqrt{ \frac{1}{-t^2+1} }
>\end{align}
>$$
>
>```tikz
>\usepackage{pgfplots}
>\begin{document}
>\begin{tikzpicture}
>\begin{axis}[
>axis x line = center,
>axis y line = center,
>xmin=-2,
>ymin=-2,
>xmax=2,
>ymax=2,
>]
>\addplot[domain=-0.9:0.9, samples=200,color=red] {sqrt(1/(-x^2+1))};
>\end{axis}
>\end{tikzpicture}
>\end{document}
>```
>
>2. $$ \begin{cases}
> y'=ty^3 \\
> y(t_{0}) =0
>\end{cases} 
>\Longrightarrow \text{la soluzione costante è 0, $\forall t_{0}\quad y(t_{0})=0$}
>$$
>
>```tikz
>\usepackage{pgfplots}
>\begin{document}
>\begin{tikzpicture}
>\begin{axis}[
>axis x line = center,
>axis y line = center,
>xmin = -2,
>ymin = -2,
>xmax = 2,
>ymax = 2,]
>
>\addplot[domain = -2:2, color = red] {0};
>\end{axis}
>\end{tikzpicture}
>\end{document}
>```
>
>3. $$\begin{align}
>&\begin{cases}
>y' = ty^3  \\
>y(0) = -1
>\end{cases}\qquad-1 = -\sqrt{ \frac{1}{0+C} } \Rightarrow C = 1 \\
>&\Rightarrow y(t) = -\sqrt{ \frac{1}{C} }
>\end{align} $$
>
>
>```tikz
>\usepackage{pgfplots}
>\begin{document}
>\begin{tikzpicture}
>\begin{axis}[
>axis x line = center,
>axis y line = center,
>xmin = -2,
>xmax = 2,
>ymin = -2,
>ymax = 2,
>]
>\addplot[domain=-0.9:0.9, color = red, samples=200] {-sqrt(1/(-x^2+1))};
>\end{axis}
>\end{tikzpicture}
>\end{document}
>```
>
>>[!oss]
>> Per determinare quale delle soluzioni usare dobbiamo guardare il segno della $y(t_0)$ così da determinare quale tra le soluzioni possa ammetere quel segno.

>[!oss]
>Se il dominio di $f$ è disconnesso è utile determinare solo le soluzioni che giaccono nella stessa regione di $t_0$

>[!teorema] Esistenza e unicità globale di Cauchy
>Siano $J \subseteq \mathbb{R} \in a,b : J \to \mathbb{R}$ continua. Per ogni $t_{0} \in J, y_{0} \in \mathbb{R}$ il problema di Cauchy.
> $$ \begin{cases}
> y'(t) = a(t)y(t) + b(t) \\
> y(t_{0}) = y_{0}
>\end{cases} $$
Ha un unica soluzione $y(t)$ definita $\forall t \in J$

$$ y'(t) = a(t)y(t) + b(t)\qquad a,b \text{ contiua su } J $$