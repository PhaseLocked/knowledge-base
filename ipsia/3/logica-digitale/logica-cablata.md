# WLC (Logica cablata)
Il tipo di sistema di controllo che analizziamo oggi si chiama logica cablata, consiste in un circuito composto da varie "porte logiche" che, connesse tra di loro, determinano il comportamento del circuito.

Queste porte logiche nel mondo reale possono essere componenti realizzati ad hoc o piccoli circuiti che possiamo realizzare in assenza di una soluzione già pronta.

Le porte logiche hanno uno o più ingressi e una sola uscita; esse operano in logica binaria, cioè i segnali sia in ingresso che in uscita possono essere o veri o falsi, accesi o spenti, aperti o chiusi etc...

## Tipi di porte logiche
![Porte logiche](/resources/images/porte-logiche.png)

Descriviamo il loro funzionamento e le rispettive tabelle di verità, ovvero le tabelle che descrivono il comportamento della porta ad ogni possibile valore che possiamo applicare ai suoi ingressi.

- NOT: inverte i segnali.

| 1 | X |
| :---: | :---: |
| 0 | 1 |
| 1 | 0 |

- AND: dall'inglese "e", l'uscita è attiva solo se tutti e due gli ingressi sono attivi.

| 1 | 2 | X |
| :---: | :---: | :---: |
| 0 | 0 | 0 |
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 1 | 1 |

- NAND: AND i cui l'uscita è invertita, cioè è come se aggiungessimo una NOT all'uscita di una AND.

| 1 | 2 | X |
| :---: | :---: | :---: |
| 0 | 0 | 1 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 1 | 0 |

- OR: dall'inglese "o" in senso largo, l'uscita è attiva quando almeno un ingresso è attivo.

| 1 | 2 | X |
| :---: | :---: | :---: |
| 0 | 0 | 0 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 1 | 1 |

- NOR: OR la cui uscita è invertita.

| 1 | 2 | X |
| :---: | :---: | :---: |
| 0 | 0 | 1 |
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 1 | 0 |

- XOR: OR esclusiva cioè "o" inteso in senso stretto, l'uscita è attiva se solo un'ingresso è attivo.

| 1 | 2 | X |
| :---: | :---: | :---: |
| 0 | 0 | 0 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 1 | 0 |

- NXOR: una XOR con l'uscita invertita.

| 1 | 2 | X |
| :---: | :---: | :---: |
| 0 | 0 | 1 |
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 1 | 1 |