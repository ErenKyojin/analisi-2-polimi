---
alias: sistema differenziale lineare
---
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
>[!def] sistema differenziale lineare
>Un sistema differenziale lineare di ordine $n$ a coefficienti costanti è:
>$$ 
>\begin{cases}
>y_{1}'(t) = a_{1,1}y_{1}(t) + \dots + a_{1,n}y_{n}(t) + b_{1}(t) \\
>\vdots \\
>y_{n}'(t) = a_{n,1}y_{1}(t) + \dots + a_{n,n}y_{n}(t) + b_{n}(t)
>\end{cases} $$
>Con
>$A = a_{i,j} \in M_{n,n} \mathbb{R}$
>$b_{i} : J \subseteq \mathbb{R} \to \mathbb{R}$ funzioni continue
>$y_{i} : j \subseteq \mathbb{R} \to \mathbb{R}$ incognite



## [[Problema di Cauchy#Problema di Cauchy in sistemi differenziali lineari|Problema di Cauchy]]
Il problema di Cauchy nei sistemi differenziali lineari assume un carattere più generale, approfondimento nel file relativo.

# Soluzioni
>[!def]
>Dato un sistema differenziale lineare $n \times n$, omogeneo, chiamo sistema fondamentale di soluzioni una famiglia di $n$ soluzioni linearmente indipendenti:
>$$ y_{o_{1}}(t), \dots, y_{o_{n}}(t) $$
>Base dello spazio vettoriale delle saoluzioni


## Risoluzione esplicita di alcuni sistemi omogenei
1. $A \in M_{n,n} \mathbb{R}$ [[diagonalizzabilità|diagonalizzazione]] reale
2. $A \in M_{2,2} \mathbb{R}$ con autovalori complessi coniugati


## Integrale generale del sistema omogeneo
dato un sistema omogeneo $\mathbf{y}'(t) = A\mathbf{y}(t)$ con $A$ [[diagonalizzabilità|diagonalizzabile]], si scrive
$$ y_{o}(t) = e^{At} \cdot \mathbf{c} \qquad \mathbf{c} \in \mathbb{R}^n$$
Verifichiamo che questa forma coincida con quella del primo teorema della [[diagonalizzabilità]]

$$ \begin{align}
y_{o}(t) &= e^{At} \cdot \mathbf{c} = S \cdot e^{\Lambda t}\cdot \underbrace{ S^{-1} \cdot \mathbf{c} }_{ = \mathbf{c}\text{ nuova cost} } \\
&=S \cdot e^{\Lambda t} \cdot \mathbf{c} = \\
&=\begin{bmatrix}
\mathbf{v_{1}} & \dots &\mathbf{v}_{n}
\end{bmatrix} 
\cdot
\begin{bmatrix}
e^{\lambda_{1}t} & \dots & 0 \\
0& \ddots & 0 \\
0 & \dots & e^{\lambda_{n}t}
\end{bmatrix}
\end{align} $$