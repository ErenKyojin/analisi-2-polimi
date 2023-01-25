
Iniziamo con un esempio:

>[!esempio]
>Segnale sonoro periodico:
>$$ f(x) = 3\cos(x) + \sin(2x) + \cos(10x) $$
>
>Per trasmettere il segnale è sufficiente comunicare i coefficienti, infatti
>
>Coefficienti di| n = 0 | n=1 | n=2 | n= 3 | ... | n=10 | ...
>--- | --- | --- | --- | --- | --- | --- | --- |
>$cos(x)$ |  0 | 3 | 0 | 0 | ... | -1 | ...
>$\sin(x)$ | 0 | 0 | -1 | 0 | ... | 0 | ...
>
>Così facendo si può ricomporre il segnale


>[!oss]
>Non si può decomporre attraverso [[serie di taylor]], in quanto vogliamo lavorare anche con segnali che non hanno derivabilità garantita, inoltre vogliamo avere la possibilità di isolare frequenze diverse.


La teoria di Fourier ci permette di decomporre un segnaler periodico (non necessariamente regolare) nella combinazione lineare di infinite funzioni trigonometriche:
$$ f(x) = a_{0} + \sum_{n=1}^\infty [a_{n} \cos(nx) + b_{n} \sin(nx)]$$
 >[!oss]
 >La proprietà di periodicità passa al limite
 
 