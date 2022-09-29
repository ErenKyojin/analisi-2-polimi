# Determinante wronskiano
Supponiamo di conoscere $n$ soluzioni $y_{o_{1}},\dots,y_{o_{n}}$ di un [[Sistemi differenziali lineari|sistema differenziale lineare]] omogoeneo $n \times n$:
Sistema fondamentale $\Leftrightarrow$ esiste $t_{0} : \det(\mathbf{y_{o_{1}}}(t_{0}),\dots ,\mathbf{y_{o_{n}}}) \neq 0$


>[!def]
>Si chiama matrice wronskiana la matrice di funzioni ottenuta affiancando un sistema fondamentale di soluzioni
>$$ W(t) = \underbrace{ [\mathbf{y_{o_{1}}}(t) | \dots | \mathbf{y_{o_{n}}}(t)] }_{ \text{linearmente indipendenti} } $$

>[!oss]
>La matrice Wronskiana non è univocamente definita

>[!oss]
>Con la matrice Wronskiana possiamo scrivere in un modo compatto l'integrale generale del sistema omogeneo:
>$$ \mathbf{y}_{o}(t) = W(t) \cdot  $$