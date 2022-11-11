
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



Possiamo dare una definizione informale di parametrizzazioni equivalenti come due parametrizzazioni che hanno il medesimo sostegno percorso lo stesso numero di volte (eventualmente in verso opposto). Più formalmente:

>[!def]
>due parametrizzazioni continue $\mathbf{r}(t) : I \to \mathbb{R}^3, \mathbf{v}(s) : J \to \mathbb{R}^3$
>si dicono equivalenti se esiste $\phi(s) : J \to I$ continua e **biunivoca** tale che:
> $$ \mathbf{v} (s) = \mathbf{r}(\phi(s)) = \mathbf{r} \circ \phi(s) : J \to \mathbb{R}^3 $$

Nell'esempio: 
$\mathbf{v}(s) = \mathbf{r} (2s) \quad s=\frac{t}{2} \iff t = 2s$ cioè $\phi(s) = 2s$
$\mathbf{w}(s) = \mathbf{r}(-s)$ $s = -t \iff t = -s$ cioè $\phi(s) = -s$

>[!oss]
>$\phi$ biunivoca $\iff \phi$ monotona
> - crescenete $\implies$ stesso verso
> - decrescente $\implies$ verso opposto


## Curve regolari
Data una curva nel piano o nello spazio come determino in ogni punto la direzione tangente alla curva?
$$ \begin{pmatrix}
x_{1} \\
x_{2}
\end{pmatrix} = 

\begin{pmatrix}
r_{1}(t) \\
r_{2}(t)
\end{pmatrix}$$
Per ogni $t_{1}$ la direzione tangente alla curva nel punto $\mathbf{r}(t)$ è:
$$ \begin{bmatrix}
r_{1}'(t) \\
r_{2}'(t)
\end{bmatrix} $$


>[!esempio]
>$I = \mathbb{R}$ $$
>\mathbf{r}(t) = \begin{bmatrix}
> r_{1}(t) \\
r_{2}(t)
>\end{bmatrix} = \begin{bmatrix}
t \\
t^2
\end{bmatrix}$$
Dico che la direzione tangente alla curva nel punto $$\mathbf{r}(t) = \begin{bmatrix}
>r_{1}'(t) \\
>r_{2}'(t)
>\end{bmatrix} = \begin{bmatrix}
1  \\
2t
\end{bmatrix}$$
>
> $t=0\quad \mathbf{r}(0) = [0\quad 0]^T \implies \mathbf{r}'(0)= [1 \quad 0]^T$ 
> $t = -1\quad \mathbf{r}(-1)=[-1\quad 1]^T \implies \mathbf{r}'(-1)=[1\quad 2]^T$
> $t=2\quad \mathbf{r}(2) = [2\quad 4]^T \implies \mathbf{r}'(2)=[2\quad 4]^T$
> Ovviamente dobbiamo traslare al punto $t$ in quanto la soluzione è il vettore applicato nell'origine
>
>>[!oss]
>>la direzione tangente ha il verso uguale a dove si sta spostando il punto, inoltre il modulo non è di nostro interesse.


Inoltre $r_{1},r_{2}$ devono essere almeno #derivabili

>[!esempio]
>$I = \mathbb{R}$
>$$ \mathbf{r}(t) = \begin{bmatrix}
>r_{1}(t) \\
>r_{2}(t)
\end{bmatrix} =
\begin{bmatrix}
>t^3 \\
>t^2
\end{bmatrix}$$
>$r_{1},r_{2}$ derivabili
>$$ \mathbf{r}'(t) = \begin{bmatrix} 
>r_{1}'(t) \\
>r_{2}'(t)
>\end{bmatrix} =
>\begin{bmatrix}
>3t^2 \\
>2t
>\end{bmatrix}$$
>
> Disegno il sostegno:
> $$ y(t) = t^2 = (t^3)^{2/3} = x^{2/3}$$
Che non è derivabile in $0$ (punto cuspide)
>$$ \mathbf{r}'(0)=\begin{bmatrix}
0 \\
0
\end{bmatrix} $$
Essendo il grafico di una funzione continua rientra nell'esempio 3, una possibile parametrizzazione è anche
> $$ \mathbf{v}(s) = \begin{bmatrix}
>s \\
>s^{2/3}
>\end{bmatrix} $$

# Lunghezza di una curva
Siano $[a,b] \subseteq \mathbb{R}$ limitato e $\mathbf{r} : [a,b] \to \mathbb{R}^3$ la parametrizzazione di una curva regolare avente sostegno $\gamma$ allora
$$ lunghezza(\gamma) = \int_{a}^b \! \,||\mathbf{r}'(t)|| \mathrm{d}t  $$

>[!teorema] Invarianza della lunghezza di una curva per riparametrizzazioni
>$[a,b] \subseteq \mathbb{R}$ limitato
>$\mathbf{r} : [a,b] \to \mathbb{R}^3$ parametrizzazione di una curva regolare di sostegno $\gamma$
>$\mathbf{v} : [c,d] \to \mathbb{R}^3, \mathbf{v}(s) = \mathbf{r}(\phi(s))$ parametrizzazione equivalente di sostegno $\delta$
>allora $lunghezza(\gamma) = lunghezza(\delta)$
>
>>[!dim] #dim 5
>>$lunghezza(\gamma) := \int_{a}^b \! ||\mathbf{r}'(t)||\, \mathrm{d}t$
>>$lunghezza(\delta) := \int_{c}^d \! ||\mathbf{v}'(s)||\, \mathrm{d}t$
>>Ricordando che
>>$$ \mathbf{v}(s) = \begin{bmatrix}
>>v_{1}(s) \\
>>v_{2}(s) \\
>>v_{3}(s)
>>\end{bmatrix} = \mathbf{r}(\phi(s))=\begin{bmatrix}
>> r_{1}(\phi(s)) \\
>> r_{2}(\phi(s)) \\
>> r_{3}(\phi(s))
>>\end{bmatrix}$$
>>Allora
>>$$ \mathbf{v}'(s) = \begin{bmatrix}
>>r_{1}'(\phi(s)) \phi'(s) \\
>>r_{2}'(\phi(s)) \phi'(s) \\
>>r_{3}'(\phi(s)) \phi'(s)
>>\end{bmatrix} $$
>>$$ ||\mathbf{v}'(s) || = ||\mathbf{r}'(\phi(s))'||\cdot|\phi'(s)| $$
>>Allora la lunghezza è:
>>$$lunghezza(\delta)= \int_{c}^d \! ||\mathbf{r}'(\phi(s))|| \cdot |\phi'(s)|\, \mathrm{d}s $$
>>Pr definiziano di [[parametrizzazione]] equivalente $\phi$ è biunivoca, cioè sempre crescente o sempre decrescente.
>>1. ---
>>Prendiamo il caso crescente, quindi $\phi'(s) \geq 0 \forall s \in [c,d] \implies Lunghezza(\delta) =$
>>$$ = \int_{c}^d \! ||\mathbf{r}'(\phi(s))|| \fbox{$\phi'(s)\, \mathrm{d}s$}_{= \mathrm{d}t}  $$
>>Cambio di variabile nell'integrale $t=\phi(s), \mathrm{d}t = \phi'(s) \mathrm{d}s$
>>$$ \implies \int_{a}^b \! ||\mathbf{r}'(t)||\, \mathrm{d}t   = lunghezza(\gamma)$$
>>2. ---
>>Prendiamo il caso decrescente, quindi $\phi'(s) \leq 0 \forall s \in [c,d]$ allora $$\begin{align}
>>lunghezza(\delta) &= \int_{c}^d \! ||\mathbf{r}'(\phi(s))|| \cdot |\phi'(s)|\, \mathrm{d}s \\
>> &=\int_{c}^d \! ||\mathbf{r}'(\phi(s))||\cdot |-\phi'(s)|\, \mathrm{d}s 
>>\end{align}$$
>>
>>$t = \phi(s), \mathrm{d}t = \phi'(s)\mathrm{d}s$
>>dato che $\phi$ è decrescente: $\phi(c) = b \quad \phi(d) = a$
>>$$ lunghezza(\delta) = \int_{b}^a \! ||\mathbf{r}'(t)||\, (-\mathrm{d}t) = \int_{a}^b \! ||\mathbf{r}'(t)|| \, \mathrm{d}t = lunghezza(\gamma)   $$


>[!oss]
>Essendo $$ \begin{align}
>&r_{1},r_{2},r_{3} &\in C^1([a,b]) \\
>&v_{1},v_{2},v_{3} &\in C^1([a,b]) \\
>&\mathbf{v}  = \mathbf{r} \circ \phi
>\end{align} $$
>Allora $\phi : [c,d] \to [a,b]$ di [[classe C|classe]] $C^1$


# Curva regolare a tratti
>[!def]
>Si dice regolare a tratti una curva $\mathbf{r} : I \to \mathbb{R}^3$ tale che:
>1. $\mathbf{r}$ continua in $I$
>2. Ad eccezzione di un numero finito di valori $a < t_{1} < t_{2} < \ldots < t_{k} < b$ la curva è regolare


## Lunghezza di una curva regolare a tratti:
$$ lunghezza(\gamma) = \int_{a}^{t_{1}} \! ||\mathbf{r}'(t)|| \, \mathrm{d}t + \int_{t_{1}}^{t_{2}} \! ||\mathbf{r}'(t)||\, \mathrm{d}t + \ldots + \int_{t_{k}}^{b} \!||\mathbf{r}'(t)|| \, \mathrm{d}t   $$