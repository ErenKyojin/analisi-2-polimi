# Sistemi differenziali lineari
Introduciamo l'argomento partendo da una considerazione, ossia la legge di Newton:
$$ F = ma \Rightarrow y''(t) = \frac{F}{m}$$
Infatti è semplice dimostrare che l'accelerazione è la derivata seconda dello spostamento.
Otteniamo quindi una [[EDO del secondo ordine]] #lineare
A questo punto definiamo due nuove funzioni:
- $y_{1} (t) = y(t)$ Posizione
- $y_{2}(t) = y'(t) = y_{1}'(t)$ velocità

$$ \begin{cases}
y_{1}'(t) = y_{2}(t) &\longrightarrow \text{la velocità è la derivata delle posizione} \\
y_{2}'(t) = y_{1}'' &\longrightarrow \text{l'accelerazione è la derivata della velcità}
\end{cases} $$
Possiamo quindi scrivere che:
$$ y''(t) = \frac{F}{m} \Leftrightarrow \begin{cases}
y_{1}'(t) = y_{2}(t) \\
y_{2}'(t) = \frac{F}{m}
\end{cases} $$
Arriviamo quindi all'osservazione di introduzione:
>[!oss]
>Una generica EDO lineare, di ordine $n$, può essere trasformato in un sistema di $n$ EDO lineari del 1° ordine.
>


## Forma matriciale

Ritornando all'esempio di introduzione,
$$ \begin{cases}
y_{1}'(t) = y_{2}(t) \\
y_{2}'(t) = \frac{F}{m}
\end{cases}
\Longleftrightarrow \begin{bmatrix}
y_{1}'(t) \\
y_{2}'(t)
\end{bmatrix}
= 
\begin{bmatrix}
0 & 1 \\
0 & 0
\end{bmatrix}
\cdot
\begin{bmatrix}
y_{1}(t) \\
y_{2}(t)
\end{bmatrix}
+
\begin{bmatrix}
0 \\
\frac{F}{m}
\end{bmatrix}
$$
Che possiamo riscrivere come:
$$ \mathbf{y'(t)} = A \cdot \mathbf{y(t)} + \mathbf{b(t)} $$
con
$$ \mathbf{y'(t)} = \begin{bmatrix}
y_{1}(t) \\
y_{2}(t)
\end{bmatrix}
\qquad
A =
\begin{bmatrix}
0 & 1 \\
0 & 0
\end{bmatrix}
\qquad
\mathbf{b(t)} = \begin{bmatrix}
0 \\
\frac{F}{m}
\end{bmatrix}
$$

# DEF
>[]