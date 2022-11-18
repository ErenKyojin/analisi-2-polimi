L'obiettivo dell'ottimizzazione libera è il trovare minimi o massimi locali in una funzione, in analisi 1 i punti candidati sono quelli con derivata prima = 0, ma è poi necessario guardare la derivata seconda.

Per l'ottimizzazione libera sono necessarie le [[derivate seconde]] e la [[matrice hessiana]]

## Ottimizzazione 2D

>[!def]
>Sia $A \subseteq \mathbb{R}^2$ sottonsieme qualsiasi (aperto / chiuso / ne aperto ne chiuso, limitato / illimitato)
>$f : A \to \mathbb{R}$
>Un punto $(x_{0},y_{0}) \in A$ si dice
>#### - Punto di massimo globale (o assoluto) per $f \in A$
>se
>$$ f(x_{0},y_{0}) \geq f(x,y)  \qquad\forall(x,y) \in A$$
>Il valore $f(x_{0},y_{0})$ è detto valore di massimo globale o assoluto ed $(x_{0},y_{0})$ punto di massimo
>
> #### - Punto di massimo locale (o relativo) per $f \in A$
> Se esiste $\delta > 0$ tale che
>  $$ f(x_{0},y_{0}) \geq f(x,y)\quad \forall (x,y) \in B_{\delta}(x_{0},y_{0}) \cap A $$
>
>Il valore $f(x_{0},y_{0})$ è il valore di massimo locale o relativo.


>[!oss]
> i punti di massimo appartengono all'insieme $A$ e possono essere interni o di frontiera
>
>Il valore di massimo assoluto è **unico** ma potrebbe essere assunto in più punti

Analogamente minimo girando le disuguaglianze


>[!def]
>Se $x_{0},y_{0}$ è punto di massimo o di minimo, locale o globale per $f \in A$ allora è detto punto di estremo

# Ottimizzazione libera
>[!oss] Anticipazione:
Se voglio determinare
> $$ \max f(x,y)\quad\text{e}\quad \min f(x,y) $$
> Con $A$ chiuso e limitato considero separatamente:
> $A \setminus \partial A =$ parte interna di $A$ è aperto $\to$ Fermat
> $\partial A$ studio separatamente ([[ottimizzazione vincolata]])


>[!def] Ottimizzazione libera
>Con ottimizzazione libera si intende ottimizzazione su un insieme aperto, ossia si applica il [[teorema di fermat]] e non quello di [[teorema di weierstrass|weierstrass]]
>

