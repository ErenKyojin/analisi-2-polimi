$$ A \subseteq \mathbb{R}^3 \int\!\int\!\int_{A} \! f(x,y,z)\, \mathrm{d}x  \! \, \mathrm{d}y  \! \, \mathrm{d}z  $$


# Integrali doppi

## Regioni semplici
>[!def] 
>$D \subseteq \mathbb{R}^2$ è detta regione-$y$ semplice se $$D = \{(x,y) \in \mathbb{R}^2 : x \in [a,b], g_{1}(x) \leq y \leq g_{2}(x)\}$$
> con $[a,b]$ limitato $g_{1} \leq g_{2}$ continue in $[a,b]$

>[!def]
>$D \subseteq \mathbb{R}^2$ è detta regione $x$-semplice se
> $$ D = \{(x,y) \in \mathbb{R}^2 : y \in [c,d], h_{1}(y) \leq x \leq h_{2}(y)\} $$
> Con $[c,d]$ limitato e $h_{1} \leq h_{2}$ continue in $[c,d]$



```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[axis lines = center]
\addplot[domain = -3.1:3.1, samples=200,color = red]{-sqrt(1 - x^2)};
\addplot[domain = -3.1:3.1, samples=200,color = blue]{sqrt(1-x^2)};
\end{axis}
\end{tikzpicture}
\end{document}
```

$g_{1} = -\sqrt{ 1 - x^2 }$ in rosso e $g_{2} = \sqrt{ 1 - x^2 }$ in blu, abbiamo una regione $y$-semplice, che possiamo immaginare colorarsi con linee verticali

Quindi la formula per l'area è
$$ Area(D) = \int_{a}^b \! (g_{2}(x) - g_{1}(x))\, \mathrm{d}x  $$
analogamente per le regioni $x$-semplici

>[!oss]
>Il volume del solido che ha $D$ come base
 e altezza $h$ è
 > $$ Volume = Area(D) \cdot h $$
 > Ossia 
 > $$ \int\!\int_{D} \!h \,  \mathrm{d}x  \! \, \mathrm{d}y  = Area(D) \cdot h$$

 
----- 


Significato geometrico dell'integrale doppio è il volume con segno sottostante alla curva, oppure la massa di una superficie 2d

---
## Integrabilità delle funzioni continue
Siano $D \subseteq \mathbb{R}^2$ è una regione semplice $f : D \to \mathbb{R}$ continua in $D$ allora $f$ è integrabile in $D$


>[!oss]
>Le regioni semplici per come le abbiamo definite sono chiuse e limitate, $f$ è continua, quindi per il [[teorema di Weierstrass]] $f$ è limitata su $D$
>- è possibile costruire una funzione limitata non continua non integrabile simile alla funzione di Dirichlet


>[!oss]
>Non vale l'implicazione opposta
>>[!ESEMPIO]
>>
>>$f(x,y) = 2$ sulla parte alta di un quadrato
>>$f(x,y) = 1$ sulla parte bassa di un quadrato
>>L'integrale di $f$ è la somma degli integrali

>[!oss]
>Se $\Omega \subseteq \mathbb{R}^2$ è unione di regioni semplici posso integrare sui vari pezzi separatamente e poi fare le somme




## Metodi di risoluzioni

### - [[Formule di riduzione nel piano]]

### - [[cambiamento di variabile]]



# Integrali tripli
Integrale di una funzione di tre variabili in una regione spaziale
$$ \iiint_{E} f(x,y,z) \mathrm{d}x\ \mathrm{d}y\ \mathrm{d}z \quad E \subseteq \mathbb{R}^3 $$
>[!oss]
>Se $f \geq 0$ interpretazione fisica: E è un corpo rigido nello spazio, f densità di massa


>[!oss]
>Se $f(x,y,z)=1$ costante
> $$ \iiint_{D} 1 \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z$$


## Metodi risolutivi

Vedremo [[integrazione per fili]] su regioni semplici dello spazio, dove si svolge prima un integrale singolo poi un integrale doppio ed [[integrazione per strati]] su regioni non necessariamente semplici ma che si prestano ad essere affettate e dove si svolge prima un integrale doppio poi un integrale singolo.
--- ---

### Applicazione fisica
Massa e baricentro

$E \subseteq \mathbb{R}^3$ $f : E \to \mathbb{R}, f \geq 0$ continua

- massa(E) = $\iiint_{E} \! f(x,y,z)\, \mathrm{d}x \, \mathrm{d}y\, \mathrm{d}z$
- baricentro è $(x_{b}, y_{b}, z_{b})$ dove 
$$ \begin{align}
x_{b} = \frac{1}{massa(E)} \cdot \iiint_{E} \! x f(x,y,z)\, \mathrm{d}x \, \mathrm{d}y\, \mathrm{d}z  \\
y_{b} = \frac{1}{massa(E)} \cdot \iiint_{E} \! y f(x,y,z)\, \mathrm{d}x \, \mathrm{d}y\, \mathrm{d}z  \\
z_{b} = \frac{1}{massa(E)} \cdot \iiint_{E} \! z f(x,y,z)\, \mathrm{d}x \, \mathrm{d}y\, \mathrm{d}z 
\end{align}$$


