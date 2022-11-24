In questa sezione vogliamo determinare i massimi ed i minimi di una funzione $f(x,y)$ quando $(x,y)$ verifica una condizione aggiuntiva della forma $$F(x,y) = 0$$
cioè il vincolo è espresso come insieme di livello nullo di una funzione $F(x,y)$

>[!esempio] Vincolo circonferenza $F(x,y) = x^2 + y^2 - R^2$

 >[!esempio] Vincolo triangolo $P_{1}, P_{2}, P_{3}$
 
 >[!esempio]
 >$$ f(x,y) = x^2 y $$
 >Vincolo $F(x,y) = 0$ con $F(x,y) = x^2 + y^2 - 1$
 >Chiamiamo $Z$ il vincolo nel piano $x,y$
 >$$Z = \{(x,y) \in \mathbb{R}^2 : F(x,y) = 0\} = \{(x,y) \in \mathbb{R}^2 : x ^2 + y^2 = 1\}$$ 
 >Che è la circonferenza unitaria
>
>```tikz
\usepackage{pgfplots}
\begin{document}
\begin{tikzpicture}
\begin{axis}[colormap/viridis]
\addplot3[surf, samples = 16, domain = -5:5]{x^2*y};
\end{axis}
\end{tikzpicture}
\end{document}
>```

>[!def]
>Siano $A \subseteq \mathbb{R} ^2$ aperto, $f, F \in C^1(A)$
>poniamo
> $$ Z = \{(x,y) \in A : F(x,y) = 0\} $$
> un punto $(x_{0},y_{0}) \in Z$ si dice:
> - Punto di massimo relativo o locale per $f$ vincolato a $Z$
> Se esiste $\delta > 0$ tale che
>  $$ f(x_{0},y_{0}) \geq f(x,y)\quad \forall (x,y) \in B_{\delta}(x_{0},y_{0}) \cap Z $$
>
> - Punto di massimo assoluto per $f$ vincolato a $Z$ se
>  $$ f(x_{0},y_{0}) \geq f(x,y)\quad \forall(x,y) \in Z $$
>
> - analogamente min
> - punto di estremo vincolato: un massimo vincolato od un minimo vincolato


>[!esempio] Ottimizzazione con vincolo di uguaglianza tramite metodo di sostituzione
>
>Nel modello di Cobb-Douglas si vuole massimizzare la funzione profitto
> $$ P(x,y) = \sqrt{ xy } $$
> dove $x$ è il lavoro e $y$ il capitale, con il vincolo di budget
>  $$ F(x,y) = \frac{x}{2} + \frac{y}{2} - 1 = 0 $$
>  Per ipotesi $x,y$ non negative
>$$ Z = \{(x,y) \in \mathbb{R}^2: x + y = 2, x \geq 0, y \geq 0\} $$
>$y = 2 - x$ vincolo positivo
>
>Metodo di sostituzione: considero la restrizione di $f$ al vincolo $Z$
> $$ g(x) = \sqrt{ x \cdot(2 - x) } \quad x \in\ ? $$
> Ricavo dove varia $x$
> $$ \begin{cases}
>&x = 2 - y \\
> &x \geq 0 \\
 &y \geq 0
\end{cases} \implies \begin{cases}
> x \geq 0 \\
x \leq 2
\end{cases} \implies x \in [0,2]$$
>cerco il massimo globale di $g(x)$ in $[0,2]$
>
> $x_{0} = 1$ punto di massimo assoluto per $g$ in $[0,2] \implies ?$
