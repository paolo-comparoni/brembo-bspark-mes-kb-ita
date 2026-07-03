# B-Spark_Golden set_W1_template per SIT-UAT — Foglio: Issues M013_M014_M015

> Documento sorgente: `E:\BremboDocs\GoldenSet\B-Spark_Golden set_W1_template per SIT-UAT.xlsx`  
> Tipo: Excel (.xlsx) · Foglio: **Issues M013_M014_M015** · Righe dati: 25 · Colonne: 2

| DATA MIGRATION OBJECT | ISSUES |
| --- | --- |
| BOM | File estratto il 19/12 da AX con le logiche di CZ senza implementare le necesarie modifiche condivise per W1 (come dichiarato da IT Brembo). |
|  | Componenti mancanti nel file / modificati manualmente da Panzeri a valle meeting del 07/01 per ovviare a diverse casistiche:<br>- rispettare le regole definite per il data model in quanto l'estrattore non è in grado di recuperare il "main material" e ciò non consente il ;<br>- recuperare i Co-product delle BOM delle anime;<br>- Subcontracting non standard Ostrava non li becca<br>regole rework in painting<br>- Panzeri il 12/01 invia dicendo che estrattore è da rivedere in tal senso per Mock2 |
|  | Materiali padri/componenti non ricevuti nel file M012 |
|  | Data inizio validità non aggiornata |
|  | ID Alfanumerico della posizione |
|  | Componenti a qtà 0,000 |
| ROUTING | File estratto il 19/12 da AX con le logiche di CZ senza implementare le necesarie modifiche condivise per W1 (come dichiarato da IT Brembo). |
|  | L'estrattore non è in grado di estrarre i cicli multi-fase: modifiche ad estrattore necessarie per Mock-2.<br>Per Mock-1 Brembo probabilmente procederà a modifiche manuali del file (TBC by Brembo) |
|  | Cicli già esistenti per la denominazione fornita... vedi l’elenco nel prossimo commento; |
|  | Operazioni con centro di lavoro mancante (valore vuoto non consentito) / centro di lavoro inesistente... -> Brembo ha dovuto integrare/modificare la tabella di trascodifica dei work center utilizzata dall'estrattore |
|  | ID gruppo ciclo duplicato assegnato a materiali diversi in stabilimenti differenti; |
|  | Data inizio validità predefinita è 01/01/2025, non 01/01/2024; |
|  | Intervallo di validità quantità superiore: valore predefinito ricevuto = 0 ; |
|  | Campo rilevanza per il costing mancante; |
|  | Compilare il valore WERKS_WORK_CNTR : la mancanza di questo campo ha comportato per Capgemini notevole effort per dover eseguire n check per poter assegnare al ciclo le corrette operazioni data la mancanza del plant in chiave e il campo chiave del ciclo duplicato per plant (SAP supporta chiave ciclo univoca non legata al plant) |
| ASSEGNAZIONE COMPONENTI AD OPERAZIONI | Non è stato ricevuto il file contente , nel caso di cicli multifase, l'assegnazione dei componenti della BOM all'operazione corretta. Questo step non può esser fatto in maniera disgiunta dalla migrazione massiva dei cicli e pertanto sarebbe da fare con uno strumento diverso dal cockpit SAP. Per Mock1 questo task è in carico a user Brembo. |
| ROUTING CLASSIFICATION | La classificazione dei cicli per Mock1 sarà caricata manualmente in SAP da Capgemini su indicazione di Brembo mentre per Mock2 ci sarà fornito file per migrazione massiva in SAP. Non avendo potuto caricare i cicli, questo oggetto non è stato ancora lavorato |
| REFERENCE ROUTING (Mold preparation) | Per Mock1 non sono stati ricevuti file su questo oggetto. In data 08.01 Brembo ha condiviso che il caricamento in SAP sarà eseguito manualmente da loro user. Meeting di allineamento convocato da Brembo in data 14.01 |
| PRODUCTION VERSION | File estratto il 19/12 da AX con le logiche di CZ senza implementare le necesarie modifiche condivise per W1 (come dichiarato da IT Brembo). |
|  | Nuova codifica versione produzione non considerata nell'estrattore |
|  | Data inizio validità non aggiornata |
|  | Material Maximum Lot Size Quantity non coerente con quella presente nel ciclo |
|  | campo VERTO (Distribution Key) non valorizzato |
|  | Non avendo potuto caricare i dati anagrafici precedenti propedeutici non è stato possibile eseguire alcun tentativo di caricamento |
