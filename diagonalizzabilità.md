---
alias: diagonalizzabile
---
# Diagonalizzabilità
$A \in M_{n,n} \mathbb{R}$ è diagonalizzabile in $\mathbb{R}$

Se e solo se i suoi autovalori sono reali e regolari
Se e solo esistono $n$ autovettori di $A$ che formano una base di $\mathbb{R}^n$

$\lambda$ Autovalore di A si dice regolare se la sua [[molteplicità algebrica]] coincide con la [[molteplicità geometrica]], ossia

>[!oss]
>$$ p(\lambda) = \det(A - \lambda I) = c(\lambda-\lambda_{1})^{\alpha_{1}}(\lambda-\lambda_{2})^{\alpha_{2}}\dots(\lambda-\lambda_{k})^{\alpha_{k}} $$
>Con $\alpha_{1}+\alpha_{2}+\dots+\alpha_{k} = n$
>
>$\lambda_{1}$ è regolare $\Leftrightarrow$ gli autovettori relativi a $\lambda$ generano uno spazio vettoriale di dimensione $\alpha_{i}$
>
>A è diagnoalizzabile $\Leftrightarrow \lambda_{i}$ è regolare $\forall i =1,\dots ,k$ 


Condizioni sufficienti per la diagonalizzabilità
- Se $A \in M_{n,n} \mathbb{R}$ ha $n$ autovalori reali distinti
$\Rightarrow$ è diagonalizzabile
- Se $A \in M_{n,n} \mathbb{R}$ è simmetrica
$\Rightarrow$ è diagonalizzabile

E la matrice diagonale di $A$ è la matrice diagonale con gli autovalori presi con la propria molteplicità algebrica


>[!teorema]
>$A \in M_{n,n}\mathbb{R}$ diagonalizzabile reale con autovalori $\lambda_{1},\dots,\lambda_{n} \in \mathbb{R}$ e relativi autovettori linearmente indipendenti $\mathbf{v}_{1},\dots,\mathbf{v}_{n} \in \mathbb{R}^n$
>
>Un sistema fondamentale di soluzioni del sistema omogeneo $\mathbf{y}'(t) = A\mathbf{y}(t)$ è:
>$$ y_{o_{1}}(t) = e^{\lambda_{1}t} \mathbf{v}_{1}, \dots, \mathbf{y}_{o_{n}}(t)=e^{\lambda_{n}t}\mathbf{v}_{n} $$
>
>Equivalentemente l'integrale generale è
>$$ \mathbf{y}_{o}(t) = c_{1}e^{\lambda_{1}}\mathbf{v}_{1} + \dots+ c_{n}e^{\lambda_{n}t}\mathbf{v}_{n}\qquad(c_{1},\dots,c_{n} \in \mathbb{R})$$
>

>[!oss]
>$A\quad n \times n$ diagonalizzabile reale $\Rightarrow$ soluzioni esponenziali $\Rightarrow$ Generalizzando il caso $\Delta > 0$ delle [[EDO del secondo ordine]] lineari

