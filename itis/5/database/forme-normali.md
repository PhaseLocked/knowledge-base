# Forme normali
Le forme normali sono proprietà dei database relazionali che servono a garantire l'assenza di certi difetti.


## Anomalie
### Anomalia di inserimento
Anomalia che rende impossibile inserire i dati.

Esempio: voglio creare un ingrediente, nella rispettiva tabella però ho inserito come colonna anche la lista allergeni, in questo momento non so chi sarà il fornitore dell'ingrediente e quindi anche quali allergeni contiene.
Per questo motivo non posso creare il nuovo elemento, in quanto il DBMS vuole tutti i valori per creare un nuovo record.

### Anomalia di aggiornamento
Aggiornamento che porta il database in uno stato inconsistente, cioè un'informazione non viene aggiornata in tutte le sue istanze, generando risultati anomali.

Esempio: ho una tabella con la lista degli studenti, i corsi a cui partecipano e il numero di matricola.
Se lo studente partecipa a più corsi e si vuole cambiare il numero di matricola, se non ci assicuriamo di aggiornare ogni singolo record avremo lo stesso studente con più matricole, e il database darà risultati inconsistenti.

### Anomalia di cancellazione
La cancellazione di un dato porta alla perdita di altri dati collegati che si desiderava mantenere.

## Definizioni
### Attributo
Una delle "colonne" della nostra tabella

### Dipendenza funzionale
Una dato è dipendente funzionalmente se la presenza di un un insieme di attributi A determina la presenza di un attributo B.

$B \rightarrow A$

Si dice che B dipende da A.

## Forme normali
### Prima
- Il contenuto di un attributo deve essere atomico (un solo valore, semplice e indivisibile).
- Il valore di qualsiasi attributo in un record sia un valore singolo del dominio, cioè valori nella stessa colonna devono essere dello stesso tipo.

### Seconda
- Rispetta la prima forma normale.
- Tutti i suoi attributi non-chiave dipendono dall’intera chiave, cioè non possiede attributi che dipendono soltanto da una parte della chiave.

*Nota: si applica solo in caso di chiavi composte*

### Terza
- Rispetta la seconda forma normale.
- Tutti gli attributi non-chiave dipendono direttamente dalla chiave, cioè non possiede attributi che dipendono da altri attributi che non sono in chiave.