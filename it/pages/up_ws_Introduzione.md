e delle tabelle di base, raramente viene usato "stand-alone"; da qui l'esigenza di caricare i dati su UP e, successivamente, di recuperarli
per mostrarli all'esterno (portali web, pannelli a rotazione, ecc.)

UP è integrato coi sistemi ESSE3 o UGOV/ESSE3 (vedi sezione corrispondente cliccando [qui](up_integraz_Introduzione.md) ),
ma a partire dalla release 10.00.00.00 vengono rilasciati, tra le altre cose, i Webservices standard di input/output,
che permettono l'inserimento e la lettura dei dati direttamente da UP (ove necessario).

Nasce così il modulo UP_WS che implementa dei servizi di Import e Export.

I webServices sono stati implementati con tecnologia WCF e per ora sono "aperti".

Per maggiori informazioni riferirsi alle sezioni specifiche:
  *  [UP WS Import](up_ws_import.md)
  *  [UP WS Export](up_ws_export.md)




**N.B:** per esigenze di internazionalizzazione la documentazione e i WS sono in lingua **inglese**.
