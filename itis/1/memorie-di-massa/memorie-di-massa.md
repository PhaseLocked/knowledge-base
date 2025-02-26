# Memorie di massa

## Dispositivi hardware

### HDD
Gli HDD o Hard Disk Drive sono dei dispositivi che  contengono dei dischi rigidi coperti da una polvere di metallo magnetizzata, su questi dischi passa una testina che legge e scrive i dati leggendo o cambiando la direzione dei poli del campo magnetico prodotto dalla polvere metallica.

La vita media di un HDD si misura normalmente in ore.

### SSD
Gli SSD o Solid State Drive sono delle memorie di massa caratterizzati dall'uso di chip di memoria NAND, ovvero circuiti dotati di celle dove una carica elettrica viene intrappolata./
Ogni cella può contenere uno o più bit, quindi invece che differenziare solo fra cella scarica o carica si possono riconoscere più livelli intermedi garantendo maggiore quantità di memoria, in base a questo le SSD vengono categorizzate come:
- SLC (Single Level Cell): celle con solo un bit.
- MLC (Multi Level Cell): celle con due bit.
- TLC (Triple Level Cell): celle a tre bit.
- QLC (Quad Level Cell): celle a quattro bit.

Ovviamente l'uso di più bit per cella comporta maggiore usura dell'SSD, in quanto una cella viene progettata per un certo numero di scritture, avendo più bit sulla stessa cella causa un maggior numero di scritture e quindi accorcia la vita della cella.

La vita media di una SSD si misura in TBW (Total Bytes Written), cioè nel numero totale di byte scritti per cui l'unità è progettata.

Quando viene rilevata l'imminenza del guasto dell'SSD il controller abilita la modalità di sola lettura per consentirci di trasferire i dati prima del guasto.

### Vista interna di HDD e SSD
![SSD vs HDD](/resources/images/ssd-vs-hdd.png)

## Suddivisione logica della memoria
Indipendentemente dalla tecnologia hardware che usiamo possiamo pensare alle memorie di massa come ad un blocco di dati.

Per gestire questo blocco di memoria usiamo le partizioni, a cui possiamo pensare come a delle "fette" di memoria.

Queste partizione necessitano di essere memorizzate da qualche parte, per questo scopo esistono il MBR (Master Boot Record) e la GPT (GUID Partition Table).

Nella nostra trattazione affronteremo solo il GPT.

### GPT

Il GPT è una tabella delle partizioni, si trova all'inizio del disco e possiede una copia di backup alla fine.
Si compone nel seguente modo:

- Protective MBR (LBA 0): MBR semplificato inserito per motivi di compatibilità con computer vecchi.

- Header GPT (Intestazione) (LBA 1): una sezione con una serie di informazioni riguardante la tabella delle partizioni come:

    - Codice identificativo della GPT.

    - Parti del disco usabili dall'utente.

    - Numero e dimensione delle voci della tabella delle partizioni.

    - La dimensione e posizione del GPT

    - Dimensione e posizione del GPT di backup.

    - Checksum della GPT (si usa per capire se i dati sono corrotti e se è necessario usare la GPT di backup).

- Tabella partizioni (LBA 2 - 33):una lista di partizioni, ogni voce contiene:

    - Il GUID del tipo di partizione (un codice che indica il tipo della partizione).

    - Il GUID univoco dell apartizione (Il codice che individua la partizione).

    - Inizio partizione (LBA di 64 bit).
    
    - Fine partizione (LBA di 64 bit).

### Struttura logica memoria di massa con GPT
![GPT](/resources/images/gpt-disk.png)