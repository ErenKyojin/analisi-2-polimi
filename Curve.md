
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


Il viceversa non è vero, esistono infinite parametrizzazioni associate al medesimo sostegno

>[!esempio]
>Riprendiamo il primo esempio
> $$ \begin{cases}
> r_{1}(t) = R \cos t \\
> r_{2}(t) = R \sin t
>\end{cases} \qquad t\in [0, 2\pi)$$
>Parametrizzazioni diverse, aventi lo stesso sostegno:
>
> $$ \begin{cases}
> v_{1}(s) = r_{1}(2s) = r\cos (2s) \\
> v_{2}(s) = r_{2}(2s) = r \sin(2s)
>\end{cases} \qquad s=\frac{t}{2}, s \in [0, \pi)$$
>è una parametrizzazione più rapida, il punto si muove il doppio più velocemente.
>
> $$ \begin{cases}
> w_{1}(s) = r_{1}(-s) = R \cos(-s) = R\cos(s) \\
> w_{2}(s) = r_{2}(-s) = R \sin(-s) = -R \sin(s)
>\end{cases} \quad s=-t, s \in (-2\pi,0]$$
> 
> Con tutte queste parametrizzazioni otteniamo sempre la stessa circonferenza, quello che cambia sono velocità (e verso) di percorrenza


>[!warning] Attenzione
> $$ \begin{cases}
> z_{1}(s) = R \cos (2s) \\
> z_{2}(s) = R \sin (2s)
>\end{cases}\qquad s = (-2\pi,0] $$
> In questo caso facciamo il giro due volte! Non va bene, bisogna considerare la parametrizzazione a "parità" di giri. Non è la stessa curva di prima



Possiamo dare una definizione informale di parametrizzazioni equivalenti come due parametrizzazioni che hanno il medesimo sostegno percorso lo stesso numero di volte.
Eventualmente in verso opposto



