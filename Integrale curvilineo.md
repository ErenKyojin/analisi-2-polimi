Supponiamo che una [[Curva regolare]] (o [[Curve#Curva regolare a tratti]])
$$ \mathbf{r} : [a,b] \to \mathbb{R}^3 $$
Rappresenti un filo avente densità di massa
 $$ \delta(t) \quad t \in[a,b] $$
 Massa del filo: $$\int_{a}^b \delta(t) \! ||\mathbf{r}(t)|| \, \mathrm{d}t$$


>[!esempio]
>
> $$\mathbf{r}(t) = \begin{bmatrix}
>t \\
>t \\
>2t^2
>\end{bmatrix} \qquad t \in [0,1]$$
>
>avente densità di massa $\delta(t) = f(\mathbf{r}(t))$ dove $f(x,y,z = x)$ ossia
> $$ \delta(t) = f(\mathbf{r}(t))= \mathbf{r_{1}}(t) = t $$


Introduciamo quindi l'integrale curvilineo:

>[!def]
>$[a,b] \subset \mathbb{R}$ limitato
>$\mathbf{r}:[a,b] \to \mathbb{R}^3$ curva regolare di sostegno $\gamma$
>$f(\mathbf{(t)})$ continua, $t \in[a,b]$
>L'integrale curvilineo di $f$ lungo $\gamma$ che si indica $\int_{\gamma} \! f\, \mathrm{d}s$ e si calcola come:
> $$ \int_{a}^b \! f(\mathbf{r}(t))\ ||\mathbf{r}'(t)||\, \mathrm{d}t  $$


>[!oss]
>- $\int \! f\, \mathrm{d}s \implies \mathrm{d}s \to ||\mathbf{r}'(t) dt||$
>- Quando $f(\mathbf{r}(t)) \leq 0$ l'integrale curvilineo ha comunque sanso
>- Se $\gamma$ è regolare a tratti
> $$\implies \int_{\gamma} \!f \, \mathrm{d}s = \int_{\gamma_{1}} \!f \, \mathrm{d}s + \ldots + \int_{\gamma_{*}} \!f \, \mathrm{d}s $$