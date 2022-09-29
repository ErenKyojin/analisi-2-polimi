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

>[!teorema]
>$A \in M_{n,n}\mathbb{R}$ diagonalizzabile reale con autovalori $\lambda_{1},\dots,\lambda_{n} \in \mathbb{R}$ e relativi autovettori linearmente indipendenti $\mathbf{v}_{1},\dots,\mathbf{v}_{n} \in \mathbb{R}^n$
>
>Un sistema fondamentale di soluzioni del sistema omogeneo $y'(t) = A$