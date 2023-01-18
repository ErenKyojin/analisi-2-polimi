---
alias
---
# Equazioni differenziali ordinarie di primo ordine

>[!def]
>Un'equazione differenziale del primo ordine è una relazione che coinvolge una funzione incognita $y(t)$ e la sua derivata prima $y'(t)$
>
>Espressa in forma normale:
>$$ y'(t) = f(t,y(t)) $$


>[!esempio]
>$$ y'(t) = t \sqrt{ y(t)^2 + 1 } $$
>è in forma normale con $f(t,s)= t\sqrt{ s^2 + 1 }$.
>Guardiamo poi il [[dominio]], per il quale dobbiamo considerare entrambe le variabili, abbiamo $S^2 + 1>0\ \ \forall s \in \mathbb{R}$.
>E invece $t$ che ha chiaramente $\mathbb{R}$ come dominio, il dominio di definizione dell'equazione differenziale è: $\mathbb{R} \times \mathbb{R} = \mathbb{R}^2$.
> $s$ inoltre dipende da $t$, abbiamo quindi $s = y(t)$.

>[!esempio]
>$$ y'(t) = \frac{1}{t}\qquad t>0  \Longrightarrow f(t,s) = \frac{1}{t} \cdot \fbox1$$
>$f$ non dipende esplicitamente da $s$. Il dominio di $f$:
>$$D = \{(t,s) : \mathbb{R}^2 : t \neq 0, s \in \mathbb{R}\} $$
>
>```tikz
>\begin{document}
>\usetikzlibrary{calc}
>\usetikzlibrary{patterns,arrows.meta}
>\begin{tikzpicture}[domain=0:4]
>\draw[color = lightgray, thin] (-3.9,-2.9) grid (3.9,2.9) node[midway, below left]{$\mathbf{0}$};
>\draw[-Stealth,color = red] (0,-3) -- (0,3) node[right,color=gray] {$\mathbf{x}$};
>\draw[-Stealth] (-4,0) -- (4,0) node[above] {$\mathbf{y}$};
>\end{tikzpicture}
>\end{document}
>```
>$$\begin{align}
>&y'(t) = \frac{1}{t},\quad t>0 \Rightarrow y(t) = \ln(t) + C\quad t>0, C \in \mathbb{R} \\ \\
>&y'(t) = \frac{1}{t},\quad t<0 \Rightarrow y(t) = \ln(-t) + C\quad t<0, C \in \mathbb{R}
>\end{align}
>$$

Le [[soluzioni]] di un equazione differenziale di primo ordine si possono trovare in modi diversi in base all'equazione.

# [[EDO a variabili separabili]]

# EDO del 1° ordine lineari

>[!def]
>Una EDO del 1° ordine lineare in forma normale è
>$$ y'(t) = a(t)y(t) + b(t) $$
>Con $a,b : J \subset \mathbb{R} \to \mathbb{R}$ continue
>
>$J$ è il più grande insieme su cui $a,b$ sono definite, si chiama [[EDO omogenea associata]] la forma
>$$ y'(t) = a(t)y(t) $$
>Quindi con $b(t) = 0$

>[!esempio]
>$$ \begin{align}
>&y'(t) + \frac{y(t)}{1+t} = \frac{2}{1+t}  \\
>&y'(t) = -\frac{y(t)}{1+t} + \frac{2}{1+t}  \\
>&a(t) = -\frac{1}{1+t},\qquad b(t) = \frac{2}{1+t}\quad J = \mathbb{R} \setminus {-1} \\
&f(t,y) = -\frac{y}{1+t} + \frac{2}{1+t}
>\end{align}$$
>Il dominio di $f : (\mathbb{R} \setminus {-1}) \times \mathbb{R} = J \times \mathbb{R}$
>
>```tikz
>\usepackage{pgfplots}
>\pgfplotsset{compat=1.16}
>\begin{document}
>\begin{tikzpicture}
>\begin{axis}[
>axis x line = middle,
>axis y line = middle,
>xmin = -3,
>xmax = 3,
>ymin = -3,
>ymax = 3,
>]
>\draw[dashed] (-1,-3) -- (-1,3);
>\end{axis}
>\end{tikzpicture}
>\end{document}
>```
>L'EDO è lineare rispetto alla $y$, avremo sempre $y^n$


Da qui deriva il [[principio di sovrapposizione]]

Per la soluzione [[formula risolutiva per EDO lineari del 1° ordine]]

## Esistenza e unicità globale per EDO del primo ordine non lineari

>[!teorema]
>$y'(t) = f(t,y(t))$
>$$ f : A \to \mathbb{R}\ con\ A = [a,b] \times \mathbb{R} $$
>
>$\dfrac{ \partial f }{ \partial y }$ esiste ed è continua in tutto $A$
>
>(cioè vale unicità locale in tutto $A$, quindi unicità globale)
>
>Se inoltre esiste $M > 0$ tale che
>$$ |\frac{ \partial f }{ \partial y } (t,y)| \leq M\quad \forall (t,y) \in A $$
>Allora $\forall (t_{0},y_{0}) \in A$ il problema di cauchy $y(t_{0}) = y_{0}$ ha soluzione unica, definita $\forall t \in [a,b]$

>[!oss]
>Se la EDO è lineare $f(t,y) = a(t)y + b(t)$ con $a,b : J \to \mathbb{R}$ continue, abbiamo già enunciato esistenza e unicità globale infatti:
>$$ [c,d] \subseteq J\quad \frac{ \partial f }{ \partial y } (t,y) = a(t) $$
>$$ |\frac{ \partial f }{ \partial y } (t,y)| = |a(t)| \leq \underset{t \in [c,d]}{\max}|a(t)| = M $$
>L'ultimo per il [[Teorema di Weierstrass#1D]] 

### Interpretazione intuitiva
$|\frac{ \partial f }{ \partial y } | \leq M$ cioè $f$ maggiorata da $a(t)y + b(t)$, quindi $y'$ cresce al più come $y$

