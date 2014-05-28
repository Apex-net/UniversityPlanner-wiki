
# Configurazione
Il sistema richiede una configurazione preliminare, che è possibile gestire direttamente via web dall'apposito menù, che da accesso a tutte le tabelle essenziali. Il sistema di configurazione gestisce anche i dati necessari alla pianificazione logistica delle attività. 

Le tabelle del sistema sono essenzialmente raggruppate in “anagrafiche di base” e nelle tabelle contenenti le principali entità in gioco: Persone, Risorse, Eventi, Calendari. Ciascuna di queste contiene a sua volta una serie di tabelle di configurazione di base.

## Anagrafiche di base
Le anagrafiche di base sono tutte le tabelle delle principali entità strutturali del programma

![](uploads/images/Configurazione.png)

### Tabelle importate da ESSE3:
Di questa sezione fanno parte tutte le tabelle che vengono importate da ESSE3, per le quali dunque sono disabilitate le funzioni di aggiunta e cancellazione. E' invece possibile modificarne le caratteristiche. A queste tabelle vanno aggiunte quella delle persone (solo per quanto riguarda i docenti) e delle risorse fisse.
Per aggiungere nuovi dati necessari occorre quindi aggiungere prima il dato in ESSE3 ed effettuare l'import del nuovo dato

### Strutture organizzative (_Facoltà prima della Rel. 12.01.00.00_)
La tabella delle Strutture organizzative dell'ateneo, che sono caratterizzate da codice e  descrizione.  

**NB:** questa anagrafica sostituisce Facoltà e Dipartimenti, che vengono unite in un'unica tabella con tipologia differente.

### Città
La tabella presenta l'anagrafica delle città italiane

### Edifici
La tabella consente di gestire le anagrafiche degli edifici a disposizione dell'ateneo per la pianificazione delle risorse fisse o mobili.

### Tipi Attività
Sono le descrizioni codificate delle tipologie di attività didattica, con cui vengono tipicamente dettagliati gli insegnamenti (lezioni, laboratori, esercitazioni, ecc…)

### Attività Didattiche
Le attività didattiche sono gli insegnamenti, o comunque tutto ciò che corrisponde all' erogazione di una attività formativa universitaria volta al riconoscimento nella carriera degli studenti. Ai fini del sistema vengono qui gestiti come dati fondamentali sono codice e descrizione

### Corsi
Questa tabella contiene i codici e le descrizioni dei corsi di laurea offerti dall'ateneo. Per corsi di studio nella eccezione più ampia si intendono tutti i corsi oggetto di programmazione didattica o pianificazione logistica (Corsi di laurea, dottorati, corsi interni per il personale, ecc..)

### Qualifiche
Sono l'attributo fondamentale del tipo persone “docenti”, che indicano quale ruolo essi possono assumere nelle attività didattiche. In base alla qualifica (codice e descrizione) un docente sarà classificato inoltre come interno o esterno.

### Lingue
Lingue con cui gestire il programma di studio della singola attività didattica.

### Settori Scientifico Disciplinari
Tabella dei settori scientifico disciplinari codificati dal MIUR (MAT/01, MAT/02,…)

### Ambiti
Sono i raggruppamenti ufficiali dei settori scientifico disciplinari stabili da MIUR, a questi possono aggiungersi presso alcuni atenei ambiti di sede

### Tipo Attività Formativa (TAF)
Tabella delle tipologie di attività formative codificate dal MIUR (Es: di base, caratterizzante, affine-integrativa,…)

### Tipi Partizionamento
E' un attributo di una attività didattica che indica con quale criterio sono stati eventualmente divisi (AK, LZ, matricole pari/dispari, ecc..)

### Percorsi
Sono i curricula, gli indirizzi che lo studente può scegliere all'interno di un Corso di studio.

### Anni Accademici
La tabella memorizza tutti gli anni accademici con i quali il sistema dovrà lavorare

### Contesti
Contiene tutti i vari contesti all'interno dei quali opererà il programma.

### Modalità didattiche
Modalità di insegnamento delle attività didattiche.

### Sedi
In questa tabella sono memorizzate tutte le sedi italiane.

### Tipi Corso
Contiene tutti i tipi di corso ai quali possono iscriversi gli studenti.

### Tipi Strutture Organizzative
Memorizza tutti i vari tipi di Strutt. Org.



## Import/export dati

### Import da ESSE3 
La funzione consente di effettuare import di dati da ESSE3 

![](uploads/images/up_manual_26022010_161925.png)

In particolare consente l'import delle **tabelle di base** (vedi anagrafiche successive), per le quali la procedura effettua un import incrementale: cioè è possibile lanciare la procedura di import più volte senza impattare sui dati delle tabelle già importati.   

Per quanto riguarda invece gli **eventi **(attività didattiche ed esami) e i **vincoli **(regole di scelta) la procedura di import <span style="text-decoration:underline">**riscrive tutte le volte**</span> i dati, <span style="text-decoration:underline">**cancellando**</span> quelli precedentemente inseriti, è quindi fortemente sconsigliato allo stato attuale effettuare l'import in più soluzioni.   


N.B è necessario impostare correttamente **l'anno accademico sorgente **e quello di **destinazione**. Tipicamente verrà fatto l'import da un anno precedente solo per creare la base dati di lavoro per la programmazione didattica.   

  Al termine dell'elaborazione viene visualizzato il log della procedura, con segnalazione del numero di record importati e degli errori o scarti effettuati 
  


### Trace  
  La funzione consente di visualizzare l'esito delle procedure massive di caricamento dati in UniversityPlanner 


#### Messaggi di LOG

  *  **Inizio Procedura / Fine Procedura**
I messaggi di Inizio e Fine Procedura assumono valori significativi nel momento in cui l'utente finale sceglie di eseguire la copia template impegni per tutte le strutture organizzative, in quanto nel log viene inserita una riga per identificare l'inizio e la fine della copia template di ogni singola Struttura organizzativa. Tutto quello che si trova tra questi due ID è riguardante la struttura organizzativa presente nella descrizione.
![](uploads/images/up_manual_20110714_151100.png)
<br/>
  *  **Errore**
La tipologia Errore nei messaggi, viene usata per evidenziare quegli impegni che sono stati copiati ma con qualcosa di mancante (es. date periodo).
Per esempio se non è stata trovata la corrispondenza del periodo nel calendario degli eventi futuri, il log riporta il messaggio: <br/>
`date del periodo non inserite per l'impegno collegato all'evento DESCRIZIONE EVENTO e ANNO.`<br/>
Inoltre sempre in questa categoria di messaggi possiamo trovare gli errori che sono stati rilevati dal data base durante l'inserimento o la cancellazione di impegni, in questo caso è necessario contattare direttamente il sistemista.<br/>
  *  **Warning**
Nei Warning vengono racchiusi tutti quei messaggi nei quali ci sono stati piccoli problemi, tipo se i numeri degli eventi logici e fisici sono di numeri diversi tra i due anni, di seguito un elenco dei possibili messaggi di warning:<br/>
`Evento Futuro NON Trovato Evento: 2010|2011|1|2008|0115G|P0001|120006|120006/2|N0\N0|########|S1<br/>
Numero eventi diversi tra i due anni, per l'evento di partenza: 2010|2011|1|2003|0112D|P0003|22051|22051|A1\LZ|########|S2 <br/>
TEMPLATE_IMPEGNI date del periodo non inserite per l'impegno collegato all'evento 21018 Statistica per i mercati finanziari|2011<br/>
Presenza di più Eventi Riga Evento: 2010|2011|3|2008|0327G|P0403|140077|140077/1|N0\N0|########|S1`<br/>
La stringa che è presente nei messaggi di warning è così composta:<br/>
`2010|2011|1|2008|0115G|P0001|120006|120006/2|N0\N0|########|S1`<br/>
`''ANNO di Partenza | Anno di Arrivo | progressivo Strutt. Org. | Anno Ordinamento | Codice Corso | Codice Percorso |  Codice Attività Didattica |  Codice UD | Codice Partizionamento | Codice Sede | Codice Periodo''`<br/>
  *  **Altro**
Con la tipologia **ALTRO**, il sistema evidenzia il numero di impegni che ha trovato nell'anno di partenza e quelli che ha copiato nell'anno di arrivo. <br/>
![](uploads/images/up_manual_20110714_125200.png)<br/>
In questo modo se si sceglie in caso di copia modalità incrementale, si riesce ad avere una visione immediata di quanti impegni sono stati copiati da un anno accademico all'altro.

### Allineamento Docenti 

La maschera "Allineamento Docenti" permette di verificare gli impegni di Didattica che hanno docenti assegnati non allineati con i docenti assegnati a livello di Evento. Una volta verificati questi impegni c'è la possibilità di riallineare i docenti assegnati, cioè sostituire i docenti assegnati all'impegno con quelli assegnati all'Evento dell'impegno (che si assume siano quelli validi). La visibilità di questa maschera è esclusiva per gli utenti di ruolo "Supervisore" e si accede dal menu di Configurazione, Import Export, Allinea Docenti. La maschera permette di cercare gli impegni in due modalità:<br/>
1.  ricerca per calendario
2.  ricerca da data a data



#### Ricerca modalità Calendario
<br/>
![](uploads/images/up_manual_20110714_100500.png)

<br/>
<br/>
Questa modalità di ricerca permette di selezionare un calendario dalla drop down list, la funzione recupera tutti gli impegni degli eventi che hanno tale calendario associato. Per facilitare la ricerca si può scrivere dentro la dropdown list e in automatico verranno filtrati i calendari che iniziano con tale descrizione.

#### Ricerca modalità Da data A data
<br/>
![](uploads/images/up_manual_20110714_101000.png)

<br/>
<br/>
Questa modalità di ricerca permette di selezionare una data inizio e data fine per le quali verranno filtrati gli impegni. 
<br/><br/>

Una volta impostato un filtro cliccando sul pulsante "Cerca" verrà elaborata la ricerca degli impegni non allineati per tale filtro. Terminata l'elaborazione verrà visualizzata una griglia con l'elenco degli impegni trovati e con le relative caratteristiche.<br/>

<br/>
![](uploads/images/up_manual_20110714_101300.png)<br/>


Individuati gli impegni non allineati si possono selezionare quelli che si intendono allineare (per selezionarli o deselezionarli tutti utilizzare i due pulsanti in alto nella prima colonna). Una volta selezionati cliccando sul pulsante "Allinea Docenti Impegno" verrà lanciata l'elaborazione di allineamento per gli impegni selezionati, alla fine di tale operazione verrà restituito un messaggio all'utente che avvisa se l'operazione è andata a buon termine o se sono occorsi degli errori.

### Copia Settimana Template (dalla release 11.02.00.00)

La maschera “Copia Settimana Template” è visibile ai soli utenti con ruolo: supervisore, configuratore e pianificatore.<br/>
La maschera permette la copia  degli impegni presenti di una certa Strutt. Org. nella settimana template da un anno accademico all'altro. <br/>
Gli utenti con ruolo supervisore e configuratore possono permettere la copia della settimana template anche per “tutte le Strutt. Org.”.<br/>

![](uploads/images/up_manual_20110714_105400.png)

La procedura di copia, parte considerando tutti gli eventi dell'anno di partenza che sono **visibili** e con **stato diverso da ELI**, confronta a seconda della metodologia di copia e a seconda dei vari flag attivati dall'utente, gli eventi dell'anno successivo che siano visibili e con stato diverso da ELI.<br/>
A seconda dell'integrazione di UP si comporta in modo differente.<br/>
_Integrato con ESSE3_, oltre all'_anno accademico_ e la _Strutt. Org._ scelti, gli eventi dell'anno successivo vengono equiparati considerando l'offerta didattica, così considerata:<br/>
_Anno Ordinamento, Corso, Percorso di studio, Attività Didattica, UD _<br/>
Mentre per quanto riguarda l'_Anno Regolamento_  viene equiparato con l'anno di regolamento + anni di differenza tra gli anni da copiare. Inoltre viene considerata anche la parte della Logistica equiparando il _Partizionamento studenti_ e il _Periodo_ <br/>
_integrato con U-GOV_, la procedura di copia considera, oltre _Strutt. Org._ e l'_anno accademico_, la seguente offerta didattica:<br/>
_Anno Ordinamento, Corso, Percorso di studio, Attività Didattica, UD _<br/>
E per l'**Anno Regolamento**  si considera sommando la differenza tra gli anni da copiare.<br/> 
Per la parte della Logistica di U-GOV si considera oltre al _Partizionamento studenti_ e _Periodo_ anche, se presente, la _Sede_.<br/>
Analizziamo ora i vari campi di scelta che l'utente può selezionare presenti nella maschera.<br/>
Il **Tipo Copia**, può essere:  _Incrementale_ o _Cancella_ e _Copia_.<br/><br/>

![](uploads/images/up_manual_20110714_111500.png)<br/><br/>

Modalità_** Incrementale**_: il sistema se trova l'evento corrispondente con i criteri sopra riportati, presente nell'anno accademico di arrivo, controlla che tale evento non sia già presente nella settimana template del nuovo anno. Se è presente non esegue alcuna operazione, mentre se non è presente inserisce l'impegno, considerando anche gli altri criteri scelti dall'utente.<br/>

Modalità _Cancella e Copia_: dopo aver trovato l'evento corrispondente nell'anno nuovo, **cancella** tutti gli impegni presenti nella settimana template per quella Strutt. Org. e per quell'anno. Poi a seconda delle scelte dell'utente esegue la copia.<br/>

Scelte aggiuntive da parte dell'utente finale<br/>
![](uploads/images/up_manual_20110714_120800.png)
<br/><br/>
  *  **Copia Veloce**
<span style="text-decoration:underline">Check attivo</span>: copia direttamente l'impegno presente nella settimana template, se l'evento fisico dell'anno successivo, è stato trovato, senza eseguire successivi controlli.<br/>
<span style="text-decoration:underline">Check NON attivo</span>: controlla il pacchetto completo dell'evento dell'anno successivo, andando a confrontare tutti gli eventi logici dell'anno di partenza con gli eventi logici dell'anno successivo. I confronti tra i due eventi vengono eseguiti sempre con le chiavi condizionali riportate sopra<br/>
Se il sistema trova la corretta corrispondenza tra eventi logici, allora copia direttamente l'impegno.<br/>
Durante la copia sia che sia alzato o meno il check del copia veloce, il sistema esegue altri controlli riguardanti i **calendari** presenti negli eventi e le **date del periodo** dell'impegno.<br/>
Se le date del periodo dell'impegno di partenza sono presenti, allora il sistema cerca il calendario corrispondente dell'evento futuro, ed inserisce l'impegno nella settimana template con le date trovate. Se viene a mancare la corrispondenza tra i due calendari, allora nel nuovo impegno vengono inserite le stesse date dell'impegno di partenza aumentando il solo anno nella data. <br/>
Mentre se le date del periodo dell'impegno non sono presenti, cerca sempre se esiste il calendario dell'evento, altrimenti inserisce l'impegno privo di date e segnala all'utente nel log l'errore verificatosi.<br/><br/>

  *  **Copia Stato Bozza**
<span style="text-decoration:underline">Check attivo</span>: il sistema cerca di copiare anche gli impegni presenti nella settimana template dell'anno di partenza, nella settimana template dell'anno successivo.<br/>
<span style="text-decoration:underline">Check NON attivo</span>: il sistema esclude dalla copia gli impegni che non sono stati pubblicati.<br/><br/>

  *  **Copia Note**
<span style="text-decoration:underline">Check attivo</span>: vengono copiate le eventuali note presenti nell'impegno della settimana template.<br/>
<span style="text-decoration:underline">Check NON attivo</span>: le note non vengono considerate.<br/>
<br/>
Dopo aver inserito i criteri di copia, l'utente finale esegue l'operazione cliccando sul pulsante copia, a questo punto il sistema elabora e restituisce con un messaggio l'esito della operazione. Se l'operazione ha ottenuto esito positivo, il sistema visualizza un LOG dove vengono segnalate le operazioni eseguite.<br/>
Analisi del LOG che il sistema restituisce ad operazione conclusa.<br/>
L'utente finale nel momento della conclusione della copia della settimana template, si trova una maschera riportata sotto, dove vengono visualizzati i messaggi salvati sul LOG dal sistema durante l'operazione.<br/>

![](uploads/images/up_manual_20110714_125100.png)<br/>
A seconda del tipo del messaggio (Inizio Procedura, Altro, Warning, Errore, Fine Procedura) l'utente visualizza immediatamente se sono stati rilevati ERRORI durante l'operazione.



## Persone

Le persone raccolgono i dati di tutti i principali attori dell'attività universitaria, i cui dati servono sia ai fini della organizzazione che dell'accesso come utilizzatori al sistema. Le persone sono essenzialmente gestite sia come singoli che come gruppi. 

![](uploads/images/up_manual_26022010_165437.png)

### Autorizzazioni

La finestra delle Autorizzazioni, si trova nella voce di menù Configurazione/Persone/Autorizzazioni ed è visibile ai soli utenti con ruolo Supervisore e Configuratore.
A differenza delle altre finestre, in tale maschera se l'utente si posiziona su una riga, si trova in automatico in modalità di modifica dei dati, e posizionandosi nella riga successiva, ha il salvataggio automatico delle modifiche apportate precedentemente.

In tale maschera l'utente può decidere se rendere visibile, modificabile agli utenti finali, ciascuna form, voce di menù principale, di menù secondario e report.
Per menù principale si intende la toolbar che si trova in alto a destra dello schermo.

![](uploads/images/Toolbar_Principale.png)

Per menù secondario invece si intende il menù che si trova a sinistra del browser.

![](uploads/images/up_manual_26022010_165437.png)

E' consigliabile all'utente Configuratore, raggruppare tale schermata per Tipo Persona e per Tipo Funzione, in modo tale che abbia immediatamente una visuale completa di cosa è visibile o non all'utente finale.

![](uploads/images/Autorizzazioni.png)

La cancellazione della riga o eliminazione del check di una voce di menù per tipo persona, permette al configuratore di non far visualizzare la voce di menù o report o form all'utente finale.
I flag di insert, update e delete sono esclusivamente per permettere all'utente finale di modificare i dati presenti in ciascuna maschera. Inoltre il flag di abilitato, permette la visualizzazione della form in sola lettura all'utente, senza necessario non checcare i singoli flag di inserimento, cancellazione e aggiornamento della form e senza modificare il layout della stessa.
Anche i report visibili nella maschera stampa del Web e del Client sono gestiti come autorizzazioni per tipo persona da questa maschera.

E' inoltre possibile inserire nuove righe di autorizzazione per eventuali nuovi ruoli ("tipi persone").

### Tipi Persone 
E' una tabella che consente di gestire i tipi persona che il sistema dovrà contemplare in fase poi di accessi e permessi (ruoli). I profili attualmente gestiti sono:

_Supervisore:_ Accede in modifica a tutte le funzionalità di Configurazione, Agende, Client pianificazione orario. Per avere accesso come prenotatore deve avere una Strutt. Org. associata.  

_Pianificatore:_ Accede in modifica a tutte le funzionalità di Configurazione e Client pianificazione orario, in sola visualizzazione all'agenda web. L'accesso è filtrato dalla Strutt. Org. di appartenenza  

_Amministrativo:_ Accede in modifica a tutte le funzionalità di Configurazione, Agende/ programmazione didattica, con accesso filtrato dalla Strutt. Org. di appartenenza  

_Prenotatore:_ Accede in modifica a tutte le funzionalità di Agende eccetto la programmazione didattica, con accesso filtrato dalla Strutt. Org. di appartenenza  

_Docente:_ Accede in modifica a tutte le funzionalità Agende con accesso filtrato dai soli impegni di competenza.  

_Configuratore:_ Accede in modifica a tutte le funzionalià di configurazione.  

_Guest:_ Accede in lettura alla sola sezione delle Informazioni  

_Studente_  

_Tirocinante_  


**N.B: ATTENZIONE! E' necessario indicare per ogni profilo (ruolo) le tipologie eventi sulle quali può agire nelle maschere web di Gestione degli impegni**


### Regimi
I regimi rappresentano il volume di impegno del docente nell'ateneo (tempo pieno, tempo parziale,ecc..) che può costituire elemento utile per la determinazione del costo standard del tipo docente

### Tipi Contratto
la tabella dei tipi contratto raccoglie le descrizioni dei tipi contratto applicabili solo alla tipologia di docenti esterni (contrattisti) e  il relativo costo orario al netto degli oneri, che vengono espressi sempre in forma oraria nella colonna successiva.

### Costi Standard
La tabella dei costi standard si applica solo alle qualifiche di tipo interno, e permette di indicare i costi di ciascuna combinazione qualifica + regime. Ogni riga della tabella indicherà quindi il costo standard di una qualifica e un determinato regime, il costo è eventualmente anche storicizzabile per anno. Oltre al costo orario che è da considerare come costo complessivo, viene indicato anche il valore degli oneri relativi. Le ultime colonne infine consentono di inserire per ogni combinazione qualifica + regime l'impegno didattico minimo espresso in ore, e il relativo  “costo orario eccedente”. Tale valore esprimerà il costo di tutte le ore  eccedenti rispetto a quelle previste dall'impegno didattico minimo.

### Persone: _Funzione principale_
Nel caso di persona singola, in base alla tipologia (ruolo) varia anche il set di dati gestiti.   

_**Comuni a tutte le tipologie di persone sono i dati generali, le preferenze, e l'account.**_

Dalla versione 10.02.00.00, in alto a sinistra della maschera Persone, è stato inserito una lista valori che mostra nella griglia sottostante il filtro inserito.
I possibili filtri sono: _Tutti, Solo Utenti, Solo Docenti_.

Il fitro _Tutti_ visualizza l'elenco completo delle persone con **tutti** i relativi campi dove è possibile effettuare modifiche alle righe (è identica alla visualizzazione delle rel. precedenti).

![](uploads/images/UP_WEB - PERSONE - Tutti.PNG)

Filtro _Solo Utenti_, visualizza nella griglia l'elenco delle persone che hanno il campo _Utente_ valorizzato, di tutte le tipologie (docenti, studenti, configuratori...).   

A differenza del filtro _Tutti_, tale filtro visualizza i soli campi che servono per la gestione della persona dal punto di vista: "utente dell'applicativo".

![](uploads/images/UP_WEB - PERSONE - Solo Utenti.PNG)

Filtro _Solo Docenti_. Con tale filtro vengono visualizzate le persone che sono di tipo persona _Docente_.   

A differenza del filtro _Tutti_, tale filtro visualizza i soli campi che servono per la gestione della persona dal punto di vista della docenza.   

_NB: Se è necessario dare accesso al sistema ad un docente, utilizzare il filtro _**Tutti**_ o _**Solo Utenti**_.''

![](uploads/images/UP_WEB - PERSONE - Solo Docenti.PNG)

#### Dati generali
_Id:_ progressivo numerico attribuito dal programma non modificabile  

_Nome:_ nome proprio  

_Cognome:_ Cognome  

_Email:_ indirizzo di posta elettronica  

_Reale:_ indica se la persona è reale, o virtuale. Virtuale serve per creare attori (docenti, collaboratori, amministrativi,ecc..) tipo o gruppi, che verranno poi sostituiti da persone reali.  

_Tipo persona:_ indica il tipo persona che da accesso alla gestione dei dati propri della tipologia  

_Abilitata:_ abilita o meno l'accesso al sistema  

_Calendario:_ visualizza il calendario assegnato alla persona  

_Opzioni calendario:_ contiene le modifiche di disponbilità della persona rispetto al calendario selezionato. Per ogni giorno è possibile inserire orario inizio e fine della disponibilità  

_Strutt. Org. visibile:_ visualizza il filtro sui dati visibili alla persona  


#### Account
_User:_ User di accesso della persona  

_Password:_ password di accesso della persona  


#### Altri dati del docente:
Oltre ai dati relativi all'account solo per il tipo persona “docente” sono gestibili sono i seguenti:

_Strutt. Org._ Strutt. Org. di appartenenza del docente (possono essere anche più di una). Una sola però può essere classificata come Strutt. Org. di appartenenza (SI/NO)   

_Dipartimento:_dipartimento di afferenza del docente  

_Settore Scientifico Disciplinare:_ Settore di insegnamento del docente  

_Qualifica:_ ruolo del docente  

_Regime:_ regime di impegno  

_Incarichi docenti:_ Elenco degli incarichi del docente, ogni riga riporta l'anno, l'attività didattica, lo stato di approvazione dell'incarico, ruolo, ore, tipo copertura, costo  


### Associa/Disassocia Strutture Organizzative Docenti

Nelle nuove versioni di UP è stata aggiunta una funzionalità che consente di associare o disassociare i docenti alle strutture organizzative.
Questa funzionalità è utile affinchè in UP_CLIENT i docenti appaiano nei filtri delle strutture organizzative corrispondenti.
Per utilizzare questa caratteristica è necessario recarsi in _Configurazione->Persone->Persone_, scegliere dal menù a tendina l'opzione _Solo Docenti_ oppure _Tutti_, selezionare i docenti interessati e cliccare sull'apposito pulsante. Si vedano le seguenti immagini.

![](uploads/images/UP_WEB - PERSONE - Solo Docenti Ass_Disass.PNG)

![](uploads/images/UP_WEB - PERSONE - Tutti Ass_Disass docente.PNG)

<br>
Una volta effettuate queste operazioni si presenterà una nuova finestra che consentirà di selezionare le strutture organizzative volute.

![](uploads/images/UP_WEB - PERSONE - Ass_Disass popup.PNG)

### Associa/Disassocia Strutture Organizzative Utenti

Nelle nuove versioni di UP è stata aggiunta una funzionalità che consente di associare o disassociare gli utenti alle strutture organizzative.
Questa funzionalità è utile affinchè in UP_CLIENT gli utenti possano gestire le strutture organizzative corrispondenti.
Per utilizzare questa caratteristica è necessario recarsi in _Configurazione->Persone->Persone_, scegliere dal menù a tendina l'opzione _Solo Utentu_ oppure _Tutti_, selezionare gli utenti interessati e cliccare sull'apposito pulsante. Si vedano le seguenti immagini.

![](uploads/images/UP_WEB - PERSONE - Solo Utenti Ass_Disass.PNG)

![](uploads/images/UP_WEB - PERSONE - Tutti Ass_Disass Utente.PNG)

<br>
Una volta effettuate queste operazioni si presenterà una nuova finestra che consentirà di selezionare le strutture organizzative volute.

![](uploads/images/UP_WEB - PERSONE - Ass_Disass popup.PNG)

### Gruppi persone
Il sistema consente anche di codificare gruppi di persone, che possono esistere indipendentemente dai componenti che ne fanno o ne faranno parte. In questo modo è possibile fissare degli eventi o delle attività, assegnarle ad un calendario o agenda propri del gruppo ( Consiglio di Strutt. Org., Commissione d'esame, ecc..). L'anagrafica del gruppo si deve creare in persone inserendo un nome e marcandola come “non reale”.

_Id:_ progressivo numerico attribuito dal programma non modificabile  

_Nome:_ nome del gruppo  

_Tipo persona:_ indica il tipo persone che faranno parte del gruppo  

_Abilitata:_ abilita o meno l'accesso al sistema  

_Persone reali righe:_ è l'elenco delle persone reali che caratterizzeranno il gruppo, e che quindi ne erediteranno gli impegni  



## Risorse
Le risorse, intese come “strutture fisiche”, che il sistema gestisce sono di due tipi, risorse fisse e risorse mobili, le tipologie sono codificabili nelle omonime tabelle di anagrafica.

![](uploads/images/up_manual_26022010_180529.png)

 
### Tipi Risorse Fisse
Sono le descrizioni codificate delle tipologie di risorse fisse utilizzate dall'ateneo (laboratori, aule multimediali, ecc..)

### Tipi Risorse Mobile
Sono le descrizioni codificate delle tipologie di risorse mobili utilizzate dall'ateneo (video proiettori, lavagne luminose, ecc..)

### Piani 
La tabella consente di gestire le anagrafiche anche dei piani degli edifici a disposizione dell'ateneo per la pianificazione delle risorse fisse o mobili. 


### Risorse Fisse
Le risorse fisse sono le strutture logistiche di cui dispone l'ateneo (aule, laboratori, ecc..). Ciascuna risorsa è caratterizzabile da un set di dati generali ed alcuni di dettaglio.

 
![](uploads/images/up_manual_26022010_180735.png)

#### Generale:
_Id:_ progressivo numerico attribuito dal programma non modificabile  

_Codice:_  codice della risorsa   

_Descrizione:_ descrizione denominazione della risorsa  

_Responsabile:_ persona responsabile della risorsa, il responsabile   

_Stato Disponibilità:_ può assumere tre valori: Non Prenotabile, Solo Prenotabile, Impegnabile (valore di default)  

_Calendario:_ Calendario assegnato alla risorsa  


#### Caratteristiche:
_Numero Posti:_ capienza della struttura (campo non ancora gestito)  

_Num. Max posti:_ numero massimo di posti  

_Acc. Disabili:_  risorsa dotata di accesso per i disabili  

_Proiettore:_  risorsa dotata di proiettore  

_Acc. alla rete:_  risorsa dotata di accesso ad internet  


#### Ubicazione
_Lavagna luminosa:_  risorsa dotata di lavagna luminosa  

_Città:_ città   

_Edificio:_ Edificio di ubicazione  

_Piano:_ Piano dell'edificio di ubicazione

Ci sono poi una serie di attributi che possono avere una relazione uno a molti con la singola risorsa:

_tipo:_ è possibile indicare uno o più tipi di risorsa, al quale la risorsa appartiene  

_dipartimento:_ è possibile indicare uno o più dipartimenti, ai quali la risorsa appartiene  

_Strutt. Org.:_ è possibile indicare una o più Strutt. Org., alle quali la risorsa appartiene  

_divisioni:_ è possibile indicare una o più divisioni, alle quali la risorsa appartiene  

_Corsi:_ è possibile indicare uno o più Corsi di studio, ai quali la risorsa appartiene  

_Persone:_ è possibile indicare una o più persone, alle quali la risorsa afferisce  

_Opzioni calendario disponibilità della risorsa:_ per ogni risorsa è possibile gestire un calendario di disponibilità della risorsa stessa. Nella funzione è possibile impostare per ogni giorno della settimana un orario  



#### Impegnabilità

Una Risorsa Fissa può essere impegnabile attraverso la scelta da parte dell'utente dello stato di impegnabilità.

![](uploads/images/up_manual_17092010_122701.png)

Lo stato può assumere tre diversi valori:</br>
  *  MAI: la risorsa fissa non comparirà **MAI **in nessun elenco di aule. Utilizzabile per esempio quando un aula è chiusa per lavori.</br>
  *  CON AUTORIZZAZIONE: impostando tale stato di impegnabilità della risorsa, si esprime la necessità di avere una persona **responsabile **della risorsa stessa, che possa decidere se autorizzare o meno l'occupazione dell'aula. Di default la regola base è _**per Strutt. Org._, cioè la risorsa fissa associata ad una particolare Strutt. Org., resta sempre _impegnabile _(conferma immediata) per tutti gli utenti di quella Strutt. Org. e _prenotabile _per gli utenti delle altre Strutt. Org.. L'utente con il ruolo **pianificatore della Strutt. Org. in oggetto è l'unico che può decidere lo stato di occupazione della risorsa fissa attraverso la maschera _Risorse Fisse <del>> [Conferma Prenotazione](up_web_Risorse.ashx.md#Conferma_prenotazioni_1)_.
In alternativa è possibile specificare una **singola persona **come responsabile dell'aula, valorizzando l'apposito campo (Id Resp.). La risorsa fissa viene resa **prenotabile **a tutti gli utenti diversi dal responsabile. Solo il responsabile ha la possibilità di confermare o rifiutare la prenotazione della risorsa fissa attraverso l'apposita maschera presente nella voce di menù _Risorse Fisse </del>> [Conferma Prenotazione](up_web_Risorse.ashx.md#Conferma_prenotazioni_1)_. Fino al compimento di tale operazione lo stato della risorsa fissa rimarrà _**Prenotato**_. Alla conferma lo stato passerà a _**Confermato**_. Gli altri utenti, potranno controllare lo stato della loro prenotazione dalla maschera _Risorse Fisse -->[Gestione Prenotazioni](up_web_Risorse.ashx.md#Gestione_prenotazioni_2)_.</br>
  *  SEMPRE: l'impegnabilità della risorsa fissa è **sempre **disponibile per chiunque (conferma immediata). </br>

Per poter modificare lo stato delle risorse fisse è stato inserito, dalla versione 10.05.00.00, un pannello in alto della finestra come riportato sotto dalla figura

![](uploads/images/up_manual_30052011_114902.png)

L'utente finale può modificare lo stato di una singola risorsa fissa alla volta, con gli appositi check posti vicino alla riga della risorsa fissa.
Una volta effettuata la scelta della risorsa fissa, l'utente seleziona lo stato in cui vuole modificare la risorsa e conferma l'operazione. 
Il sistema esegue l'operazione immediatamente e visualizza il successo dell'avvenuta operazione. ### Associazione più Strutt. Org.
E' stata introdotta nella versione 10.02.00.00 la possibilità di associare contemporaneamente a più aule un numero maggiore di uno di Strutt. Org..
Attraverso la nuova finestra inserita in alto alla maschera

![](uploads/images/up_manual_08062010_101401.png)

selezionando una o più risorse fisse, il pulsante _Associa Strutt. Org. permette di selezionare una o più Strutt. Org. per associarle a tale risorsa fissa.

![](uploads/images/up_manual_08062010_102001.png)

La disassociazione delle Strutt. Org. alle risorse fisse è possibile da due punti della maschera Risorse Fisse.
Nel dettaglio della risorsa fissa è possibile cancellare singolarmente una o più Strutt. Org. tramite il cancel generale.

![](uploads/images/up_manual_08062010_102501.png) 

Oppure se si voglio eliminare tutte le Strutt. Org. di più risorse fisse tramite il pulsante _Disassocia Strutt. Org., il sistema disassocia contemporaneamente tutte le Strutt. Org. alle risorse fisse selezionate dall'utente. Il sistema chiede conferma e esegue l'operazione richiesta.

![](uploads/images/up_manual_08062010_102901.png)





### Risorse Mobili
Le risorse mobili sono generalmente le attrezzature utilizzate nell'ateneo delle quali occorre gestire l'utilizzo essendo condivise da più utenti. Saranno ad esempio, i video proiettori portatili, lavagne luminose, notebooks, ecc…

![](uploads/images/up_manual_26022010_181729.png)

 
_Id:_ progressivo numerico attribuito dal programma non modificabile  

_Codice:_  codice della risorsa   

_Descrizione:_ descrizione denominazione della risorsa  

_Tipo Id:_ progressivo numerico attribuito dal programma non modificabile  

_Codice:_  codice del tipo di risorsa   

_Descrizione:_ descrizione/denominazione del tipo risorsa mobile   

_Calendario:_ Calendario assegnato alla risorsa  

_Note:_ Campo note libero  

_Opzioni calendario disponibilità della risorsa:_ per ogni risorsa è possibile gestire un calendario di disponibilità della risorsa stessa. Nella funzione è possibile impostare per ogni giorno della settimana un orario.  



## Eventi
Gli eventi rappresentano l'entità chiave di tutto il programma. Tutto ciò che può essere oggetto di pianificazione dal punto di vista logistico, temporale, o di assegnazione di risorse umane è trattato come evento. Quindi ad esempio anche le attività didattiche sono a tutti gli effetti eventi, anche se di tipo particolare. In questa sezione del sistema di configurazione si possono gestire alcune tabelle ausiliarie alla gestione degli eventi.

![](uploads/images/up_manual_26022010_183217.png)

### Tipi Priorità 
Una tabella per gestire i livelli di priorità ad uso del programma in fase di programmazione logistica e calendarizzazione degli eventi: (es: Alta, media, bassa, ecc..) 


### Tipi Evento
Sono le descrizioni codificate delle tipologie di eventi utilizzati dall'ateneo (attività didattiche, consigli di Strutt. Org., seminari, ecc…)

### Divisioni
Sono aggregazioni di corsi di studio tipicamente determinate dalla tipologia (Es: laurea triennale, laurea specialistica, ecc..)

### Aree
Sono raggruppamenti liberi di insegnamenti (attività didattiche), caratterizzati da un codice e una descrizione


### Eventi
Gli eventi sono strutturati in **testata **ed **eventi riga**. La testata riassume i caratteri generali dell'evento (quali ad esempio  il tipo, il responsabile, il calendario) mentre l'evento riga rappresenta un dettaglio orario omogeneo dell'evento, che è oggetto di pianificazione. Ciascun evento riga può essere collegato a persone, risorse fisse e risorse mobili. Tali collegamenti vengono definiti **pre-impegni** o **proposte di impegno**, delle risorse o delle persone, perché a tutti gli effetti una volta che l'evento riga verrà spalmato nel calendario, le risorse e le persone risulteranno appunto impegnate in quella determinata attività. Quindi l'agenda delle persone e delle risorse saranno riempite di quelle attività a seconda di come verrà pianificato.

#### Eventi: testata
_Id:_ progressivo numerico attribuito dal programma non modificabile  

_Descrizione:_ descrizione denominazione dell'evento generale  

_Versione:_ nel caso di attività didattica la versione di riferimento  

_Tipo evento:_ indica la tipologia di evento (attività didattica, esame, ecc..)  

_Privato:_ indica se l'evento è visibile solo alle persone coinvolte oppure da tutti  

_Priorità:_ è possibile associare una priorità definita all'evento  

_Responsabile:_ persona responsabile dell'evento   

_Calendario:_ Calendario assegnato all'evento  

_Stato di lavorazione:_ mostra lo stato di lavorazione  

_Stato di trasferimento:_ mostra lo stato di trasferimento  

_Provenienza:_ indica se l'evento è stato migrato da qualche applicativo esterno (ESSE3)

**Altri dati che caratterizzano l'evento di tipo attività didattica:**  

_Anno accademico:_ anno accademico di riferimento dell'evento  

_Collegato a:_ nel caso l'evento in questione non sia un evento reale, ma una denominazione diversa di un altro evento in questo campo risulta l'evento “nativo” e o evento base al quale si riferisce  

_Tipo collegamento:_ questo campo esplicita la natura del collegamento indicato nel campo precedente: (condivisione, contestualizzazione, mutuazione)   

_Attività didattica:_ attività didattica fisica di riferimento dell'evento  

_Corso:_ corso di laurea di afferenza dell'evento  

_Percorso:_ percorso di laurea di afferenza dell'evento  

_Strutt. Org.:_ Strutt. Org. di riferimento dell'evento  

_Dipartimento:_ dipartimento di riferimento dell'evento  

_Area:_ area di insegnamento dell'evento- attività didattica  

_Tipo partizionamento:_ tipo partizionamento dell'evento- attività didattica  

_Anno curriculum:_ anno di corso dello studente in cui l'evento- attività didattica compare nel corso  di laurea/percorso precedentemente indicato

#### Eventi: riga
_Riga_id:_ progressivo numerico attribuito dal programma non modificabile  

_Descrizione:_ descrizione denominazione del dettaglio dell'evento

**Attributi che esprimono le esigenze di calendarizzazione dell'evento:**  

_Qta Ore:_ durata in ore  

_Costanza nello spazio:_ flag che indica se l'evento deve essere pianificato mantenendo  se possibile la stessa risorsa fissa di allocazione  

_Costanza nel tempo:_ flag che indica se l'evento deve essere pianificato mantenendo se possibile lo stesso orario (giorno-ora)  

_Unità min incontro:_ indica la quantità di tempo minima erogabile (1 ora, ½ ora, ecc..) dell'evento nel giorno  

_Unità max incontro:_ la quantità di tempo massima erogabile (1 ora, ½ ora, ecc..) dell'evento nel giorno 

**Attributi che esprimono esigenze logistiche dell'evento:**  

_Numero posti:_ numero di partecipanti previsto all'evento  di dettaglio  

_Tipo risorsa fissa:_ Tipo di risorsa fissa da utilizzare per quest'evento  

_Accesso disabili:_ flag che indica la necessità di una risorsa fissa con accesso disabili  

_Lavagna luminosa:_ flag che indica la necessità di una risorsa fissa con lavagna luminosa  

_Pc:_ flag che indica la necessità di una risorsa fissa con pc  

_Accesso alla rete:_ flag che indica la necessità di una risorsa fissa con accesso alla rete  

_Proiettore:_ flag che indica la necessità di una risorsa fissa con proiettore  

_Città:_ città in cui l'evento ha luogo  

_Piano:_ piano di ubicaione  

_Edificio:_ edificio di ubicazione

**Attributi degli eventi riga di tipo attività didattica:**  

_TAF:_ indica la tipologia di attività formativa (A,B, C,…) a cui le  ore erogate corrsipondono  

_Unità di misura:_ indica l'unità di misura dell'attività (cfu, annualità, esemtralità,ecc..)  

_Crediti:_ crediti formativi universitari che valorizzano l'attività  

_Tipo attività:_ indica il tipo di attività corrispondente (lezione, esercitazione, ecc..)   

_% ripartizione costi:_ indica quale percentuale del costo dell'evento viene conteggiata nel budget dell'anno accademico di riferimento.  

_Ambito:_ Ambito scientifico disciplinare dell'attività  

_Settore scientifico disciplinare:_ Settore scientifico disciplinare dell'evento riga

#### Proposte di impegno

**Per le persone:**
_pers_id:_ identificativo della persona  

_Nominativo:_ nome della persona associata all'evento riga  

_Approvato:_ approvazione del pre-impegno  

_ruolo:_ ruolo con cui partecipa all'evento riga  

_ore:_ ore dell'evento riga assegnate alla persona  

_Tipo copertura:_ indica il tipo di copertura (in caso di docente) di una attività didattica

**Per le risorse fisse:**
_risorsa fissa:_ identificativo della risorsa fissa  

_codice:_ codice della risorsa fissa associata all'evento riga  

_Descrizione:_ descrizione della risorsa fissa associata all'evento riga  

_Approvato:_ approvazione del pre-impegno

**Per le risorse mobili:**
_risorsa mobile:_ identificativo della risorsa mobile  

_Codice:_ codice della risorsa fissa associata all'evento riga  

_Descrizione:_ descrizione della risorsa fissa associata all'evento riga  

_Approvato:_ approvazione del pre-impegno  

_Quantità:_ore per cui la risorsa risulta impegnata


## Calendari
Questa sezione comprende i calendari associati a risorse persone o eventi, e i template di calendari, intesi come modelli di date di non disponibilità che possono venire applicati a determinati calendari


![Immagine](uploads/images/up_manual_26022010_184822.png)


### Calendari
Un calendario è un periodo di tempo definito con una data di inizio e una data di fine all'interno del quale è possibile inserire eventi.

I suoi attributi sono:  

_Id:_ progressivo numerico attribuito dal programma non modificabile  

_Descrizione:_ descrizione denominazione del calendario  

_Da Data:_ data di inizio del calendario  

_A Data:_ data di fine del calendario  

_Anno Accademico:_ anno accademico al quale il calendario è associato  

_Generazione automatica:_ flag che indica che le date di inizio e di fine devono essere prelevate dall'anno accademico  

_Strutt. Org.:_ Strutt. Org. di appartenenza del calendario  

_Corso:_ corso associato al calendario  

_Note:'' Note facoltative sul calendario  


### Template di calendario
Un template di calendario è un elenco di date di non disponibilità propagabile su altri calendari. Per ogni giornata è possibile anche indicare una causale di non disponibilità (es: Chiusura, Ferie, ecc..) selezionabile da un elenco personalizzabile di voci. Ad esempio è possibile fare un template unico con tutte le festività di un determinato anno accademico. E' possibile gestire template diversificati per singole Strutt. Org..


![Immagine](uploads/images/up_manual_26022010_184907.png)



### Associa template
Attraverso questa funzione è possibile associare un template ad uno o più calendari.
Nella testata si seleziona un template precedentemente definito, nel dettaglio intermedio è possibile invece inserire i criteri di ricerca dei calendari ai quali si desidera applicare il template, e nella parte inferiore si possono visualizzare tutti i calendari risultanti e selezionarli per l'associazione/dissociazione al template selezionato.


![Immagine](uploads/images/up_manual_19062010_100001.png)



**N.B:** per ciascun calendario attraverso il pulsante destro del mouse, si possono gestire gli altri template già associati al calendario stesso (Mostra Template Associati)!
Viene visualizzata la seguente schermata con l'Elenco dei Template associati al calendario.


![Immagine](uploads/images/up_manual_19062010_102801.png)
