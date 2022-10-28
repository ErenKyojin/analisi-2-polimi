L'idea per calcolare la lunghezza di una [[Curve|curva]] è dividerla in segmenti e chiamare $P_{0},\dots,P_{n}$ i punti sulla curva che delimitano questi segmenti. È simile al procedimento per le somme di Cauchy rienmann:
$$ \begin{align}
\text{Lunghezza} &\approx \sum_{i=0}^n ||P_{i+1} - P_{i}|| =  \\
&=\sum_{i=0}^n ||\mathbf{r}(t_{i+1})- \mathbf{r}(t_{i})|| = \\
&=\sum_{i=0}^n ||\frac{\mathbf{r}(t_{i+1}-\mathbf{r}(t_{i}))}{t_{i+1}-t_{i}}|| \cdot (t_{i+1}-t_{i}) = \\
& \approx \int ||\mathbf{r}'(t)|| \! \, \mathrm{d}t 
\end{align}$$



Quindi siano $[a,b] \subseteq \mathbb{R}$ limitato e $\mathbf{r} : [a,b] \to \mathbb{R}^3$ la parametrizzazione di una [[curva regolare]] avente sostengno $\gamma$ allora
$$ \text{lunghezza($\gamma$)} = \int_{a}^b \! ||\mathbf{r}'(t)|| \, \mathrm{d}t  $$
