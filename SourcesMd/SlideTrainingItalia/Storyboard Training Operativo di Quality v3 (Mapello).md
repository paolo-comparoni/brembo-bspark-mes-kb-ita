# Storyboard Training Operativo di Quality v3 (Mapello)

> Documento sorgente: `E:\BremboDocs\SlideTrainingItalia\Storyboard Training Operativo di Quality v3 (Mapello).pptx`  
> Tipo: PowerPoint (.pptx) · Slide: 44


## Slide 1: (senza titolo)

- QUALITY OPERATOR TRAINING

- OPERATORI DI QUALITÀ

- Processo Operativo Opcenter MES

- Mapello · GIUGNO 2026

**Note del relatore:**

Benvenuti al training operativo di Quality per il plant di Mapello. In questa sessione percorriamo il processo operativo su Opcenter MES, dai casi guida fino alla configurazione di sistema.


## Slide 2: (senza titolo)

- AGENDA

- INDICE DEL TRAINING

- 01

- Introduzione al training e casi guida

- Approccio bottom-up, casi di studio e confronto “Com’era” / “Come sarà”

- 02

- Reportistica extra-sistema (Power BI)

- Il risultato finale: cruscotti di produzione e qualità

- 03

- Flusso operativo dell'utente (Opcenter MES)

- I 9 punti del percorso operatore, dall'accesso alla genealogia

- 04

- Configurazione di sistema

- Master Data e arricchimento del Ciclo (Routing/BOP)

- +

- Appendice — Modifica della lingua di sistema

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Il percorso si articola in quattro capitoli più un'appendice: introduzione e casi guida, reportistica Power BI, flusso operativo MES e configurazione di sistema.


## Slide 3: (senza titolo)

- Brembo Rollout Italia

- 3

- OPCENTER MES TRAINING - QUALITY

- Link di Accesso: L’ingresso al sistema avviene tramite browser utilizzando i seguenti indirizzi (Interfaccia Gestionale per configurazione/supervisione e Terminale Operatore per l'attività in linea):
- Sito di Mapello
  - Interfaccia Gestionale (Basic UI - Engineering/Supervisione): https://it-qlt.mes.brembo.com/sit-ui/Mapello/DSBasic.Siemens_OPC_EXDSBasic
  - Terminale Operatore (Repetitive UI - Production Lines): https://it-qlt.mes.brembo.com/sit-ui/Mapello/DSBasic.BremboRepetitive_Mapello
- Sito di Curno
  - Interfaccia Gestionale (Basic UI - Engineering/Supervisione): https://it-qlt.mes.brembo.com/sit-ui/Curno/DSBasic.Siemens_OPC_EXDSBasic
  - Terminale Operatore (Repetitive UI - Production Lines): https://it-qlt.mes.brembo.com/sit-ui/Curno/DSBasic.BremboRepetitive_Curno

**Note del relatore:**

L'accesso al sistema avviene da browser. L'Interfaccia Gestionale (Basic UI) è dedicata a configurazione e supervisione, il Terminale Operatore (Repetitive UI) all'attività in linea. Sono disponibili gli indirizzi specifici per i siti di Mapello e di Curno.


## Slide 4: (senza titolo)

- 01

- INTRODUZIONE AL TRAINING E CASI GUIDA

**Note del relatore:**

Primo capitolo: introduzione al training e ai casi guida che useremo come riferimento.


## Slide 5: (senza titolo)

- 01 · INTRODUZIONE

- APPROCCIO AL TRAINING

- Il programma è focalizzato sulle attività operative quotidiane e adotta un percorso formativo dal basso verso l'alto.

- DAL CAMPO - OPERATORI

- Si parte dalle interazioni quotidiane dell'utente con il sistema MES (Avanzamento di Fabbrica).

- AL BACK-OFFICE - SUPERVISORI

- Si prosegue con le configurazioni che abilitano controlli, documenti e comportamenti di qualità.

- SU CASI REALI

- I casi studio rappresentano i processi reali attivi nei due plant.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Il training segue un approccio bottom-up: prima ciò che l'operatore fa ogni giorno, poi il back-office che lo abilita.


## Slide 6: (senza titolo)

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

- 01 · INTRODUZIONE

- CASI DI STUDIO E DATI DI TRAINING

- Ogni esempio si basa su scenari reali e copre la gestione end-to-end del processo di qualità in fonderia: dall'identificazione dell'ordine e delle specifiche tecniche, alla gestione delle non conformità (gestite esclusivamente tramite scarto diretto e scarto per singola cavità), fino alla chiusura del flusso documentale.

- ESEMPIO 1

- Casting (Fonderia)

- ESEMPIO 2

- Cutting (Taglio)

- ESEMPIO 3

- Heat Treatment (Tratt. Termico)

- Work Center

- GUGCL171

- Materiale

- SEMIPINZA S.O. FUSA — 20450700_011

- Work Order

- 1131507 · 1131508 · 1131509

- Batch

- 2601AANW · 2601AANX · 2601AANY

- Processo

- GRAVITY CASTING — 50037673 · New

- Linea / Macchina

- MACHINE 1 - I LINE

- Work Center

- GMMCT02M

- Materiale

- SEMIPINZA S.O. GREZZA — 20450700_CUT

- Work Order

- 1131510 · 1131511 · 1131512

- Batch

- 2601AANZ · 2601AAOA · 2601AAOB

- Buffer

- PSGMMCT02M

- Processo

- TAGLIO — 30204135 · New

- Linea / Macchina

- MANUAL CUTTING BAND SAW GROUP

- Work Center

- GHHTT032

- Materiale

- SEMIPINZA S.O. GREZZA — 20450700_HTT

- Work Order

- 1131513 · 1131514 · 1131515

- Batch

- 2601AAOC · 2601AAOD · 2601AAOE

- Buffer

- PSGHHTT03G

- Processo

- TRATTAMENTO TERMICO — 30204136 · New

- Linea / Macchina

- TT NOVAC 2

**Note del relatore:**

Ogni esempio si basa su scenari reali e copre la gestione end-to-end del processo di qualità in fonderia: dall'identificazione dell'ordine e delle specifiche tecniche, alla gestione delle non conformità (gestite esclusivamente tramite scarto diretto e scarto per singola cavità), fino alla chiusura del flusso documentale


## Slide 7: (senza titolo)

- 01 · L'EVOLUZIONE DEL DAY-BY-DAY

- CONFRONTO COM’ERA VS COME SARA’

- La logica di base del lavoro in linea non cambia. Ciò che cambia radicalmente è il livello di sicurezza del processo (Poka-Yoke) e l'interattività dell'interfaccia, che ora guida l'operatore passo dopo passo.

- AS-IS

- Microsoft AX

- Griglia testuale, controlli a memoria

- →

- TO-BE

- Opcenter Repetitive UI

- Task ineludibili, feedback visivo, guida passo-passo

- TRE AREE DI CONFRONTO

- A Lancio ordine ed esecuzione controlli qualità

- B Dichiarazione delle difettosità e degli scarti

- C Gestione documentale integrata

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

La logica di base non cambia: ordine, articolo e intestazioni restano. Cambiano la sicurezza di processo (Poka-Yoke) e l'interattività dell'interfaccia, che guida l'operatore passo dopo passo.


## Slide 8: (senza titolo)

- AS-IS VS TO-BE · A

- LANCIO ORDINE E CONTROLLI QUALITÀ

- AS-IS · MICROSOFT AX

- Griglia testuale in Avanzamento di Fabbrica: per registrare i controlli l'operatore deve ricordarsi di cliccare "Dati Qualità per CDI" e inserire i risultati in tabella.

- Fig. A.1 — Griglia operativa AX con comando "Modifica Dati di Qualità".

- TO-BE · OPCENTER REPETITIVE UI

- Il controllo qualità diventa un "task ineludibile": al lancio dell'ordine compare l'icona arancione a forma di aeroplanino ( Show Quality ) se ci sono test obbligatori.

- Fig. A.2 — Work Order con task "Show Quality" attivo (icona arancione).

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Con AX i controlli vanno ricordati e inseriti a mano. Con Opcenter il controllo qualità diventa un task ineludibile: l'icona arancione Show Quality compare quando ci sono test obbligatori.


## Slide 9: (senza titolo)

- AS-IS VS TO-BE · A

- REGISTRAZIONE RISULTATI: IL BLOCCO POKA-YOKE

- Nel nuovo Quality Inspection Panel l'operatore inserisce il valore misurato (es. altezza taglio o spessore pastiglia). A differenza di AX, il MES fornisce un feedback visivo immediato:

- ● Barra VERDE

- Valore a disegno / conforme

- ● Barra ROSSA

- Valore fuori tolleranza

- IL BLOCCO FUNZIONALE

- Finché l'ispezione non viene eseguita e validata, il MES disabilita fisicamente i tasti "Complete" e "Partial Complete" , impedendo di dichiarare la produzione o far avanzare il pezzo.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Nel Quality Inspection Panel l'operatore inserisce il valore misurato e riceve feedback immediato. Finché l'ispezione non è validata, Complete e Partial Complete restano bloccati.


## Slide 10: (senza titolo)

- AS-IS VS TO-BE · B

- DICHIARAZIONE DIFETTOSITÀ E SCARTI

- AS-IS · MICROSOFT AX

- La dichiarazione dello scarto è legata alle registrazioni di consumo: logiche che possono generare errori nei giornali di magazzino (es. consumi FIFO vs LIFO).

- Fig. B.1 — Procedura attuale AX per la dichiarazione degli scarti.

- TO-BE · OPCENTER REPETITIVE UI

- Pannello visivo dedicato (Defect Declaration Panel): il tasto "Defect" apre una griglia con icone (coni di segnalazione) che mostrano le causali di scarto applicabili a quel Work Center.

- Fig. B.2 — Defect Declaration Panel con selezione guidata delle causali.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

In AX la dichiarazione dello scarto è legata ai consumi e può generare errori a magazzino. In Opcenter c'è un Defect Declaration Panel visivo, con icone che mostrano le causali applicabili al Work Center.


## Slide 11: (senza titolo)

- AS-IS VS TO-BE · C

- GESTIONE DOCUMENTALE INTEGRATA

- PRIMA

- L'operatore cerca disegni tecnici, RPF o PDF separatamente su LinkerSys o cartelle di rete (MPM).

- CON OPCENTER

- La documentazione è "in contesto": il tasto Documents apre automaticamente PDF, RPF e disegni legati esclusivamente a quell'ordine, a quella macchina o a quell'articolo.

- Fig. C.1 — Pannello "Linked Documents": documenti tecnici associati al Work Order.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Oggi disegni, RPF e PDF si cercano su LinkerSys o cartelle MPM. Con Opcenter la documentazione è in contesto: il tasto Documents apre i file legati a quell'ordine, macchina o articolo.


## Slide 12: (senza titolo)

- 02

- REPORTISTICA EXTRA-SISTEMA (POWER BI)

**Note del relatore:**

Secondo capitolo: la reportistica extra-sistema su Power BI, ovvero il risultato finale alimentato dalle azioni degli operatori nel MES.


## Slide 13: (senza titolo)

- 02 · POWER BI

- IL RUOLO DI POWER BI

- Le azioni compiute dagli operatori nel MES alimentano direttamente i cruscotti aziendali su Power BI (aggiornati in pseudo real-time ). La loro consultazione è la procedura standard raccomandata per superare i limiti di navigazione dell'interfaccia base Siemens e avere il quadro completo di produzione e qualità.

- 3.1

- Navigazione Dati di Base (BOM & Routing)

- 3.2

- Genealogia Globale

- 3.3

- Analisi degli Scarti (Scrap Report)

- 3.4

- Risultati delle Quality Inspection

- 3.5

- Monitoraggio Non-Conformances (NC)

- 3.6

- Situazione Logistica (Stock Report)

- 3.7

- Production Report KPI

- Dal risultato atteso ai passaggi a sistema (Cap. 03)

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Le azioni nel MES alimentano i cruscotti Power BI in pseudo real-time. È la procedura standard per superare i limiti di navigazione dell'interfaccia base Siemens e avere il quadro completo di produzione e qualità.


## Slide 14: (senza titolo)

- POWER BI · 3.1

- NAVIGAZIONE DATI DI BASE

- BOM & ROUTING DATA MODEL

- Filtrare e navigare in modo intuitivo tra Ordini di Produzione, Materiali, Cicli di Lavoro (BOP) e Work Center , con una panoramica immediata delle anagrafiche e del carico di lavoro.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Il modello dati BOM & Routing permette di navigare in modo intuitivo tra ordini, materiali, cicli (BOP) e work center, con panoramica immediata di anagrafiche e carico di lavoro.


## Slide 15: (senza titolo)

- POWER BI · 3.2

- GENEALOGIA GLOBALE

- TRACCIABILITÀ PROFONDA

- Partire da un lotto scartato e ricostruire retrospettivamente l'intera storia produttiva, oppure tracciare in avanti il destino dei pezzi di una colata.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

La genealogia globale, detta Il Polpo, è lo strumento di tracciabilità profonda: da un lotto scartato si ricostruisce a ritroso l'intera storia, o si traccia in avanti il destino dei pezzi di una colata.


## Slide 16: (senza titolo)

- POWER BI · 3.3

- ANALISI DEGLI SCARTI — SCRAP REPORT

- NON CONFORMITÀ DEFINITIVE

- Cruscotti per interrogare le Non Conformità definitive per materiale, Work Center , periodo e singolo collo (Handling Unit Poly).

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Cruscotti dedicati alle Non Conformità definitive, interrogabili per materiale, work center, periodo e singolo collo (Handling Unit Poly).


## Slide 17: (senza titolo)

- POWER BI · 3.4

- RISULTATI DELLE QUALITY INSPECTION

- ESTRAZIONE TABULARE

- Tutti i test qualitativi eseguiti, essenziale per consultare rapidamente le note inserite dagli operatori a bordo macchina (es. anomalie su singole cavità).

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Estrazione tabulare di tutti i test qualitativi eseguiti: utile per consultare rapidamente le note inserite dagli operatori a bordo macchina, ad esempio anomalie su singole cavità.


## Slide 18: (senza titolo)

- POWER BI · 3.5 – 3.7

- NC, STOCK & PRODUCTION KPI

- 3.5

- Non-Conformances

- Lista completa delle anomalie aperte, in lavorazione o chiuse tramite Sentencing.

- 3.6

- Stock Report

- Accesso in sola lettura alle giacenze nei buffer di linea e allo storico dei movimenti di magazzino.

- 3.7

- Production KPI

- Indicatori di performance e valore economico degli scarti (Scrap Value).

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Completano il quadro: il monitoraggio delle NC aperte/chiuse, lo stock report in sola lettura sui buffer di linea e i KPI di produzione con il valore economico degli scarti.


## Slide 19: (senza titolo)

- 03

- FLUSSO OPERATIVO DELL'UTENTE (OPCENTER MES)

- 14 punti · dall'accesso al sistema alla verifica della genealogia

**Note del relatore:**

Terzo capitolo: il flusso operativo dell'utente in Opcenter MES, scandito nei nove punti del percorso operatore.


## Slide 20: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 1

- ACCESSO AL SISTEMA E RICONOSCIMENTO DEL WORK ORDER

- Accesso tramite Repetitive UI , previa selezione del Work Center con l'icona aeroplanino. Identificare plant, Work Center, Work Order, quantità associate e la presenza di controlli qualità e documenti.

- Verificare lo stato dell'ordine (da avviare, in lavorazione, completati). Le icone Show Quality e il pannello Documents confermano l'associazione di piani di ispezione e documentazione tecnica.

- Fig. 1 — Repetitive senza controlli di qualità.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 1: accesso via Repetitive UI dopo aver selezionato il Work Center. Si identificano plant, WO, quantità e la presenza di controlli e documenti; le icone Show Quality e Documents confermano le associazioni.


## Slide 21: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 2

- DOCUMENTI E CONTROLLI QUALITÀ

- L'interfaccia si aggiorna dinamicamente in base alla configurazione del Work Order. In presenza di controlli qualità configurati, l'icona Show Quality è evidenziata in arancione.

- Consultare la documentazione disponibile nel pannello di destra ( Right Zone ) e verificare l'impatto dei controlli di qualità sul completamento dell'attività operativa.

- Fig. 2 — Repetitive con controlli di quality e documentazione caricata.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 2: l'interfaccia si aggiorna in base alla configurazione del WO. Con controlli configurati Show Quality è arancione; si consultano i documenti nella Right Zone e si valuta l'impatto dei controlli sul completamento.


## Slide 22: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 3

- AVVIO DELL'ORDINE E TRACCIABILITÀ

- Il Work Order costituisce l' elemento centrale del flusso , collegando: materiali in ingresso, attività svolta, controlli eseguiti, eventuali non conformità, dichiarazioni di produzione e genealogia finale.

- Avviare l'ordine tramite il comando "Start" , inserendo la quantità di pezzi da lavorare.

- Fig. 3 — Avvio dell'ordine di lavorazione.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 3: il Work Order è l'elemento centrale del flusso e collega materiali, attività, controlli, NC, dichiarazioni e genealogia. Si avvia con Start indicando la quantità da lavorare.


## Slide 23: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 4

- ESECUZIONE DELLE ISPEZIONI E BLOCCO FUNZIONALE

- Le ispezioni obbligatorie (100% o inizio turno/ordine) attivano un blocco funzionale : i tasti "Complete" e "Partial Complete" sono inibiti fino alla validazione dei test.

- La procedura distingue controlli attributivi (OK/NOK) e variabili (valori numerici con tolleranze). Nel Quality Inspection Panel si inseriscono i valori reali con feedback visivo immediato (barra verde/rossa); i risultati sono salvati nello storico dell'ordine.

- Fig. 8 — Inserimento risultati delle ispezioni di qualità.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 4: le ispezioni obbligatorie attivano un blocco funzionale — Complete e Partial Complete restano inibiti fino alla validazione. Si distinguono controlli attributivi (OK/NOK) e variabili, con feedback verde/rosso.


## Slide 24: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 5

- DICHIARAZIONE DEI CONSUMI (COMPOMENTI)

- L'operatore registra l'ingresso fisico dei componenti tramite scansione del barcode del contenitore o selezione dell'unità materiale prevista dal flusso. L'azione scala automaticamente la quantità dal buffer/stock e collega il materiale all'ordine.

- Per l'esercitazione, l'unità di carico può essere creata manualmente, assicurando disponibilità immediata del materiale.

- Punto fondamentale: costruisce il legame tra esecuzione, genealogia e qualità del dato .

- Fig. 4 — Materiale in pre-macchina · Fig. 5 — Consumo materiali cassone.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 5: si registra l'ingresso fisico dei materiali via barcode o selezione dell'unità. L'azione scala la quantità dal buffer e lega il materiale all'ordine, costruendo il legame tra esecuzione, genealogia e qualità del dato.


## Slide 25: (senza titolo)

- Tracciabilità «Hard»: L’operatore deve scansionare o inserire manualmente l'identificativo del barcode. Con un'unica azione, il sistema acquisisce automaticamente codice materiale, lotto e quantità. Il materiale scansionato viene "scalato" dal buffer di linea e associato alla produzione in corso.
- In caso di materiali "Hard Traced", il sistema bloccherà la dichiarazione finale di produzione se tutti i componenti obbligatori non sono stati scansionati correttamente.
- Tracciabilità «Soft»: Scansione opzionale (consigliata), altrimenti il sistema consuma quel materiale con logica FIFO al momento della chiusura.
- Nessuna tracciabilità:  L'operatore visualizza i materiali ma non deve inserire dati manualmente. Il sistema esegue il consumo automatico in base alle quantità prodotte dichiarate al termine dell'operazione.

**Note del relatore:**

Punto 6: la tracciabilità dei consumi si articola su tre livelli. Hard: barcode obbligatorio, con blocco della dichiarazione finale se manca un componente. Soft: scansione consigliata, altrimenti consumo FIFO alla chiusura. Nessuna tracciabilità: consumo automatico in base alle quantità dichiarate.


## Slide 26: (senza titolo)

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 7: in Fonderia la tracciabilità è governata dall'Original Batch, il lotto di colata che segue il materiale lungo tutto il processo ed evita di mescolare cassoni di colate diverse nello stesso ordine. Generato al primo consumo al Casting, vincola in modo bloccante le fasi di Taglio e Trattamento Termico.


## Slide 27: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 8

- NON CONFORMANCE — COMPONENTE

- Per registrare materiale difettoso in ingresso (es. anime fallate), accedere al pannello Defect Declaration. Selezionare la quantità da scartare dal contenitore di provenienza e associare la causale tecnica rilevata.

- IL SISTEMA GESTISCE AUTOMATICAMENTE

- Aggiornamento Quantità: Ricalcolo delle quantità buone ancora disponibili per la produzione dell'ordine
- Gestione Logistica Fonderia: Nessuna creazione di contenitori di scarto o etichette fisiche. Il materiale viene convertito automaticamente in "chili di ritorno" (lega da rifondere) senza creare giacenze
- Integrazione ERP: Invio automatico dei messaggi di scarico a SAP
- .

- Fig. 6 — Non conformità pezzo in ingresso · Fig. 7 — Identificatore dello scarto in entrata.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

- ⚠️ REGOLA MAPELLO (FONDERIA): Sui componenti in ingresso non è attiva la Quarantena (Candidate); l'unica opzione di risoluzione consentita a sistema è lo Scarto Diretto (Immediate Scrap)

**Note del relatore:**

Punto 8: per registrare materiale difettoso in ingresso (es. anime fallate) si usa il pannello Defect Declaration, indicando quantità e causale tecnica. Il sistema ricalcola le quantità buone, converte lo scarto in chili di ritorno senza creare giacenze e invia i messaggi a SAP. Regola Mapello: sui componenti in ingresso è ammesso solo lo Scarto Diretto, senza Quarantena.


## Slide 28: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 9

- NON CONFORMANCE — PRODOTTO IN USCITA

- Fig. 9 — Dichiarazione quarantena pezzo prodotto · Fig. 10 — Identificativo cassone in quarantena.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

- Per segnalare difetti sul prodotto appena fuso (il "ragno") si utilizzano i pulsanti Defect Declaration o l'apposito pannello Defect on Cavity. Occorre selezionare la causale tecnica appropriata all'anomalia rilevata.

- OPZIONI DISPONIBILI

- Scarto Immediato (Immediate Scrap): Scarto dell'intero pezzo prodotto, destinato direttamente alla rifusione
- Scarto per singola Cavità (Defect on Cavity): Segnalazione a sistema di una singola parte difettosa. Il MES memorizza l'informazione e sottrarrà automaticamente la quantità scartata nella fase di lavorazione successiva
- .

- ⚠️ REGOLA MAPELLO (FONDERIA): Anche sul prodotto in uscita non è consentito l'uso dello stato "Candidate" (Quarantena)

**Note del relatore:**

Punto 9: i difetti sul prodotto appena fuso (il ragno) si dichiarano con Defect Declaration o Defect on Cavity, scegliendo la causale tecnica. Le opzioni sono lo Scarto Immediato dell'intero pezzo o lo scarto per singola cavità, sottratto automaticamente nella fase successiva. Anche in uscita, a Mapello non è consentita la Quarantena.


## Slide 29: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 10

- NON CONFORMANCE — PRODOTTO IN USCITA`—  SCARTO DI CAVITÁ

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 10: con il pulsante Declare NC si apre una nuova Non-Conformità e si scarta la singola cavità della mold segnandola con una “X” direttamente sul pannello. Quando l'operatore del taglio consuma il ragno nella fase di cutting, il MES genera automaticamente lo scarto per le cavità marcate.


## Slide 30: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 11

- DECISIONE DEL SUPERVISORE - SENTENCING (⚠️ NON APPLICABILE A MAPELLO)

- Il Supervisore analizza le Non Conformità aperte dal terminale operatore e conclude il ciclo della qualità tramite il Sentencing , definendo il destino finale del materiale sospeso a sistema.

- Ogni Sentencing su materiale in quarantena genera un Outbound Message verso SAP ERP, tecnicamente un "Good Movement" , che indica all'ERP dove spostare contabilmente il materiale — garantendo l'allineamento tra giacenza a sistema e realtà fisica.

- Fig. 11 — Sentencing "Close and Return to Work" · Fig. 12 — Dichiarazione produzione.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 11: il Supervisore conclude il ciclo qualità con il Sentencing, decidendo il destino del materiale sospeso. Ogni sentencing genera un Outbound Message verso SAP (Good Movement) che allinea giacenza a sistema e realtà fisica.


## Slide 31: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 12

- GLI STATI DEL SENTENCING (⚠️ NON APPLICABILE A MAPELLO)

- Stato

- Significato operativo

- Impatto tecnico / SAP

- Quarantine (current)

- Stato di partenza in attesa di giudizio; l'MTU è bloccata e isolata dal flusso.

- Nessun messaggio di risoluzione logistica ancora inviato a SAP.

- Close & Return to Work Buono

- Materiale idoneo (falso allarme/deroga): rientra subito nel flusso di produzione.

- Good Movement da "Quarantena" a "Buono"; unità sbloccata, nessun impatto sui KPI, WO avanza.

- Scrap Scarto interno definitivo

- Pezzo irrecuperabile per difetto interno; spostato fisicamente nella baia scarti.

- Good Movement verso "Scrap"; SAP riduce la quantità producibile e alimenta il KPI Scrap Rate.

- Bremborework
- Conto lavoro responsabilità Brembo

- Riparazione fisica interna: i resi per conto lavoro implicano un vero e proprio cambio del codice a sistema tramite un ordine dedicato.

- Opcenter genera un nuovo WO di rework; SAP registra movimento e costi; a fine ciclo la quantità rientra nel WO originale.

- External Rework
- Conto lavoro responsabilità esterna

- Riparazione non eseguibile internamente: invio a fornitore esterno.

- La logistica lancia in SAP un ordine di conto lavoro per uscita, lavorazione e cambio codice al rientro.

- External Scrap Causa esterna

- Scarto imputabile a processo/fornitore esterno (es. difetto rilevato ai Raggi X).

- Materiale scartato; la causale isola la responsabilità e gestisce il reso senza gravare sui KPI interni.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

I sei stati applicabili nel Sentencing: dalla quarantena di partenza al rientro a buono, allo scarto interno, alle rilavorazioni interna ed esterna, fino allo scarto per causa esterna — ciascuno con un preciso impatto su SAP e KPI.


## Slide 32: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 13

- CHIUSURA DELL'ATTIVITÀ E VERIFICA GENEALOGIA

- Al termine del processo, consultare la pagina "As Built Order" per il registro storico completo dell'ordine.

- CORRELA INDISSOLUBILMENTE

- ▸ Lotti consumati ▸ Risultati delle ispezioni ▸ Dichiarazioni di difetto ▸ Decisioni di sentencing ▸ Quantità prodotte e scartate

- Fig. 13 — Dichiarazione produzione · Fig. 14 — Tracciamento ispezioni · Fig. 15 — Tracciamento non conformità.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 13: a fine processo la pagina As Built Order fornisce il registro storico completo, correlando lotti consumati, ispezioni, dichiarazioni di difetto, sentencing e quantità prodotte/scartate.


## Slide 33: (senza titolo)

- Visualizzazione gerarchica completa che lega Work Order a ogni singola MTU, Batch o numero di serie.
- Integrazione Dati Produzione e Qualità:
  - Tracciabilità dei materiali consumati e prodotti.
  - Associazione automatica dei risultati dei test alla genealogia del pezzo.

- FONDERIA
- Colata e solidificazione del greggio

- LAVORAZIONEMECCANICA
- Tornitura, fresatura, foratura

- TRATTAMENTOSUPERFICIALE
- Ossidazione, verniciatura

- ASSEMBLAGGIO
- Montaggio pinza / componenti

- PACKAGING
- Confezionamento e spedizione

- FORWARD TRACEABILITY  →  dall'origine al prodotto finito

- BACKWARD TRACEABILITY  ←  dal prodotto finito all'origine

- Forward Traceability
- Seguire un lotto, un CDI/Handling Unit o un requisito dal punto di origine verso le fasi successive. Utile per confermare quali pezzi finiti sono stati prodotti da un determinato lotto di greggio o per monitorare l'avanzamento della produzione nelle varie fasi del ciclo.
- Esempio: dato un lotto in Fonderia, verificare quanti pezzi sono arrivati al Packaging e con quali esiti qualitativi.

- Backward Traceability
- Partendo da un difetto rilevato o da un pezzo finito, risalire alle fasi precedenti fino al lotto di origine, alla materia prima e al fornitore. Ogni misura, scarto e decisione di sentencing è legata indissolubilmente al CDI/MTU del pezzo.
- Esempio: da un reclamo cliente sul prodotto in Packaging, risalire alla colata di Fonderia e al lotto di materia prima.

- CONCETTO CHIAVE · PUNTO 14

- RICERCA NELLA GENEALOGIA

**Note del relatore:**

Punto 14: la genealogia offre una vista gerarchica che lega il Work Order a ogni MTU, batch o numero di serie lungo tutte le fasi, dalla fonderia al packaging. Con la forward traceability si segue un lotto verso le fasi successive; con la backward traceability si risale da un difetto o da un reclamo fino alla colata e alla materia prima d'origine.


## Slide 34: (senza titolo)

- 04

- CONFIGURAZIONE DI SISTEMA (ENGINEERING)

**Note del relatore:**

Quarto capitolo: la configurazione di sistema lato Engineering — Master Data e arricchimento del Routing.


## Slide 35: (senza titolo)

- Brembo Rollout Italia

- 35

- GESTIONE QUALITA’

  - Il MES come layer operativo: Siemens Opcenter Discrete opera al Livello 3 dello standard ISA-95, agendo come l'interfaccia che converte i dati provenienti dall'ERP in istruzioni operative per lo Shop Floor e trasmette i flussi di produzione (conforme e scarto) verso i sistemi gestionali
  - Architettura Modulare: La soluzione adotta una struttura funzionale modulare per coordinare in un unico ambiente digitale i diversi domini operativi — tra cui produzione, logistica, qualità e manutenzione — garantendo l'integrazione di tutte le componenti funzionali della fabbrica
  - Il Modulo di Quality: governa la conformità dei processi definendo i requisiti tecnici (Engineering), validando i dati "As-Built" in linea (Runtime) e amministrando le non conformità (Supervisione), assicurando la tracciabilità a lungo termine
  - Integrazione Qualità-Produzione: Le ispezioni "In-Process" 📋 sono integrate direttamente nelle fasi di lavorazione standard del ciclo di lavoro (BOP). Il controllo qualitativo viene visualizzato come un task operativo obbligatorio per l'operatore, rendendo la verifica della conformità parte integrante dell'esecuzione fisica del pezzo

**Note del relatore:**

Opcenter Discrete opera al Livello 3 dello standard ISA-95: converte i dati dell'ERP in istruzioni per lo Shop Floor e restituisce i flussi di produzione e scarto ai gestionali. L'architettura è modulare e il modulo Quality governa requisiti tecnici (Engineering), validazione dei dati As-Built (Runtime) e gestione delle non conformità (Supervisione), con le ispezioni in-process integrate come task obbligatori nel ciclo.


## Slide 36: (senza titolo)

- CONFIGURAZIONE · PUNTO 10

- MASTER DATA — CARATTERISTICHE, ISPEZIONI & DOCUMENTI

- La gestione dei dati anagrafici avviene in Back-Office ( Basic UI ) e si articola su Caratteristiche, Definizione delle Ispezioni e Documenti. Le caratteristiche (Attributive, Variabili, Visuali) sono collegate alle ispezioni.

- Principio dell'ereditarietà : i parametri configurati nel Routing (BOP) sono trasferiti nativamente ai Work Order al download da SAP.

- La pagina "Documents" è anagrafica centrale per file tecnici, disegni e istruzioni, con versioning e categorizzazione.

- Fig. 16 — Ispezioni · Fig. 17 — Tolleranza e valore nominale · Fig. 18 — Anagrafica documenti.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 10: i Master Data si gestiscono in Basic UI — Characteristics, Inspection Definition e Documents. Per ereditarietà i parametri del Routing passano nativamente ai Work Order al download da SAP.


## Slide 37: (senza titolo)

- CONFIGURAZIONE · PUNTO 11

- ARRICCHIMENTO (ENRICHMENT)

- L'arricchimento qualitativo avviene primariamente a livello di Routing (BOP) : lo scheletro del processo ricevuto da SAP viene integrato con i parametri tecnici e di qualità necessari all'esecuzione nel MES.

- Principio dell'Inheritance : al caricamento di una nuova versione di Routing, il MES tenta il merge automatico copiando piani di controllo e documenti dalla versione precedente.

- In caso di incompatibilità strutturale (es. variazione nel numero di operazioni) può servire un allineamento manuale.

- Fig. 19 — Inserimento dei controlli di qualità nel routing.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Punto 11: l'arricchimento qualitativo avviene a livello di Routing (BOP). Il MES, al caricamento di una nuova versione, tenta il merge automatico copiando piani di controllo e documenti dalla versione precedente.


## Slide 38: (senza titolo)

- CONFIGURAZIONE · PUNTO 12

- EREDITARIETÀ E INTERVENTI MANUALI

- I Work Order ereditano nativamente le configurazioni dal Routing al download da SAP. L'arricchimento manuale della BOP via Basic UI è operazione straordinaria (nuovi prodotti o revisioni tecniche).

- Se un ordine è già stato importato privo di ispezioni, si interviene eccezionalmente sul singolo ordine via Work Order Operation Detail .

- IL SALVATAGGIO ABILITA SUL TERMINALE

- ▸ Presenza di controlli qualità ▸ Documentazione associata ▸ Esperienza utente coerente con il training

- Fig. 20 — Collegamento a documento esistente · Fig. 21 — Aggiunta delle quality inspection al Work Order.

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

L'arricchimento manuale della BOP è straordinario. Se un ordine arriva senza ispezioni si interviene sul singolo ordine via Work Order Operation Detail. Il salvataggio allinea Back-Office e Repetitive UI.


## Slide 39: (senza titolo)

- APPENDICE

- MODIFICA DELLA LINGUA DI SISTEMA

- Nota: per gli operatori di linea l'interfaccia deve rimanere in Italiano per la sicurezza dei processi. L'opzione è riservata a back-office e supervisori.

- Schermata di accesso

- Selezione diretta della lingua nella pagina di Login. (Fig. 6.1)

- Profilo utente — UMC

- User Profile → Change Language → seleziona → Save. (Fig. 6.2)

- Profilo — Repetitive UI

- Icona utente → My Profile → seleziona → Save. (Fig. 6.3)

- Effetto: traduzione in tempo reale di home page, barra laterale e cruscotti operativi (eseguire il refresh del browser).

- QUALITY OPERATOR TRAINING — MAPELLO

- B-SPARK MES

**Note del relatore:**

Appendice: Opcenter è multi-lingua. Per gli operatori di linea l'interfaccia resta in Italiano per sicurezza; la lingua si cambia dalla schermata di login, dal profilo UMC o dal profilo Repetitive UI, con effetto in tempo reale dopo un refresh.


## Slide 40: UI – 1. Pagine di Engineering & Pianificazione (Master Data)

- Brembo Rollout Italia

- 40

- UI – 1. Pagine di Engineering & Pianificazione (Master Data)

|  | Characteristics | Elenco generale delle caratteristiche: Attributive (OK/NOK), Variabili (numeriche) o Visuali. |
| --- | --- | --- |
|  | Characteristic Detail | Qui si impostano Valori Nominali e Tolleranze, opzionalmente potremmo collegare la misura a una o piú "Potential Failure (opzione non utilizzata per non creare NC di tipo diverso) |
|  | Inspection Definitions<br><br> | Configurazione delle frequenze (100%, Time/Part/Unit Based) e associazione della caratteristica. |
|  | Inspection Detail | Nella tab Referenced Materials si possono ridefinire target e tolleranze per ogni singolo Part Number |
|  | Failures | Catalogo generale dei difetti tecnici censiti nel sistema. |
|  | Failure Details | Definizione della gerarchia tra difetti (Failure e Sub-Failures). |

|  | Non Conformance Lifecycles | Definizione dei workflow per le anomalie (stati come Open, In Progress, Closed). |
| --- | --- | --- |
|  | NC Lifecycle Detail | Regole tecniche di transizione tra gli stati e ruoli autorizzati alla chiusura. |
|  | Documents | Gestione della libreria documentale (PDF tecnici, RPF, FAOM). |
|  | Document Detail | Scheda per la revisione e categorizzazione dei singoli documenti. |

- OPCENTER MES TRAINING - QUALITY

**Note del relatore:**

Panoramica delle pagine di Engineering e pianificazione per i Master Data: Characteristics e relativo dettaglio (valori nominali e tolleranze), Inspection Definitions con le frequenze, il catalogo Failures, i Non Conformance Lifecycles e la libreria Documents. Sono le anagrafiche su cui si fonda la configurazione della qualità.


## Slide 41: UI – 1. Pagine di Engineering & Pianificazione (Integrazione Processo)

- Brembo Rollout Italia

- 41

- UI – 1. Pagine di Engineering & Pianificazione (Integrazione Processo)

|  | As Planned BOPs and Processes | Struttura del ciclo di lavoro (Routing/BOP) ereditato da SAP. |
| --- | --- | --- |
|  | As Planned BOPs and Processes Detail | Associazione Engineering: Si collegano le Inspection Definitions alle specifiche operazioni. |
|  | Work Orders | Elenco degli ordini di produzione; l'ordine eredita automaticamente i controlli via Enrichment. |
|  | Work Order Operation Detail | Associazione manuale (*): Consente di linkare ispezioni o documenti a ordini già rilasciati (usato nel training). |

- Ogni gruppo  accede alle UI e prende visione delle varie pagine

- OPCENTER MES TRAINING - QUALITY

**Note del relatore:**

Pagine di integrazione di processo: As Planned BOPs and Processes per il ciclo ereditato da SAP, con associazione delle Inspection Definitions alle operazioni, e i Work Orders che ereditano i controlli via Enrichment. Il Work Order Operation Detail consente l'associazione manuale di ispezioni o documenti a ordini già rilasciati, come nell'esercitazione.


## Slide 42: UI – 2. Pagine di Runtime & Esecuzione (Production Line)

- Brembo Rollout Italia

- 42

- UI – 2. Pagine di Runtime & Esecuzione (Production Line)

|  | Operator<br>         Terminal <br>         (Repetitive) | Schermata principale: il pulsante "Show Quality" diventa arancione se ci sono ispezioni obbligatorie. |
| --- | --- | --- |
|  | Quality <br>Inspection<br>Panel | Maschera per l'inserimento dei valori reali; il sistema valida con barre verdi (OK) o rosse (NOK). |
|  | Defect               Declaration<br>Panel | Pannello per dichiarare difetti tecnici o scarti (es. scarto cavità o sub-unit in fonderia). |

- Ogni gruppo  accede alle UI e prende visione delle varie pagine

- OPCENTER MES TRAINING - QUALITY

**Note del relatore:**

Pagine di runtime sulla linea di produzione: l'Operator Terminal (Repetitive) con il pulsante Show Quality che diventa arancione in presenza di ispezioni obbligatorie, il Quality Inspection Panel per l'inserimento dei valori con validazione verde/rossa e il Defect Declaration Panel per dichiarare difetti e scarti.


## Slide 43: UI – 3. Pagine di Supervising (Decisione e Tracciabilità)

- Brembo Rollout Italia

- 43

- UI – 3. Pagine di Supervising (Decisione e Tracciabilità)

- OPCENTER MES TRAINING - QUALITY

- Ogni gruppo  accede alle UI e prende visione delle varie pagine

|  | Non Conformances | Elenco e monitoraggio di tutte le segnalazioni aperte dalle linee di produzione. |
| --- | --- | --- |
|  | Non Conformance Details | Sentencing: Il supervisore decide il destino del pezzo (Scrap, Rework o Return to work). |
|  | As Built Order | Tracciabilità Totale: Registro storico indissolubile con esiti qualità, consumi e log delle attività del Work Order [18, 25.1]. |

**Note del relatore:**

Pagine di supervisione: Non Conformances per il monitoraggio delle segnalazioni aperte dalle linee, il Non Conformance Detail dove il supervisore esegue il Sentencing (Scrap, Rework o Return to Work) e l'As Built Order, registro storico completo con esiti qualità, consumi e log delle attività del Work Order.


## Slide 44: (senza titolo)

- QUALITY OPERATOR TRAINING · Mapello

- Grazie per l'attenzione.

- Paolo Comparoni

- Engineering

- Emanuele Merlo

- Engineering

**Note del relatore:**

Grazie per l'attenzione. Spazio alle domande. Riferimenti: Paolo Comparoni ed Emanuele Merlo, Engineering.
