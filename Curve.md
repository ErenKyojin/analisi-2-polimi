
# Curve nel piano e nello spazio

Il sostegno della curva è la traccia nel piano o nello spazio lasciata dal punto.
La parametrizzazione di una curva piana sono due funzioni di $t$ (In generale per $\mathbb{R}^n$ sono $n$ funzioni di $t$)

>[!def]
>Una curva nello spazio è definita da:
>- 3 funzioni **continue**:
> $$ \begin{align}
> t \in I \subseteq \mathbb{R} \mapsto \begin{pmatrix}
> r_{1}(t) \\
>r_{2}(t) \\
>r_{3}(t)
>\end{pmatrix} = \mathbf{r}(t) \in \mathbb{R}^3
>\end{align} $$
è la parametrizzavi one della curva
>
> - l'immagine dell'intervallo $I$ tramite $\mathbf{r} = [r_{1}\quad r_{2}\quad r_{3}]^T$
> 	$\gamma = \{(x_{1},x_{2},x_{3}) \in \mathbb{R}^3 : (x_{1},x_{2},x_{3})=r_{1}(t),r_{2}(t),r_{3}(t)$ per qualche $t \in I\}$
> 	è il **sostegno** della curva e coincide con il percorso della curva

>[!oss]
>Come caso particolare quando $r_{3}(t) = 0 \forall t$ otteniamo una curva piana



>[!esempio]
>Circonferenza nel piano
>$I = [0,2\pi)$ $$\mathbf{r(t)} = \begin{pmatrix}
> r_{1}(t) \\
>r_{2}(t)
>\end{pmatrix} = \begin{pmatrix}
> R \cos(t) \\
R\sin(t)
\end{pmatrix}$$ 
>il sostegno di $\mathbf{r}$ è la circonferenza centrata nell'origine di raggio $R$
> $$ \gamma = \{(X_{1},x_{2}) \in \mathbb{R}^2 : \text{esiste }t \in [0,2\pi) t.c. \begin{pmatrix}
> x_{1} \\
>x_{2} 
\end{pmatrix} = \begin{pmatrix}
> R\cos t \\
R\sin t
\end{pmatrix}\} $$
>
>
>
>>[!oss]
>>Il sostegno non è il grafico di una funzione

>[!esempio]
>$I = [0,2\pi)$ 
>$$ \mathbf{r}(t) = \begin{pmatrix}
>r_{1}(t) \\
>r_{2}(t)
>\end{pmatrix} =
>\begin{pmatrix}
> a\cos t \\
b \sin t
\end{pmatrix}$$
Il sostegno è un ellisse che passa per $(0,b)$ e $(a,0)$

>[!oss]
>Se $f : I \subseteq \mathbb{R} \to \mathbb{R}$ continua $\implies$ il suo grafico è il sostegno di una curva piana

Partiamo da un esempio
$$ f(x) = \frac{x^2}{4}, x \in [-3,3] $$
$$\gamma = \left\{ (x,y) \in \mathbb{R}^2 : x \in [-3,3], y=\frac{x^2}{4} \right\}$$
Vogliamo parametrizzare questo sostegno con $t$ ed il modo più semplice è ponendo $t = x$
$$ \mathbf{r}(t) = \begin{pmatrix}
r_{1}(t) \\
r_{2}(t)
\end{pmatrix}  = 
\begin{pmatrix}
t \\
\frac{t^2}{4}
\end{pmatrix}\qquad t\in[-3,3]$$
Per una generica $f$ continua:
$$ \mathbf{r}(t) = \begin{pmatrix}
r_{1}(t) \\
r_{2}(t)
\end{pmatrix} = \begin{pmatrix}
t \\
f(t)
\end{pmatrix}\qquad t \in I$$
>[!oss]
>Nessuna ipotesi sull'[[intervallo]] $I$

>[!oss]
>Il sostegno è univocamente determinato dalla [[parametrizzazione]]
>