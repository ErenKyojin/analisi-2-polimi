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
>