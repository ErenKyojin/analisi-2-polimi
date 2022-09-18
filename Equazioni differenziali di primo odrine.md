---
alias
---
# Equazioni differenziali di primo ordine

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


# EDO del 1° ordine lineari

>[!def]
>Una EDO del 1° ordine lineare in forma normale è
>$$ y'(t) = a(t)y(t) + b(t) $$
>Con $a,b : J \subset \mathbb{R} \to \mathbb{R}$ continue
>
>$J$ è il più grande insieme su cui $a,b$ sono definite, si chiama [[EDO omogenea associata]] la forma
>$$ y'(t) = a(b)y(t) $$
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
>\begin{document}
>\begin{tikzpicture}
>\begin{axis}[
>axis x line = center,
>axis y line = center]
>\addplot[] {x=-1};
>\end{axis}
>\end{tikzpicture}
>\end{document}
>```

