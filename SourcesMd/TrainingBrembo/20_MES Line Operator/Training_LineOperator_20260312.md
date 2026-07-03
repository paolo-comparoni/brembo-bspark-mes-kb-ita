---
title: "Training Line Operator - Dimostrazione Flusso di Lavoro (20260312)"
source_file: "SourcesMd/TrainingBrembo/20_MES Line Operator/Training_LineOperator_20260312.md"
project: "Brembo B-Spark"
scope: "Core_Standard_Manual"
plants: [CURNO]
---

# Training_LineOperator_20260312

> Documento sorgente: `E:\BremboDocs\TrainingBrembo\20_MES Line Operator\Training_LineOperator_20260312.pptx`  
> Tipo: PowerPoint (.pptx) · Slide: 20


## Introduzione al training Line Operator

- LINE OPERATOR
- DIMOSTRAZIONE DEL FLUSSO DI LAVORO
- Febbraio 2026
- TRAINING LINE OPERATOR


## Accesso al sistema con Windows Authentication

- Brembo Rollout Italia
- 2
- ACCESSO AL SISTEMA
- TRAINING LINE OPERATOR
  - Curno: Opcenter Execution - Login

- Brembo Rollout Italia
- 3
- ACCESSO AL SISTEMA
- TRAINING LINE OPERATOR
- Il login avviene con la Windows Authentication, cliccando prima sulla «rotellina» e poi su «use your current windows ……»


## Use Case 1 Casting – Composizione team di turno e selezione ordine di lavorazione

- Ogni macchina ha il suo gruppo di Lavoro.
- Prima di avviare qualsiasi Work Order (ordine di produzione) o operazione sulla macchina, è fondamentale che l'operatore si registri correttamente nel gruppo di lavoro (Team) associato alla postazione. Questa operazione garantisce la corretta tracciabilità delle attività e la sicurezza del processo.

- Brembo Rollout Italia
- 4
- USE CASE 1: CASTING – SELEZIONE DELL'ORDINE DI LAVORAZIONE
- TRAINING LINE OPERATOR

- Scansione Badge: La modalità più rapida consiste nello scansionare il proprio badge (barcode); il sistema riconoscerà automaticamente l'utente e lo aggiungerà al gruppo di lavoro
- Il sistema non permette di avviare o gestire ordini se non c'è almeno un operatore registrato nel team della stazione.

**Note del relatore:**

Con quale logica viene scelto il WO dalla lista? C'è un piano di produzione? Gli ordini con completamento parziale sono prioritari?

- Il sistema MES è sincronizzato con il gestionale centrale ERP «SAP».
- Quando l'ufficio pianificazione approva e rilascia un ordine di produzione, tutte le informazioni necessarie vengono trasmesse alla postazione di lavoro.
- In termini pratici, troverete l'ordine già pronto sul monitor con tutti i dettagli necessari per iniziare: il tipo di materiale, le quantità da produrre e la sequenza delle operazioni da seguire.

- Brembo Rollout Italia
- 5
- USE CASE 1: CASTING – SELEZIONE DELL'ORDINE DI LAVORAZIONE
- TRAINING LINE OPERATOR

**Note del relatore:**

Con quale logica viene scelto il WO dalla lista? C'è un piano di produzione? Gli ordini con completamento parziale sono prioritari?

- I tre numeri: Ogni riquadro mostra tre quantità:
- Pezzi ancora da avviare
- Pezzi in lavorazione
- Pezzi completati.
- Icone di Stato:
- Cerchio verde: indica un ordine nuovo
- Cerchio con rombo giallo: un ordine in pausa
- Cerchio con lunetta blu: un ordine attivo.
- Triangolo arancione: Indica che l'ordine ha prodotto scarti o pezzi in quarantena che richiedono attenzione.
- E' possibile impostare filtri e ordinare la visualizzazione.

- Brembo Rollout Italia
- 6
- USE CASE 1: CASTING – SELEZIONE DELL'ORDINE DI LAVORAZIONE
- TRAINING LINE OPERATOR

**Note del relatore:**

Con quale logica viene scelto il WO dalla lista? C'è un piano di produzione? Gli ordini con completamento parziale sono prioritari?


## Use Case 1 Casting – Visualizzazione e avvio dell'ordine di lavorazione

- Brembo Rollout Italia
- 7
- USE CASE 1: CASTING – AVVIO DELL'ORDINE DI LAVORAZIONE
- TRAINING LINE OPERATOR
- Visualizzazione dettagli ordine di lavorazione.

- Brembo Rollout Italia
- 8
- USE CASE 1: CASTING – AVVIO DELL'ORDINE DI LAVORAZIONE
- TRAINING LINE OPERATOR


## Use Case 1 Casting – Gestione contenitore parziale a cambio turno

- Se all'avvio di un ordine il sistema rileva la presenza di un container parziale, il MES segnala all'operatore che per quell'ordine esiste un cassone in sospeso e suggerisce di completare quello per primo.
- Questa funzione è pensata per gestire i cambi turno: l'operatore che entra nel turno può "agganciarsi" al cassone lasciato a metà dal collega del turno precedente, terminare il cassone e generare l'etichetta definitiva.

- Brembo Rollout Italia
- 9
- USE CASE 1: CASTING – AVVIO DELL'ORDINE DI LAVORAZIONE – CON CONTENITORE PARZIALE
- TRAINING LINE OPERATOR

- Se il supervisore decide che quel cassone non deve essere ulteriormente riempito (ad esempio per un cambio materiale urgente), l'operatore può utilizzare la funzione Close Partial Container per chiuderlo definitivamente con la quantità ridotta attuale e inviare l'informazione a SAP.

- Brembo Rollout Italia
- 10
- USE CASE 1: CASTING – AVVIO DELL'ORDINE DI LAVORAZIONE - CON CONTENITORE PARZIALE
- TRAINING LINE OPERATOR


## Use Case 1 Casting – Avvio ordine, stato avanzamento e controllo materiali

- Brembo Rollout Italia
- 11
- USE CASE 1: CASTING – AVVIO DELL'ORDINE DI LAVORAZIONE
- TRAINING LINE OPERATOR
- Avvio ordine di lavorazione (senza contenitori parziali già presenti)
- NOTA: Se si cerca di avviare una quantità superiore a quella pianificata, il sistema potrebbe bloccare o permettere l'avvio in base alla tolleranza impostata in fase di pianificazione.

- Stato e Avanzamento
- Questa parte mostra i dati dell'ordine e le quantità prodotte:
- Final Material & Description: Visualizza il codice tecnico e la descrizione del prodotto in lavorazione.
- Production Finish Good: Indica la quantità massima che puoi completare in base ai materiali effettivamente consumati/scansionati.
- Good Quantity (Buoni): Il totale dei pezzi conformi già completati per l'operazione.
- Scrap Quantity (Scarti): Il totale dei pezzi dichiarati scarti o difettosi.

- Brembo Rollout Italia
- 12
- USE CASE 1: CASTING – AVVIO DELL'ORDINE DI LAVORAZIONE
- TRAINING LINE OPERATOR
- Visualizzazione ordine avviato.

- Quantità Richiesta: il totale necessario per completare l'ordine.
- Quantità Disponibile/Mancante: il sistema evidenzia eventuali mancanze con icone di avviso per segnalare la necessità di nuovi approvvigionamenti.

- Brembo Rollout Italia
- 13
- USE CASE 1: CASTING – AVVIO DELL'ORDINE DI LAVORAZIONE
- TRAINING LINE OPERATOR


## Use Case 1 Casting – Semaforo stato chiamata materiali

- Semaforo di stato chiamata:
- Grigio: inviata ma non presa in carico.
- Giallo: presa in carico dal magazzino.
- Verde: disponibile.
- Rosso: errore o movimentazione bloccata.

- Brembo Rollout Italia
- 14
- USE CASE 1: CASTING – CHIAMATA MATERIALI
- TRAINING LINE OPERATOR


## Use Case 1 Casting – Dichiarazione di produzione e Original Batch

- Brembo Rollout Italia
- 15
- USE CASE 1: CASTING – DICHIARAZIONE DI PRODUZIONE
- TRAINING LINE OPERATOR
- Pulsante COMPLETE per dichiarare la produzione dei pezzi buoni.
- Si seleziona il Container Type (tipo di imballo) corretto per istruire SAP sui materiali di confezionamento (coperchi, layer).
- Viene attribuito l'«Original Batch» (lotto di colata) che garantirà la tracciabilità totale fino a fine processo. Questo identificatore è cruciale poiché il sistema bloccherà qualsiasi tentativo di mescolare lotti diversi, all'interno dello stesso cassone, nelle fasi di lavorazione successive.

**Note del relatore:**

Configurazione Stampo (Mold): Se lo stampo non è mappato nel backend con il Part Number corretto, il MES blocca lo Start. È responsabilità del Back Office garantire che l'anagrafica stampi sia aggiornata.


## Use Case 1 Casting – Dichiarazione difettosità

- Brembo Rollout Italia
- 16
- USE CASE 1: CASTING – DICHIARAZIONE DIFETTOSITA'
- TRAINING LINE OPERATOR


## Use Case 1 Casting – Chiusura ordine e Shadow Movement verso SAP

- Chiusura Totale: L'ordine passa in stato "Complete".
- Chiusura Parziale: Utile a fine turno per stampare un'etichetta temporanea e permettere al collega subentrante di completare il cassone.
- Shadow Movement: Una volta completato, il MES informa SAP che sposta virtualmente il materiale verso la fase successiva (es. Cutting) senza interventi manuali.

- Brembo Rollout Italia
- 17
- USE CASE 1: CASTING – CHIUSURA ORDINE
- TRAINING LINE OPERATOR


## Use Case 2 Cutting – Dichiarazione co-prodotti e by-products

- Parliamo di «co-products» (coprodotti) quando da un unico materiale di input -il ragno fuso- si ottengono intenzionalmente più prodotti distinti (es. pinza destra e pinza sinistra) durante la stessa operazione.
- Nel pannello di completamento, il sistema mostra all'operatore entrambi i codici (es. prodotto 800 e prodotto 900). L'operatore deve dichiarare le quantità prodotte per ciascun part number, che verranno poi stoccate in cassoni CDI separati per le fasi successive.
- Oltre ai co-prodotti, il sistema traccia automaticamente i «by-products» (sottoprodotti) come materozze e trucioli, che vengono comunicati a SAP per la gestione dei ritorni e delle rifusioni.
- NOTA: Non è possibile completare interamente la produzione del prodotto principale se rimangono quantità residue di co-prodotto non dichiarate; il sistema impone la gestione di entrambi i flussi per mantenere l'allineamento con SAP.

- Brembo Rollout Italia
- 18
- USE CASE 2: CUTTING – DICHIARAZIONE DEI CO-PRODUCT
- TRAINING LINE OPERATOR

**Note del relatore:**

Macchina GMPOB02M

- L'operatore preme il tasto Complete nella barra laterale destra.
- Nell'interfaccia di completamento, il sistema visualizza distintamente i codici di tutti i prodotti previsti (es. il prodotto 800 come principale e il 900 come co-prodotto).
  - L'operatore deve inserire la quantità di pezzi buoni prodotti per ciascun codice.
  - È possibile dichiarare anche eventuali scarti specifici per il co-prodotto selezionando la relativa voce nel pannello delle difettosità.
- I pezzi buoni del prodotto principale e del co-prodotto andranno messi in cassoni separati, ognuno con la propria etichetta CDI definitiva generata dal sistema.
- Non è obbligatorio seguire un ordine fisso (si può dichiarare prima il main e poi il co-product o viceversa), ma non è possibile chiudere l'ordine se rimangono quantità di co-prodotto non dichiarate. Il sistema blocca la procedura per garantire che tutti i pezzi derivanti dal taglio siano correttamente tracciati.
- Oltre ai co-prodotti, il sistema traccia in automatico i By-products (sottoprodotti, es. i trucioli), che vengono comunicati a SAP per la contabilità dei materiali di recupero.

- Brembo Rollout Italia
- 19
- USE CASE 2: CUTTING – DICHIARAZIONE DEI CO-PRODUCT
- TRAINING LINE OPERATOR

**Note del relatore:**

Macchina GMPOB02M


## Back-office linea: Work in Progress App e ristampa etichette CDI

- Brembo Rollout Italia
- 20
- BACK-OFFICE LINEA – WORK IN PROGRESS APP
- TRAINING LINE OPERATOR
- Print History
- Questa funzionalità permette di monitorare e gestire l'attività di etichettatura del sistema.
- L'attività principale per un supervisore è la consultazione dello storico delle stampe che consente la ristampa di etichette (CDI) smarrite o danneggiate.
