# Integrazione per fili su regionie $z$ semplici

>[!def]
>$E \subseteq \mathbb{R}^3$ è $z$-semplice se 
>$$ E = \{(x,y,z) \in \mathbb{R}^3: (x,y) \in D, h(x,y) \leq z \leq h_{2}(x,y)\} $$
>con $D \subseteq \mathbb{R}^2$ regione semplice nel piano, $h_{1} \leq h_{2}$ continue su $D$
>
>```tikz
>\usepackage{pgfplots}
>\pgfplotsset{compat=1.16}
>\begin{document}
>\begin{tikzpicture}
>\begin{axis}[colormap/viridis]
>\addplot3[domain = -3:3, surf, samples=20]{x*y};
>\end{axis}
>\end{tikzpicture}
>\end{document}
>```

