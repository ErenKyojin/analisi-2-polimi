La matrice hessiana è la matrice delle derivate delle derivate parziali
$$ H_{f} (x_{0},y_{0}) = \begin{bmatrix}
\end{bmatrix}$$

>[!esempio]
> $$ \begin{align}
> &\nabla f(x,y) = \begin{bmatrix}
\sin y \\
x \cos y
\end{bmatrix} \\
>
>&H_{f}(x,y) = \begin{bmatrix}
>0 & \cos y \\
\cos y & -x\sin y
\end{bmatrix}
>\end{align} $$




# Forme quadratiche
>[!def]
>Sia $f \in C^2(A)$ chiamiamo forma quadratica indotta da $H_{f}(x_{0},y_{0})$
>$q : \mathbb{R}^2 \to \mathbb{R}$
> $$
> q(h_{1},h_{2})= \begin{bmatrix}
>h_{1} & h_{2}
\end{bmatrix}
>  H_{f}(x_{0},y_{0})\begin{bmatrix}
>h_{1} \\
h_{2}
\end{bmatrix} = \langle \begin{bmatrix}
>h_{1}  & h_{2}
\end{bmatrix},
> H_{f}(x_{0},y_{0}) \cdot
> \begin{bmatrix}
> h_{1} \\
h_{2}
\end{bmatrix}
\rangle $$



In modo esplicito:

$$ \begin{align}
q(h_{1},h_{2}) &= \begin{bmatrix}
h_{1} & h_{2}
\end{bmatrix} \cdot 
\begin{bmatrix}
\frac{ \partial^2 f }{ \partial x^2 }(x_{0},y_{0}) & \frac{ \partial^2 f }{ \partial x \partial y } (x_{0},y_{0})\\
\frac{ \partial^2 f }{ \partial x\partial y }(x_{0},y_{0}) & \frac{ \partial^2 f }{ \partial y^2 }(x_{0},y_{0})    
\end{bmatrix} \cdot \begin{bmatrix}
h_{1} \\
h_{0}
\end{bmatrix} = \\
&=\frac{ \partial^2 f }{ \partial x } h_{1}^2 + 2\frac{ \partial^2 f }{ \partial x \partial y} (x_{0},y_{0}) h_{1}h_{2} + \frac{ \partial^2 f }{ \partial y^2 }(x_{0},y_{0}) h_{2}^2  
\end{align} $$




## Segno della formula quadrata
$q$ definita $\iff \det A > 0$ 
- definita positiva
- Definita negativa

$q$ semi definita $\iff \det A = 0$
- semidefinita positiva
- semidefinita negativa

$q$ non definita $\iff \det A < 0$


### ris
Definita positiva $\implies$ minimo
semidefinita negativa $\implies$ flesso (sella di cavallo)


>[!esempio]
>$f(x,y) = x \sin y$
>$$ H_{f}(x,y) = \begin{bmatrix}
> 0 & \cos y \\
\cos y & -x \sin y
\end{bmatrix} $$
> $$ H_{f}(0,0) = \begin{bmatrix}
> 0 & 1 \\
1 & 0
\end{bmatrix} $$
> $$ q(h_{1},h_{2}) = (h_{1}\quad h_{2}) \begin{bmatrix}
>0 &1 \\
>1 &0
\end{bmatrix} 
\begin{pmatrix}
>h_{1} \\
h_{2}
\end{pmatrix} = 2h_{1}h_{2}$$
> f.q. indefinita