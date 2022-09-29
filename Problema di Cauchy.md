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

$$
\begin{align}
y'(t) &= a(t)y(t) + b(t)\qquad a,b \text{ contiua su } J  \\
&=f(t,y(t))
\end{align}$$
Con $f$ lineare rispetto a $y : f(t,y) = a(t)y+b(t)$, dominio di definizione di $f = J \times \mathbb{R}$ 
Quindi il teorema ci dice che:
1. dati qualsiasi $(t_{0},y_{0}) \in J \times \mathbb{R}$ c'è una soluzione della EDO passante per $(t_{0},y_{0})$:
—> i grafici della soluzioni riempiono $J \times \mathbb{R}$
2. Essa è unica:
—> i grafici delle soluzioni non si intersecano
3. La soluzione è definita $\forall t \in J$
—> per le variabili separabili, che non sono quindi lineari, non è necessario
—> se $a,b$ costanti $\Rightarrow J = R$

# Problema di Cauchy per [[EDO del secondo ordine]] lineari
per cercare una soluzione specifica dobbiamo risolvere il [[Problema di Cauchy]] del tipo:
$$ 
\begin{cases}
a(t)y''+b(t)y' + c(t)y = f(t) \\
y'(t_{0}) = v_{0} \\
y (t_{0}) = y_{0}
\end{cases}
$$


1. determiniamo l'integrale generale
2. Imponiamo le condizioni iniziali
3. Sostituire i valori nella formula dell'integrale generale

>[!esempio]
>$$ y'' - 3y' + 2y = t $$
>con $y(0) = 1, y'(0) = -1$ e l'integrale generale
>$$y(t) = c_{1}e^t+c_{2}e^{2t}+\frac{t}{2}+\frac{3}{4} \qquad c_{1},c_{2} \in \mathbb{R}$$
>
>$$ y(0) = c_{1} e^0 +c_{2}e^0 + \frac{0}{2} + \frac{3}{4} = \fbox{$c_{1}+c_{2}+\frac{3}{4} = 1$}$$
>Calcoliamo la derivata prima
>$$ y'(t) = c_{1}e^t+2c_{2}e^{2t} + \frac{1}{2} $$
>imponiamola a 0
>$$ y'(0) = c_{1}e^0 + 2c_{2}e^{2\cdot 0} + \frac{1}{2} = \fbox{$c_{1} + 2c_{2}+\frac{1}{2} = -1$}  $$
>
>
>Mettiamo le due parti evidenziate a sistema:
>$$ \begin{cases}
>c_{1}+c_{2}+\frac{3}{4} =1 \\
>c_{1}+2c_{2}+\frac{1}{2} = -1
>\end{cases} 
>\Rightarrow \begin{cases}
>c_{1} = 2 \\
c_{2} = -\frac{7}{4}
>\end{cases}$$
>
>E sostituisco nell'integrale generale:
>$$ y(t) = 2e^t-\frac{7}{4}e^{2t}+\frac{t}{2}+\frac{3}{4} $$
>L'unica e sola soluzione del problema di Cauchy


# Problema di Cauchy in sistemi differenziali lineari

Come si scrive un problema di Cauchy in un [[Sistemi differenziali lineari|sistema differenziale lineare]]? 
Partiamo da un esempio:
>[!esempio]
>$$ y''(t) - 2y'(t) = t $$
>E diamo un generico problema di Cauchy
>$$ \begin{cases}
>y(t_{0}) = y_{0} \\
>y'(t_{0}) = v_{0}
>\end{cases} $$
>Trasformo le EDO in sistema:
>$$ \begin{cases}
> y_{1}(t) = y(t) \\
> y_{2}(t) = y'(t)
>\end{cases} \Rightarrow \begin{cases}
>y'(t) = y_{2}(t) \\
>y_{2}'(t) = 2y_{2}(t)+t 
>\end{cases}
>$$



>[!def]
>Dato $\mathbf{y}'(t) = A \cdot \mathbf{y(t)} + \mathbf{b}(t)\qquad n\times n$
>con $b_{j} : J \subseteq \mathbb{R} \to \mathbb{R}$
>
>Dati $t_{0} \in J, y_{0} \in \mathbb{R}^n$
>Chiamiamo problema di Cauchy:
>$$ \begin{cases}
>\mathbf{y'}(t) = A \cdot y'(t) + \mathbf{b}(t)  \\
>\mathbf{y}(t_{0}) = \mathbf{y}_{0}
>\end{cases}$$
>
>>[!esempio]
>>Al tempo $t_{0} = 0$ posizione $1$ e velocità nulla
>>$$ \begin{cases}
>>y_{1}'(t) = y_{2}(t) \\
>>y_{2}'(t) = 2y_{2}+t \\
>>y_{1}(0) = 1 \\
>>y_{2}(0) = 0
>>\end{cases} $$
>>$$
>>\mathbf{y}(t) = \begin{bmatrix}
>>y_{1}(t) \\
>>y_{2}(t)
>>\end{bmatrix}
>>\qquad
>>A = \begin{bmatrix}
>>0 & 1 \\
>>0 & 2
>>\end{bmatrix}
>>\qquad\mathbf{b}(t) = \begin{bmatrix}
>>0 \\
>>t
\end{bmatrix}$$
>> $$ t_{0} = 0\qquad y_{0} = \begin{bmatrix}
1 \\
0
\end{bmatrix} $$

>[!oss]
>In un problema di Cauchy di un sistema lineare avremo sempre derivate prime di ogni funzione.