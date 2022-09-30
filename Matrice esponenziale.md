# Matrice esponenziale
>[!def]
>Data $A \in M_{n,n} \mathbb{R}$ la matrice esponenziale $e^A$ è definita dalla serie:
>$$ e^A = \sum_{k=0}^\infty \frac{A^k}{k!} = I_{n} + A + \frac{A^2}{2} + \frac{A^3}{3!}$$
Che è convergente per ogni A


Se A è [[diagonalizzabilità|diagonalizzabile]], come si calcola $e^A$?
$$ A = S \Lambda S^{-1} $$
Con $\Lambda$ Diagnoale ed $S = (\mathbf{v}_{1} | \dots | \mathbf{v_{n}})$ autovettori.
Quindi 
$$ e^A = S e^\Lambda S^{-1} $$
$$ e^\Lambda = \begin{bmatrix}
e^{\lambda_{1}} &\dots &  0 & \dots &  0 \\
\vdots & &  \ddots & &  \vdots\\
0 & \dots  & 0 & \dots & e^{\lambda n}
\end{bmatrix} $$