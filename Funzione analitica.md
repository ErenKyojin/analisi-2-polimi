>[!def]
>Una funzione di una variabile reale $f$ è detta nalaitcica reale nell'intervallo non vuoto $(a,b)$ se è somma di una serie di potenza in $(a,b)$; cioè se esistono $x_{0} \in(a,b), a_{n} \in \mathbb{R}:$
>$$ f(x) = \sum_{n=0}^\infty a_{n}(x-x_{0})^n\qquad\forall x \in(a,b) $$


Se $f$ è analitica in $(a,b)$
- qual è la regolarità minima di $f$?
	* $f$ derivabie ad ogni ordine in $(a,b)$
* Chi sono i coefficienti $a_{n}$? 
	 $$ \begin{align}
&f(x_{0}) = \sum_{n=0}^\infty a_{n}(x_{0}-x_{0})^n =a_{0} \\
&f'(x) = \sum_{n=1}^\infty a_{n}n(x-x_{0})^{n-1} \\
&f'(x_{0}) = \sum_{n=1}^\infty a_{n}n (x_{0}-x_{0})^n = a_{1}(x_{0}-x_{0})^0+0+0 = a_{1}  \\
&f''(x_{0}) = a_{2}
\end{align} $$


>[!teorema] Funzioni analitiche totali
>Se $f$ è analitica reale in un intervallo non vuoto $(a,b)$ allora è derivabile ad ongi ordine in $(a,b)$ e per ogni $x_{0} \in (a,b)$ è sviluppabile in [[serie di taylor]]
>$$ f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(x_{0})}{n!} (x-x_{0})^n\qquad x \in (a,b)$$ 
>
>Inoltre detto $R$ il raggio di convergenza della serie, l'identità è verificata per ogni $x \in (x_{0}- R, x_{0}+R)$ 


>[!esempio]
>Serie espononenziale


