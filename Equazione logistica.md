# EQUAZIONE LOGISTICA:
$y(t)$ gli individui infetti al tempo $t$
$y : \mathbb{R}^+ \to \mathbb{R}^+$

È logico pensare che l'incremento di infezioni dipenda dal numero di individui infetti.
Prima di studiare l'equazione logistica però vediamone una versione semplificata:

### Equazione di malthus
$$ y'(t) = ky(t) $$
con $y'(t)$ tasso di crescita, $k$ coefficiente di proporzionalità (tasso di natalità - tasso di mortalità)

Le soluzioni sono quindi la costante $y(t) = 0$ o $y(t) = ce^{kt}$,


```tikz
\usepackage{pgfplots}
\begin{document}
\begin{tikzpicture}
\begin{axis}[
axis y line = center,
axis x line = center,
]
\addplot[samples = 200, domain = -2:2] {exp(2*x)};
\draw (1,1) -- (2,2);
\end{axis}
\end{tikzpicture}
\end{document}
```
Che in effetti approssima bene inizialmente l'andamento epidemiologico, tuttavia non prende in considerazione la mancanza di risorse, per questo si utilizza l'equazione logistica

>[!def] Equazione logistica
>$$ y'(t) = ky(t) - hy(t)^2 $$
>Con il secondo termine $hy(t)^2$ che caratterizza la competizione, ha coe soluzioni $\frac{h}{k}$ costante 