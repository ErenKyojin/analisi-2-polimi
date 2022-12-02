Col cambiamento di variabile negli integrali doppi si intende solitamente il passaggio alle coordinate polari

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[axis lines = left]
\addplot[domain = -3:3, samples=25]{cos(deg(x))};
\end{axis}
\end{tikzpicture}

\hskip 5pt

\begin{tikzpicture}
\begin{axis}[axis lines = left]
\addplot[domain = -3:3, samples=200]{x};
\end{axis}
\end{tikzpicture}
\end{document}
```

$$\phi(r,t) = \begin{bmatrix}
\phi_{1}(r,\theta) \\
\phi_{2}(r,\theta)
\end{bmatrix} = \begin{bmatrix}
r \cos \theta \\
r \sin \theta
\end{bmatrix} = 
\begin{bmatrix}
x \\
y
\end{bmatrix}$$

$$ $$
Per il cambio di variabile nell'integrale dobbio dobbiamo inserire
 $$ \mathrm{d}x\, \mathrm{d}y \longrightarrow |\det J_{\phi}(r,\theta)| \mathrm{d}r, \mathrm{d}\theta $$
 Con $J_{\theta}$ [[matrice jacobiana]]
 $$ |\det J_{\phi}(r,\theta)| = |r \cos^2 \theta + r \sin^2 \theta| = |r| = r $$
E quindi la formula per il cambio di variabile è
$$ \iint_{E} \! f(x,y)\, \mathrm{d}x \, \mathrm{d}y = \iint_{D} \!f(r \cos \theta, r \sin \theta)\fbox{$r$}\, \mathrm{d}r \, \mathrm{d}\theta $$
Con $r$ evidenziato determinante della jacobiana

>[!esempio]
>$$ \iint_{E} \! \frac{xy^2}{x^2+y^2}\, \mathrm{d}x \, \mathrm{d}y = \iint_{D} \! r \cos \theta \sin^2 \theta\ r\, \mathrm{d}r \, \mathrm{d}\theta $$



Idea della formula di cambiamenti di variabili negli integrali:
- Supponiamo prima che la trasformazione $T : \mathbb{R}^2 \to \mathbb{R}^2$  sia lineare

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[axis lines = left]
\addplot[domain = -3:3, samples=25]{cos(deg(x))};
\end{axis}
\end{tikzpicture}

\hskip 5pt
$$
A
$$
\begin{tikzpicture}
\begin{axis}
\addplot{x};
\end{axis}
\end{tikzpicture}
\end{document}
```

$$ \begin{bmatrix}
x \\
y
\end{bmatrix} = T(u,v) = A \begin{bmatrix}
u \\
v
\end{bmatrix}$$
$$ Area(T(Q)) = |\det A|  \cdot Area(Q)$$
Poichè il volume è base per altezza devo tener conto di come cambia la misura della base

- Se la trasformazione non è lineare approssimo con la derivata prima

>[!oss]
>Condizione sulla trasformazione $\phi$ per poter fare il cambio di variabile nell'integrale $\phi$ di classe $C^1$ biunivoca tra aperti
>$\det J_{\phi(u,v)} \neq 0$ e limitato $\forall u,v$
>