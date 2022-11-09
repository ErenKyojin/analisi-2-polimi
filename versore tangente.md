>[!def]
>Data una [[Curve|curva]] regolare $\mathbf{r} : I \to \mathbb{R}^3$ definiamo $\forall t \in I$ il versore tangente
> $$ \mathbf{T}(t) = \frac{\mathbf{r}'(t)}{||\mathbf{r}'(t)||}$$

 Il versore tangente ha:
- direzione parallela alla retta tangente alla curva nel punto $\mathbf{r}(t)$
 - norma unitaria $||\mathbf{T}(t)|| = 1 \forall t$
 - Verso concorde con il verso di percorrenza della curva

Più esplicitamente:
$$
\begin{align}
 \mathbf{r}'(t) &= \begin{bmatrix}
r_{1}'(t) \\
r_{2}'(t) \\
r_{3}'(t)
\end{bmatrix} \qquad \mid\mid \mathbf{r}'(t)\mid\mid = \sqrt{ r_{1}'(t)^2 + r_{2}'(t)^2 + r_{3}'(t)^2 } \\ \\

I(t) &= \begin{bmatrix}
\frac{r_{1}'(t)}{||\mathbf{r}'(t)||} \\
\frac{r_{2}'(t)}{||\mathbf{r}'(t)||} \\
\frac{r_{3}'(t)}{||\mathbf{r}'(t)||}

\end{bmatrix}

\end{align}
$$
>[!esempio]
Prendiamo come esempio il ramo di iperbole:
