>[!def]
>Sia $A \subseteq \mathbb{R}^2$ aperto
>$f : A \to \mathbb{R}$ derivabile in $(X_{0},y_{0}) \in A$
>Se $\nabla f (x_{0},y_{0}) = \begin{bmatrix}0 & 0\end{bmatrix}^T$ allora $(x_{0},y_{0})$ è detto punto critico o punto stazionario

>[!def]
>Un punto critico di $f$ che non è punto estremale di $f$ è detto punto di sella


```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[colormap/viridis, hide axis]
\addplot3[
	surf,
	samples= 18,
	domain= -2:2
]
{x*sin(deg(y))};
\addlegendentry{\(x * \sin y\)};
\end{axis}

\end{tikzpicture}
\end{document}
```

In pratica se cerco i punti estremavi di una funzione $f$ in un insieme $A$ aperto
- Se $f$ è derivabile in tutto A: determino i punti critici di $f$ in $A$ e poi stabilisco quali sono massimo minimo e selle.
- Se $f$ ha punti di non derivabilità li includo tra i candidati

>[!oss]
> Se $f$ è anche differenziabile li includo tra i candidati
> 1. Il piano tangente al grafico di $f$ in $(x_{0},y_{0},f(x_{0},y_{0}))$ è orizzontale
> 	$$ z = f(x_{0},y_{0}) + \underbrace{ \langle \nabla f(x_{0},y_{0}), \begin{bmatrix}
>x-x_{0} \\
y-y_{0}
\end{bmatrix}\rangle }_{ = 0 } $$
>
>2. $\forall \mathbf{v} \subseteq \mathbb{R}^2\quad ||\mathbf{v}|| = 1$ si ha 
> $$ \frac{ \partial f }{ \partial \mathbf{v} } (x_{0},y_{0}) = \langle \nabla f(x_{0},y_{0}), \mathbf{v}\rangle = 0 $$


>[!esempio]
>Determinare tutti i punti critici di
>
$$ f(x,y) = 3x^2 + y^2 - x^3y $$
>
>
>```tikz
>\usepackage{pgfplots}
>\begin{document}
>\begin{tikzpicture}
>\begin{axis}[colormap/viridis]
>\addplot3[
>	surf,
>	samples=16,
>	domain = -5:5
>	]
>{3*x^2 + y^2 - x^3 *y};
>\end{axis}
>\end{tikzpicture}
>\end{document}
>```
>
>Ricaviamo il sistema in generale non lineare:
>$$ 
>\begin{cases}
>6x - 3x^2y = 0 \\
>2y - x^3 = 0
>\end{cases}
>$$
>ad occhio $(0,0)$ è soluzione:
>$$ \begin{align}
>&\begin{cases}
>3x(2-xy) = 0 \\
>y = \frac{x^3}{2}
>\end{cases} \\
>&\begin{cases}
>y= \frac{2}{x} \\
>y =\frac{x^3}{2} 
>\end{cases} \implies \begin{cases}
>y = \frac{2}{x} \\
>x^4 = 4
>\end{cases} \\
>&\begin{cases}
>x = \pm \sqrt{ 2 } \\
>y = \frac{2}{x}
>\end{cases}
>\end{align}$$
>
>Quindi grazie al [[teorema di fermat]] ci riconduce ai tre punti critici
>
>
> $$ (0,0)\quad (\sqrt{ 2 },\sqrt{ 2 })\quad(-\sqrt{ 2 }, \sqrt{ 2 }) $$


# Classifficazione di punti critici
Criterio hessiana:
>[!teorema]
>$A \subseteq \mathbb{R}^2$ aperto
>$f \in C^2(A)$ [[classe C]]
>$x_{0} = (x_{0},y_{0}) \in A$ punto critico per $f$ ($\nabla f(\mathbf{x_{0}}) = \mathbf{0}$)
>
>Denotiamo $q$ la forma quadratica indotta dalla [[matrice hessiana]] $H_{f}(\mathbf{x_{0}})$ cioè
>$$ q(h_{1},h_{2}) = \begin{bmatrix}
> h_{1} & h_{2}
\end{bmatrix} H_{f}(\mathbf{x_{0}}) \cdot \begin{bmatrix}
h_{1} \\
h_{2}
\end{bmatrix} $$
Allora:
>1. Se $q$ è definita positiva $\implies \mathbf{x_{0}}$  è punto di min
>2. se $q$ è definita negativa $\implies \mathbf{x_{0}}$ punto di max
>3. se $q$ è indefinita $\implies \mathbf{x_{0}}$ punto di sella
>
>>[!dim] #dim 9
>>Essendo $\nabla f (\mathbf{x_{0}}) = \mathbf{0}$ la formula di taylor al secondo ordine diventa:
>> $$ f(\mathbf{x_{0}}) = f(\mathbf{x_{0}}) + \frac{1}{2}q(\mathbf{h}) + o(||\mathbf{h}||^2) $$
>> 1. $q$ definita positiva, cioè $q(\mathbf{h}) > 0\quad \forall \mathbf{h}$
>> 	$\implies f(\mathbf{x_{0}} + \mathbf{h}) > f(\mathbf{x_{0}}) + o (||\mathbf{h}||^2)$
>> 	$\implies$ in una pialletta $f(\mathbf{x_{0}}+\mathbf{h}) > f(\mathbf{x_{0}})$
>> 	$\implies \mathbf{x_{0}}$ punto di minimo locale
>>
>>2. $q$ definita negativa $q(\mathbf{h}) < 0\quad\forall \mathbf{h} \implies f(\mathbf{x_{0}}+\mathbf{h}) < f(\mathbf{x_{0}}) + o(||\mathbf{h}||^2)$
>>3. $q$ indefinita, cioè esiste $\mathbf{h}_{p}, \mathbf{h}_{n}$ tale che
>> $$ q(\mathbf{h}_{p}) \quad e \quad q(\mathbf{h}_{n}) $$
>> $$ \implies \begin{align}
>>&f(\mathbf{x}_{0} + \mathbf{h}_{p}) > f(\mathbf{x_{0}}) + o(||\mathbf{h}_{p}||^2) \\
>>&f(\mathbf{x_{0}} + \mathbf{h}_{n}) < f(\mathbf{x_{0}}) + o(||\mathbf{h}_{n}||^2)
>>\end{align}
>>\implies \mathbf{x_{0}} \text{ sella} $$
>
>>[!warning]
>>Se $q$ è semidefinita il criterio della matrice hessiana non da alcuna informazione, quindi può succedere qualsiasi cosa, infatti esiste $\mathbf{h}_{0} + 0$ tale che $q(\mathbf{h}_{0}) = 0$
>>$\implies f(\mathbf{x_{0}}+\mathbf{h}_{0}) = f(\mathbf{x_{0}})+o(||\mathbf{h}_{0}||^2)$
>>Il resto non è più trascurabile

## Come applicare il criterio hessiano:
1. $\det(H_{f} (x_{0},y_{0})) > 0$ e $\frac{ \partial^2 f }{ \partial x^2 }(x_{0},y_{0}) > 0 \implies min$
2. $\det(H_{f}(x_{0},y_{0})) > 0$ e $\frac{ \partial^2 f }{ \partial x^2 }(x_{0},y_{0}) < 0 \implies max$
3. $\det(H_{f}(x_{0},y_{0})) < 0 \implies$ sella
>[!warning]
>$\det(H_{f}(x_{0},y_{0})) = 0$ precedere in altro modo


>[!esempio]
>$f(x,y) = 3x^2 + y^2 - x^3y$
>voglio trovare i punti di estremo locale di $f$ in $\mathbb{R}^2$
>Per il [[Teorema di fermat#2D]] i punti di estremo vanno ricercati tra i punti critici.
>
> I punti critici li abbiamo calcolati in un esempio precedente e sono:
> $(0,0),\quad (\sqrt{ 2 },\sqrt{ 2 }),\quad(-\sqrt{ 2 },-\sqrt{ 2 })$
> $$ \begin{align}
>&H_{f}(x,y) = \begin{bmatrix}
> 6 -6xy & -3x^2 \\
>-3x^2 & 2
>\end{bmatrix}  \\
>&H_{f}(0,0) = \begin{bmatrix}
>6 & 0 \\
0 & 2
\end{bmatrix} \\
>&H_{f}(\sqrt{ 2 },\sqrt{ 2 }) = 
\begin{bmatrix}
> -6 & 6 \\
-6 & 2
\end{bmatrix}
>\end{align}$$
>
>$\det H_{f}(0,0) = 12 > 0, \frac{ \partial^2 f }{ \partial x^2 }(0,0) = 6 > 0 \implies min$
>$\det H_{f}(\sqrt{ 2 },\sqrt{ 2 }) = -48 < 0 \implies$ sella
In conclusione L'unico punto di estremo è l'origine che è anche punto di minimo locale

Domanda aggiuntiva (0,0) minimo globale?
Considerando la restrizione di $f$ alla retta $y = x$
$$ \begin{align}
f(x,y) &= 3x^2 + y^2 - x^3y \\
g(x) &= f(x,x) = 4x^2 - x^4 \\
\lim_{ x \to \infty } f(x,x) &= 4x^2 - x^4 = -\infty
\end{align} $$


## Indagine diretta $\det = 0$

Cosa fare quando troviamo un punto ciritico della funzione $f$ ma il [[criterio dell'hessiana]] non si applica, ossia quando $\det H_{f}(\mathbf{x_{0}}) = 0$
($\nabla f (\mathbf{x_{0}}) = \mathbf{0}, \mathbf{x_{0}} \in A$ aperto)

>[!esempio]
>determinare i punti di estremo
>$$ f(x,y) = x^4 - 6 x^2 y^2 + y^4 $$
>e classificarli
>$f$ definita in $\mathbb{R}^2$ e la [[classe C]]$^2(\mathbb{R}^2)$
>Cerco i punti di estremo sul dominio di $f$ cioè $\mathbb{R}^2$. Essendo aperto, per il [[Teorema di fermat]] i punti di estremo vanno ricercati tra i punti critici.
>L'unico punto critico è l'origine $(0,0)$
>Ma il $\det H_{f}(0,0) = 0 \implies$ non posso applicarne il criterio .
>
>La strategia per evitare il problema è di fissare una direzione, studiamo quindi
>$y=0 \quad f(x,0) = x^4$
>$y = x\quad f(x,x) = xˆ4 - 6x^4 + x^4 = -x^4$
>Globalmente $(0,0)$ è una sella per $f$, $f$ non ha punti di estremo locali
>
>```tikz
>\usepackage{pgfplots}
>\begin{document}
>\begin{tikzpicture}
>\begin{axis}[colormap/viridis]
>\addplot3[
>	surf,
>	samples = 16,
>	domain = -5:5] 
>	{x^4 - 6 *x^2 *y^2 + y^4 };
>\end{axis}
>\end{tikzpicture}
>\end{document}
>```

Alternativamente posso studiare il segno di $f$ attorno al punto candidato

