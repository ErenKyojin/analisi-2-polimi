>[!esempio]
>$f(x,y) = x^2y$
> $$ Z = {(x,y) \in \mathbb{R}^2 : F(x,y) = 0}\quad F(x,y) = x^2 +y^2 - 1 $$
> 
> ### Svolgimento
> Determino i punti $\in Z$ nei quali non valgono le ipotesi del teorema
>  $$ \begin{cases}
\nabla F (\mathbf{x}) = \mathbf{0} \\
F(\mathbf{x}) = \mathbf{0}
\end{cases}
\quad \begin{cases}
> 2x = 0 \\
2y = 0 \\
x^2 + y^2 = 1
\end{cases}$$
Non ha soluzione, $\nabla F$ si annulla solo nell'origine che non appartiene a $Z$
>
> Cerco quindi $x,y,\lambda \in \mathbb{R}$ tali che
> $$ \begin{cases}
>\nabla f(x,y) = \lambda \nabla F(x,y) \\
>F(x,y) = 0
\end{cases}\quad
\begin{cases}
>2xy = \lambda 2x \\
x^2 = \lambda 2y \\
>x^2 + y^2 = 1
\end{cases}$$
>$$ \begin{cases}
>xy = \lambda x \\
x^2 = 2\lambda y \\
x^2 + y^2 = 1
>\end{cases} $$
>Se $x = 0$ allora $\begin{cases}0 = 2xy\\
>y^2 = 1
\end{cases}\quad$ $\begin{cases} \lambda = 0 \\
y = \pm 1
\end{cases}$
Cioè ottengo come candidati $(0,-1)$ e $(0,1)$ con $\lambda = 0$
>
>Se $x \neq 0$ e $y = \lambda$ allora $\begin{cases}y = \lambda
\\x^2 = 2 \lambda ^ 2
\\2\lambda^2 + \lambda^2 = 1
\end{cases}$
>$$ \begin{cases}
>y = \lambda \\
x^2 = 2\lambda^2 = \frac{2}{3} \\
\lambda = \pm \frac{1}{\sqrt{ 3 }}
>\end{cases} $$
>se $\lambda = \frac{1}{\sqrt{ 3 }}\implies x = \pm\sqrt{ \frac{2}{3} },\quad y=\frac{1}{\sqrt{ 3 }}$
>Altri due candidati
>$$ P_{1} = \left( \sqrt{ \frac{2}{3} }, \frac{1}{\sqrt{ 3 } }\right), P_{2} =\left( -\sqrt{ \frac{2}{3} } \right) $$