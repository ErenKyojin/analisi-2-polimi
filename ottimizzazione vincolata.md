dominio vincolato con bordo o solo bordo

Se cerco i [[punti estremali]] di $f$ in un insieme non aperto non è sufficiente applicare il [[Teorema di fermat]] nella parte interna dell'insieme perchè potrebbero esserci estremanti anche sul bordo..
Infatti ci possono essere punti di massimo o minimo assoluti sui bordi


Strategia:

0. Se $A$ è chiuso e limitato ed $f$ è continua $\implies$ [[Teorema di Weierstrass]]
1. applico il [[Teorema di fermat]] nell'insieme aperto $A\ \setminus$ (bordo di $A$)
2. Cerco eventuali punti estremanti di $f$ sul bordo di $A$ $\implies$ [[vincolo di uguaglianza]]

>[!success] Buona notizia
>In ottimizzazione vincolata solitamente è richiesto di determinare solo massimo e minimo assoluti

>[!oss]
Se il vincolo è :
> - lineare $\implies$ sostituzione
> - non lineare $\implies$ [[Moltiplicatori di Lagrange]]
> 

Confronto tra [[teorema di fermat]] e [[Moltiplicatori di Lagrange]]

| | Fermat | Lagrange
--- | --- | ---
ambito di utilizzo | [[Ottimizzazione libera]] (su un aperto)| [[ottimizzazione vincolata]] con vincolo di uguaglianza (su una curva)|
Afferma che, sotto opportune ipotesi | $\mathbf{x_{0}}$ punto di estremo $\implies \nabla f (\mathbf{x_{0}} = \mathbf{0}$ | $\mathbf{x_{0}}$ punto di estremo vincolato $\implies \nabla f(\mathbf{x_{0}}) \parallel \nabla F(\mathbf{x_{0}})$</br> (purchè $\lambda_{0} \neq 0$)[^long]

[^long]: Se $\lambda_{0} = 0$ significa che $\mathbf{x_{0}}$ è punto di estremo libero ed il vincolo $Z$ passa proprio per $\mathbf{x_{0}}$



