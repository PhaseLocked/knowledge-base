# Bootstrap

## Cos'è
Il bootstrap, letteralmente "allacciarsi gli stivali" è la procedura eseguita da un computer per avviarsi.

## Fasi
- Caricamento del firmware nella RAM.
- Inizio esecuzione firmware da parte della CPU.
- POST (Power On Self Test): test dei componenti hardware fondamentali.
- EFI Partition lookup: il firmware cerca in tutte le memorie di massa del sistema per le partizioni di tipo EFI, che contengono i file necessari al caricamento del sistema operativo.
- Kernel loading: il kernel del sistema operativo viene caricato in RAM e eseguito dalla CPU.
- Mount: il kernel monta le partizioni che contengono il resto del sistema operativo.
- Init: una volta preparato il computer, il kernel avvia il primo processo, chiamato init, che avvierà tutti i servizi necessari all'utente.

## Definizioni

### Kernel
Il cuore del sistema operativo, si occupa di gestire le risorse hardware del computer, viene eseguito in modalità privilegiata a differenza di tutti gli altri programmi; tutti i programmi eseguiti in sieme al kernel si dice vivano in kernel-space, un errore critico in questo spazio causa un crash del sistema operativo.

### Modalità privilegiata/kernel-space
Una modalità di esecuzione della CPU, consente al programma di eseguire qualsiasi comando e concede accesso illimitato alle risorse del sistema.

### EFI Partition
Una partizione dedicata all'avvio, contiene i file necessari a caricare il kernel (o un programma intermedio come un bootloader).\
Nello specifico il firmware UEFI cerca un file in una posizione specifica con un nome specifico in base all'architettura della CPU del computer.\
Esempio: in un sistema x64 il file è
```
/EFI/Boot/bootx64.efi
```
mentre in un sistema Itanium è
```
/EFI/Boot/bootia64.efi
```
*Nota: il firmware non controlla maiuscolo e minuscolo.*

### Bootloader
Programma intermedio che carica un sistema operativo, utile come menu in computer dove più sistemi operativi sono installati, o dove il kernel non è in un formato accettato direttamente dal firmware.