---
alias: sistema differenziale lineare
---
# [[Sistemi]] differenziali lineari
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


### 1. Integrale generale del sistema omogeneo
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
 \cdot 
\begin{bmatrix}
c_{1} \\
\vdots \\
c_{n}
\end{bmatrix} =  \\
&=c_{1}e^{\lambda t} \mathbf{v}_{1} + \dots + c_{n} e^{\lambda _{n}t} \mathbf{v}_{n}
\end{align} $$

>[!error]
>Se a non è diagonalizzabile reale, le soluzioni non sono tutte esponenziali!


>[!tldr]
>$A$ $\quad n \times n$ diagonalizzabile
>$\lambda_{1}, \dots , \lambda_{n}\rightarrow$ autovalori
>$\mathbf{v}_{1},\dots,\mathbf{v}_{n} \to$ autovettori linearmente indipendenti
>$S=(\mathbf{v_{1}},\dots,\mathbf{v_{n}})$
>$$ y_{o}(t) = c_{1}e^{\lambda_{1}}t \mathbf{v}_{1} + \dots + c_{n}e^{\lambda_{n}t}\mathbf{v}_{n} $$
>$$ e^A = S \begin{bmatrix}
>e^{\lambda_{1}}  & &0 \\
>&\ddots \\
>0& & e^{\lambda_{n}}
>\end{bmatrix} 
>S^{-1}$$

### 2.  con autovalori complessi coniugati

$A \in M_{2,2}$ con autovalori $\lambda, \overline{\lambda}$ con $Im(\lambda) \neq 0$
Chiamo $\mathbf{v} \in \mathbb{C}^2$ L'autovettore associato a $\lambda$ (o $\overline{\lambda}$, nel cui caso è sufficiente cambiare i $\lambda \text{ in }\overline{\lambda}$
Un sistema fondamentale di soluzioni del sistema omogeneo
$$ \mathbf{y}'(t) = A\mathbf{y}(t) $$
è:
$$ \mathbf{y}_{o_{1}} = Re(e^{\lambda t}\mathbf{v})\qquad \mathbf{y_{o_{2}}}= Im(e^{\lambda t} \mathbf{v}) $$
Equivalentemente l'integrale generale è dato dalla combinazione:
$$ y_{o}(t) = c_{1}Re(e^{\lambda t}\mathbf{v}) + c_{2}Im(e^{\lambda t}\mathbf{v}) $$
>[!oss]
>Nel caso di un sistema che deriva da una [[EDO del secondo ordine]], questo caso corrisponde al caso $\Delta < 0$.

>[!oss]
>$$ ay''+by' + cy = 0\qquad\qquad y = y_{1},\quad y_{2} = y_{1}' $$
>$$ \begin{cases}
>y_{1}' = y_{2} \\
>y_{2}' = -\frac{b}{a}y_{2} -\frac{c}{a}y_{1}
>\end{cases} $$
>La cui matrice $A$ è:
>$$ A = \begin{bmatrix}
>0 & 1 \\
>-\frac{c}{a} & -\frac{b}{a}
>\end{bmatrix} $$
>Per le [[EDO del secondo ordine]] lineari, osservando come le impostiamo, avremo sempre 0 ed 1 nella colonna superiore

>[!esempio]
>$$ \begin{cases}
y_{1}' = 2y_{1} + y_{2} \\
y_{2}' = -y_{1} + 2y_{2}
\end{cases}
\qquad A= 
\begin{bmatrix}
>2 & 1 \\
-1 & 2
\end{bmatrix}$$
>Autovalori:
>$$ \begin{vmatrix}
>2-\lambda & 1 \\
>1 & 2-\lambda
\end{vmatrix} = (2-\lambda)^2+1 \geq 1$$
Quindi non ha zeri reali, e gli zeri complessi sono:
>$$ \Rightarrow (2-\lambda^2)= -1\qquad 2 - \lambda = \pm i\qquad \lambda = 2 \pm i $$
>Scegliamo $\lambda = 2+i$
>Cerchiamo un autovettore relativo a $\lambda$:
>$$ (A - \lambda I) \begin{bmatrix}
>v_{1} \\
v_{2}
>\end{bmatrix} = 0 \Rightarrow
>\begin{bmatrix}
>-i & 1 \\
>-1 & i
\end{bmatrix}
>\begin{bmatrix}
>v_{1} \\
>v_{2}
>\end{bmatrix}=0 \Rightarrow \mathbf{v = \begin{bmatrix}
>1 \\
>i
\end{bmatrix}}
>$$
>Abbiamo quindi un sistema fondamentale di soluzioni omogene $y_{o_{1}}, y_{o_{2}}$:
>$$ \begin{align}
>&y_{o_{1}} (t) = Re(e^{\lambda t} \mathbf{v}) = Re\left(e^{(2+i)t} \begin{bmatrix}
1 \\
i
\end{bmatrix}\right) \\
>&y_{o_{2}}(t) = Im(e^{\lambda t} \mathbf{v}) = Im \left(e^{(2+i)t}\begin{bmatrix}
>1 \\
i
\end{bmatrix}\right)
\end{align} $$
>E infine attraverso la [[formula di eulero]]
>
>$$ \begin{align}
>&\mathbf{y}_{o_{1}}(t) = Re \begin{pmatrix}
>e^{2t}(\cos t + i \sin t) \\
>i e^{2t}(\cos t + i \sin t)
>\end{pmatrix} = \begin{bmatrix}
>e^{2t} \cos t \\
>-e^{2t} \sin t
>\end{bmatrix} \\
>&\mathbf{y}_{o_{1}}(t) = \begin{bmatrix}
>e^{2t} &\sin t \\
>e^{2t} &\cos t
\end{bmatrix}
>\end{align} $$



## Sistemi lineari non omogenei
Per risolvere un sistema non omogeneo:
1. Risolvo il sistema omogeneo associato
Trovo $n$ soluzioni linearmente indipendenti (ossia una [[Determinante wronskiano|matrice wronskiana]] $W(t)$)
$\Rightarrow$ l'integrale generale del sistema omogeneo è $W \cdot \mathbf{c},\quad \mathbf{c} \in \mathbb{R}^n$

2. (a) cerco una soluzione particolare col metodo di somiglianza ed applico il [[teorema di struttura]] $$ \mathbf{y} (t) = \mathbf{y}_{o}(t) + \mathbf{y}_{p}(t) = W(t) \cdot \mathbf{c} + \mathbf{y_{p}}(t) $$
2. (b) alternativamente uso $W(t)$ per calcolare l'integrale generale:
$$ \begin{align}
y(t) &= W(t) \left( \int \! [W(\tau)]^{-1} \cdot \mathbf{b}(\tau)\, \mathrm{d} \tau  \right)  \\
&= W(t) \int \! W(\tau)^{-1}\, \mathrm{d} \tau + W(t) \cdot \mathbf{c}
\end{align}$$

**In particolare** se $A$ è diagonalizzabile reale, una matrice Wronskiana è:
$$ W(t) = e^{At},\qquad\mathbf{y}(t) = e^{At}\left[ \int \! e^{-A \tau} \cdot \mathbf{b} (\tau)\, \mathrm{d}\tau + \mathbf{c} \right] $$
Analogo alla [[formula risolutiva per EDO lineari del 1° ordine]]

>[!oss]
>Questa formula ci richiede di integrare un vettore componente per componente

>[!esempio]
