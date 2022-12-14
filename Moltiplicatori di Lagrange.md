Sappiamo che il [[teorema di fermat]] indica i punti candidati di estremo libero, allo stesso modo il metodo dei moltiplicatori fornisce i punti candidati di estremo vincolato. Tra i candidati di estremo vincolato l selezioniamo massimo e minimo assoluti confrontando i valori di $f$

>[!teorema]
>$A \subseteq \mathbb{R}^2$ aperto $f,F \in C^1(A)$
>Sia $\mathbf{x_{0}} = (x_{0},y_{0})$ punto di estremo vincolato per $f$ sul vincolo
> $$ Z = \{(x,y) \in A : F(x,y) = 0\} $$
> Supponiamo inoltre che
> $$ \nabla F(\mathbf{x_{0}}) \neq \mathbf{0} $$
> Allora esiste $\lambda \in \mathbb{R}$ detto moltiplicatori di Lagrange tale che
>  $$ \fbox{$\nabla f(\mathbf{x_{0}}) = \lambda_{0} \nabla F(\mathbf{x_{0}})$} $$
> 

>[!oss] 
>scriviamo le condizioni
> $$ \nabla f(x_{0},y_{0}) = \lambda_{0} \nabla F(x_{0},y_{0})\quad e \quad(x_{0},y_{0}) \in Z $$
> in modo più esplicito:
> $$ \begin{cases}
> \frac{ \partial f }{ \partial x } (x_{0},y_{0}) = \lambda_{0} \frac{ \partial F }{ \partial x } (x_{0},y_{0}) \\
>\frac{ \partial f }{ \partial y } (x_{0},y_{0}) = \lambda_{0} \frac{ \partial F }{ \partial y } \\
F (x_{0},y_{0}) = 0 
>\end{cases} $$
>Sistema non lineare di 3 equazioni nelle 3 incognite $x_{0},y_{0},\lambda_{0}$
>
> In pratica:
> i punti candidati sono le soluzioni di 
> $$ \begin{cases}
> \nabla F(\mathbf{x_{0}}) = \mathbf{0} \\
F(\mathbf{x_{0}}) = 0
>\end{cases}
>\qquad
>\begin{cases}
>\nabla f(\mathbf{x_{0}}) = \lambda_{0} \nabla F(\mathbf{x_{0}}) \\
F(\mathbf{x_{0}}) = 0
>\end{cases}
>
>$$
>Che sono rispettivamente i punti di $Z$ dove **non** si applica il teorema ed il sistema dei moltiplicatori di lagrange



>[!oss] $\lambda_{0} = 0$ è ammissibile

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
>Se $x = 0$ allora $\begin{cases}0 = 2\lambda y\\
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
>$$ P_{1} = \left( \sqrt{ \frac{2}{3} }, \frac{1}{\sqrt{ 3 } }\right), P_{2} =\left( -\sqrt{ \frac{2}{3} }, \frac{1}{\sqrt{ 3 }}  \right) $$
>Se $\lambda = - \frac{1}{\sqrt{ 3 }}$ altri due candidati
>$$ P_{3} = \left( \sqrt{ \frac{2}{3} }, -\frac{1}{\sqrt{ 3 }} \right), P_{4} = \left( - \sqrt{ \frac{2}{3} } , -\frac{1}{3}\right)  $$
>E chiamandi $P_{5} = (0,1)$ e $P_{6} = (0,-1)$ 
>Confrontando i valori $f(P_{i})$
>Trovo massimo e minimi vincolati.
>- Punti di massimo $P_{1},P_{2}$ $\quad f(P_{1}) = f(P_{2})$
>- #TODO 


$\nabla f(\mathbf{x_{0}}) = \lambda_{0} \nabla F(\mathbf{x_{0}})$ :
- Con $\lambda_{0} \neq 0 \implies$ paralleli
- Con $\lambda_{0} = 0 \implies \mathbf{x_{0}}$ punto critico libero



### Interpretazione geometrica del teorema di lagrange nel caso $\lambda_{0} \neq 0$

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.8}
\begin{document}
\begin{tikzpicture}
\begin{axis}[colormap/viridis]
\addplot[domain=-3:3,samples=18]{1/(x*x)};
\end{axis}
\end{tikzpicture}
\end{document}
```
