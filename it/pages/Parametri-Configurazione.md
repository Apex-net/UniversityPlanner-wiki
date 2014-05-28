

# Parametri Configurazione


## Configurazioni


Suddivisione dei parametri di configurazioni generale a seconda dell'argomento.

### Parametri generali

<table border="1" cellspacing="0" cellpadding="1">
<thead><tr>
<td>Codice Parametro</td>
<td>Descrizione</td>
<td>Valore Default</td>
<td>Possibili Valori </td>
<td>Utente</td>
</tr></thead>
<tr>
<td> ARROTONDA_RESIDUO_ISCRITTI</td>
<td>Arrotonda il residuo iscritti a 0 in caso di numero negativo</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> CANC_DATI_LIST_WARNING</td>
<td>Flag di default della Lista warning che mi indica se cancellare ultima elaborazione alla uscita</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> CDA_USER_EXCHANGE</td>
<td>User per connettersi ad Exchange</td>
<td>  
</td>
<td>Esempio: m.rossi@dominio.it</td>
<td>  
</td>
</tr><tr>
<td> CDA_PASSW_EXCHANGE </td>
<td>Password per connettersi ad Exchange</td>
<td>  
</td>
<td>Alfanumerico</td>
<td>  
</td>
</tr><tr>
<td> DEFAULT_LIMIT_FOR_BOOKING_RESULTS</td>
<td>Upper limit for number of rows when searching a classroom to book it.</td>
<td>-1</td>
<td>Zero or negative values mean use default maximum value</td>
<td>  
</td>
</tr><tr>
<td> DEFAULT_SEPARATORE_ISNULL_DES_PAR</td>
<td>Carattere da usare in caso di valore nullo nelle descrizioni parametriche. Esempio: ISNULL(campo,carattere)</td>
<td>-</td>
<td>I caratteri più usati sono: -(trattino); (spazio);.(punto);...(puntini di sospensione); ma si può usare qualsiasi carattere</td>
<td>  
</td>
</tr><tr>
<td> DES_CAPTION</td>
<td>Descrizione Caption</td>
<td>DEV_BASE_IT_UP</td>
<td>  
</td>
<td>  
</td>
</tr><tr>
<td> STATO_IMPEGNO_DEFAULT</td>
<td>Default Stato Impegno proposto dalla form NewImpegno alla creazione del nuovo impegno</td>
<td>2</td>
<td>'0' - NON CONFERMATO; '1' - CONFERMATO; '2' - PUBBLICATO</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> FLG_MULTILINGUA</td>
<td>Flag per la gestione Multilingua nelle stampe</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr>
</table>

  
  
  
  



### Parametri Esami

<table border="1" cellspacing="0" cellpadding="1">
<thead><tr>
<td>Codice Parametro</td>
<td>Descrizione</td>
<td>Valore Default</td>
<td>Possibili Valori </td>
<td>Utente</td>
</tr></thead>
</tr><tr>
<td> ESAMI.DTM_SLOT_DETT_IMP_RF</td>
<td>Durata degli Slot Impegni Risorse Fisse Presenze Dettaglio</td>
<td>01/01/1900 01:00:00</td>
<td>  
</td>
<td>  
</td>
</tr><tr>
<td> ESAMI.FLG_RILEV_PRES_ES </td>
<td>Flag per la gestione della Rilevazione Presenze Esami</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.COMANDI_DI_PULIZIA_ESA_DA_DATA </td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere a partire da quale data appello valgono gli script di pulizia per gli eventi esami </td>
<td>01/01/3000</td>
<td>data appello in formato dd/mm/yyyy: es. 20/02/2009</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_CREA_TAPPI</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se aggiungere i record "tappo" per le attività di tipologia Esame del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_UPD_DTM_IMPEGNO</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se fare l'update della data dell'appello sull'impegno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_UPD_DURATA_IMPEGNO </td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se fare l'update della durata dell'appello sull'impegno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_UPD_NUM_ISCRITTI</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se fare l'update del numero iscritti per tipologia Esame del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_UPD_ORA_INIZIO_IMPEGNO</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se fare l'update dell'ora di inizio dell'appello sull'impegno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_UPD_STATO_IMP</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se fare l'update dello stato dell'appello sull'impegno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_EV_ESA</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare o meno le note evento per tipologia Esame del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_EV_PUBBL_ESA</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare le note evento per tipologia Esame come pubblicate del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_IMP_ESA</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare o meno le note impegno per tipologia Esame del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_IMP_PUBBL_ESA</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare le note impegno per tipologia Esame come pubblicate del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr>
</table>

  
  
  
  



### Paramentri da UGOV

<table border="1" cellspacing="0" cellpadding="1">
<thead><tr>
<td>Codice Parametro</td>
<td>Descrizione</td>
<td>Valore Default</td>
<td>Possibili Valori </td>
<td>Utente</td>
</tr></thead>
</tr><tr>
<td> IMPORT_DA_UGOV.ESPORTA_CALEND_STD</td>
<td>Durante l'import della didattica da U-GOV, scegliere se importare o meno i calendari standard di Ugov (raggruppati per Anno Acc/Periodo/Corso di studio)</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_DA_UGOV.ESPORTA_EVENTI_DA_ANNO</td>
<td>Durante l'import della didattica da U-GOV, scegliere l'anno a partire dal quale viene considerata la didattica di UGOV</td>
<td>1900</td>
<td>Es: 2008 - tutti gli eventi con anno accademico >= 2008</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_DA_UGOV.ESPORTA_NOTE_DID</td>
<td>Durante l'import della didattica da U-GOV, scegliere se importare o meno le note delle AD_GEN e degli Eventi Master concatenate</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_DA_UGOV.ESPORTA_VINCOLI</td>
<td>Durante l'import della didattica da U-GOV, scegliere se importare o meno le regole di scelta come Vincoli di UP</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_DA_UGOV.IMPORT_CALEND_NON_STD</td>
<td>Durante l'import della didattica da U-GOV, scegliere se importare o meno i calendari non standard da Ugov (vedi tabella CONFIG_IMPORT_CALEND). NB: per attivare i calendari non standard il parametro IMPORT_DA_UGOV.ESPORTA_CALEND_STD deve essere uguale a 0</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr>
</table>

  
  
  
  


### Parametri Import UP

<table border="1" cellspacing="0" cellpadding="1">
<thead><tr>
<td>Codice Parametro</td>
<td>Descrizione</td>
<td>Valore Default</td>
<td>Possibili Valori </td>
<td>Utente</td>
</tr></thead>
</tr><tr>
<td> IMPORT_UP.COMANDI_DI_PULIZIA_DID_DA_ANNO</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere a partire da quale anno valgono gli script di pulizia per gli eventi di didattica </td>
<td>3000</td>
<td>anno accademico: es. 2009</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.COMANDI_DI_PULIZIA_ESA_DA_DATA </td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere a partire da quale data appello valgono gli script di pulizia per gli eventi esami </td>
<td>01/01/3000</td>
<td>data appello in formato dd/mm/yyyy: es. 20/02/2009</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.GESTIONE_CAMBIO_CALEND </td>
<td>Durante l'import della didattica da U-GOV, scegliere quali azioni eseguire al cambio di calendario di un evento con impegni già inseriti</td>
<td>SOSP</td>
<td>'SOSP' - mette gli impegni in stato Sospeso; 'DEL' - cancella tutti gli impegni;  'DEL_AULE' - cancella solo le aule associate; 'NONE' - non fa nulla; </td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_CHECK_UPD_PACCHETTO</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se controllare la consistenza dei pacchetti per tipologia Esame dal sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_CREA_TAPPI</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se aggiungere i record "tappo" per le attività di tipologia Esame del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_UPD_DTM_IMPEGNO</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se fare l'update della data dell'appello sull'impegno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_UPD_DURATA_IMPEGNO </td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se fare l'update della durata dell'appello sull'impegno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_UPD_NUM_ISCRITTI</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se fare l'update del numero iscritti per tipologia Esame del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_UPD_ORA_INIZIO_IMPEGNO</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se fare l'update dell'ora di inizio dell'appello sull'impegno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_ESA_UPD_STATO_IMP</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se fare l'update dello stato dell'appello sull'impegno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_EV</td>
<td>Durante l'import dalle tabelle di interfaccia, scegliere se importare o meno le note evento del sistema esterno.</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_EV_ESA</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare o meno le note evento per tipologia Esame del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_EV_LOG</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare o meno le note evento per tipologia Logistica del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_EV_PUBBL_ESA</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare le note evento per tipologia Esame come pubblicate del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_EV_PUBBL_LOG</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare le note evento per tipologia Logistica come pubblicate del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_IMP</td>
<td>Durante l'import dalle tabelle di interfaccia, scegliere se importare o meno le note impegno del sistema esterno.</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_IMP_ESA</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare o meno le note impegno per tipologia Esame del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_IMP_LOG</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare o meno le note impegno per tipologia Logisitca del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_IMP_PUBBL_ESA</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare le note impegno per tipologia Esame come pubblicate del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.IMPORTA_NOTE_IMP_PUBBL_LOG</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere se importare le note impegno per tipologia Logistica come pubblicate del sistema esterno</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.PULISCI_ELAB_BEFORE</td>
<td>Durante l' import dalle tabelle di interfaccia, scegliere il numero di giorni precedenti i quali verranno eliminate le elaborazioni dalle tabelle di interfaccia. Lasciare il value = -1 per NON cancellare mai</td>
<td>-1</td>
<td>Es: 10 - verranno eliminate tutte le elaborazioni con data < (sysdate - 10) </td>
<td>  
</td>
</tr><tr>
<td> IMPORT_UP.UPDATE_DATE_CALEND</td>
<td>Durante l'import della didattica da U-GOV, scegliere se aggiornare le date dei calendari o lasciarle gestire manualmente dall'utente</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr>
</table>

  
  
  
  



### Parametri Lookup Risorse Fisse
**I seguenti parametri vengono utilizzati <span style="text-decoration:underline">SOLO</span> in UP_WEB. **<br/>
Per maggiori informazioni sul comportamento dei check di congruenza di rimanda alla pagina [CheckCongruenze](up_client_CheckCongruenze.md).

<table border="1" cellspacing="0" cellpadding="1">
<thead><tr>
<td>Codice Parametro</td>
<td>Descrizione</td>
<td>Valore Default</td>
<td>Possibili Valori </td>
<td>Utente </td>
</tr></thead>
</tr><tr>
<td> LOOKUP_RF.FLG_CHECK_RF_COMP</td>
<td>Nella lookup delle aule decidere se attivare il check di congruenza sulla compatibilità aule</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
 </td>
</tr><tr>
<td> LOOKUP_RF.FLG_CHECK_RF_DISP</td>
<td>Nella lookup delle aule decidere se attivare il check di congruenza sulla disponibilità</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> LOOKUP_RF.FLG_CHECK_RF_ENT_PREN</td>
<td>Nella lookup delle aule decidere se il check di congruenza debba Ignorare le Entità Prenotate</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> LOOKUP_RF.FLG_CHECK_RF_IMP_SOSP</td>
<td>Nella lookup delle aule decidere se attivare il check di congruenza per gli impegni in stato sospeso</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> LOOKUP_RF.FLG_CHECK_RF_SOVR</td>
<td>Nella lookup delle aule decidere se attivare il check di congruenza sulla sovrapposizione aule</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr>
</table>

  
  
  
  


### Parametri UP Client
<br/>

<table border="1" cellspacing="0" cellpadding="1">
<thead><tr>
<td>Codice Parametro</td>
<td>Descrizione</td>
<td>Valore Default</td>
<td>Possibili Valori </td>
<td>Utente</td>
</tr></thead>
</tr><tr>
<td> UP_CLIENT.CONTROLLO_PUBBL_ESA_STATO_BOZZA</td>
<td>Abilitare il controllo della pubblicazione di esami solo se lo stato attivazione evento è attivo</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_COMPATIB_RF</td>
<td>Controllo di Compatibilità tra Eventi e Aule <br/> <span style="text-decoration:underline">**NOTA:** Il flag parametrizza anche le lookup delle risorse fisse di UP_CLIENT</span> </td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_DISP_EVENTO</td>
<td>Controllo disponibilità Calendario Evento</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_DISP_PERS</td>
<td>Controllo disponibilità Calendario Docente</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_DISP_RF</td>
<td>Controllo disponibilità Calendario Aule <BR/> <span style="text-decoration:underline">**NOTA:** Il flag parametrizza anche le lookup delle risorse fisse di UP_CLIENT</span>  </td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_DISP_RM</td>
<td>Controllo disponibilità Calendario Risorse Mobili</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_IGNORA_ENTITA_PREN</td>
<td>Ignora Risorse in stato Prenotato</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_IGNORA_PARTIZ</td>
<td>Ignora Partizioni diverse</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_IGNORA_SOSPESI</td>
<td>Ignora gli impegni sospesi</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_SOVRAPP_PERS</td>
<td>Controllo di Sovraopposizione Persone</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_SOVRAPP_RF</td>
<td>Controllo di Sovraopposizione Risorse Fisse <br/>  <span style="text-decoration:underline">**NOTA:** Il flag parametrizza anche le lookup delle risorse fisse di UP_CLIENT</span> </td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_SOVRAPP_RM</td>
<td>Controllo di Sovraopposizione Risorse Mobili</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_TEMPL_COMPATIB_RF</td>
<td>Nella lookup risorse fisse template se effettuare il controllo di compatibilità aule</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_TEMPL_SOVRAPP_RF</td>
<td>Nella lookup risorse fisse template se effettuare il controllo di sovrapposizione aule</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_CONGR_VINCOLI</td>
<td>Controllo Vincoli di Obbligatorietà</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_PUBBL_NO_PERS</td>
<td>Avviso in caso di pubbl. di impegni senza Docenti</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_PUBBL_NO_RF</td>
<td>Avviso in caso di pubbl. di impegni senza Aule</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_CHK_PUBBL_NO_RM</td>
<td>Avviso in caso di pubbl. di impegni senza Ris. Mobili</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_FRMEVENTI_CHILD</td>
<td>Flag per gestire la finestra degli eventi di tipo child o no</td>
<td>1</td>
<td>'1' - finestra MdiChild; '0' - finestra non MdiChild</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_FRMLISTAWARN_CHILD</td>
<td>Flag per gestire la finestra dell'elenco warning di tipo child o no</td>
<td>1</td>
<td>'1' - finestra MdiChild; '0' - finestra non MdiChild</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_FRMSCHEDULER_CHILD</td>
<td>Flag per gestire la finestra di pianificazione di tipo child o no</td>
<td>1</td>
<td>'1' - finestra MdiChild; '0' - finestra non MdiChild</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_MODIFY_EV_NOT_IN_FILTER</td>
<td>Modifica impegni non presenti nel filtro eventi</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.FLG_REFRESH_AUTO</td>
<td>Flag per decidere se aggiornare tutte le finestre aperte ad ogni modifica</td>
<td>1</td>
<td>'1' - Automatico; '0' - Manuale</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.GEST_IMP_DEFAULT_STATO_RICERCA</td>
<td>Default dello stato impegno da ricercare nella Window Form Gestione Impegni</td>
<td>1</td>
<td>'0' - NON CONFERMATO; '1' - CONFERMATO; '2' - PUBBLICATO; '3' - SOSPESO ; '4' - TUTTI</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.IND_TIPO_LABEL</td>
<td>Tipo label degli impegni del pianificatore (influenza la colorazione)</td>
<td>3</td>
<td>  
</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.QTA_DUR_INTERVALLO</td>
<td>Durata intervallo in minuti</td>
<td>  
</td>
<td>Valore numerico in minuti</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.QTA_DUR_SLOT</td>
<td>Durata slot in minuti</td>
<td>60</td>
<td>Valore numerico in minuti</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.QTA_ORE_ACC</td>
<td>Ore accademiche corrispondenti</td>
<td>1</td>
<td>Valore numerico in ore</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_CLIENT.SHOW_FORM_POST_IMPORT</td>
<td>Imposta se mostrare la form post import all'apertura del Client dopo il login</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td>  
</td>
</tr>
</table>

  
  
  
  



### Parametri Descrizione per Stampe

<table border="1" cellspacing="0" cellpadding="1">
<thead><tr>
<td>Codice Parametro</td>
<td>Descrizione</td>
<td>Valore Default</td>
<td>Possibili Valori </td>
<td>Utente</td>
</tr></thead>
</tr><tr>
<td> UP_REPORTS.DES_BREVE_EVENTO</td>
<td>Descrizione reports breve evento</td>
<td>COALESCE(CAST(cod_tipo_att AS VARCHAR(4000)), '-')  ||  ' '  || COALESCE(CAST(cda_ud AS VARCHAR(4000)), '-')</td>
<td>Sintassi standard ANSI</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_REPORTS.DES_BREVE_EVENTO_APEX_FORMAT</td>
<td>Descrizione reports breve evento formato Apex</td>
<td>{cod_tipo_att} {cda_ud}</td>
<td>Sintassi formato APEX</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_REPORTS.DES_LUNGA_EVENTO</td>
<td>Descrizione reports lunga evento</td>
<td>'\[' || COALESCE(CAST(cda_ud AS VARCHAR(4000)), '-') || '\] ' || COALESCE(CAST(des AS VARCHAR(4000)), '-') || ' (' || COALESCE(CAST(des_tipo_att AS VARCHAR(4000)), '-') || ') ' || COALESCE(CAST(des_tipo_parti AS VARCHAR(4000)), '-')</td>
<td>Sintassi standard ANSI</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_REPORTS.DES_LUNGA_EVENTO_APEX_FORMAT</td>
<td>Descrizione reports lunga evento formato Apex</td>
<td>\[{cda_ud}\] {des} ({des_tipo_att}) {des_tipo_parti} </td>
<td>Sintassi formato APEX</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_REPORTS.DES_PERSONA</td>
<td>Descrizione reports persona</td>
<td>COALESCE(CAST(DES_COGNOME AS VARCHAR(4000)), '-') || ' ' || COALESCE(CAST(DES_NOME AS VARCHAR(4000)), '-')</td>
<td>Sintassi standard ANSI</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_REPORTS.DES_PERSONA_APEX_FORMAT</td>
<td>Descrizione reports persona formato Apex</td>
<td>{des_cognome} {des_nome}</td>
<td>Sintassi formato APEX</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_REPORTS.DES_RIS_FISSA</td>
<td>Descrizione reports risorsa fissa</td>
<td>COALESCE(CAST(des_rf AS VARCHAR(4000)), '-')</td>
<td>Sintassi standard ANSI</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_REPORTS.DES_RIS_FISSA_APEX_FORMAT</td>
<td>Descrizione reports risorsa fissa formato Apex</td>
<td>{des_rf}</td>
<td>Sintassi formato APEX</td>
<td>![](uploads/images/check2.gif)</td>
</tr>
</table>

  
  
  
  


### Parametri UP WEB
<table border="1" cellspacing="0" cellpadding="1">
<thead><tr>
<td>Codice Parametro</td>
<td>Descrizione</td>
<td>Valore Default</td>
<td>Possibili Valori </td>
<td>Utente</td>
</tr></thead>
</tr><tr>
<td> UP_WEB.DEFAULT_CONTENT_PAGE</td>
<td>Gestione della pagina di default alla apertura di up web </td>
<td>Informazioni|Informazioni|Informazioni</td>
<td>tutte le pagine del menu secondario</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_WEB.STYLESHEETTHEME</td>
<td>Gestione del tema di up_web come StyleSheetTheme (alternativo a UP_WEB.THEME)</td>
<td>PlasticBlue</td>
<td>'Office2003Blue','RedWine',... tutti i temi di App_themes,</td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_WEB.THEME</td>
<td>Gestione del tema di up_web come Theme (alternativo a UP_WEB.STYLESHEETTHEME)</td>
<td>  
</td>
<td>'Office2003Blue','RedWine',... tutti i temi di App_themes,</td>
<td>![](uploads/images/check2.gif)</td>
</tr>
</table>


  
  
  
  


### Parametri UP WEB PUBL
<table border="1" cellspacing="0" cellpadding="1">
<thead><tr>
<td>Codice Parametro</td>
<td>Descrizione</td>
<td>Valore Default</td>
<td>Possibili Valori </td>
<td>Utente</td>
</tr></thead>
</tr><tr>
<td> UP_WEB_PUBL.ABILITA_STAMPE</td>
<td>Imposta se abilitare le stampe del web pubblico</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE; </td>
<td> </td>
</tr><tr>
<td> UP_WEB_PUBL.TIPO_APERT_STAMPE</td>
<td>Imposta il tipo di apertura delle stampe nel web pubblico</td>
<td>P</td>
<td>'P' - PopUp; 'O' - Open (Nuova Pagina); 'R' - Redirect (Stessa Pagina);</td>
<td> </td>
</tr><tr>
<td> UP_WEB_PUBL.DEFAULT_VISUAL_STAMPE</td>
<td>Imposta il default di visualizzazione delle stampe nella from della configurazione</td>
<td>VIS</td>
<td>'VIS' - visualizzazione; 'HTM' - html; 'EXP_PDF' - export PDF; 'EXP_XLS' - export EXCEL; 'EXP_DOC' - export WORD;</td>
<td> </td>
</tr><tr>
<td> UP_WEB_PUBL.REPORT_PANEL_VISIBLE</td>
<td>Imposta se visualizzare il pannello nel risultato delle stampe</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE; </td>
</tr><tr>
<td> UP_WEB_PUBL.REPORT_TOOLBAR_VISIBLE</td>
<td>Imposta se visualizzare la toolbar nel risultato delle stampe</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE; </td>
<td> </td>
</tr><tr>
<td> UP_WEB_PUBL.IGNORE_ANNO_REGDID</td>
<td>Indica se nella costruzione della chiave logica degli eventi va ignorato o meno l'anno di coorte (o regolamento didattico). Solitamente i dati importati da SIADI lo gestiscono, quelli da ESSE3 no.</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE; </td>
<td> </td>
</tr><tr>
<td> UP_WEB_PUBL.QTA_DUR_SLOT</td>
<td>Indica lo slot di default per le stampe</td>
<td>60</td>
<td>numerico </td>
<td>![](uploads/images/check2.gif)</td>
</tr><tr>
<td> UP_WEB_PUBL.QTA_DUR_INTERVALLO</td>
<td>Indica l'intervallo di default per le stampe</td>
<td>15</td>
<td>numerico </td>
<td>![](uploads/images/check2.gif)</td>
</tr>
</table>

  
  
  
  



### Parametri UP WS OUT
<table border="1" cellspacing="0" cellpadding="1">
<thead><tr>
<td>Codice Parametro</td>
<td>Descrizione</td>
<td>Valore Default</td>
<td>Possibili Valori </td>
<td>Utente</td>
</tr></thead>
</tr><tr>
<td> WSOUT_RF.FLG_CHECK_RF_DISP</td>
<td>WS di inserimento dell'impegno e aule, decidere se attivare il check di congruenza sulla disponibilità </td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE;</td>
<td><br/></td>
</tr><tr>
<td> WSOUT_RF.FLG_CHECK_RF_SOVR</td>
<td>WS di inserimento dell'impegno e aule, decidere se attivare il check di congruenza sulla sovrapposizione aule</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE; </td>
<td><br/></td>
</tr><tr>
<td> WSOUT_RF.FLG_CHECK_RF_COMP</td>
<td>WS di inserimento dell'impegno e aule, decidere se attivare il check di congruenza sulla compatibilità aule</td>
<td>1</td>
<td>'1' - TRUE; '0' - FALSE; </td>
<td><br/></td>
</tr><tr>
<td> WSOUT_RF.FLG_CHECK_RF_IMP_SOSP</td>
<td>WS di inserimento dell'impegno e aule, decidere se attivare il check di congruenza per gli impegni in stato sospeso</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE; </td>
<td><br/></td>
</tr><tr>
<td> WSOUT_RF.FLG_CHECK_RF_ENT_PREN</td>
<td>WS di inserimento dell'impegno e aule, decidere se il check di congruenza debba Ignorare le Entità Prenotate</td>
<td>0</td>
<td>'1' - TRUE; '0' - FALSE; </td>
<td><br/></td>
</tr>
</table>




  
  
  
  

