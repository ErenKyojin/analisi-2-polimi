# Serie di funzioni
Partiamo da un esempio
>[!esempio]
>$$\begin{align}
> e^x &= \sum_{n=0}^{+\infty} \frac{x^n}{n!} = 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \dots \qquad&&\forall x \in \mathbb{R} \\
> \frac{1}{1-x} &= \sum_{n=0}^{+\infty} x^n = 1 + x + x ^2 + x^3 + \dots \qquad&&\text{serie geometrica per } x \in (-1,1)
>\end{align} $$



>[!def]
>Date dalle funzioni $f : J \subseteq \mathbb{R} \to \mathbb{R}, (n=0,1,2,3,\dots)$
> La serie di funzioni di termine generale $f_{n}(x)$ è la successione delle somme parziali
> $$ S_{0} (x) = f_{0}(x)\qquad S_{1}(x) = f_{0}(x) + f_{1}(x) \qquad \dots\qquad S_{k}^{(x)} = \sum_{n=0}^k f_{n}(x) \quad\dots$$

>[!oss]
>Fissato $\overline{x} \in J$ si tratta di una serie numerica, e la serie di funzioni [[convergenza semplice|converge]] puntualmente (o semplicemente) nel punto $\overline{x} \in J$ se la serie numerica di termine generale $f_{n}(\overline{x})$ è convergente, ossia esiste finito il limite delle somme parziali:
>$$ \lim_{ k \to \infty } S_{k}(\overline{x}) = \lim_{ k \to \infty } \sum_{n=0}^k f_{n}(\overline{x})$$
>Chiamiamo insieme di convergenza puntuale (o semplice) l'insieme $E \subseteq J$ di punti in cui la serie converge puntualmente.
>Nell'insieme $E$ risulta così definita una nuova funzione detta somma delle serie, che si indica con il simbolo:
>$$ f(x) = \sum_{n=0}^{+\infty}f_{n}(x) \qquad (x \in E) $$
>$\Rightarrow f(x) = \lim_{ k \to \infty }S_{k}(x)$

>[!oss]
>La serie converge assolutamente in $\overline{ x} \in J$ se la serie numerica di termini generale $\mid f_{n}(z)\mid$ converge.

>[!oss]
>La convergenza assoluta implica la convergenza semplice in $\overline{x}$


>[!esempio] Esempio fondamentale
>Questo esempio servirà per le [[Serie di potenze]] –> le serie di taylor ne sono un caso particolare
>$$ \sum_{n=0}^{+\infty} x^n $$
>
>
>L'insieme convergente puntuale $E = (-1,1) = \{|x| < 1\}$, la convergenza in $E$ è anche assoluta:
>$\Rightarrow$ per $x \leq -1$ indeterminata
>per $x \geq 1$ divergente
>per x $\in E = (-1,1)$ somma $\frac{1}{1-x} = \sum_{n=0}^{+\infty} x^n$

>[!error]
>Se le $f_{n}(x)$ sono cotinue/derivabili/integrabili, anche $f$ resterà continua/derivabili/integrabili?
>
>Il dubbio viene dallo "scambiare" i due limiti, se non fosse una serie sarebbe ovvio dalla linearità della derivata/integrale.

## [[Convergenza totale]]
