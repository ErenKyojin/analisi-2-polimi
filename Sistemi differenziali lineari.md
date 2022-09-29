# Sistemi differenziali lineari
Introduciamo l'argomento partendo da una considerazione, ossia la legge di Newton:
$$ F = ma \Rightarrow y''(t) = \frac{F}{m}$$
Infatti è semplice dimostrare che l'accelerazione è la derivata seconda dello spostamento.
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
>Una generica EDO