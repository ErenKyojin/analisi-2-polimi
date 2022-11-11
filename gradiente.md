Il gradiente di una funzione $f$ è il vettore delle sue derivate parziali, si indica con:

$$ \nabla f(x_{0},y_{0}) = \begin{bmatrix}
\frac{ \partial f }{ \partial x } (x_{0},y_{0})  \\
\frac{ \partial f }{ \partial y }  (x_{0},y_{0})
\end{bmatrix}  \in \mathbb{R}^2$$
Per calcolare il gradiente di una funzione derivabile in $\mathbf{x_{0}}$ semplicemente is applicano le regole di derivazione di analisi 1, svolgendo i calcoli per variabili diverse.

>[!esempio]
>Potenziale elettrico $V(\mathbf{x}) = \frac{1}{||\mathbf{x}||}$
>$$ V(x_{1},x_{2},x_{3}) = \frac{1}{\sqrt{ x_{1}^2+x_{2}^2+x_{3}^2 }} \qquad E(\mathbf{x}) = -\nabla V(\mathbf{x})$$
>$$\begin{align}
>  &=(x_{1}^2+x_{2}^2+x_{3}^2)^{-1/2} \\
> \frac{ \partial V }{ \partial x_{i} } = -\frac{1}{2}(x_{1}^2+x_{2}^2+x_{3}^2)^{-\frac{3}{2}} \cdot \frac{ \partial  }{ \partial x_{i} } (x_{1}^2+x_{2}^2+x_{3}^2) = -\frac{1}{2}||\mathbf{x}||^{-3} 2x_{i}
>\end{align}  $$



>[!teorema] Formula del gradiente
>$A \subseteq \mathbb{R}^2$ aperto, $\mathbf{x_{0}} = (x_{0},y_{0}) \in A$
>$f : A \to R$ differenziabile in $\mathbf{x_{0}}$ allora $f$ ammette [[derivate direzionali]] in ogni direzione $\mathbf{v}$ ed inoltre
>$$ \fbox{$\frac{ \partial f }{ \partial \mathbf{v}}(\mathbf{x_{0}})= \langle \nabla f(\mathbf{x_{0}}),\mathbf{v} \rangle$}$$
>
>>[!dim] #dim 7
>>Devo dimostrare che
>> $$ \lim_{ t \to 0 } \frac{f(\mathbf{x_{0}+t\mathbf{v}})-f(\mathbf{x_{0}})}{t} = \langle \nabla f(\mathbf{x_{0}}),\mathbf{v}\rangle $$
>> Scelgo $\mathbf{h} = t\mathbf{v}$ nella definizione di differenziabilità
>> $$ \begin{align}
>>f(\mathbf{x_{0}}+t\mathbf{v}) - f(\mathbf{x_{0}}) = \langle\nabla f(\mathbf{x_{0}},t\mathbf{v}) \rangle + o (||t\mathbf{v}||)
>>\end{align} $$
>>Divido per $t$ e faccio il limite $t \to 0$
>>
>> $$ \begin{align}
>>\lim_{ t \to 0 } \frac{f(\mathbf{x_{0}}+t\mathbf{v})-f(\mathbf{x_{0}})}{t} &= \lim_{ t \to 0 } \frac{t \langle \nabla f(\mathbf{x_{0}}) \mathbf{v}\rangle + o(|t|)}{t} = \\
&= \lim_{ t \to 0 }\langle \nabla f(\mathbf{x_{0}}),\mathbf{v} \rangle + \lim_{ t \to 0 } \frac{o(|t|)}{t} \\
&= \langle \nabla f(\mathbf{x_{0}}), \mathbf{v}\rangle + 0
>>\end{align} $$

>[!esempio]
>$f(x,y) = e^{x^2y}$
>$\mathbf{x_{0}} = (1,1)$, $\mathbf{v}=\frac{1}{\sqrt{ 2 }}[1,1]^T$
>$$ \begin{align}
>\frac{ \partial f }{ \partial x } (x,y) = 2xye^{x^2y} \\
>\frac{ \partial f }{ \partial y } (x,y) = x^2e^{x^2y}
>\end{align} $$
>Derivate parziali definite e continue in $\mathbb{R}^2 \implies$ per il teorema del differenziale totale $f$ è differenziabile in ogni punto e in ogni direzione e vale la formula del gradiente
>
> $$ \nabla f(1,1) = \begin{bmatrix}
> 2e \\
>e
>\end{bmatrix} $$
>$$ \begin{align}
\frac{ \partial f }{ \partial \mathbf{v} } (1,1) = \langle \nabla f(1,1), \mathbf{v}\rangle = \langle[2e\quad e]^T, \frac{1}{\sqrt{ 2 }}[1,1]\rangle = \frac{3e}{\sqrt{ 2 }} 
\end{align} $$

