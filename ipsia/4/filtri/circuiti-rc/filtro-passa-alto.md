# Filtro passa-alto

### Esempio
![Filtro passa-alto](/resources/images/filtro-passa-alto.png)

## Definizione
I filtri passa-alto sono circuiti in corrente alternata il cui scopo è far passare la corrente ad alte frequenze.

Se analizziamo il grafico della tensione in uscita in relazione alla frequenza possiamo notare come, al salire della frequenza, la tensione aumenta.

![Grafico andamento tensione su frequenza](/resources/images/grafico-filtro-passa-alto.png)

## Frequenza di taglio
Come possiamo osservare l'effetto del filtro non è immediato, bensì graduale, per questo motivo dobbiamo definire arbitrariamente quando consideriamo il segnare passante e quando invece oscurato; la frequenza che divide queste due "bande" viene chiamata "frequenza di taglio".

Per convenzione stabiliamo che la frequenza di taglio sia quando il segnale in uscita dal filtro sia a $1 \over\sqrt{2}$ ($\pm 0.7071$ ovvero $\pm 70\%$) rispetto al segnale in ingresso.

Nel caso del circuito RC la formula per la frequenza di taglio è determinata dalle caratteristiche del circuito, nello specifico:

$ft = {1 \over 2\pi RC}$
