
### - Edo lineari del primo ordine 
sfruttiamo la [[formula risolutiva per EDO lineari del 1° ordine]]


### Edo a variabili separabili
Porto $y$ e $y'$ dallo stesso lato dell'equazione ed integro, riconoscendo l'integrale

### Edo di bernoulli

### Edo lineari del secondo ordine

#### coefficenti costanti omogenee
 risolvo attraverso il polinomio caratteristico

$$ay'' + by'  + cy = 0 \implies a\lambda^2 + b\lambda + c = 0$$
In base ai risultati del polinomio:

- Se $\lambda_{1,2}$ reali ($\Delta > 0$): $$ y = C_{1} e^{\lambda_{1}x} + C_{2}e^{\lambda_{2}x} $$
- Se $\lambda_{1,2}$ complesse ($\lambda_{1,2} = \alpha + i\beta$, $\Delta<0$): $$ y = e^{\alpha t}(C_{1} \cos \beta x + C_{2} \sin \beta x)$$
- Se $\lambda_{1,2} = \lambda_{0}$($\Delta = 0$): $$ y = C_{1}e^{\lambda t} + tC_{2}e^{\lambda t} $$
#### coefficienti costanti non omogenee
$$ ay'' + by' + cy = f(x) $$

Le risolviamo sfruttando il teorema di struttura, ossia una soluzione generica si può ottenere sommando la soluzione dell'omogenea ad una soluzione particolare, calcoliamo la soluzione dell'omogenea sostituendo $f(t)=0$ e procedendo come sopra, chiamiamo questa soluzione $y_{o}$.

Dobbiamo adesso trovare una soluzione particolare $y_{p}$ e lo facciamo sfruttando il metodo di somiglianza:
- $f(t) = ax^n$ => una soluzione sarà"
	- del tipo $y_{p} = A_{n}x^n + A_{n-1}x^{n-1} + \dots + A_{0}$ in generale
	- del tipo $y_{p} = x(A_{n}x^n + A_{n-1}x^{n-1} + \dots + A_{0})$ se $\lambda = 0$ soluzione dell'omogenea con molteplicità algebrica 1
	- del tipo $y_{p} = x^2(A_{n}x^n + A_{n-1}x^{n-1} + \dots + A_{0})$ se $\lambda = 0$ soluzione dell'omogenea con molteplicità algebrica 1

- $f(t) = ae^{bx}$
	- del tipo $y_{p} = Ae^{bx}$
	- del tipo $y_{p} = tAe^{bx}$  se $\lambda = b$ soluzione dell'omogenea

- $f(t) = a_{1}\cos(bx) + a_{2}\sin(bx)$
	- $A_{1}\cos(bx) + A_{2} \sin(bx)$


### sistemi di equazioni differenziali

####  Diagonalizzabili
della formula $\mathbf{Y}' = A\mathbf{Y}$ o
$$ \begin{cases}
y_{1}' = a_{11}y_{1} + a_{12}y_{2}  \\
y_{2}' = a_{21}y_{1} + a_{22}y_{2} 
\end{cases} $$

Se $A$ è diagonalizzabile allora con gli autovalori $\lambda_{1,2}$ e gli autovettori associati $\mathbf{u_{1}}, \mathbf{u_{2}}$
$\mathbf{Y} = C_{1}\mathbf{u_{1}}e^{\lambda_{1}x} + C_{2}\mathbf{u_{2}}e^{\lambda_{2}x}$

#### Non diagonalizzabili

Deriviamo la prima equazione