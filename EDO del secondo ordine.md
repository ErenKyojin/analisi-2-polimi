# [[EDO]] del secondo ordine


Prendiamo un esempio dalla fisica, presa una particella e definita la sua posizione $y(t)$, allora la sua velocità è $y'(t)$ e l'accelerazione è $y''(t)$.
Data poi la legge fondamentale della dinamica
$$ F = ma \Longrightarrow F = mf'' $$
Allora $$ my'' = F(t,y,y') $$
Che è una equazione differenziale ordinaria, di secondo ordine in quanto la derivata di ordine maggiore è la seconda.

In altri campi della fisica come termodinamica e fluidodinamica, si utilizzano [[EDO alle derivate parziali]]







# EDO del secondo ordine lineari

Hanno forma
$$ a(t)y''(t) + b(t)y'(t) + c(t)y(t) = f(t) $$
$a \neq 0, f$ definito forzante.

>[!esempio]
>```tikz
>\usepackage{circuitikz}
>\begin{document}
>\begin{circuitikz}[american, voltage shift=0.5]
>\draw (0,6)
>to[vsource, v=E] (0,0)
>to[short] (0,6) -- (2,6)
>to[R=R] (2,4)
>to[L=L] (2,2)
>to[C=C] (2,0)
>(2,0) -- (0,0);
>\end{circuitikz}
>\end{document}
>```
>
>Circuito RLC in serie, vogliamo determinare la carica $q(t)$ e la corrente $i(t) = q'(t)$.
>$$ \begin{align}
>&Li'(t) + Ri(t) + \frac{q(t)}{C} = E(t) \\
>&Lq''(t)+Rq'(t)+\frac{1}{C}q(t)=E(t) \\
>&Li''(t) + Ri'(t) + \frac{1}{C}i(t) = E'(t)
\end{align}$$


# Soluzioni di una EDO del secondo ordine lineare

Partiamo da un esempio
>[!esempio]
>$$ y'' = 0 $$
>Che ha come soluzione ogni equazione lineare $y = c_{1}t+c_{2}$ per ogni $c_{1},c_{2} \in \mathbb{R}$
>Ed, abbiamo quindi infinite soluzioni.

Per la precisione abbiamo $\infty^2$ soluzioni.
Per cercare l'integrale generale, ossia la struttura di ogni soluzione, dobbiamo capire il perchè queste equazione siano dette lineari.
Vediamo il primo membro della generica EDO del secondo ordine lineare come un operatore
$$ y \mapsto \fbox{$a \frac{d^2}{dt^2}+b \frac{d}{dt} + c$} \mapsto ay'' + by'+cy $$
$$y \mapsto L \mapsto ay''+by'+cy$$
Proprietà importante di $L$ è la linearità, ossia $L(c_{1}y_{1}+ c_{2}y_{2}) = c_{1}L(y_{1}) + c_{2}L(y_{2})$, che ci fornisce il [[principio di sovrapposizione]]

## Caso omogeneo
$Ly = 0 \Leftrightarrow ay'' + by' + cy = 0$
Quindi ogni combinazione lineare delle soluzioni è a sua volta soluzione, ossia l'insieme $S$ delle soluzioni forma uno [[spazio vettoriale]], di dimensione uguale all'ordine dell'equazione ([[teorema di struttura]]).

>[!esempio]
>$$ y'' + 4y = 0 $$
>verifichiamo che l'integrale generale è
>$$ \begin{align}
>&y(t) = C_{1} \cos 2t + C_{2}\sin 2t\quad \forall C_{1}, C_{2} \in \mathbb{R} \\
> \\
>&y_{1}(t) = \cos 2t &&y_{2}(t)=\sin 2t\\
>&y_{1}(t)' = -2 \sin 2t &&y_{2}(t)'=2\cos 2t\\
>&y_{1}(t)'' = -4 \cos 2t &&y_{2}''(t) = -4 \sin 2t
>\end{align}$$ 
>Sostituiamo nell'equazione di partenza.
>$$ -4\cos 2t + 4\cos 2t  = 0 \quad\forall t \in \mathbb{R}$$
>Verificato quindi $y_{1}$ è soluzione.
> $$ -4\sin 2t + 4\sin 2t = 0\quad \forall t \in \mathbb{R}$$
> Quindi anche $y_{2}$ è soluzione, verifichiamo quindi che il loro rapporto non sia costante:
> $$ \frac{\sin 2t}{\cos 2t} = \tan 2t$$
> Non costante.

## Caso completo o non omogeneo
$$ a(t)y''+b(t)y'+c(t)y = f(t) $$

In questo caso il [[principio di sovrapposizione]] si può applicare solo se una delle due soluzioni è dell'omogenea, ossia

>[!Esempio] 1
>$$ \begin{align}
>&y_{0} \text{ soluzione di } Ly = 0  \\
>&Ly_{0} = 0 \\
>\\
>&y_{p} \text{ soluzione di } Ly = f \\
>&Ly_{p} = f
>\end{align} 
>$$
>E quindi
>$L(y_{0} + y_{P}) = Ly_{0} + Ly_{P} = 0 + f = f$

Alternativamente, avendo due soluzioni non omogenee, possiamo trovare l'omogenea tramite la differenza
>[!esempio] 2
>$$ \begin{align}
>&y_{1} \text{ soluzione di } Ly = f  \\
>&Ly_{1} = f \\
>\\
>&y_{2} \text{ soluzione di } Ly = f \\
>&Ly_{2} = f
>\end{align} 
>$$
>E quindi
>$L(y_{1} - y_{2}) = Ly_{1} - Ly_{2} = f - f = 0$

QUINDI, data una soluzione qualsiasi $y_{P}$, tutte le altre soluzioni è della forma $y = y_{0} + y_{P}$, si arriva quindiu al [[teorema di struttura#Teorema di struttura per le equazioni complete]]


## Caso a coefficienti costanti
$$ ay'' + by' + cy = 0 $$
con $a,b,c \in \mathbb{R}$. Dal [[teorema di struttura]] per trovare ogni soluzione è sufficiente trovare due soluzioni linearmente indipendenti, ossia non multiple l'una dell'altra.

>[!esempio]
>$$ y'' + 4y' +3y = 0 $$
>Possiamo pensare di trovare funzioni la cui derivata è proporzionale alla funzione stessa, ossia $e^{\lambda t}$
>$$ \begin{align}
>&y = e^{\lambda t} \\
>&y' = \lambda e^{\lambda t}  \\
>&y'' = \lambda^2 e^{\lambda t}
>\end{align} $$
>
>Sostituiamo:
>$$ e^{\lambda t}(\lambda^2+4\lambda+3) = 0 $$
>Che è uguale a $0$ se e solo se:
>$$ \lambda^2 + 4\lambda + 3 = 0 $$
>Equazione di secondo grado in lambda le cui radici sono $\lambda_{1} = -1, \lambda_{2} = -3$, che ci danno come risultato $y_{1}, y_{2}$ rispettivamente.
>Per verificare che sono indipendenti basta dividerli tra loro:
>$$ \frac{y_{1}(t)}{y_{2}(t)} = \frac{e^{-t}}{e^{-3t}} = e^{2t}$$

Quindi data un'equazione lineare omogenea del secondo ordine a coefficienti costanti:
$$ ay'' + by' + cy = 0 $$
Le soluzioni si trovano attraverso la formula $$(a \lambda^2 + b \lambda + c) = 0$$
Questo polinomio è detto [[polinomio caratteristico]] e si chiama $P(\lambda)$, l'equazione $P(\lambda) = 0$ è detta invece [[equazione caratteristica]], trovati $\lambda_{1}, \lambda_{2}$, attraverso il teorema di struttura
$$ y(t) = C_{1}e^{\lambda_{1}t}+C_{2}e^{\lambda_{2}t} $$

Ovviamente in questi casi abbiamo ipotizzato di avere due $\lambda$ distinti, ossia un $\Delta$ positivo.

### Caso con $\Delta < 0$ 
Dall'[[equazione caratteristica]] otteniamo $\lambda_{1},\lambda_{2}$ complessi, che usiamo per trovare soluzioni reali tramite $u_{1}$ e $u_{2}$
$$ \lambda_{1} = \alpha + i\beta\qquad \lambda_{2} = \alpha - i\beta$$
E l'integrale generale è:
$$ y(t) = e^{\alpha t} (C_{1} \cos(\beta t)+ C_{2} \sin(\beta t)) $$
>[!esempio]
>$$ y''+2y'+10y=0  \longrightarrow \lambda^2+2\lambda + 10 = 0 $$
>$\Delta = -36 < 0 \Rightarrow \lambda_{1,2} = -1 \pm 3i$
>$$\begin{align}
>&y_{1}(t) = e^{(-1+3i)t} \qquad &&y_{2}(t) = e^{(-1-3i)t} \\
>&y_{1}= e^{-t}(\cos 3t + i \sin 3t) &&y_{2}(t) = e^{-t}(\cos 3t - i \sin 3t)
>\end{align}$$
>
>Per passare alla versione reale di queste due funzioni, utilizziamo due funzioni $u_{1}, u_{2}$ che sfruttano la linearità di queste due soluzioni per tornare nel dominio reale.
>
>$$ \begin{align}
>&u_{1}(t) = \frac{y_{1}(t) + y_{2}(t)}{2} = e^{-t} \cos 3t \\
>&u_{2}(t) = \frac{y_{1}(t) - y_{2}(t)}{2i} = e^{-t} \sin 3t
>\end{align} $$
>Quindi $u_{1},u_{2}$ soluzioni reali linearmente indipendenti ($\frac{u_{1}}{u_{2}} = \cot 3t$)

# Problema di Cauchy
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


