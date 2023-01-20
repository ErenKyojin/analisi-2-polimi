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
$$ y \mapsto \fbox{$a \frac{d^2}{dt^2}y+b \frac{d}{dt}y + c$} \mapsto ay'' + by'+cy $$
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

### caso con $\Delta >0$

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

### caso $\Delta = 0$
Possiamo trovare solo una soluzione, $\lambda_{1} = \lambda_{2} = \lambda$, e quindi
$$ \begin{align}
& y_{1}(t) = Ce^{\lambda t} \\
& y_{2}(t) = ?
\end{align} $$
Per utilizzare il principio di sovrapposizione per determinare la soluzione generica non ci basta $y_{1}$, abbiamo anche bisogno di un altra soluzione linearmente indipendente.
Cerchiamo una funzione $C(t) : y_{2} = C(t)e^{3t}$
$y'_{2}(t) = e^{3t}[C'(t) + 3C(t)]$
$y_{2}''(t) = e^{3t}[C''(t)+6C'(t)+9C(t)]$
$$ \begin{align}
&y'' -6y' + 9y = 0 \\
&C''(t) = 0 \\
&\Rightarrow C'(t) = C_{1} \\
&\Rightarrow C(t) = C_{1}t + C_{2}
\end{align} $$
Di cui la più semplice è $C_{1}=1, c_{2}=0$ ossia $C(t) = t$ e quindi l'integrale generale è:
$$ y(t) = C_{1}e^{\lambda t} + C_{2}te^{\lambda t}$$

>[!TLDR] 
>
>Discriminante | radici di $P(\lambda)$ | $y_{1}(t)$ | $y_{2}(t)$
> -| -|-|-|
> $\Delta>0$ | $\lambda_{1} \neq \lambda_{2},\quad\lambda_{1,2} \in \mathbb{R}$ | $e^{\lambda_{1}t}$| $e^{\lambda_{1}t}$
> | $\Delta = 0$| $\lambda_{1} = \lambda_{2}\quad\lambda_{1,2} \in \mathbb{R}$ | $e^{\lambda_{1}t}$| $te^{\lambda_{2}t}$
> | $\Delta < 0$| $\lambda_{1,2} = \alpha + i \beta,\quad \lambda_{1,2} \in \mathbb{C}$ | $e^{\alpha t} \cos \beta t$ | $e^{\alpha t} \sin \beta t$


Per ottenere una soluzione specifica dobbiamo, come al solito, risolvere il [[Problema di Cauchy]], ed è quindi richiesto sapere la situazione iniziale.