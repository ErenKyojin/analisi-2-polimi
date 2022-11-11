```mermaid
graph LR
	A[Derivabilità e </br> differenziabiltà] --> B[ottimizzazione </br> libera] --> C[ottimizzazione </br> vincolata]
```

# Derivabilità e differenziabilità


>[!multi-column]
>
>>[!esempio]
>>$$ hp: f \text { differenziabile in } \mathbf{x}_{0} $$
>>$$ f(\mathbf{x}_{0} + h) = f(\mathbf{x}_{0}) + \nabla \langle f(\mathbf{x}_{0}), \mathbf{x} - \mathbf{x}_{0}\rangle + o(||\mathbf{h}||)  $$
>>$$ f(\mathbf{x}) = f(\mathbf{x}_{0}) + \langle\mathbf{x}-\mathbf{x}_{0}\rangle + o (||\mathbf{x} - \mathbf{x}_{0}||) $$
>>piano tangente $z = f(\mathbf{x}_{0}) + \langle \nabla f(\mathbf{x_{0}}), \mathbf{x-\mathbf{x_{0}}}\rangle$
>
>>[!esempio]
>>$$ hp: f \text{ derivabile in } x_{0} $$
>>$$ f(x_{0}+h) = f(x_{0}) + f'(x_{0})h + o(|h|) $$
>>$$ f(x) = f(x_{0}) + f'(x_{0})(x-x_{0}) + o(|x-x_{0}|) $$
>>retta tangente $y = f(x_{0}) + f'(x_{0})(x-x_{0})$



## Derivate parziali e gradiente
>[!def]
>$A \subseteq \mathbb{R}^2$ aperto, $(x_{0},y_{0}) \in A\quad f : A \to \mathbb{R}$
>Le derivate parziali di $f$ in $x_{0},y_{0}$ sono:
>$$\begin{align}
> &\frac{ \partial f }{ \partial x } (x_{0},y_{0}) =\lim_{ h \to 0 } \frac{f(x_{0}+h,y_{0}) - f(x_{0},y_{0})}{h}    \\
> &\frac{ \partial f }{ \partial y } (x_{0},y_{0}) = \lim_{ h \to 0 } \frac{f(x_{0}, y_{0}+h) - f(x_{0},y_{0})}{h} 
>\end{align}$$
>Se entrambe le derivate parziali di $f$ esistono diciamo che $f$ è derivabile in $(x_{0},y_{0})$. In questo caso organizziamo le derivate in un vettore detto [[gradiente]] che si indica con $\nabla f(x_{0},y_{0})$


Ci sono due casi nel quale è necessario usare la definizione per determinare se $f$ è derivabile e per il cacolo delle derivate parziali:
1. $f$ è definita per casi:
 $$ f(x,y) = \begin{cases}
g(x,y)\qquad &(x,y) \neq \mathbf{x_{0}} \\
f(x) &x = \mathbf{x_{0}}
\end{cases} $$
In questo caso calcolo $\frac{ \partial f }{ \partial x } f(\mathbf{x_{0}})$ e $\frac{ \partial f }{ \partial y } f(\mathbf{x_{0}})$ e se entrambe esistono finiti allora $f$ è derivabile in $\mathbf{x_{0}}$ e ho ottenuto $\nabla f(\mathbf{x_{0}})$
altrimenti $f$ non è derivabile in $\mathbf{x}_{0}$
2. Nella definizione di $f$ compare $t^\alpha$ con $\alpha \in (0,1)$ o $|t^\alpha|$ con $\alpha \in (0,1]$ per qualche $t  = g(x,y)$
Devo usare la definizione $\forall (x,y)$ tale che $g(x,y) = 0$

In tutti gli altri casi posso concludere che $f$ è derivabile senza dover sfruttare la definizione.


# Differenziabilità
>[!def]
>$A \subseteq \mathbb{R}^2$ aperto $f : A \to \mathbb{R}$
>Diciamo che $f$ è differenziabile in $\mathbf{x_{0}} = (x_{0},y_{0}) \in A$ se
>1. $f$ è derivabile in $\mathbf{x_{0}}$
>2. $f(\mathbf{x_{0}+h}) = f(\mathbf{x_{0}}) + \langle \nabla f(\mathbf{x_{0}}),\mathbf{h}\rangle + R(\mathbf{h})$ con $R(\mathbf{h}) = o(||\mathbf{h}||)$ cioè $$\lim_{ \mathbf{h} \to (0,0)} \frac{R(\mathbf{h})}{||\mathbf{h}||} = 0$$
>