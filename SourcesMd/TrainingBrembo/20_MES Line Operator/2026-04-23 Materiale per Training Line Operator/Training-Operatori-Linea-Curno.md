# Training-Operatori-Linea-Curno

> Documento sorgente: `E:\BremboDocs\TrainingBrembo\20_MES Line Operator\2026-04-23 Materiale per Training Line Operator\Training-Operatori-Linea-Curno.pptx`  
> Tipo: PowerPoint (.pptx) · Slide: 46


## Slide 1: (senza titolo)

- Engineering Presentation Template

- 1


## Slide 2: OPERATORI DI LINEA

- OPERATORI DI LINEA

- PROCESSO OPERATIVO OPCENTER MES

- CURNO - APRILE 2026

- LINE OPERATOR TRAINING


## Slide 3: AGENDA

- In questa lezione analizzeremo alcuni casi d’uso reali per dimostrare il funzionamento del sistema e le operazioni.
- USE CASE 1 - MACHINING: Ciclo completo dell’ordine di lavorazione utilizzando a modello il Machining.
- USE CASE 2 - ASSEMBLY: Esecuzione di un ordine di Assembly.
- BACK OFFICE: Spiegazione delle aree del sistema dove è possibile monitorare anagrafica, ordini di lavorazione, ristampare etichette.
- DOMANDE E RISPOSTE

- LINE OPERATOR TRAINING - CURNO

- 3

- AGENDA

- USE CASE 1: MACHINING


## Slide 4: INTRODUZIONE

- USE CASE 1: MACHINING

- LINE OPERATOR TRAINING - CURNO

- 4

- INTRODUZIONE

- USE CASE 1: MACHINING

- A scopo dimostrativo verrà presa a modello l’esecuzione di un ordine di lavorazione nell’area di MACHINING.
- Le operazioni elencate sono in larga parte comuni anche alle altre aree.


## Slide 5: ACCESSO AL SISTEMA

- LINE OPERATOR TRAINING - CURNO

- 5

- ACCESSO AL SISTEMA

- INTRODUZIONE

  - Repetitive Curno:  https://it-qlt.mes.brembo.com/sit-ui/Curno/DSBasic.BremboRepetitive_Curno


## Slide 6: ACCESSO AL SISTEMA

- LINE OPERATOR TRAINING - CURNO

- 6

- ACCESSO AL SISTEMA

- INTRODUZIONE

- Sulla postazione in linea di produzione il login avverrà tramite lettura badge.
- L’accesso con le credenziali, username e password, sarà riservato agli operatori di back-office.


## Slide 7: INTRODUZIONE

- LINE OPERATOR TRAINING - CURNO

- 7

- INTRODUZIONE

- USE CASE 1: MACHINING

- Alcune operazioni che richiedono l’integrazione con SAP/EWM (es. flusso materiali da un’area all’altra) non potranno essere mostrate.
- Le schermate del sistema mostrate in questa presentazione saranno in inglese, mentre in produzione saranno disponibili in italiano e con la terminologia comunemente utilizzata in Brembo.


## Slide 8: SELEZIONE DELLA POSTAZIONE DI LAVORO

- La «Repetitive» è la pagina che accoglie l’operatore dopo il login e mostra gli Equipment associati alla postazione di lavoro «Work Center».
- Se il terminale è associato a una sola macchina, il sistema visualizzerà direttamente la lista degli ordini di lavorazione per quella macchina nella pagina «Operator Landing».
- Se il PC gestisce più macchine, il sistema visualizzerà la pagina «Equipment Selection», dove l'operatore dovrà selezionare il Work Center specifico (es. GUGCL231) su cui intende operare dalla lista proposta e cliccare su "Save".
- NOTA: In condizioni di normale produzione solo un ordine di lavorazione può essere attivo sul Work Center (salvo macchine in grado di produrre in parallelo).
- Durante il training questo limite è disabilitato per permettere di esercitarsi.

- LINE OPERATOR TRAINING - CURNO

- 8

- SELEZIONE DELLA POSTAZIONE DI LAVORO

- USE CASE 1: MACHINING

- NOTA: Nel sistema di training non esiste ancora l’associazione Work Center/Equipment, per cui tutte le postazioni di lavoro sono tutti visibili.


## Slide 9: DATI PER GLI STUDENTI

- Mentre gli istruttori spiegano, i partecipanti provano ad eseguire le stesse operazioni in parallelo.

- LINE OPERATOR TRAINING - CURNO

- 9

- DATI PER GLI STUDENTI

- USE CASE 1: MACHINING

**Note del relatore:**

Assegnazione Work Order agli studenti.


## Slide 10: DATI PER GLI STUDENTI

- LINE OPERATOR TRAINING - CURNO

- 10

- DATI PER GLI STUDENTI

- USE CASE 1: MACHINING

| CURNO |  | Machining | Assembly |
| --- | --- | --- | --- |
|  | Macchina | SMMML023 | SACSA025 + SQMAN008 |
|  | Materiale 1 IN | 20D49902 | Vedi tabella a lato |
|  | Materiale 2 IN | P0019000 | - |
|  | Buffer | PSSMMML023 | - |
|  | Part Number | 20D49938_LSM.A | 20E22121.A |
|  | Esempio Work Order | 1109090 | 1109415 |

| Materiale | Descrizione | Quantità |
| --- | --- | --- |
| 5150220 | PARA POLVERE | 4 pce |
| 5385110 | TAPPO A PERDERE | 2 pce |
| 5442461 | VITE | 8 pce |
| 5454227 | COPIGLIA | 4 pce |
| 20419665 | MOLLA | 2 pce |
| 20451769 | LAMIERINO | 8 pce |
| 20490811 | PERNO | 4 pce |
| 20E221AC | PINZA P4.40 ROSSO 30C | 2 pce |
| 4T867310 | PASTIGLIA BRM0018/1 | 2 pce |
| 4T867312 | PASTIGLIA BRM0018/1 | 2 pce |
| 98499933_CAP | ETICHETTA PORSCHE | 2 pce |
| D10416000_SIT | GREASE MOLYKOTE CU7439 V1 | 4.68 g |

**Note del relatore:**

Assegnazione Work Order agli studenti.


## Slide 11: SELEZIONE DELL’ORDINE DI LAVORAZIONE

- Ogni macchina ha il suo gruppo di Lavoro.
- Prima di avviare qualsiasi Work Order (ordine di produzione) o operazione sulla macchina, è fondamentale che l'operatore si registri correttamente nel gruppo di lavoro (Team) associato alla postazione. Questa operazione garantisce la corretta tracciabilità delle attività e la sicurezza del processo.

- LINE OPERATOR TRAINING - CURNO

- 11

- SELEZIONE DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING

- Scansione Badge: La modalità più rapida consiste nello scansionare il proprio badge (barcode); il sistema riconoscerà automaticamente l'utente e lo aggiungerà al gruppo di lavoro

- Il sistema non permette di avviare o gestire ordini se non c'è almeno un operatore registrato nel team della stazione.

**Note del relatore:**

Con quale logica viene scelto il WO dalla lista? C’è un piano di produzione? Gli ordini con completamento parziale sono prioritari?


## Slide 12: SELEZIONE DELL’ORDINE DI LAVORAZIONE

- Il sistema MES è sincronizzato con il gestionale centrale ERP «SAP».
- Quando l'ufficio pianificazione approva e rilascia un ordine di produzione, tutte le informazioni necessarie vengono trasmesse alla postazione di lavoro.
- In termini pratici, troverete l'ordine già pronto sul monitor con tutti i dettagli necessari per iniziare: il tipo di materiale, le quantità da produrre e la sequenza delle operazioni da seguire.

- LINE OPERATOR TRAINING - CURNO

- 12

- SELEZIONE DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING

**Note del relatore:**

Con quale logica viene scelto il WO dalla lista? C’è un piano di produzione? Gli ordini con completamento parziale sono prioritari?


## Slide 13: SELEZIONE DELL’ORDINE DI LAVORAZIONE

- I TRE NUMERI: Ogni riquadro mostra tre quantità:
- Pezzi ancora da avviare
- Pezzi in lavorazione
- Pezzi completati.
- STATO OPERAZIONE:
- Stato iniziale: l’operazione non è ancora pronta per l’avvio (dipendenze precedenti non soddisfatte).
- Operazione pronta per l’esecuzione: tutte le dipendenze sono state completate con successo.
- Operazione attualmente in esecuzione: il lavoro su questa fase è stato avviato dall’operatore.
- Esecuzione parziale: tipico di produzioni serializzate o a lotti flessibili dove solo parte della quantità è stata lavorata.
- Stato di blocco preventivo: impostato spesso automaticamente (es. per dichiarazione di non conformità) per fermare il flusso al raggiungimento di questa fase.
- Operazione conclusa con successo: tutti i task previsti per la fase sono terminati.
- Operazione non eseguita; si verifica se una fase opzionale viene saltata o se l’ordine viene annullato (abort) o modificato escludendo tale fase.
- Segnala la presenza di una Non-Conformità aperta associata all’operazione.
- Segnala che è necessaria o imminente un’ispezione di qualità.
- E’ possibile ordinare la visualizzazione dei riquadri in base allo stato.

- LINE OPERATOR TRAINING - CURNO

- 13

- SELEZIONE DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING

**Note del relatore:**

Con quale logica viene scelto il WO dalla lista? C’è un piano di produzione? Gli ordini con completamento parziale sono prioritari?


## Slide 14: AVVIO DELL’ORDINE DI LAVORAZIONE

- LINE OPERATOR TRAINING - CURNO

- 14

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING

- Visualizzazione dettagli ordine di lavorazione.


## Slide 15: AVVIO DELL’ORDINE DI LAVORAZIONE

- LINE OPERATOR TRAINING - CURNO

- 15

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING


## Slide 16: AVVIO DELL’ORDINE DI LAVORAZIONE

- LINE OPERATOR TRAINING - CURNO

- 16

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING


## Slide 17: AVVIO DELL’ORDINE DI LAVORAZIONE

- LINE OPERATOR TRAINING - CURNO

- 17

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING


## Slide 18: AVVIO DELL’ORDINE DI LAVORAZIONE

- LINE OPERATOR TRAINING - CURNO

- 18

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING

- Avvio ordine di lavorazione (senza contenitori parziali già presenti)

- NOTA: Se si cerca di avviare una quantità superiore a quella pianificata, il sistema potrebbe bloccare o permettere l'avvio in base alla tolleranza impostata in fase di pianificazione.


## Slide 19: AVVIO DELL’ORDINE DI LAVORAZIONE

- Stato e Avanzamento
- Questa parte mostra i dati dell'ordine e le quantità prodotte:
- Final Material & Description: Visualizza il codice tecnico e la descrizione del prodotto in lavorazione.
- Production Finish Good: Indica la quantità massima che puoi completare in base ai materiali effettivamente consumati/scansionati.
- Good Quantity (Buoni): Il totale dei pezzi conformi già completati per l’operazione.
- Scrap Quantity (Scarti): Il totale dei pezzi dichiarati scarti o difettosi.

- LINE OPERATOR TRAINING - CURNO

- 19

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING

- Visualizzazione ordine avviato


## Slide 20: AVVIO DELL’ORDINE DI LAVORAZIONE

- Quantità Richiesta: il totale necessario per completare l'ordine.
- Quantità Disponibile/Mancante: il sistema evidenzia eventuali mancanze con icone di avviso per segnalare la necessità di nuovi approvvigionamenti

- LINE OPERATOR TRAINING - CURNO

- 20

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING


## Slide 21: AVVIO DELL’ORDINE DI LAVORAZIONE

- L’icona segnala che il materiale disponibile nel buffer (area pre-macchina/PSA) è insufficiente per completare la quantità dell’ordine in produzione.
- È collegata al campo “Production Finish Good”: il sistema calcola quanti pezzi finiti sono realizzabili in base al componente più scarso
- Il simbolo permette di identificare rapidamente il materiale critico che sta rallentando o bloccando l’avanzamento
- Quando compare, l’operatore deve effettuare una chiamata materiale tramite le apposite icone (muletto o telefono) per richiedere il rifornimento
- Dopo il caricamento e la scansione del materiale:
  - la quantità torna sufficiente
  - l’avviso scompare
  - il materiale viene evidenziato in verde

- LINE OPERATOR TRAINING - CURNO

- 21

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: MACHINING


## Slide 22: CHIAMATA MATERIALI

- Semaforo di stato chiamata:
- Verde: chiamata disponibile.
- Giallo: presa in carico dal magazzino.
- Rosso: errore o movimentazione bloccata.
- Grigio: inviata ma non presa in carico.

- LINE OPERATOR TRAINING - CURNO

- 22

- CHIAMATA MATERIALI

- USE CASE 1: MACHINING


## Slide 23: CONSUMO MATERIALI

- LINE OPERATOR TRAINING - CURNO

- 23

- CONSUMO MATERIALI

- USE CASE 1: MACHINING

- Tracciabilità «Hard»: L’operatore deve scansionare o inserire manualmente l'identificativo del barcode. Con un'unica azione, il sistema acquisisce automaticamente codice materiale, lotto e quantità. Il materiale scansionato viene "scalato" dal buffer di linea e associato alla produzione in corso.
- In caso di materiali "Hard Traced", il sistema bloccherà la dichiarazione finale di produzione se tutti i componenti obbligatori non sono stati scansionati correttamente.
- Tracciabilità «Soft»: Scansione opzionale (consigliata), altrimenti il sistema consuma quel materiale con logica FIFO al momento della chiusura.
- Nessuna tracciabilità:  L'operatore visualizza i materiali ma non deve inserire dati manualmente. Il sistema esegue il consumo automatico in base alle quantità prodotte dichiarate al termine dell'operazione.


## Slide 24: DICHIARAZIONE DIFETTI

- LINE OPERATOR TRAINING - CURNO

- 24

- DICHIARAZIONE DIFETTI

- USE CASE 1: MACHINING


## Slide 25: DICHIARAZIONE DI PRODUZIONE PARZIALE

- LINE OPERATOR TRAINING - CURNO

- 25

- DICHIARAZIONE DI PRODUZIONE PARZIALE

- USE CASE 1: MACHINING

- Pulsante Partial Complete per dichiarare la produzione.
- Utile ad esempio a fine turno per stampare un'etichetta temporanea e permettere al collega subentrante di completare il cassone.


## Slide 26: DICHIARAZIONE DI PRODUZIONE COMPLETA

- LINE OPERATOR TRAINING - CURNO

- 26

- DICHIARAZIONE DI PRODUZIONE COMPLETA

- USE CASE 1: MACHINING

- Pulsante Complete per dichiarare la produzione dei pezzi buoni.


## Slide 27: DICHIARAZIONE DI PRODUZIONE

- LINE OPERATOR TRAINING - CURNO

- 27

- DICHIARAZIONE DI PRODUZIONE

- USE CASE 1: MACHINING


## Slide 28: AVVIO DELL’ORDINE DI LAVORAZIONE – CON CONTENITORE PARZIALE

- Se all’avvio di un ordine il sistema rileva la presenza di un container parziale, il MES segnala all'operatore che per quell'ordine esiste un cassone in sospeso e suggerisce di completare quello per primo.
- Questa funzione è pensata per gestire i cambi turno: l'operatore che entra nel turno può "agganciarsi" al cassone lasciato a metà dal collega del turno precedente, terminare il cassone e generare l'etichetta definitiva.

- LINE OPERATOR TRAINING - CURNO

- 28

- AVVIO DELL’ORDINE DI LAVORAZIONE – CON CONTENITORE PARZIALE

- USE CASE 1: MACHINING


## Slide 29: AVVIO DELL’ORDINE DI LAVORAZIONE – CON CONTENITORE PARZIALE

- Se il supervisore decide che quel cassone non deve essere ulteriormente riempito (ad esempio per un cambio materiale urgente), l'operatore può utilizzare la funzione Close Partial Container per chiuderlo definitivamente con la quantità ridotta attuale e inviare l'informazione a SAP

- LINE OPERATOR TRAINING - CURNO

- 29

- AVVIO DELL’ORDINE DI LAVORAZIONE – CON CONTENITORE PARZIALE

- USE CASE 1: MACHINING


## Slide 30: DICHIARAZIONE DI PRODUZIONE

- LINE OPERATOR TRAINING - CURNO

- 30

- DICHIARAZIONE DI PRODUZIONE

- USE CASE 1: MACHINING


## Slide 31: DICHIARAZIONE DI PRODUZIONE

- LINE OPERATOR TRAINING - CURNO

- 31

- DICHIARAZIONE DI PRODUZIONE

- USE CASE 1: MACHINING


## Slide 32: DICHIARAZIONE DI PRODUZIONE

- LINE OPERATOR TRAINING - CURNO

- 32

- DICHIARAZIONE DI PRODUZIONE

- USE CASE 1: MACHINING


## Slide 33: GESTIONE VEICOLI A GUIDA AUTONOMA (AGV)

- Sulla barra laterale è presente un pulsante «aggregato», cioè che apre un menù a comparsa con tutte le azioni possibili:
- Chiamata Vuoti (Call Empty): Richiesta di un contenitore vuoto basata sul materiale di imballaggio necessario.
- Reso Vuoti (Return Empty): Invio a magazzino di contenitori non più necessari in linea.
- Chiamata Alveolari (Call Alveolari): Richiesta di separatori alveolari.
- Reso Alveolari (Return Alveolari): Ritorno a magazzino di separatori alveolari non più necessari.
- Reso Trucioli: Missioni specifiche per materiali di scarto (chips), che solitamente prevede lo svuotamento del contenitore pieno e il ritorno di uno vuoto.
- La funzionalità di chiamata AGV è visibile solo per i Work Center abilitati (es. lavorazioni meccaniche).
- Il MES non gestisce direttamente il movimento fisico, ma interfaccia le necessità della linea con i sistemi EWM e Toyota AGV Control System.

- LINE OPERATOR TRAINING - CURNO

- 33

- GESTIONE VEICOLI A GUIDA AUTONOMA (AGV)

- USE CASE 1: MACHINING


## Slide 34: GESTIONE VEICOLI A GUIDA AUTONOMA (AGV)

- Le baie rappresentano i punti fisici di carico/scarico lungo la linea. Nel MES, ogni baia è configurata come un Equipment di tipo "Bay" ed è collegata univocamente a un Buffer specifico.
- Selezione della Baia: Per effettuare una chiamata, l'operatore deve selezionare la baia di destinazione dal un menu a tendina. Il sistema mostra solo le baie fisicamente associate al buffer della macchina in uso, riducendo il rischio di errori di consegna.
- Monitoraggio: Il pulsante di chiamata cambia colore per fornire un feedback in tempo reale sullo stato della missione:
- Grigio: Chiamata inviata, in attesa di presa in carico da parte di EWM.
- Giallo: Missione accettata; l'AGV è in movimento verso la baia.
- Verde: Missione completata con successo; materiale consegnato o prelevato.
- Rosso: Errore (es. materiale non trovato o problema tecnico AGV); il pulsante si riabilita per un nuovo tentativo.
- I dati richiesti sono nelle missioni sono sempre: baia di prelievo o consegna e codice materiale per tutte le missioni previste.

- LINE OPERATOR TRAINING - CURNO

- 34

- GESTIONE VEICOLI A GUIDA AUTONOMA (AGV)

- USE CASE 1: MACHINING


## Slide 35: GESTIONE VEICOLI A GUIDA AUTONOMA (AGV)

- Al momento del "Complete", una checkbox (attiva di default) permette di innescare automaticamente la missione di prelievo del contenitore pieno, previa selezione della baia
- L'operatore dispone che può deselezionare la check box per impedire al sistema di scatenare la chiamata AGV al momento della chiusura.

- LINE OPERATOR TRAINING - CURNO

- 35

- GESTIONE VEICOLI A GUIDA AUTONOMA (AGV)

- USE CASE 1: MACHINING


## Slide 36: ATTIVITÀ NON PRODUTTIVE

- Le attività non produttive (N-P Activities) sono compiti che, pur essendo necessari, non contribuiscono direttamente alla produzione fisica dei pezzi.
- Includono mansioni come la pulizia dell'area di lavoro, la manutenzione degli utensili, le attività di formazione o il setup delle macchine.
- L'operatore interagisce con queste attività tramite la Operator Landing Page seguendo questi passaggi:
- Accede tramite il pulsante N-P Activities sulla barra dei comandi.
- Sceglie una o più attività dalla lista preimpostata.
- Può associare l'attività non produttiva a un contesto specifico, ad esempio collegandola a un determinato ordine di lavorazione, a un'operazione, a una macchina o a un cassone.
- Il sistema registra l'ora di inizio. Se necessario può inserire anche attività svolte nel passato, se non sono state registrate al momento dell'effettivo inizio.
- Al termine, seleziona l'attività e la dichiara come completata, registrando così la data e l'ora correnti nel log di sistema

- TRAINING LINE OPERATOR - MAPELLO

- 36

- ATTIVITÀ NON PRODUTTIVE

- USE CASE 1: CASTING


## Slide 37: INTRODUZIONE

- USE CASE 2: ASSEMBLY

- LINE OPERATOR TRAINING - CURNO

- 37

- INTRODUZIONE

- USE CASE 2: ASSEMBLY

- In questo use case eseguiremo un ordine di ASSEMBLY.
- Le slide contengono un focus sulle specificità di questa area dal punto di vista MES.


## Slide 38: BACK-OFFICE LINEA

- BACK-OFFICE

- LINE OPERATOR TRAINING - CURNO

- 38

- BACK-OFFICE LINEA


## Slide 39: BACK-OFFICE LINEA – DS BASIC: APPLICAZIONI DI SUPERVISIONE

- Print History
- Work Orders
- Work Order in Progress
- Container Types
- Buffer

- LINE OPERATOR TRAINING - CURNO

- 39

- BACK-OFFICE LINEA – DS BASIC: APPLICAZIONI DI SUPERVISIONE

- BACK-OFFICE LINEA

  - DSBasic Curno: https://it-qlt.mes.brembo.com/sit-ui/curno/DSBasic.Siemens_OPC_EXDSBasic/#/screen/home.homeCard


## Slide 40: BACK-OFFICE LINEA – WORK IN PROGRESS APP

- LINE OPERATOR TRAINING - CURNO

- 40

- BACK-OFFICE LINEA – WORK IN PROGRESS APP

- BACK-OFFICE LINEA

- Print History
- Questa funzionalità permette di monitorare e gestire l'attività di etichettatura del sistema.
- L'attività principale per un supervisore è la consultazione dello storico delle stampe che consente la ristampa di etichette (CDI) smarrite o danneggiate.


## Slide 41: BACK-OFFICE LINEA – WORK ORDER

- Work Orders
- Permette di visualizzare lo stato degli ordini di lavorazione.
- Visualizzare la lista degli ordini di lavorazione che sono stati ricevuti.
- Il supervisore può visualizzare la genealogia as-built.
- La lista delle quality inspections.
- Lista non-conformances.

- LINE OPERATOR TRAINING - CURNO

- 41

- BACK-OFFICE LINEA – WORK ORDER

- BACK-OFFICE LINEA


## Slide 42: BACK-OFFICE LINEA – WORK  ORDER IN PROGRESS

- Work Order in Progress (WIP)
- È l'applicazione dedicata al monitoraggio in tempo reale dell'avanzamento della produzione.
- Consente di vedere quali ordini sono in lavorazione, la loro percentuale di completamento e su quali macchine specifiche si trovano.
- Il supervisore monitora le quantità effettive prodotte rispetto a quelle scartate o messe in quarantena.
- Permette di prendere decisioni repentine per ottimizzare il flusso o ripianificare le operazioni per evitare tempi morti.

- LINE OPERATOR TRAINING - CURNO

- 42

- BACK-OFFICE LINEA – WORK  ORDER IN PROGRESS

- BACK-OFFICE LINEA


## Slide 43: BACK-OFFICE LINEA – CONTAINER TYPES

- Container Types
- Definisce le caratteristiche del contenitore, come la capacità massima di pezzi per ogni materiale compatibile e la proprietà di riutilizzabilità.

- LINE OPERATOR TRAINING - CURNO

- 43

- BACK-OFFICE LINEA – CONTAINER TYPES

- BACK-OFFICE LINEA


## Slide 44: BACK-OFFICE LINEA – BUFFER

- Buffer
- Aree di stoccaggio nell’impianto.
- Il supervisore:
- Può creare, modificare e cancellare i buffer definiti per l'impianto.
- Può cambiare lo stato del buffer.
- Può visualizzare quali MTU sono contenute in un determinato buffer e aggiungerne di nuove manualmente se necessario

- LINE OPERATOR TRAINING - CURNO

- 44

- BACK-OFFICE LINEA – BUFFER

- BACK-OFFICE LINEA


## Slide 45: DOMANDE E RISPOSTE

- Spazio alle vostre domande.

- USE CASE 1: MACHINING

- 45

- DOMANDE E RISPOSTE


## Slide 46: Grazie per l’attenzione.

- EMANUELE MERLO

- Functional & Business Analysis Specialist

- Grazie per l’attenzione.

- TRAINING LINE OPERATOR - MAPELLO
