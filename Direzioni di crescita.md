Se $f$ è [[Calcolo differenziale|differenziabile]] in $\mathbf{x_{0}}$
$$ \frac{ \partial f }{ \partial \mathbf{v} } \langle \nabla f(\mathbf{x_{0}}), \mathbf{v} \rangle  = 0$$
con $\mathbf{v}$ vettore di norma unitaria, allora può essere che:
- $\nabla f(\mathbf{x_{0}})= \mathbf{0}$
- $\nabla f (\mathbf{x_{0})} \perp \mathbf{v}$

Cioè se $\nabla f(\mathbf{x_{0}}) \neq 0$ allora la derivata direzionale di $f$ in $\mathbf{x_{0}}$ è nulla nella direzione ortogonale a $\nabla f(\mathbf{x_{0}})$

%%#TODO tikzjax issue pgfplots%%

>[!teorema] Teorema ortogonalità del gradiente alle curve di livello. Ossia direzione di crescita nulla.
>Sia $A \subseteq \mathbb{R}^2$ aperto, $f : A \to \mathbb{R}$ differenziabile in $A$ 
>l'insieme di livello $I_{k}$ è il sostegno di una curva regolare $\mathbf{r}$ allora:
> $$ \langle \nabla f(\mathbf{r}(t)), \mathbf{r}'(t)\rangle = 0\quad \forall t$$


$\mathbf{r}(t_{0}) = \mathbf{x}_{0} \implies \mathbf{r}'(t_{0})$ direzione tangente alla curva $\mathbf{r}(t)$, cioè alla curva di livello.

Questo teorema dice che:
1. se $\nabla f(\mathbf{x_{0}}) \neq \mathbf{0}$ allora $\nabla f(\mathbf{x_{0}}) \perp$ curva di livello passante per $\mathbf{x_{0}}$
2. grazie alla formula del gradiente risulta nulla anche la derivata direzionale:
 $$ 0 = \langle \nabla f(\mathbf{r}(t)), \mathbf{r'}(t)\rangle = \frac{ \partial f }{ \partial \mathbf{v} } \mathbf{r}(t) $$ con $\mathbf{v} = \mathbf{r'}(t)$ 
 Cioè la derivata direzionale di $f$ nella direzione tangente alla curva di livello è nulla.
>[!dim] #dim 8
>Per ipotesi $I_{k}$ coincide con il sostegno della curva regolare $\mathbf{r}(t)$, cioè
> $$ I_{k} = \{\mathbf{r}(t), t \in J\} $$
> In particolare $f(\mathbf{r}(t)) = k\quad \forall t \in J$
> Chiamo $F : J \to \mathbb{R}$ la funzione composta $F(t) = f(\mathbf{r}(t)) = f \cdot \mathbf{r}(t)$ 
> Da un lato $F(t)=k\quad \forall t \implies F'(t) = 0\quad\forall t$
> D'altro canto per il teorema di derivazione della funzione composta:
>  $$ F'(t) = \langle \nabla f(\mathbf{r}(t)), \mathbf{r}'(t)\rangle$$
>  quindi per le ultime due osservazioni
>  $$\implies\langle \nabla f(\mathbf{r}(t)), \mathbf{r}'(t)\rangle =0$$


>[!teorema] Teorema di direzioni di massima e minima crescita
>$A \subseteq \mathbb{R}^2$ aperto, $\mathbf{x_{0}} \in A$
>$f : A \to \mathbb{R}$ differenziabile in $\mathbf{x_{0}}$
>$\nabla f(\mathbf{x_{0}}) \neq 0$
>Allora:
>1. $\forall \mathbf{v} \in \mathbb{R}^2$ di norma unitaria (ossia per ogni direzione) si ha che
> $$ |\frac{ \partial f }{ \partial \mathbf{v} } (\mathbf{x_{0}})| \leq ||\nabla f(\mathbf{x_{0}})|| $$
> 2. Detti $\mathbf{v}_{max} = \frac{\nabla f(\mathbf{x_{0}})}{||\nabla f(\mathbf{x_{0}})||}$ e $\mathbf{v}_{min} = \frac{-\nabla f(\mathbf{x_{0}})}{||\nabla f(\mathbf{x_{0}})||}$ si ha
>  $$ \frac{ \partial f }{ \partial \mathbf{v}_{max} }(\mathbf{x_{0}}) = ||\nabla f (\mathbf{x}_{0})||\qquad \frac{ \partial f }{ \partial \mathbf{v}_{min} }(\mathbf{x_{0}}) = - ||\nabla f(\mathbf{x_{0}})||  $$
>
>>[!dim] facoltativa
>>ide della dim
>> $$ \frac{ \partial f }{ \partial \mathbf{v} } = \langle \nabla f(\mathbf{x_{0}}),\mathbf{v}\rangle $$
>> Con cauchy schwartz:
>>  $$  |\frac{ \partial f }{ \partial \mathbf{v} } (\mathbf{x_{0}})| \leq ||\nabla f(\mathbf{x_{0}})|| \cdot ||\mathbf{v}|| $$

Questi teoremi ci aprono le porte all'[[ottimizzazione libera]]
