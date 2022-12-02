$$ E = \{(x,y,z) \in \mathbb{R}^3 : a \leq z \leq b, (x,y) \in E_{z} \text{ con } E_{z} \subseteq \mathbb{R}^2 \text{ semplice}\} $$

![[Pasted image 20221202120917.png]]

$$ \fbox{$\iiint_{E} \!f(x,y,z) \, \mathrm{d}x \, \mathrm{d}y\, \mathrm{d}z = \int_{a}^b \! \left(\iint_{E_{z}} \! f(x,y,z)\, \mathrm{d}x \, \mathrm{d}y\right)\, \mathrm{d}z$} $$

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.18}
\begin{document}
\begin{tikzpicture}
\begin{axis}[colormap/viridis]
\addplot3[domain = -3:3, surf, samples=20]{sqrt(1 - x^2 - y^2)};
\end{axis}
\end{tikzpicture}
\end{document}
```