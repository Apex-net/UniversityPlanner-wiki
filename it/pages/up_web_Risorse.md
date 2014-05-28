
# Gestione risorse
prova

![](uploads/images/up_manual_20100303_130303.png)

Le funzioni di questa sezione permettono di effettuare prenotazioni per aule o risorse mobili e di gestire le prenotazioni qualora l'utente sia responsabile di qualche risorsa.

## Nuova Prenotazione
Consente di fare ricerche di disponibilità di strutture dell'ateneo ed inoltrare una richiesta di utilizzo (prenotazione) al gestore della struttura. In assenza di responsabile della struttura l'utente potrà direttamente occupare lo slot di tempo trovato libero nell'agenda della struttura.

![](uploads/images/up_manual_20100303_130600.png)

_Da data:_ data inizio del periodo all'interno del quale cercare una disponibilità di allocazione  

_A data:_ data fine del periodo all'interno del quale cercare la disponibilità di allocazione  

_Durata prevista impegno:_ ore previste di durata dell'evento-impegno da allocare  

_Selezione giorni della settimana:_ checkando i singoli giorni, la ricerca si concentra solo sui giorni indicati in modalità “OR”  

_Risorse necessarie:_ Caratteristiche delle risorse fisse necessarie allo svolgimento dell'impegno (tipo risorsa, numero posti, accesso alla rete, ecc..).
E' possibile anche richiedere la disponibilità di una risorsa fissa in particolare ricercandola dall'apposito campo ris.fissa, dove verrà aperta la lookup delle risorse fisse con le eventuali caratteristiche della risorsa stessa.  

_Logistica:_ strutture logistiche di afferenza della risorsa necessarie (Strutt. Org., corso di studio, dipartimento,…)  

_Ubicazione:_ Ubicazione fisica della risorsa che si richiede (Città, edificio, piano)  


![](uploads/images/up_manual_20100303_132425.png)


Il risultato della ricerca mostra gli slot liberi sulle singole risorse. I record sono ordinabili secondo diversi criteri (data, giorno, aula, ora, capienza) per dare modo all'utente di individuare meglio quelli desiderati.
Selezionare lo slot desiderato, e cliccare su “nuovo impegno”.Si accede alla funzione per creare l'evento-impegno per l'occupazione della risorsa (vedi  [Nuovo impegno](up_web_Calendari.ashx.md#Nuovo_Impegno_2)).

## Conferma prenotazioni
Questa funzione web è ad uso del responsabile di una risorsa fissa o mobile, per confermare o rifiutare le prenotazioni da parte di altri utenti. Ogni riga è una prenotazione che riporta: l'aula, data e ora della prenotazione, l'evento.

![](uploads/images/up_manual_20100303_180655.png)

L'operatore può consultare i dettagli dell'evento, e accettare oppure rifiutare la prenotazione. In caso di accettazione l'impegno passa da stato “prenotato” a stato “confermato”. In caso di rifiuto, viene cancellata la prenotazione.



## Gestione prenotazioni
E' la funzione web ad uso di chiunque abbia effettuato una prenotazione di una risorsa fissa o mobile. E' possibile monitorare lo stato globale della prenotazione e del dettaglio
delle risorse coinvolte.

![](uploads/images/up_manual_20100303_180557.png)


## Gestione rilevazione presenze
E' la funzione web ad uso del di un operatore addetto alla rilevazione delle presenze reali agli impegni schedulati. E' prevista analoga funzionalità che su supporto palmare.

Selezionare edificio e piano. Per default, come giorno di rilevazione si propone la data corrente. Lanciando la ricerca si recuperano tutti gli impegni in un piano-edificio

![](uploads/images/up_manual_20100303_171655.png)

I risultati possono essere ordinati per ora, evento, aula, per agevolare l'operatore nell'individuazione degli impegni da completare

![](uploads/images/up_manual_20100303_171743.png)


Dalla maschera di lancio è inoltre possibile stampare il report cartaceo di rilevazione presenze.

![](uploads/images/up_manual_20100303_171755.png)


**Gestione rilevazione presenze (Esami)**  

Nel caso in cui la rilevazione venga effettuata per Tipo Evento “Esami”, il modulo fornisce il dettaglio delle singole ore.

![](uploads/images/up_manual_20100303_171802.png)

Nell'esempio è riportato il caso di un Impegno della durata di 4 ore, dalle 8:30 alle 12:30, in cui sono state evidenziate le 4 righe relative all'inserimento delle presenze.

Tramite il bottone “Stampa Modulo” si accede alla stampa del modulo, che in questo caso è stata allineata alla form, riportando tante righe quante sono le ore di durata dell'impegno (4 in questo esempio).  

![](uploads/images/up_manual_20100303_171809.png)


Nel caso fossero state già caricate delle presenze, ma l'Impegno dovesse essere cambiato in una sua identificazione (es. incrementato di un ora), è possibile scegliere di ricaricare la form Tramite il bottone “Ricrea Dett Pres Esami”, previo aver selezionato una delle righe dell'Impegno modificato.

![](uploads/images/up_manual_20100303_171816.png)

![](uploads/images/up_manual_20100303_171823.png)

In questo modo verrà inserita una nuova riga, relativa allo slot orario aggiunto (nell'esempio 12:30), e erranno cancellate le presenze già caricate (solo per l'Impegno in esame).  
 
