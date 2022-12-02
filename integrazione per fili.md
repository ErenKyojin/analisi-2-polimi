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
>\begin{axis}[colormap/viridis, grid]
>\addplot3[domain = -3:3, surf, samples=20]{x*y};
>\end{axis}
>\end{tikzpicture}
>\end{document}
>```
>#todo



Integrazioni per fili immaginiamo di ottenere la massa di un filo, per poi far passare il filo in ogni punto dello spazio


>[!def]
$$ E = {(x,y) \in D, h_{1}(x,y) \leq z \leq g_{2}(x,y)} $$
$f : E \to \mathbb{R}$ continua, allora $f$ è integrabile in $E$ e
 $$ \iiint_{E} \! f(x,y,z)\, \mathrm{d}x \, \mathrm{d}y\, \mathrm{d}z = \iint_{D} \! \left( \int_{h_{1}(x,y)}^{h_{2}(x,y)} \! f(x,y,z)\, \mathrm{d}z \right) \, \mathrm{d}x \, \mathrm{d}y$$

Spiegazione:
Fissato $(\overline{x}, \overline{y}) \in D$ restringo ed integro sul filo:

$$ \int_{h_{1}(\overline{x},\overline{y})}^{h_{2}(\overline{x},\overline{y})} \!f(\overline{x},\overline{y}, z) \, \mathrm{d}z  $$
Se $f \geq 0$ è la massa del filo
Poi svolgo l'integrale doppio, lasciando variare $(x,y) \in D$

>[!esempio]
>$$ I = \iiint_{E} \! x^2z\, \mathrm{d}x \, \mathrm{d}y\, \mathrm{d}z $$
$$ E = \{\underbrace{ 0  }_{ h_{1}(x,y) }\leq z \leq \underbrace{ \sqrt{ R^2 - x^2 - y^2 } }_{ h_{2}(x,y) }\} $$
Il testo ci comunica $h_{1}, h_{2}$, tuttavia non abbiamo il dominio $D$
> $$z \leq \sqrt{ R^2 - x^2 - y^2 } \implies z^2 \leq R^2 - x^2 -y^2 \implies x^2 + y^2 + z^2 \leq R^2$$
> Che è l'equazione di una calotta
> 
>Cerco D: $\sqrt{ R^2 - x^2 -y^2 } = 0 \iff x^2 + y^2 = \mathbb{R}^2$
>$\implies$
> $$ D = B_{R}(0) = \{(x,y) \in \mathbb{R}^2 : x^2 +y ^2 \leq R^2\} $$
> Integro per fili
> $$\begin{align}
 I &= \iint_{B_{R(0)}} \! \left( \int_{0}^{\sqrt{ R^2 - x^2 - y^2 }} \! x^2 z \, \mathrm{d}z  \right)\, \mathrm{d}x \, \mathrm{d}y  = \iint_{B_{R}(0)}x^2 \cdot \left( \int_{0}^{\sqrt{ R^2 - x^2 -y^2 }} \!z \, \mathrm{d}z   \right) \! \, \mathrm{d}x \, \mathrm{d}y = \\
&= \iint_{B_{R}(0)} \!x^2 \frac{R^2 - x^2 - y^2}{2} \, \mathrm{d}x \, \mathrm{d}y
\end{align}$$ 
>Passo in coordinate polari:
 >$$ B_{R}(0) = [0,R] \times [0, 2\pi] $$
 >Funzione integrando $(r \cos \theta)^2 \cdot \frac{R^2 - r^2}{2}$
 >
>$$ \begin{align}
I &=  \int_{0}^{2\pi} \! \left( \int_{0}^R \! (r\cos \theta)^2 \cdot \frac{R^2-r^2}{2} \fbox{$r$}\, \mathrm{d}r  \right) \, \mathrm{d}\theta 
=\\
&= \dots
\end{align} $$


### Come determinare $D$ senza l'intuizione geometrica?

- Determino $D$ cercando l'intersezione tra $h_{1}$ ed $h_{2}$

>[!oss]
>x semplice $E = \{(y,z) \in D, h_{1}(y,z) \leq x \leq h_{2}(y,z)\}$
>$$ \iint_{D} \! \left( \int_{h_{1}(y,z)}^{h_{2}(y,z)} \!f(x,y,z) \, \mathrm{d}x  \right)\, \mathrm{d}y \, \mathrm{d}z $$
>Analogo per y semplice

