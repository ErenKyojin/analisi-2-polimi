```mermaid
graph LR
	A[Derivabilità e </br> differenziabiltà] --> B[ottimizzazione </br> libera] --> C[ottimizzazione </br> vincolata]
```

# Derivabilità e differenziabilità


>[!multi-column]
>
>>[!esempio]
>>$$ hp: f \text { differenziabile in } \mathbf{x}_{0} $$
>>$$ f(\mathbf{x}_{0} + h) = f(\mathbf{x}_{0}) + \nabla \langle f(\mathbf{x}_{0}), \mathbf{x} - \mathbf{x}_{0}\rangle + o(||\mathbf{h}||)  $$
>>$$ f(\mathbf{x}) = f(\mathbf{x}_{0}) + \langle\mathbf{x}-\mathbf{x}_{0}\rangle + o (||\mathbf{x} - \mathbf{x}_{0}||) $$
>>piano tangente $z = f(\mathbf{x}_{0}) + \langle \nabla f(\mathbf{x_{0}}), \mathbf{x-\mathbf{x_{0}}}\rangle$
>
>>[!esempio]
>>$$ hp: f \text{ derivabile in } x_{0} $$
>>$$ f(x_{0}+h) = f(x_{0}) + f'(x_{0})h + o(|h|) $$
>>$$ f(x) = f(x_{0}) + f'(x_{0})(x-x_{0}) + o(|x-x_{0}|) $$
>>retta tangente $y = f(x_{0}) + f'(x_{0})(x-x_{0})$



## Derivate parziali e gradiente
>[!def]
>$A \subseteq \mathbb{R}^2$ aperto, $(x_{0},y_{0}) \in A\quad f : A \to \mathbb{R}$
>Le derivate parziali di $f$ in $x_{0},y_{0}$ sono:
>$$\begin{align}
> &\frac{ \partial f }{ \partial x } (x_{0},y_{0}) =\lim_{ h \to 0 } \frac{f(x_{0}+h,y_{0}) - f(x_{0},y_{0})}{h}    \\
> &\frac{ \partial f }{ \partial y } (x_{0},y_{0}) = \lim_{ h \to 0 } \frac{f(x_{0}, y_{0}+h) - f(x_{0},y_{0})}{h} 
>\end{align}$$
>Se entrambe le derivate parziali di $f$ esistono diciamo che $f$ è derivabile in $(x_{0},y_{0})$. In questo caso organizziamo le derivate in un vettore detto [[gradiente]] che si indica con $\nabla f(x_{0},y_{0})$


Ci sono due casi nel quale è necessario usare la definizione per determinare se $f$ è derivabile e per il cacolo delle derivate parziali:
1. $f$ è definita per casi:
 $$ f(x,y) = \begin{cases}
g(x,y)\qquad &(x,y) \neq \mathbf{x_{0}} \\
f(x) &x = \mathbf{x_{0}}
\end{cases} $$
In questo caso calcolo $\frac{ \partial f }{ \partial x } f(\mathbf{x_{0}})$ e $\frac{ \partial f }{ \partial y } f(\mathbf{x_{0}})$ e se entrambe esistono finiti allora $f$ è derivabile in $\mathbf{x_{0}}$ e ho ottenuto $\nabla f(\mathbf{x_{0}})$
altrimenti $f$ non è derivabile in $\mathbf{x}_{0}$
2. Nella definizione di $f$ compare $t^\alpha$ con $\alpha \in (0,1)$ o $|t^\alpha|$ con $\alpha \in (0,1]$ per qualche $t  = g(x,y)$
Devo usare la definizione $\forall (x,y)$ tale che $g(x,y) = 0$

In tutti gli altri casi posso concludere che $f$ è derivabile senza dover sfruttare la definizione.


# Differenziabilità e piano tangente
>[!def]
>$A \subseteq \mathbb{R}^2$ aperto $f : A \to \mathbb{R}$
>Diciamo che $f$ è differenziabile in $\mathbf{x_{0}} = (x_{0},y_{0}) \in A$ se
>1. $f$ è derivabile in $\mathbf{x_{0}}$
>2. $f(\mathbf{x_{0}+h}) = f(\mathbf{x_{0}}) + \langle \nabla f(\mathbf{x_{0}}),\mathbf{h}\rangle + R(\mathbf{h})$ con $R(\mathbf{h}) = o(||\mathbf{h}||)$ cioè $$\lim_{ \mathbf{h} \to (0,0)} \frac{R(\mathbf{h})}{||\mathbf{h}||} = 0$$

Ossia $f$ è derivabile e vale lo sviluppo di taylor al primo ordine.

Esplicito: $\mathbf{x_{0}} = (x_{0},y_{0})\quad \mathbf{h}=(h_{1},h_{2})$
$$ f(x_{0}+h_{1},y_{0}+h_{2}) = f(x_{0},y_{0}) + \underbrace{ \frac{ \partial f }{ \partial x } (x_{0},y_{0})h_{1} + \frac{ \partial f }{ \partial y } (x_{0},y_{0})h_{2} }_{ \text{prodotto scalare } \langle\nabla f(\mathbf{x_{0}}),h\rangle } + R(\mathbf{h}) $$
$$ \lim_{ \mathbf{h} \to (0,0) } \frac{R(\mathbf{h})}{||\mathbf{h}||}  = \lim_{ (h_{1},h_{2}) \to (0,0) } \frac{R(h_{1},h_{2})}{\sqrt{ h_{1}^2+h_{2}^2 }} = 0$$
Scrittura equivalente ponendo $x=x_{0}+h$:
$$ f(\mathbf{x}) = f(\mathbf{x_{0}}) + \langle \nabla f(\mathbf{x_{0}}, \mathbf{x}- \mathbf{x_{0}}) \rangle + o(||\mathbf{x}|-\mathbf{x_{0}}|) $$


>[!def] 
>se $f$ è differenziabile in $\mathbf{x_{0}} = (x_{0},y_{0})$ il piano tangente al grafico di $f$ in $(\mathbf{x_{0}},f(\mathbf{x_{0}}))$ è 
> $$ z = f(\mathbf{x}_{0}) + \langle\nabla f(\mathbf{x_{0}}),\mathbf{x}-\mathbf{x_{0}}\rangle$$
 
 >[!esempio] 
 >$$ f(x,y) = e^{2x-y} \quad\text{differenziabile}$$
 >Calcolare l'equazione del piano tangente al grafico di $f$ nel punto $(1,2,f(1,2))$
 > $$ \begin{align}
> \frac{ \partial f }{ \partial x } &= e^{2x-y} \cdot 2 \\
\frac{ \partial f }{ \partial x }(1,2) &= 2  \\
\frac{ \partial f }{ \partial y } &= e^{2x-y} \cdot(-1) \\
\frac{ \partial f }{ \partial y }(1,2)  &= -1\\
f(1,2) &= 1   \\
>z &= f(1,2) + \frac{ \partial f }{ \partial x } (1,2)(x-1) + \frac{ \partial f }{ \partial y }(1,2)(y-2) =  \\
&=1 +2(x-1)-(y-2)
>\end{align} $$

## Stabilire differenziabilità
>[!def]
>$A \subseteq \mathbb{R}^2$ aperto, $f:A \to \mathbb{R}$ derivabile.
>Se $\frac{ \partial f }{ \partial x }$ e$\frac{ \partial f }{ \partial y }$ sono continue in $A$ diciamo che $f$ è di [[classe C]]$^1$ in A e scriviamo $f \in C^1(A)$


>[!teorema] Teorema del differenziale totale
>$A \subseteq \mathbb{R}^2$ aperto e $f \in C^1(A)$ allora $f$ è differenziabile in ogni punti di $A$


>[!esempio]
>Riprendendo l'esempio di prima $f(x,y) = e^{2x-y}$
>dominio di definizione $\mathbb{R}^2$.
>$$\begin{align}
> &\frac{ \partial f }{ \partial x }(x,y) = 2e^{2x-y} &\frac{ \partial f }{ \partial y}(x,y) = -e^{2x-y} 
\end{align}$$
Sono funzioni definite e continue in $\mathbb{R}^2$ quindi per il teorema del differenziale totale, $f$ è differenziabile in $\mathbb{R}^2$

c
Ci sono due casi in cui è necessario ricorrere alla definizione: gli stessi utili per la derivabilità

>[!esempio]
>$f(x,y) = yx^{1/3}$
>Provo ad applicare il teorema del differenziale totale
> $$ \frac{ \partial f }{ \partial x } (x,y) = y \frac{1}{3}x^{-2/3} \implies \text{non definita per } x = 0 $$
> Allora il teorema non sia applica in tutti i punti dell'asse y per i quali dovrei utilizzare la definizione. 


La definizione richiede di verificare il limite di due variabili:
$$ \lim_{ \mathbf{h} \to \mathbf{0} } \frac{R(\mathbf{h})}{||\mathbf{h}||} = \lim_{ \mathbf{h} \to \mathbf{0} } \frac{f(\mathbf{x_{0}+h}) - f(\mathbf{x_{0}} )- \langle\nabla f(\mathbf{x_{0},\mathbf{h}})\rangle}{||\mathbf{h}||} = 0$$

>[!teorema] Teorema differenziabile implica continua
Siano $A \subseteq \mathbb{R}^2$ aperto
 $\mathbf{x_{0}} \in A$
 $f : A \to \mathbb{R}$ differenziabile in $\mathbf{x_{0}}$
 Allora $f$ è continua in $\mathbf{x_{0}}$
 >
 >>[!dim] #Dim 6
 >>Dobbiamo dimostrare
 >>$$ \lim_{ \mathbf{x} \to \mathbf{x_{0}} } f(\mathbf{x}) = f(\mathbf{x_{0}})  $$
 >>Essendo $f$ differenziabile in $\mathbf{x}_{0}$
 >> $$ \begin{align}
> f(\mathbf{x}) - f(\mathbf{x_{0}}) &= \langle\nabla f(\mathbf{x_{0}}), \mathbf{x} - \mathbf{x_{0}}\rangle + o(||\mathbf{x}-\mathbf{x_{0}}||) \\
 |f(\mathbf{x}) - f(\mathbf{x_{0}})| &= |\langle\nabla f(\mathbf{x_{0}}, \mathbf{x} - \mathbf{x_{0}})\rangle + o(||\mathbf{x}-\mathbf{x_{0}}||)|  \\
>\text{disuguaglianza triangolare}&\leq |\langle\nabla f(\mathbf{x_{0}}),\mathbf{x}-\mathbf{x_{0}}\rangle| + o (||\mathbf{x-\mathbf{x_{0}}}||) \\
\text{TODO}&\leq ||\nabla f(\mathbf{x_{0}})||\cdot ||\mathbf{x}-\mathbf{x_{0}}|| + o(||\mathbf{x}\mathbf{x_{0}}||)
>\end{align} $$
>Quindi $$\lim_{ \mathbf{x} \to \mathbf{x_{0}} } |f(\mathbf{x})-f(\mathbf{x_{0}})| = 0 \implies \lim_{ \mathbf{x} \to \mathbf{x_{0}} } f(\mathbf{x}) = \mathbf{x_{0}} $$

Schema
$$ \begin{align}
f \in C^1(A) \implies f &\text{ differenziabile in }A \implies f &\text{ derivabile in }A \\
&\Downarrow &\cancel{ \Downarrow } \\
&f \text{ continua in A} &f \text{ continua in A}
\end{align} $$
## Altre proprietà delle funzioni differenziabili

### Derivate direzionali

>[!def]
>$A \subseteq \mathbb{R}^2$ aperto, $\mathbf{x}_{0} = (x_{0},y_{0}) \in A$, $f : A \to \mathbb{R}$, $\mathbf{v} = (v_{1},v_{2})$ di norma unitaria cioè, $||\mathbf{v}|| = 1$
>La derivata direzionale di $f$ in $\mathbf{x}_{0}$ nella direzione individuata da $\mathbf{v}$ è $$\frac{ \partial f }{ \partial \mathbf{v} } = \lim_{ t \to 0 } \frac{f(x_{0}+tv_{1}, y_{0}+tv_{2}) - f(x_{0},y_{0})}{t}$$
>Se il limite esiste finito

>[!oss]
>le derivate parziali sono casi particolari di derivate direzionali in cui
>$$ \mathbf{v} = \begin{bmatrix}
1 \\
0
\end{bmatrix} \implies \frac{ \partial f }{ \partial x }  $$


[[gradiente#formula del gradiente]]

# Derivata della composta
In analisi 1: $[f(g(x))]' = f'(g(x)) \cdot g'(x)$
Adesso abbiamo due casi:
1. Derivata della restrizione di una funzione di 2 variabili ad una curva piana

```tikz
\begin{document}
\begin{tikzpicture}
\draw[] (0,0) -- (3,0){};
\draw[] (5,0) -- (9,0){};
\draw[] (7,-2) -- (7,2){};
\draw[] (11,0) -- (14,0){};
\end{tikzpicture}
\end{document}
```
La restrizione di $f$ a $\mathbf{r}$ è la funzione composta:
$$ F(t) = (f \circ \mathbf{r})(t) = f(\mathbf{r}(t)) = f(r_{1}(t),r_{2}(t)) $$
$F: J \subseteq \mathbb{R} \to \mathbb{R}$
? $F'(t)$

Se $f$ è differenziabile e la curva $\mathbf{r}$ è regolare allora la derivata della composta 
$$ F'(t) = \langle \nabla f(\mathbf{r}(t)), \mathbf{r}'(t)\rangle = \langle
\begin{bmatrix}
\frac{ \partial f }{ \partial x } (r_{1}(t),r_{2}(t)) \\
\frac{ \partial f }{ \partial y } (r_{1}(t),r_{2}(t))
\end{bmatrix}, \begin{bmatrix}
r_{1}'(t) \\
r_{2}'(t)
\end{bmatrix}\rangle $$ 
2. **Caso 2**
	$$ G(x,y) = g(f(x,y)) : A \subseteq \mathbb{R}^2 \to \mathbb{R} $$
	Se $f$ è differenziabile e $g$ è derivabile allora:
	$$ \begin{align}
&\frac{ \partial G }{ \partial x } (x,y) = g'(f(x,y)) \cdot \frac{ \partial f }{ \partial x } (x,y)  \\
&\frac{ \partial G }{ \partial y } (x,y) = g'(f(x,y)) \cdot \frac{ \partial f }{ \partial y } (x,y) 
\end{align}$$
Cioè
$$ \nabla G(x,y) = g'(f(x,y)) \nabla f(x,y) $$


