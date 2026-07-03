---
title: "Training Operatori di Linea Mapello"
source_file: "SourcesMd/TrainingBrembo/20_MES Line Operator/2026-04-23 Materiale per Training Line Operator/Training-Operatori-Linea-Mapello (PPTX).md"
project: "Brembo B-Spark"
scope: "Operational_Training_Material"
plants: [MAPELLO]
---

# Training Operatori di Linea Mapello

> Documento sorgente: `E:\BremboDocs\TrainingBrembo\20_MES Line Operator\2026-04-23 Materiale per Training Line Operator\Training-Operatori-Linea-Mapello.pptx`  
> Tipo: PowerPoint (.pptx) · Slide: 40


## Slide 1: (senza titolo)

- Engineering Presentation Template

- 1


## Slide 2: OPERATORI DI LINEA

- OPERATORI DI LINEA

- PROCESSO OPERATIVO OPCENTER MES

- MAPELLO – Aprile 2026

- LINE OPERATOR TRAINING


## Slide 3: AGENDA

- In questa lezione analizzeremo alcuni casi d’uso reali per dimostrare il funzionamento del sistema e le operazioni.
- USE CASE 1 - CASTING: Ciclo completo dell’ordine di lavorazione utilizzando a modello il Casting.
- USE CASE 2 - CUTTING: Esecuzione di un ordine di Cutting con focus sulla dichiarazione dei co-product.
- BACK OFFICE: Spiegazione delle aree del sistema dove è possibile monitorare anagrafica, ordini di lavorazione, ristampare etichette.
- DOMANDE E RISPOSTE

- TRAINING LINE OPERATOR - MAPELLO

- 3

- AGENDA

- INTRODUZIONE


## Slide 4: ACCESSO AL SISTEMA

- TRAINING LINE OPERATOR - MAPELLO

- 4

- ACCESSO AL SISTEMA

- USE CASE 1: CASTING

  - Repetitive Mapello: https://it-qlt.mes.brembo.com/sit-ui/Mapello/DSBasic.BremboRepetitive_Mapello


## Slide 5: ACCESSO AL SISTEMA

- TRAINING LINE OPERATOR - MAPELLO

- 5

- ACCESSO AL SISTEMA

- USE CASE 1: CASTING

- Sulla postazione in linea di produzione il login avverrà tramite lettura badge.
- L’accesso con le credenziali, username e password, sarà riservato agli operatori di back-office.


## Slide 6: (senza titolo)

- USE CASE 1: CASTING

- TRAINING LINE OPERATOR - MAPELLO

- 6

- USE CASE 1: CASTING

- A scopo dimostrativo verrà presa a modello l’esecuzione di un ordine di lavorazione nell’area di Casting.
- Le operazioni elencate sono in larga parte comuni anche alle altre aree.


## Slide 7: INTRODUZIONE

- TRAINING LINE OPERATOR - MAPELLO

- 7

- INTRODUZIONE

- USE CASE 1: CASTING

- Alcune operazioni che richiedono l’integrazione con SAP/EWM (es. flusso materiali da un’area all’altra) non potranno essere mostrate.
- Le schermate del sistema mostrate in questa presentazione saranno in inglese, mentre in produzione saranno disponibili in italiano e con la terminologia comunemente utilizzata in Brembo.


## Slide 8: SELEZIONE DEL WORK CENTER

- La «Repetitive» è la pagina che accoglie l’operatore dopo il login e mostra gli Equipment associati alla postazione di lavoro «Work Center».
- Se il terminale è associato a una sola macchina, il sistema visualizzerà direttamente la lista degli ordini di lavorazione per quella macchina nella pagina «Operator Landing».
- Se il PC gestisce più macchine, il sistema visualizzerà la pagina «Equipment Selection», dove l'operatore dovrà selezionare il Work Center specifico (es. GUGCL231) su cui intende operare dalla lista proposta e cliccare su "Save".
- NOTA: In condizioni di normale produzione solo un ordine di lavorazione può essere attivo sul Work Center (salvo macchine in grado di produrre in parallelo).
- Durante il training questo limite è disabilitato per permettere di esercitarsi.

- TRAINING LINE OPERATOR - MAPELLO

- 8

- SELEZIONE DEL WORK CENTER

- USE CASE 1: CASTING

- NOTA: Nel sistema attuale non esiste ancora l’associazione Work Center/Equipment, per cui tutte le postazioni di lavoro sono tutti visibili.


## Slide 9: DATI PER GLI STUDENTI

- Mentre gli istruttori spiegano, i partecipanti provano ad eseguire le stesse operazioni in parallelo.

- TRAINING LINE OPERATOR - MAPELLO

- 9

- DATI PER GLI STUDENTI

- USE CASE 1: CASTING

**Note del relatore:**

Assegnazione Work Order agli studenti.


## Slide 10: DATI PER GLI STUDENTI

- TRAINING LINE OPERATOR - MAPELLO

- 10

- DATI PER GLI STUDENTI

- USE CASE 1: CASTING

| MAPELLO |  | CASTING | CUTTING |
| --- | --- | --- | --- |
|  | Macchina | GUGCL231 | GMPOB02M |
|  | Materiale 1 IN | BB0002K9 | 20R93800_042 |
|  | Materiale 2 IN | BB000022 | - |
|  | Buffer | PSGUGCL23G | PSGMPOB02M |
|  | Tool | S20E93800_42 | - |
|  | Part Number | 20E93800_042.A | 20D73700_CUT.A |
|  | Work Order Esempio | 1109383 | 1109147 |

**Note del relatore:**

Assegnazione Work Order agli studenti.


## Slide 11: SELEZIONE DELL’ORDINE DI LAVORAZIONE

- Ogni macchina ha il suo gruppo di Lavoro.
- Prima di avviare qualsiasi Work Order (ordine di produzione) o operazione sulla macchina, è fondamentale che l'operatore si registri correttamente nel gruppo di lavoro (Team) associato alla postazione. Questa operazione garantisce la corretta tracciabilità delle attività e la sicurezza del processo.

- TRAINING LINE OPERATOR - MAPELLO

- 11

- SELEZIONE DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: CASTING

- Scansione Badge: La modalità più rapida consiste nello scansionare il proprio badge (barcode); il sistema riconoscerà automaticamente l'utente e lo aggiungerà al gruppo di lavoro

- Il sistema non permette di avviare o gestire ordini se non c'è almeno un operatore registrato nel team della stazione.


## Slide 12: SELEZIONE DELL’ORDINE DI LAVORAZIONE

- Il sistema MES è sincronizzato con il gestionale centrale ERP «SAP».
- Quando l'ufficio pianificazione approva e rilascia un ordine di produzione, tutte le informazioni necessarie vengono trasmesse alla postazione di lavoro.
- In termini pratici, troverete l'ordine già pronto sul monitor con tutti i dettagli necessari per iniziare: il tipo di materiale, le quantità da produrre e la sequenza delle operazioni da seguire.

- TRAINING LINE OPERATOR - MAPELLO

- 12

- SELEZIONE DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: CASTING


## Slide 13: STATO DELL’ORDINE DI LAVORAZIONE

- I TRE NUMERI: Ogni riquadro mostra tre quantità:
- Pezzi ancora da avviare
- Pezzi in lavorazione
- Pezzi completati.
- STATO OPERAZIONE:
- Stato iniziale: l’operazione non è ancora pronta per l’avvio (dipendenze precedenti non soddisfatte).
- Operazione pronta per l’esecuzione: tutte le dipendenze (es. AfterEnd o AfterStart) sono state completate con successo.
- Operazione attualmente in esecuzione: il lavoro su questa fase è stato avviato dall’operatore.
- Esecuzione parziale: tipico di produzioni serializzate o a lotti flessibili dove solo parte della quantità è stata lavorata.
- Stato di blocco preventivo: impostato spesso automaticamente (es. per dichiarazione di non conformità) per fermare il flusso al raggiungimento di questa fase.
- Operazione conclusa con successo: tutti i task previsti per la fase sono terminati.
- Operazione non eseguita; si verifica se una fase opzionale viene saltata o se l’ordine viene annullato (abort) o modificato escludendo tale fase.
- Segnala la presenza di una Non-Conformità aperta associata all’operazione.
- Segnala che è necessaria o imminente un’ispezione di qualità.
- E’ possibile ordinare la visualizzazione dei riquadri in base allo stato.

- TRAINING LINE OPERATOR - MAPELLO

- 13

- STATO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: CASTING


## Slide 14: AVVIO DELL’ORDINE DI LAVORAZIONE

- TRAINING LINE OPERATOR - MAPELLO

- 14

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: CASTING

- Visualizzazione dettagli ordine di lavorazione.


## Slide 15: AVVIO DELL’ORDINE DI LAVORAZIONE

- TRAINING LINE OPERATOR - MAPELLO

- 15

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: CASTING


## Slide 16: AVVIO DELL’ORDINE DI LAVORAZIONE – CON CONTENITORE PARZIALE

- Se all’avvio di un ordine il sistema rileva la presenza di un container parziale, il MES segnala all'operatore che per quell'ordine esiste un cassone in sospeso e suggerisce di completare quello per primo.
- Questa funzione è pensata per gestire i cambi turno: l'operatore che entra nel turno può "agganciarsi" al cassone lasciato a metà dal collega del turno precedente, terminare il cassone e generare l'etichetta definitiva.

- TRAINING LINE OPERATOR - MAPELLO

- 16

- AVVIO DELL’ORDINE DI LAVORAZIONE – CON CONTENITORE PARZIALE

- USE CASE 1: CASTING


## Slide 17: AVVIO DELL’ORDINE DI LAVORAZIONE - CON CONTENITORE PARZIALE

- Se il supervisore decide che quel cassone non deve essere ulteriormente riempito (ad esempio per un cambio materiale urgente), l'operatore può utilizzare la funzione Close Partial Container per chiuderlo definitivamente con la quantità ridotta attuale e inviare l'informazione a SAP

- TRAINING LINE OPERATOR - MAPELLO

- 17

- AVVIO DELL’ORDINE DI LAVORAZIONE - CON CONTENITORE PARZIALE

- USE CASE 1: CASTING


## Slide 18: AVVIO DELL’ORDINE DI LAVORAZIONE

- Stato e Avanzamento
- Questa parte mostra i dati dell'ordine e le quantità prodotte:
- Final Material & Description: Visualizza il codice tecnico e la descrizione del prodotto in lavorazione.
- Production Finish Good: Indica la quantità massima che puoi completare in base ai materiali effettivamente consumati/scansionati.
- Good Quantity (Buoni): Il totale dei pezzi conformi già completati per l’operazione.
- Scrap Quantity (Scarti): Il totale dei pezzi dichiarati scarti o difettosi.

- TRAINING LINE OPERATOR - MAPELLO

- 18

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: CASTING

- Visualizzazione ordine avviato.


## Slide 19: AVVIO DELL’ORDINE DI LAVORAZIONE

- Quantità Richiesta: il totale necessario per completare l'ordine.
- Quantità Disponibile/Mancante: il sistema evidenzia eventuali mancanze con icone di avviso per segnalare la necessità di nuovi approvvigionamenti

- TRAINING LINE OPERATOR - MAPELLO

- 19

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: CASTING


## Slide 20: CHIAMATA MATERIALI

- Semaforo di stato chiamata:
- Grigio: inviata ma non presa in carico.
- Giallo: presa in carico dal magazzino.
- Verde: disponibile.
- Rosso: errore o movimentazione bloccata.

- TRAINING LINE OPERATOR - MAPELLO

- 20

- CHIAMATA MATERIALI

- USE CASE 1: CASTING


## Slide 21: AVVIO DELL’ORDINE DI LAVORAZIONE

- TRAINING LINE OPERATOR - MAPELLO

- 21

- AVVIO DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: CASTING

- Avvio ordine di lavorazione (senza contenitori parziali già presenti)

- NOTA: Se si cerca di avviare una quantità superiore a quella pianificata, il sistema potrebbe bloccare o permettere l'avvio in base alla tolleranza impostata in fase di pianificazione.


## Slide 22: VALIDAZIONE STAMPO

- Ogni stampo è identificato da un numero seriale univoco.
- Prima di produrre, l'operatore deve validare lo stampo inserendo o scansionando il suo numero seriale.
- Il sistema controlla abbinamento ordine di lavorazione/stampo per evitare errori.
- Ogni stampo ha un contatore di utilizzi (Strokes Counter) che viene incrementato ad ogni colata, permettendo di tracciarne l’usura e sostituirlo per mantenere la qualità della produzione.

- TRAINING LINE OPERATOR - MAPELLO

- 22

- VALIDAZIONE STAMPO

- USE CASE 1: CASTING


## Slide 23: CONSUMO MATERIALI

- LINE OPERATOR TRAINING - CURNO

- 23

- CONSUMO MATERIALI

- USE CASE 1: MACHINING

- Tracciabilità «Hard»: L’operatore deve scansionare o inserire manualmente l'identificativo del barcode. Con un'unica azione, il sistema acquisisce automaticamente codice materiale, lotto e quantità. Il materiale scansionato viene "scalato" dal buffer di linea e associato alla produzione in corso.
- In caso di materiali "Hard Traced", il sistema bloccherà la dichiarazione finale di produzione se tutti i componenti obbligatori non sono stati scansionati correttamente.
- Tracciabilità «Soft»: Scansione opzionale (consigliata), altrimenti il sistema consuma quel materiale con logica FIFO al momento della chiusura.
- Nessuna tracciabilità:  L'operatore visualizza i materiali ma non deve inserire dati manualmente. Il sistema esegue il consumo automatico in base alle quantità prodotte dichiarate al termine dell'operazione.


## Slide 24: DICHIARAZIONE DI PRODUZIONE

- TRAINING LINE OPERATOR - MAPELLO

- 24

- DICHIARAZIONE DI PRODUZIONE

- USE CASE 1: CASTING

- Pulsante COMPLETE per dichiarare la produzione dei pezzi buoni.
- Si seleziona il Container Type (tipo di imballo) corretto per istruire SAP sui materiali di confezionamento (coperchi, layer).
- Viene attribuito l’«Original Batch» (lotto di colata) che garantirà la tracciabilità totale fino a fine processo. Questo identificatore è cruciale poiché il sistema bloccherà qualsiasi tentativo di mescolare lotti diversi,  all’interno dello stesso cassone, nelle fasi di lavorazione successive.

**Note del relatore:**

Configurazione Stampo (Mold): Se lo stampo non è mappato nel backend con il Part Number corretto, il MES blocca lo Start. È responsabilità del Back Office garantire che l'anagrafica stampi sia aggiornata.


## Slide 25: SELEZIONE DELL’ORDINE DI LAVORAZIONE

- TRAINING LINE OPERATOR - MAPELLO

- 25

- SELEZIONE DELL’ORDINE DI LAVORAZIONE

- USE CASE 1: CASTING


## Slide 26: DICHIARAZIONE DIFETTI

- Pulsante Declare NC per aprire una Non-Conformità.
- Scarto Immediato
- Quarantena
- Scarto di Cavità: È possibile scartare una singola cavità della mold segnandola con una "X". Il sistema erediterà questo scarto nella fase successiva (Cutting), dove il pezzo sarà eliminato automaticamente.

- TRAINING LINE OPERATOR - MAPELLO

- 26

- DICHIARAZIONE DIFETTI

- USE CASE 1: CASTING

- Quando l'operatore del taglio «consumerà» il ragno nella fase di cutting, il MES genererà automaticamente lo scarto per le cavità che erano state marcate con la X.


## Slide 27: ATTIVITÀ NON PRODUTTIVE

- Le attività non produttive (N-P Activities) sono compiti che, pur essendo necessari, non contribuiscono direttamente alla produzione fisica dei pezzi.
- Includono mansioni come la pulizia dell'area di lavoro, la manutenzione degli utensili, le attività di formazione o il setup delle macchine.
- L'operatore interagisce con queste attività tramite la Operator Landing Page seguendo questi passaggi:
- Accede tramite il pulsante N-P Activities sulla barra dei comandi.
- Sceglie una o più attività dalla lista preimpostata.
- Può associare l'attività non produttiva a un contesto specifico, ad esempio collegandola a un determinato ordine di lavorazione, a un'operazione, a una macchina o a un cassone.
- Il sistema registra l'ora di inizio. Se necessario può inserire anche attività svolte nel passato, se non sono state registrate al momento dell'effettivo inizio.
- Al termine, seleziona l'attività e la dichiara come completata, registrando così la data e l'ora correnti nel log di sistema

- TRAINING LINE OPERATOR - MAPELLO

- 27

- ATTIVITÀ NON PRODUTTIVE

- USE CASE 1: CASTING

**Note del relatore:**

Al momento non esistono attività NP configurate nel sistema


## Slide 28: CHIUSURA ORDINE

- Chiusura Totale: L'ordine passa in stato "Complete".
- Chiusura Parziale: Utile a fine turno per stampare un'etichetta temporanea e permettere al collega subentrante di completare il cassone.
- Shadow Movement: Una volta completato, il MES informa SAP che sposta virtualmente il materiale verso la fase successiva (es. Cutting) senza interventi manuali.

- TRAINING LINE OPERATOR - MAPELLO

- 28

- CHIUSURA ORDINE

- USE CASE 1: CASTING


## Slide 29: (senza titolo)

- TRAINING LINE OPERATOR - MAPELLO

- 29

- USE CASE 2: CUTTING

- USE CASE 2: CUTTING

- In questo use case eseguiremo un ordine di cutting.
- Le slide contengono un focus sulle specificità di questa area dal punto di vista MES.


## Slide 30: USE CASE 2: CUTTING – DICHIARAZIONE DEI COPRODOTTI

- Parliamo di coprodotti (co-products) quando da un unico materiale di input si ottengono più prodotti distinti durante la stessa operazione.
- E’ il caso del cutting dove da una «mold» si possono ottenere più prodotti, ad esempio semi-pinza destra e semi-pinza sinistra.

- TRAINING LINE OPERATOR - MAPELLO

- 30

- USE CASE 2: CUTTING – DICHIARAZIONE DEI COPRODOTTI

- USE CASE 2: CUTTING

**Note del relatore:**

Macchina GMPOB02M


## Slide 31: USE CASE 2: CUTTING – DICHIARAZIONE DEI CO-PRODUCT

- L'operatore preme Complete nella barra laterale destra.
- Nell'interfaccia di completamento, il sistema visualizza distintamente i codici di tutti i prodotti previsti, ad es. il prodotto principale 20E93800 e coprodotto 20E93900.
  - L'operatore deve inserire la quantità di pezzi buoni prodotti per ciascun codice.
  - È possibile dichiarare anche eventuali scarti specifici per il co-prodotto selezionando la relativa voce nel pannello dei difetti di qualità.
- Non è obbligatorio seguire un ordine fisso (si può dichiarare prima il prodotto principale e poi il coprodotto o viceversa. Ma non è possibile completare interamente la produzione del prodotto principale se rimangono quantità residue di coprodotto non dichiarate; il sistema impone la gestione di entrambi i flussi per mantenere l'allineamento con SAP.

- TRAINING LINE OPERATOR - MAPELLO

- 31

- USE CASE 2: CUTTING – DICHIARAZIONE DEI CO-PRODUCT

- USE CASE 2: CUTTING

**Note del relatore:**

Macchina GMPOB02M


## Slide 32: (senza titolo)

- BACK-OFFICE DI LINEA

- TRAINING LINE OPERATOR - MAPELLO

- 32

- BACK-OFFICE LINEA


## Slide 33: DS BASIC: APPLICAZIONI DI SUPERVISIONE

- Print History
- Work Orders
- Work Order in Progress
- Container Types
- Buffer

- TRAINING LINE OPERATOR - MAPELLO

- 33

- DS BASIC: APPLICAZIONI DI SUPERVISIONE

- BACK-OFFICE LINEA

  - DSBasic Mapello: https://it-qlt.mes.brembo.com/sit-ui/mapello/DSBasic.Siemens_OPC_EXDSBasic/#/screen/home.homeCard


## Slide 34: WORK IN PROGRESS APP

- TRAINING LINE OPERATOR - MAPELLO

- 34

- WORK IN PROGRESS APP

- BACK-OFFICE LINEA

- Print History
- Questa funzionalità permette di monitorare e gestire l'attività di etichettatura del sistema.
- L'attività principale per un supervisore è la consultazione dello storico delle stampe che consente la ristampa di etichette (CDI) smarrite o danneggiate.


## Slide 35: WORK ORDERS

- Work Orders
- Permette di visualizzare lo stato degli ordini di lavorazione.
- Visualizzare la lista degli ordini di lavorazione che sono stati ricevuti.
- Il supervisore può visualizzare la genealogia as-built.
- La lista delle quality inspections.
- Lista non-conformances.
- Cancellare gli ordini non più necessari (abort)

- TRAINING LINE OPERATOR - MAPELLO

- 35

- WORK ORDERS

- BACK-OFFICE LINEA


## Slide 36: WORK  ORDER IN PROGRESS

- Work Order in Progress (WIP)
- È l'applicazione dedicata al monitoraggio in tempo reale dell'avanzamento della produzione.
- Consente di vedere quali ordini sono in lavorazione, la loro percentuale di completamento e su quali macchine specifiche si trovano.
- Il supervisore monitora le quantità effettive prodotte rispetto a quelle scartate o messe in quarantena.
- Permette di prendere decisioni repentine per ottimizzare il flusso o ripianificare le operazioni per evitare tempi morti.

- TRAINING LINE OPERATOR - MAPELLO

- 36

- WORK  ORDER IN PROGRESS

- BACK-OFFICE LINEA


## Slide 37: CONTAINER TYPES

- Container Types
- Definisce le caratteristiche del contenitore, come la capacità massima di pezzi per ogni materiale compatibile e la proprietà di riutilizzabilità.

- TRAINING LINE OPERATOR - MAPELLO

- 37

- CONTAINER TYPES

- BACK-OFFICE LINEA


## Slide 38: BUFFER (PRE-MACCHINA)

- Buffer
- Aree di stoccaggio nell’impianto.
- Il supervisore:
- Può creare, modificare e cancellare i buffer definiti per l'impianto.
- Può cambiare lo stato del buffer.
- Può visualizzare quali MTU sono contenute in un determinato buffer e aggiungerne di nuove manualmente se necessario

- TRAINING LINE OPERATOR - MAPELLO

- 38

- BUFFER (PRE-MACCHINA)

- BACK-OFFICE LINEA


## Slide 39: DOMANDE E RISPOSTE

- Spazio alle vostre domande.

- TRAINING LINE OPERATOR - MAPELLO

- 39

- DOMANDE E RISPOSTE

- TRAINING LINE OPERATOR - MAPELLO


## Slide 40: Grazie per l’attenzione.

- EMANUELE MERLO

- Functional & Business Analysis Specialist

- Grazie per l’attenzione.

- TRAINING LINE OPERATOR - MAPELLO
