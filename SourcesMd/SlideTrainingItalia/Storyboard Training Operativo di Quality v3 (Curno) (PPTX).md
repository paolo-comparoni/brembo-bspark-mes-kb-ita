# Storyboard Training Operativo di Quality v3 (Curno)

> Documento sorgente: `E:\BremboDocs\SlideTrainingItalia\Storyboard Training Operativo di Quality v3 (Curno).pptx`  
> Tipo: PowerPoint (.pptx) · Slide: 44


## Slide 1: (senza titolo)

- QUALITY OPERATOR TRAINING

- OPERATORI DI QUALITÀ

- Processo Operativo Opcenter MES

- CURNO · GIUGNO 2026

**Note del relatore:**

Benvenuti al training operativo di Quality per il plant di Curno. In questa sessione percorriamo il processo operativo su Opcenter MES, dai casi guida fino alla configurazione di sistema.


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

- QUALITY OPERATOR TRAINING — CURNO

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

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Il training segue un approccio bottom-up: prima ciò che l'operatore fa ogni giorno, poi il back-office che lo abilita.


## Slide 6: (senza titolo)

- 01 · INTRODUZIONE

- CASI DI STUDIO E DATI DI TRAINING

- Ogni esempio si basa su scenari reali e copre la gestione end-to-end del processo di qualità: dall'identificazione dell'ordine e delle specifiche tecniche, alla gestione delle non conformità, fino al sentencing e alla chiusura del flusso documentale.

- ESEMPIO 1

- Machining (Washing)

- Work Center

- SWHPM01M

- Operazione

- Lavaggio alta pressione

- ESEMPIO 2

- Assembly (2ª Fase)

- Work Center

- SACSA012

- Operazione

- Collaudo + completamento

- ESEMPIO 3

- Friction / Pads

- Work Center

- FMPGM01M

- Operazione

- Rettifica (MHT & SBP)

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Tre casi guida coprono la gestione end-to-end del processo di qualità: dall'identificazione dell'ordine al sentencing e alla chiusura documentale.


## Slide 7: (senza titolo)

- CASO DI STUDIO 01

- MACHINING (WASHING)

- WORK CENTER

- SWHPM01M

- High Pressure Washing Machine

- OPERAZIONE

- Lavaggio Alta Pressione

- MATERIALI E BOP ASSOCIATI

- Materiale

- Descrizione

- BOP

- WO di riferimento

- 20D17837_WSH

- Corpo pinza lavorato

- 1131378

- 1131047

- 20D17838_WSH

- Corpo pinza lavorato

- 1131379

- 1131320

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Caso 1: lavaggio ad alta pressione del corpo pinza lavorato. Due materiali con i rispettivi BOP e Work Order di riferimento.


## Slide 8: (senza titolo)

- CASO DI STUDIO 02

- ASSEMBLY (SECONDA FASE)

- WORK CENTER

- SACSA012

- Monoblocco 12 Second Assembly

- OPERAZIONE

- Collaudo + Completamento

- Tipo

- Materiale

- Descrizione

- BOP

- WO

- PINZE SX

- 20E63341

- Pinza M6.28/32/36 SX

- 30235294

- 1131383

- 20E63345

- Pinza M6.28/32/36 SX

- 30235298

- 1131387

- 20E63347

- Pinza M6.28/32/36 SX

- 30235300

- 1131386

- PINZE DX

- 20E63342

- Pinza M6.28/32/36 DX

- 30235295

- 1131384

- 20E63344

- Pinza M6.28/32/36 DX

- 30235297

- 1131388

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Caso 2: seconda fase di assemblaggio, collaudo e completamento. Materiali distinti per pinze SX e DX.


## Slide 9: (senza titolo)

- CASO DI STUDIO 03

- FRICTION / PADS (RETTIFICA)

- Gruppo 1 — Ordini MHT

- Molding & Heat Treatment · Stampaggio → Rettifica → Forno Statico

- Materiale

- BOP

- WO

- 47D66964VE_MHT

- 40010793

- 1131382

- 47D66965VE_MHT

- 40010796

- 1131131

- Gruppo 2 — Ordini SBP

- Shot Blasting & Painting · Pallinatura → Rettifica → Verniciatura

- Materiale

- BOP

- WO

- 47D66964VE_SBP

- 40010794

- 1131380

- 47D66965VE_SBP

- 40010797

- 1131381

- Operazione comune: Rettifica · per gli ordini SBP Rettifica Parallelismo — fase intermedia del ciclo.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Caso 3: rettifica delle pastiglie, in due varianti di ciclo — ordini MHT (stampaggio) e SBP (pallinatura). Stesso Work Center, operazioni diverse.


## Slide 10: (senza titolo)

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

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

La logica di base non cambia: ordine, articolo e intestazioni restano. Cambiano la sicurezza di processo (Poka-Yoke) e l'interattività dell'interfaccia, che guida l'operatore passo dopo passo.


## Slide 11: (senza titolo)

- AS-IS VS TO-BE · A

- LANCIO ORDINE E CONTROLLI QUALITÀ

- AS-IS · MICROSOFT AX

- Griglia testuale in Avanzamento di Fabbrica: per registrare i controlli l'operatore deve ricordarsi di cliccare "Dati Qualità per CDI" e inserire i risultati in tabella.

- Fig. A.1 — Griglia operativa AX con comando "Modifica Dati di Qualità".

- TO-BE · OPCENTER REPETITIVE UI

- Il controllo qualità diventa un "task ineludibile": al lancio dell'ordine compare l'icona arancione a forma di aeroplanino ( Show Quality ) se ci sono test obbligatori.

- Fig. A.2 — Work Order con task "Show Quality" attivo (icona arancione).

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Con AX i controlli vanno ricordati e inseriti a mano. Con Opcenter il controllo qualità diventa un task ineludibile: l'icona arancione Show Quality compare quando ci sono test obbligatori.


## Slide 12: (senza titolo)

- AS-IS VS TO-BE · A

- REGISTRAZIONE RISULTATI: IL BLOCCO POKA-YOKE

- Nel nuovo Quality Inspection Panel l'operatore inserisce il valore misurato (es. altezza taglio o spessore pastiglia). A differenza di AX, il MES fornisce un feedback visivo immediato:

- ● Barra VERDE

- Valore a disegno / conforme

- ● Barra ROSSA

- Valore fuori tolleranza

- IL BLOCCO FUNZIONALE

- Finché l'ispezione non viene eseguita e validata, il MES disabilita fisicamente i tasti "Complete" e "Partial Complete" , impedendo di dichiarare la produzione o far avanzare il pezzo.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Nel Quality Inspection Panel l'operatore inserisce il valore misurato e riceve feedback immediato. Finché l'ispezione non è validata, Complete e Partial Complete restano bloccati.


## Slide 13: (senza titolo)

- AS-IS VS TO-BE · B

- DICHIARAZIONE DIFETTOSITÀ E SCARTI

- AS-IS · MICROSOFT AX

- La dichiarazione dello scarto è legata alle registrazioni di consumo: logiche che possono generare errori nei giornali di magazzino (es. consumi FIFO vs LIFO).

- Fig. B.1 — Procedura attuale AX per la dichiarazione degli scarti.

- TO-BE · OPCENTER REPETITIVE UI

- Pannello visivo dedicato (Defect Declaration Panel): il tasto "Defect" apre una griglia con icone (coni di segnalazione) che mostrano le causali di scarto applicabili a quel Work Center.

- Fig. B.2 — Defect Declaration Panel con selezione guidata delle causali.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

In AX la dichiarazione dello scarto è legata ai consumi e può generare errori a magazzino. In Opcenter c'è un Defect Declaration Panel visivo, con icone che mostrano le causali applicabili al Work Center.


## Slide 14: (senza titolo)

- AS-IS VS TO-BE · C

- GESTIONE DOCUMENTALE INTEGRATA

- PRIMA

- L'operatore cerca disegni tecnici, RPF o PDF separatamente su LinkerSys o cartelle di rete (MPM).

- CON OPCENTER

- La documentazione è "in contesto": il tasto Documents apre automaticamente PDF, RPF e disegni legati esclusivamente a quell'ordine, a quella macchina o a quell'articolo.

- Fig. C.1 — Pannello "Linked Documents": documenti tecnici associati al Work Order.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Oggi disegni, RPF e PDF si cercano su LinkerSys o cartelle MPM. Con Opcenter la documentazione è in contesto: il tasto Documents apre i file legati a quell'ordine, macchina o articolo.


## Slide 15: (senza titolo)

- 02

- REPORTISTICA EXTRA-SISTEMA (POWER BI)

**Note del relatore:**

Secondo capitolo: la reportistica extra-sistema su Power BI, ovvero il risultato finale alimentato dalle azioni degli operatori nel MES.


## Slide 16: (senza titolo)

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

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Le azioni nel MES alimentano i cruscotti Power BI in pseudo real-time. È la procedura standard per superare i limiti di navigazione dell'interfaccia base Siemens e avere il quadro completo di produzione e qualità.


## Slide 17: (senza titolo)

- POWER BI · 3.1

- NAVIGAZIONE DATI DI BASE

- BOM & ROUTING DATA MODEL

- Filtrare e navigare in modo intuitivo tra Ordini di Produzione, Materiali, Cicli di Lavoro (BOP) e Work Center , con una panoramica immediata delle anagrafiche e del carico di lavoro.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Il modello dati BOM & Routing permette di navigare in modo intuitivo tra ordini, materiali, cicli (BOP) e work center, con panoramica immediata di anagrafiche e carico di lavoro.


## Slide 18: (senza titolo)

- POWER BI · 3.2

- GENEALOGIA GLOBALE

- TRACCIABILITÀ PROFONDA

- Partire da un lotto scartato e ricostruire retrospettivamente l'intera storia produttiva, oppure tracciare in avanti il destino dei pezzi di una colata.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

La genealogia globale, detta Il Polpo, è lo strumento di tracciabilità profonda: da un lotto scartato si ricostruisce a ritroso l'intera storia, o si traccia in avanti il destino dei pezzi di una colata.


## Slide 19: (senza titolo)

- POWER BI · 3.3

- ANALISI DEGLI SCARTI — SCRAP REPORT

- NON CONFORMITÀ DEFINITIVE

- Cruscotti per interrogare le Non Conformità definitive per materiale, Work Center , periodo e singolo collo (Handling Unit Poly).

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Cruscotti dedicati alle Non Conformità definitive, interrogabili per materiale, work center, periodo e singolo collo (Handling Unit Poly).


## Slide 20: (senza titolo)

- POWER BI · 3.4

- RISULTATI DELLE QUALITY INSPECTION

- ESTRAZIONE TABULARE

- Tutti i test qualitativi eseguiti, essenziale per consultare rapidamente le note inserite dagli operatori a bordo macchina (es. anomalie su singole cavità).

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Estrazione tabulare di tutti i test qualitativi eseguiti: utile per consultare rapidamente le note inserite dagli operatori a bordo macchina, ad esempio anomalie su singole cavità.


## Slide 21: (senza titolo)

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

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Completano il quadro: il monitoraggio delle NC aperte/chiuse, lo stock report in sola lettura sui buffer di linea e i KPI di produzione con il valore economico degli scarti.


## Slide 22: (senza titolo)

- 03

- FLUSSO OPERATIVO DELL'UTENTE (OPCENTER MES)

- 9 punti · dall'accesso al sistema alla verifica della genealogia

**Note del relatore:**

Terzo capitolo: il flusso operativo dell'utente in Opcenter MES, scandito nei nove punti del percorso operatore.


## Slide 23: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 1

- ACCESSO AL SISTEMA E RICONOSCIMENTO DEL WORK ORDER

- Accesso tramite Repetitive UI , previa selezione del Work Center con l'icona aeroplanino. Identificare plant, Work Center, Work Order, quantità associate e la presenza di controlli qualità e documenti.

- Verificare lo stato dell'ordine (da avviare, in lavorazione, completati). Le icone Show Quality e il pannello Documents confermano l'associazione di piani di ispezione e documentazione tecnica.

- Fig. 1 — Repetitive senza controlli di qualità.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Punto 1: accesso via Repetitive UI dopo aver selezionato il Work Center. Si identificano plant, WO, quantità e la presenza di controlli e documenti; le icone Show Quality e Documents confermano le associazioni.


## Slide 24: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 2

- DOCUMENTI E CONTROLLI QUALITÀ

- L'interfaccia si aggiorna dinamicamente in base alla configurazione del Work Order. In presenza di controlli qualità configurati, l'icona Show Quality è evidenziata in arancione.

- Consultare la documentazione disponibile nel pannello di destra ( Right Zone ) e verificare l'impatto dei controlli di qualità sul completamento dell'attività operativa.

- Fig. 2 — Repetitive con controlli di quality e documentazione caricata.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Punto 2: l'interfaccia si aggiorna in base alla configurazione del WO. Con controlli configurati Show Quality è arancione; si consultano i documenti nella Right Zone e si valuta l'impatto dei controlli sul completamento.


## Slide 25: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 3

- AVVIO DELL'ORDINE E TRACCIABILITÀ

- Il Work Order costituisce l' elemento centrale del flusso , collegando: materiali in ingresso, attività svolta, controlli eseguiti, eventuali non conformità, dichiarazioni di produzione e genealogia finale.

- Avviare l'ordine tramite il comando "Start" , inserendo la quantità di pezzi da lavorare.

- Fig. 3 — Avvio dell'ordine di lavorazione.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Punto 3: il Work Order è l'elemento centrale del flusso e collega materiali, attività, controlli, NC, dichiarazioni e genealogia. Si avvia con Start indicando la quantità da lavorare.


## Slide 26: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 4

- DICHIARAZIONE DEI CONSUMI (COMPOMENTI)

- L'operatore registra l'ingresso fisico dei componenti tramite scansione del barcode del contenitore o selezione dell'unità materiale prevista dal flusso. L'azione scala automaticamente la quantità dal buffer/stock e collega il materiale all'ordine.

- Per l'esercitazione, l'unità di carico può essere creata manualmente, assicurando disponibilità immediata del materiale.

- Punto fondamentale: costruisce il legame tra esecuzione, genealogia e qualità del dato .

- Fig. 4 — Materiale in pre-macchina · Fig. 5 — Consumo materiali cassone.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Punto 4: si registra l'ingresso fisico dei materiali via barcode o selezione dell'unità. L'azione scala la quantità dal buffer e lega il materiale all'ordine, costruendo il legame tra esecuzione, genealogia e qualità del dato.


## Slide 27: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 5

- NON CONFORMANCE — COMPONENTE

- Per registrare materiale difettoso in ingresso, accedere al pannello Defect Declaration . Selezionare la quantità da scartare o porre in quarantena dal contenitore di provenienza e associare la causale tecnica rilevata.

- IL SISTEMA GESTISCE AUTOMATICAMENTE

- ▸ Creazione del contenitore di scarto ▸ Stampa dell'etichetta di reso ▸ Invio dei messaggi a SAP ▸ Aggiornamento delle quantità buone

- Fig. 6 — Non conformità pezzo in ingresso · Fig. 7 — Identificatore dello scarto in entrata.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Punto 5: per materiale difettoso in ingresso si usa il Defect Declaration Panel. Il sistema crea il contenitore di scarto, stampa l'etichetta di reso, invia messaggi a SAP e aggiorna le quantità buone.


## Slide 28: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 6

- ESECUZIONE DELLE ISPEZIONI E BLOCCO FUNZIONALE

- Le ispezioni obbligatorie (100% o inizio turno/ordine) attivano un blocco funzionale : i tasti "Complete" e "Partial Complete" sono inibiti fino alla validazione dei test.

- La procedura distingue controlli attributivi (OK/NOK) e variabili (valori numerici con tolleranze). Nel Quality Inspection Panel si inseriscono i valori reali con feedback visivo immediato (barra verde/rossa); i risultati sono salvati nello storico dell'ordine.

- Fig. 8 — Inserimento risultati delle ispezioni di qualità.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Punto 6: le ispezioni obbligatorie attivano un blocco funzionale — Complete e Partial Complete restano inibiti fino alla validazione. Si distinguono controlli attributivi (OK/NOK) e variabili, con feedback verde/rosso.


## Slide 29: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 7

- NON CONFORMANCE — PRODOTTO IN USCITA

- Segnalare i difetti sul prodotto finale tramite il pulsante Defect Declaration , selezionando la causale tecnica e la quantità interessata.

- Lo stato "Candidate" (Quarantena) sospende l'unità materiale (MTU), ne impedisce l'avanzamento alle fasi successive e genera una Non-Conformità tracciabile nel sistema.

- Fig. 9 — Dichiarazione quarantena pezzo prodotto · Fig. 10 — Identificativo cassone in quarantena.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Punto 7: i difetti sul prodotto finale si segnalano da Defect Declaration. Lo stato Candidate (Quarantena) sospende l'MTU, ne blocca l'avanzamento e genera una NC tracciabile.


## Slide 30: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 8

- DECISIONE DEL SUPERVISORE (SENTENCING) E INTEGRAZIONE SAP

- Il Supervisore analizza le Non Conformità aperte dal terminale operatore e conclude il ciclo della qualità tramite il Sentencing , definendo il destino finale del materiale sospeso a sistema.

- Ogni Sentencing su materiale in quarantena genera un Outbound Message verso SAP ERP, tecnicamente un "Good Movement" , che indica all'ERP dove spostare contabilmente il materiale — garantendo l'allineamento tra giacenza a sistema e realtà fisica.

- Fig. 11 — Sentencing "Close and Return to Work" · Fig. 12 — Dichiarazione produzione.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Punto 8: il Supervisore conclude il ciclo qualità con il Sentencing, decidendo il destino del materiale sospeso. Ogni sentencing genera un Outbound Message verso SAP (Good Movement) che allinea giacenza a sistema e realtà fisica.


## Slide 31: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 8

- GLI STATI DEL SENTENCING

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

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

I sei stati applicabili nel Sentencing: dalla quarantena di partenza al rientro a buono, allo scarto interno, alle rilavorazioni interna ed esterna, fino allo scarto per causa esterna — ciascuno con un preciso impatto su SAP e KPI.


## Slide 32: (senza titolo)

- FLUSSO OPERATIVO · PUNTO 9

- CHIUSURA DELL'ATTIVITÀ E VERIFICA GENEALOGIA

- Al termine del processo, consultare la pagina "As Built Order" per il registro storico completo dell'ordine.

- CORRELA INDISSOLUBILMENTE

- ▸ Lotti consumati ▸ Risultati delle ispezioni ▸ Dichiarazioni di difetto ▸ Decisioni di sentencing ▸ Quantità prodotte e scartate

- Fig. 13 — Dichiarazione produzione · Fig. 14 — Tracciamento ispezioni · Fig. 15 — Tracciamento non conformità.

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Punto 9: a fine processo la pagina As Built Order fornisce il registro storico completo, correlando lotti consumati, ispezioni, dichiarazioni di difetto, sentencing e quantità prodotte/scartate.


## Slide 33: Supervisione - Genealogia

- Visualizzazione gerarchica completa che lega Work Order a ogni singola MTU, Batch o numero di serie.
- Integrazione Dati Produzione e Qualità:
  - Tracciabilità dei materiali consumati e prodotti.
  - Associazione automatica dei risultati dei test alla genealogia del pezzo.

- Brembo Rollout Italia

- 33

- Supervisione - Genealogia

- OPCENTER MES TRAINING - QUALITY

- FONDERIA
- Colata e solidificazione del greggio

- LAVORAZIONE
MECCANICA
- Tornitura, fresatura, foratura

- TRATTAMENTO
SUPERFICIALE
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


## Slide 36: (senza titolo)

- CONFIGURAZIONE · PUNTO 10

- MASTER DATA — CARATTERISTICHE, ISPEZIONI & DOCUMENTI

- La gestione dei dati anagrafici avviene in Back-Office ( Basic UI ) e si articola su Caratteristiche, Definizione delle Ispezioni e Documenti. Le caratteristiche (Attributive, Variabili, Visuali) sono collegate alle ispezioni.

- Principio dell'ereditarietà : i parametri configurati nel Routing (BOP) sono trasferiti nativamente ai Work Order al download da SAP.

- La pagina "Documents" è anagrafica centrale per file tecnici, disegni e istruzioni, con versioning e categorizzazione.

- Fig. 16 — Ispezioni · Fig. 17 — Tolleranza e valore nominale · Fig. 18 — Anagrafica documenti.

- QUALITY OPERATOR TRAINING — CURNO

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

- QUALITY OPERATOR TRAINING — CURNO

- B-SPARK MES

**Note del relatore:**

Punto 11: l'arricchimento qualitativo avviene a livello di Routing (BOP). Il MES, al caricamento di una nuova versione, tenta il merge automatico copiando piani di controllo e documenti dalla versione precedente.


## Slide 38: (senza titolo)

- CONFIGURAZIONE · PUNTO 11

- EREDITARIETÀ E INTERVENTI MANUALI

- I Work Order ereditano nativamente le configurazioni dal Routing al download da SAP. L'arricchimento manuale della BOP via Basic UI è operazione straordinaria (nuovi prodotti o revisioni tecniche).

- Se un ordine è già stato importato privo di ispezioni, si interviene eccezionalmente sul singolo ordine via Work Order Operation Detail .

- IL SALVATAGGIO ABILITA SUL TERMINALE

- ▸ Presenza di controlli qualità ▸ Documentazione associata ▸ Esperienza utente coerente con il training

- Fig. 20 — Collegamento a documento esistente · Fig. 21 — Aggiunta delle quality inspection al Work Order.

- QUALITY OPERATOR TRAINING — CURNO

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

- QUALITY OPERATOR TRAINING — CURNO

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


## Slide 44: (senza titolo)

- QUALITY OPERATOR TRAINING · CURNO

- Grazie per l'attenzione.

- Paolo Comparoni

- Engineering

- Emanuele Merlo

- Engineering

**Note del relatore:**

Grazie per l'attenzione. Spazio alle domande. Riferimenti: Paolo Comparoni ed Emanuele Merlo, Engineering.
