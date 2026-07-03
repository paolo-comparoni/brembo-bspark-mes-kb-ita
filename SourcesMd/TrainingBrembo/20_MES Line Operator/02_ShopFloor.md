# 02_ShopFloor

> Documento sorgente: `E:\BremboDocs\TrainingBrembo\20_MES Line Operator\02_ShopFloor.pptx`  
> Tipo: PowerPoint (.pptx) · Slide: 23


## Slide 1: OPERATIVITÀ SHOP FLOOR

- OPERATIVITÀ SHOP FLOOR

- PREPARARE LE PERSONE ALL'ECCELLENZA OPERATIVA

- Febbraio 2026

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 2: Panoramica Funzionalità Trattate

- Questa lezione copre l’intero flusso operativo dell’operatore di linea:
  - UI dell’operatore di linea
  - Recupero e gestione degli ordini di lavoro
  - Avvio delle operazioni
  - Consumo materiali
  - Consultazione della documentazione
  - Gestione degli scarti (componenti e prodotto finale)
  - Completamento dell’operazione e gestione dei contenitori di output
  - Passaggi logistici verso magazzino o fase successiva

- Brembo Rollout Italia

- 2

- Panoramica Funzionalità Trattate

- OPCENTER MES TRAINING - SHOP FLOOR

**Note del relatore:**

Queste funzionalità sono coerenti su tutte le linee produttive.


## Slide 3: Login e riconoscimento

- L’accesso al sistema avviene tramite un utente generico del terminale (non tramite credenziali personali).
- L’operatore accede alla landing page( pagina iniziale dell'operatore) Brembo Repetitive.
- Il sistema riconosce automaticamente il Work Center grazie alla configurazione che lo associa all’equipment/macchina.
- Se il terminale è associato a un solo Work Center, la selezione viene saltata.
- Se il terminale è mappato a più centri di lavoro, l’operatore deve selezionare manualmente quello corretto.

- Brembo Rollout Italia

- 3

- Login e riconoscimento

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 4: Visualizzazione degli ordini

- Selezionato il Work Center, il sistema rende disponibili tutte le operazioni associate corredate dai rispettivi Work Order. Mostrando esclusivamente quelli in stato attivo o i pausa (le lavorazione completate vengono escluse dalla visualizzazione
- Sono disponibili filtri aggiuntivi per restringere la lista (es. scansione barcode di ordine o lotto).

- Brembo Rollout Italia

- 4

- Visualizzazione degli ordini

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 5: Struttura e stato degli ordini di produzione

- Ogni ordine mostra tre valori principali:
- Quantità totale pianificata
- Quantità in lavorazione (WIP)
- Quantità completata
- Indicatori visivi:
- Icona verde: ordine nuovo, mai avviato
- Icona con cerchio: ordine in pausa
- Icona attiva: ordine in esecuzione

- Brembo Rollout Italia

- 5

- Struttura e stato degli ordini di produzione

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 6: Composizione del gruppo di turno

- Prima di avviare qualsiasi attività operativa, è obbligatorio comporre il team di turno: il gruppo è inizialmente vuoto, il capo turno aggiunge manualmente i membri presenti (almeno una persona deve essere dichiarata).
- Senza membri nel gruppo:
- non è possibile avviare ordini
- non è possibile dichiarare consumi, scarti o output

- Brembo Rollout Italia

- 6

- Composizione del gruppo di turno

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 7: Avvio dell’ordine e quantità producibili

- L’operatore può:
- avviare l’ordine con quantità inferiori a quella totale
- non può produrre quantità superiori al pianificato (può essere ammessa una piccola tolleranza definita a SAP e associata al WO)

- Brembo Rollout Italia

- 7

- Avvio dell’ordine e quantità producibili

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 8: Casting

- Nel processo di Casting è obbligatoria la scansione dello stampo:
- lo stampo deve essere compatibile con l’ordine
- il sistema blocca l’operazione in caso di incongruenza
- La produzione non è più contata solo in pezzi, ma in stroke (colate):
- uno stroke = una colata completa dello stampo
- il sistema traccia il ciclo di vita dello stampo e il numero di colate effettuate per garantirne la qualità

- Brembo Rollout Italia

- 8

- Casting

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 9: Casting

- Il sistema non ragiona solo in pezzi singoli, ma in “colate” (shots/strokes).
- Il sistema traccia il numero di colate per determinare il ciclo di vita dello stampo.
- Nel processo di fusione è obbligatorio scansionare l’ID dell’attrezzatura (numero di serie dello stampo). Se lo stampo scansionato non è compatibile con quello previsto da SAP, il sistema blocca ogni operazione.
- Uno stampo può contenere diverse cavità (es. otto fusioni che corrispondono a quattro pezzi vendibili). Il sistema mostra la disposizione delle cavità all’interno del materiale finale (es. quattro cavità). È possibile dichiarare il difetto su una singola cavità. Questa informazione viene trasferita al processo di taglio, dove il pezzo corrispondente verrà escluso e scartato.

- Brembo Rollout Italia

- 9

- Casting

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 10: Cutting

- È richiesto che lo stesso numero di lotto (Original Batch) prosegua lungo tutta la catena della fonderia (fusione -> taglio -> trattamento termico, ecc.).
- L’operatore scansiona l’etichetta del contenitore proveniente dalla fusione. Se il lotto del contenitore non corrisponde al lotto dell’ordine di taglio, il sistema genera un errore di “determinazione del lotto fallita” e impedisce la produzione.
- Nel taglio è possibile produrre simultaneamente due materiali diversi dallo stesso monoblocco («ragno») fuso (es. Taglio 01 e Taglio 02). I difetti possono essere dichiarati separatamente per il materiale principale o per il co-prodotto.

- Brembo Rollout Italia

- 10

- Cutting

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 11: Cutting

- L’ordine di lavorazione mostra il flusso completo composto da più fasi (es. Lavorazione -> Ossidazione -> Pulizia) eseguite in centri di lavoro diversi.

- Brembo Rollout Italia

- 11

- Cutting

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 12: Consumo materiali e gestione del buffer

- Tracciabilità:
- Hard: senza scansione non è possibile completare l’output
- Soft: il sistema può proporre materiale compatibile dal buffer, previa conferma dell’operatore
- No:  Autoconsumo, il consumo avviene appena l'operatore entra nel terminale operatore.
- Se il buffer è insufficiente, l’operatore può:
- inviare una richiesta di materiale alla logistica,
- continuare a lavorare con il materiale disponibile.

- Brembo Rollout Italia

- 12

- Consumo materiali e gestione del buffer

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 13: Chiamata Materiali

- Se il buffer di linea è vuoto, l’operatore può inviare una richiesta (staging call) alla logistica/magazzino direttamente dal terminale.Per procedere, l'operatore deve selezionare il Buffer corretto, così da permettere al sistema di generare la richiesta a SAP.

- Brembo Rollout Italia

- 13

- Chiamata Materiali

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 14: Gestione degli scarti

- Nel processo di fusione sono previste tre tipologie di dichiarazione difetti:
- Scarto di componente:
- dichiarabile sul materiale in ingresso
- possibilità di scarto immediato o quarantena (valutazione)
- riduce la quantità disponibile e aggiorna il fabbisogno
- Scarto di prodotto finale:
- dichiarabile sul materiale prodotto
- impatta direttamente sulla quantità finale da produrre
- Scarto di cavità per Casting:
- consente di scartare una singola cavità dello stampo,
- informazione utilizzata nei processi successivi (es. taglio).

- Brembo Rollout Italia

- 14

- Gestione degli scarti

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 15: Completamento del Work Order e gestione contenitori

- L’operatore può:
- completare un contenitore pieno
- effettuare un completamento parziale (es. fine turno)
- Nel completamento parziale:
- il contenitore resta aperto per il turno successivo
- viene stampata un’etichetta con la quantità parziale
- Alla chiusura definitiva:
- l’ordine viene chiuso anche in SAP
- scompare dalla lista degli ordini attivi

- Brembo Rollout Italia

- 15

- Completamento del Work Order e gestione contenitori

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 16: Documentazione Operativa

- Sono disponibili due tipologie di documenti:
- Documenti del Work Center (validi per tutti gli ordini)
- Documenti specifici dell’operazione
- I documenti (PDF, immagini) vengono caricati in fase di cut-over e sono consultabili dall’operatore prima o durante l’esecuzione.

- Brembo Rollout Italia

- 16

- Documentazione Operativa

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 17: Funzioni Supervisore – Ordine di produzione

- Activity History (Cronologia delle attività): Accesso alla cronologia completa dell’ordine. Mostra chi ha eseguito le azioni, i tempi di inizio, le quantità, i componenti assemblati e l’elenco dettagliato delle non conformità.
- Non-Conformances (Non conformità): Collegamento ai dettagli di ogni difetto, inclusa l’operazione in cui è stato generato e lo stato attuale.
- Quality inspection (Ispezione di qualità): raccoglie tutte le ispezioni effettuate.
- Material (Materiale): Lista dei materiali prodotti.

- Brembo Rollout Italia

- 17

- Funzioni Supervisore – Ordine di produzione

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 18: Gestione del tempo non produttivo  - Inserimento

- Brembo Rollout Italia

- 18

- Gestione del tempo non produttivo  - Inserimento

- OPCENTER MES TRAINING - SHOP FLOOR

- Registrazione di una singola attività non produttiva

- Creazione di un gruppo che aggrega le attività non produttive


## Slide 19: Gestione del tempo non produttivo – Associazione OrdineL’operatore può collegare all’ordine l’attività non produttiva prevista nella configurazione.

- Engineering Presentation Template

- 19

- Gestione del tempo non produttivo – Associazione OrdineL’operatore può collegare all’ordine l’attività non produttiva prevista nella configurazione.

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 20: Gestione del tempo non produttivo – Associazione OrdineL’operatore può selezionare il gruppo associato all’attività non produttiva.

- Engineering Presentation Template

- 20

- Gestione del tempo non produttivo – Associazione OrdineL’operatore può selezionare il gruppo associato all’attività non produttiva.

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 21: Gestione del tempo non produttivo – Associazione e Completamento OrdineDopo aver selezionato il gruppo, viene visualizzata la lista delle attività non produttive, in questo modo fornisce la giustificazione del tempo di fermo dell’attività produttiva. Una volta terminato il momento non produttivo, l’operatore può indicarne la conclusione.

- Engineering Presentation Template

- 21

- Gestione del tempo non produttivo – Associazione e Completamento OrdineDopo aver selezionato il gruppo, viene visualizzata la lista delle attività non produttive, in questo modo fornisce la giustificazione del tempo di fermo dell’attività produttiva. Una volta terminato il momento non produttivo, l’operatore può indicarne la conclusione.

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 22: Q&A

- GRAZIE PER L’ATTENZIONE
- ORA SPAZIO ALLE VOSTRE DOMANDE

- Brembo Rollout Italia

- 22

- Q&A

- OPCENTER MES TRAINING - SHOP FLOOR


## Slide 23: Grazie per l’attenzione.

- Annalisa Casciaro

- Technical Development
- Software Development Specialist

- Grazie per l’attenzione.

- OPCENTER MES TRAINING - SHOP FLOOR
