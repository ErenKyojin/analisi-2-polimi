# Limiti per funzioni di due variabili

>[!def]
>$A \subseteq \mathbb{R}^2$ una funzione di due variabili a valori reali $f:A \to \mathbb{R}$ è una relazione che associa ad $(x,y) \in A$ un unico valore reale
> $$ \begin{align}
>f : A \subseteq \mathbb{R}^2 &\to \mathbb{R} \\
> (x,y) &\mapsto f(x,y)
>\end{align} $$ 


chiamiamo insieme o [[dominio]] di definizione il più grande insieme sul quale $f$ è definita.
$$ grafico(f) = \{(x,y,z) \in \mathbb{R}^3 : (x,y) \in A, z = f(x)\} \subseteq \mathbb{R}^3$$
Per ogni $k \in \mathbb{R}$ l'insieme di livello di $f$ al livello $k$ 
$$ I_{k} = \{(x,y) \in A \subseteq \mathbb{R}^2 : f(x,y) = k\} $$

>[!def] Definizione di limite
>Ripasso limiti 1 variabile:
>$$\begin{align}
>|x-x_{0}| < \delta &\iff (x_{0}- \delta; x_{0} + \delta) \\
>0 < | x - x_{0}| < \delta &\iff (x_{0}-\delta,x_{0}+\delta) \setminus \{x_{0}\} 
>\end{align}$$

>[!esempio]
>$f(x,y) = \frac{x^2-y^2}{x^2+y^2}\qquad dominio(f) = \mathbb{R}^2 \setminus \{(0,0)\}$
> $$ \lim_{ (x,y) \to (0,0) }  \frac{x^2 - y^2}{x^2 + y^2} $$


>[!def] 
>siano $A \subseteq \mathbb{R}^2$ aperto,$\mathbf{x}_{0} \in A$
> $$ f : A \setminus {\mathbf{x}_{0}} \to \mathbb{R} $$
> diciamo che $f$ tende al limite $l \in \mathbb{R}$ per $\mathbf{x}$ che tende a $\mathbf{x}_{0}$ e scriviamo
> $$ \lim_{ \mathbf{x} \to \mathbf{x}_{0} } f(\mathbf{x})  = l$$
> se per ogni $\varepsilon > 0$ esiste $\delta$ tale che se
>  $$ \mathbf{x} \in B_{\delta} (\mathbf{x}_{0}) \setminus \{\mathbf{x}_{0}\}\qquad \text{ allora }\quad \mid f(x) - l\mid < \varepsilon$$


>[!oss] parafrasando
>Per ogni $\varepsilon > 0$ esiste una palletta $B_{\delta}$  contenuta nel piano $x,y$ avente la proprietà che l'immagina tramite $f$ di $B_{\delta}(\mathbf{x}_{0}) \setminus \{\mathbf{x}_{0}\}$ si trova a distanza inferiore a $\varepsilon$ dal numero $l$


>[!oss]
>
>$$\begin{align}
\mathbf{x} \in B_{\delta}(x_{0}) \setminus \{\mathbf{x}_{0}\} &\iff 0 < dist(\mathbf{x, >\mathbf{x_{0}}}) < \delta \\
&\iff 0 < \sqrt{ (x-x_{0})^2 + (y-y_{0})^2 } < \delta
\end{align}$$
Si esclude il punto $\mathbf{x}_{0}$ nel quale $f$ potrebbe non essere definita

## non esistenza di un limite
>[!oss]
Per stabilire che un limite $2D$
 $$ \lim_{ \mathbf{x} \to \mathbf{x_{0}} }f(x)  $$ non esiste è sufficiente esibire due cammini che arrivino in $\mathbf{x_{0}}$ tale che i limiti $1D$ lungo i due cammini siano diversi. Questi cammini possono essere rette o altre curve.

# Calcolo dei limiti con coordinate polari
>[!esempio]
>$$ \lim_{ (x,y) \to (0,0) } \frac{ax^2+y}{x^2+y^2}  $$
>
>1. Calcolo i limiti 1D lungo gli assi
> $$
>\lim_{ x \to 0 } f(x,0) = \lim_{ y \to 0 } f(0,y) = 0
>$$
>==il limite candidato è $0$==
>2. scrivo $f$ in coordinate polari
> $$ \begin{align}
>g(r,0) &= f(r\cos \theta + r \sin \theta) =  \\
> &=\frac{2(r \cos \theta)^2 r \sin \theta}{r^2} = \\
> &=\frac{2r^3\cos^2 \theta \sin \theta}{r^2} = \\
 &=2r \cos^2 \theta \sin \theta
>\end{align} $$
>3. Cerca una $h(r)$ che dipende solo dalla cordinata radiale $r$ tale che
> $$\fbox{$\begin{align}&\mid g(r, \theta) - l\mid \leq h(r) \\
&\lim_{ r \to 0 } h(r) = 0\end{align}$}$$
>
>Esssendo in questo caso $l=0$
>$$ |g(r, \theta) - 0| = |g(r, \theta)| = |2 \pi \underbrace{ \cos^2 \theta \sin \theta }_{ \leq 1 }| \leq 2r \xrightarrow{r \to 0} 0 $$
>Quindi
>$$ \lim_{ (x,y) \to 0 } \frac{2x^2y}{x^2+y^2} = 0$$


>[!oss]
>Se dobbiamo calcolare il limite in un punto $\mathbf{x}_{0} = (x_{0},y_{0})$ diverso dall'origine vanno utilizzate le [[coordinate polari]] centrate intorno ad $\mathbf{x}_{0}$


>[!oss]
>Se non si tratta di un quoziente di polinomi può essere necessario utilizzare i limiti notevoli di analisi 1 in uno "step 0"
>
>>[!warning]
>>Non si possono applicare i limiti notevoli dopo essere passati alle coordinate polari.

