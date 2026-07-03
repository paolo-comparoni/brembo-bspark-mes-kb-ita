---
title: "Opcenter MES Training - Operatività Shop Floor - Analysis"
source_file: "SourcesMd/TrainingBrembo/20_MES Line Operator/02_ShopFloor.md"
project: "Brembo B-Spark"
scope: "Core_Standard_Manual"
plants: [SHARED]
derived_from: "SourcesMd/TrainingBrembo/20_MES Line Operator/02_ShopFloor.md"
---

# 02_ShopFloor_Analysis

## [SHARED] Panoramica funzionalità shop floor

### Contenuto deterministico
Il documento copre l'intero flusso operativo dell'operatore di linea:
- UI dell'operatore di linea
- Recupero e gestione degli ordini di lavoro
- Avvio delle operazioni
- Consumo materiali
- Consultazione della documentazione
- Gestione degli scarti (componenti e prodotto finale)
- Completamento dell'operazione e gestione dei contenitori di output
- Passaggi logistici verso magazzino o fase successiva

### Regole operative
- Tutte le funzionalità descritte sono coerenti su tutte le linee produttive (nota del relatore).

### Tracciabilità
- Fonte: sezione `Panoramica funzionalità shop floor`
- Nota del relatore: `Queste funzionalità sono coerenti su tutte le linee produttive.`


## [SHARED] Login e riconoscimento del Work Center

### Contenuto deterministico
- Il login avviene tramite utente generico del terminale (non credenziali personali).
- Landing page: **Brembo Repetitive**.
- Il Work Center viene riconosciuto automaticamente tramite la configurazione equipment/macchina.
- Comportamento in base alla configurazione del terminale:

| Configurazione | Comportamento |
|----------------|---------------|
| Terminale associato a 1 solo Work Center | Selezione saltata automaticamente |
| Terminale mappato a più Work Center | Operatore deve selezionare manualmente |

### Regole di business
- L'identità dell'operatore non è la chiave di accesso: lo è la macchina/terminale.
- Il Work Center è il contesto operativo implicito a partire dall'accesso.

### Tracciabilità
- Fonte: sezione `Login e riconoscimento del Work Center`


## [SHARED] Visualizzazione degli ordini nel Work Center

### Contenuto deterministico
- La lista ordini mostra esclusivamente ordini in stato **attivo** o **in pausa**.
- Gli ordini completati sono esclusi dalla visualizzazione.
- Sono disponibili filtri aggiuntivi (es. scansione barcode di ordine o lotto).

### Regole di business
- Il filtro di default per stato esclude automaticamente le lavorazioni già chiuse.

### Tracciabilità
- Fonte: sezione `Visualizzazione degli ordini nel Work Center`


## [SHARED] Struttura e indicatori di stato degli ordini di produzione

### Contenuto deterministico
- Ogni ordine espone tre valori:
  1. Quantità totale pianificata
  2. Quantità in lavorazione (WIP)
  3. Quantità completata

- Indicatori visivi di stato:

| Icona | Significato |
|-------|-------------|
| Icona verde | Ordine nuovo, mai avviato |
| Icona con cerchio | Ordine in pausa |
| Icona attiva | Ordine in esecuzione |

### Tracciabilità
- Fonte: sezione `Struttura e indicatori di stato degli ordini di produzione`


## [SHARED] Composizione obbligatoria del gruppo di turno

### Contenuto deterministico
- Prima di qualsiasi attività operativa il team di turno deve essere composto.
- Il gruppo è inizialmente vuoto.
- Il capo turno aggiunge manualmente i membri (almeno 1 persona obbligatoria).

### Regole di business ed eccezioni
- **Blocco sistemistico** (hard constraint): senza almeno un membro dichiarato nel gruppo, il sistema impedisce:
  - avvio di ordini
  - dichiarazione di consumi, scarti e output

### Tracciabilità
- Fonte: sezione `Composizione obbligatoria del gruppo di turno`


## [SHARED] Avvio dell'ordine e gestione delle quantità producibili

### Contenuto deterministico
- L'operatore può avviare l'ordine con quantità inferiori al totale pianificato.
- Non è possibile produrre quantità superiori al pianificato.
- È ammessa una piccola tolleranza configurabile lato SAP e associata al Work Order.

### Regole di business ed eccezioni
- **Regola**: quantità di avvio ≤ quantità pianificata (salvo tolleranza SAP).
- **Eccezione configurabile**: tolleranza definita in SAP e propagata al WO.

### Tracciabilità
- Fonte: sezione `Avvio dell'ordine e gestione delle quantità producibili`


## [SHARED] Casting: scansione stampo, stroke, cavità e propagazione difetti

### Contenuto deterministico
- La scansione dello stampo è **obbligatoria** nel processo Casting.
- Lo stampo deve essere compatibile con l'ordine; in caso di incongruenza il sistema **blocca** l'operazione.
- L'unità di misura della produzione in Casting è lo **stroke** (colata), non il singolo pezzo:
  - 1 stroke = 1 colata completa dello stampo
- Il sistema traccia il numero di colate per gestire il ciclo di vita dello stampo.
- Uno stampo può avere più **cavità** (es. 8 fusioni = 4 pezzi vendibili).
- È possibile dichiarare il difetto su **una singola cavità**.
- L'informazione di difetto su cavità viene trasferita al processo di taglio successivo → il pezzo corrispondente viene escluso e scartato.

### Regole di business ed eccezioni
- **Regola di compatibilità stampo**: stampo scansionato ≠ stampo previsto da SAP → blocco operazione.
- **Regola di propagazione difetti cavità**: difetto dichiarato su cavità in Casting → automaticamente propagato al Cutting per esclusione.
- **Regola di tracciabilità stampo**: il ciclo di vita è governato dal conteggio stroke.

### Tracciabilità
- Fonte: sezione `Casting: scansione stampo, stroke, cavità e propagazione difetti`
- Testo origine: `Se lo stampo scansionato non è compatibile con quello previsto da SAP, il sistema blocca ogni operazione.`
- Testo origine: `Questa informazione viene trasferita al processo di taglio, dove il pezzo corrispondente verrà escluso e scartato.`


## [SHARED] Cutting: propagazione Original Batch e flusso multi-fase

### Contenuto deterministico
- Lo stesso numero di lotto (**Original Batch**) deve proseguire lungo tutta la catena della fonderia:

```
Fusione → Taglio → Trattamento termico → (fasi successive)
```

- L'operatore scansiona l'etichetta del contenitore proveniente dalla fusione.
- Se il lotto del contenitore ≠ lotto dell'ordine di taglio → errore **"determinazione del lotto fallita"** → produzione bloccata.
- Nel taglio è possibile produrre simultaneamente due materiali diversi dallo stesso monoblocco («ragno»):
  - es. Taglio 01 e Taglio 02
- I difetti possono essere dichiarati separatamente per materiale principale e co-prodotto.
- L'ordine di lavorazione mostra il flusso completo multi-fase (es. Lavorazione → Ossidazione → Pulizia) eseguite in Work Center diversi.

### Regole di business ed eccezioni
- **Regola di integrità lotto**: Original Batch del contenitore in ingresso deve corrispondere al lotto dell'ordine di Cutting.
- **Blocco sistemistico**: mismatch lotto → errore bloccante.
- **Regola co-produzione**: da un singolo input (ragno) si possono ottenere due output distinti tracciabili indipendentemente.

### Tracciabilità
- Fonte: sezione `Cutting: propagazione Original Batch e flusso multi-fase`
- Testo origine: `È richiesto che lo stesso numero di lotto (Original Batch) prosegua lungo tutta la catena della fonderia`
- Testo origine: `il sistema genera un errore di "determinazione del lotto fallita" e impedisce la produzione`


## [SHARED] Consumo materiali: livelli di tracciabilità (Hard / Soft / Autoconsumo)

### Contenuto deterministico
I tre livelli di tracciabilità per il consumo materiali:

| Livello | Comportamento |
|---------|---------------|
| **Hard** | Senza scansione non è possibile completare l'output |
| **Soft** | Il sistema propone materiale compatibile dal buffer; l'operatore conferma |
| **No (Autoconsumo)** | Il consumo avviene automaticamente all'accesso al terminale operatore |

- In caso di buffer insufficiente, l'operatore può:
  - inviare una richiesta di materiale alla logistica
  - continuare a lavorare con il materiale disponibile

### Regole di business
- Il livello di tracciabilità è una configurazione di sistema, non una scelta dell'operatore.
- Solo il livello Hard impone un blocco fisico alla dichiarazione output.

### Tracciabilità
- Fonte: sezione `Consumo materiali: livelli di tracciabilità (Hard / Soft / Autoconsumo)`


## [SHARED] Chiamata materiali: staging call al magazzino

### Contenuto deterministico
- L'operatore può inviare una **staging call** al magazzino/logistica direttamente dal terminale.
- Prerequisito: selezionare il Buffer corretto per permettere al sistema di generare la richiesta verso SAP.

### Regole di business
- La richiesta materiale è generata a SAP dal MES, non manualmente dall'operatore fuori sistema.
- Il buffer di destinazione è obbligatorio per l'inoltro della richiesta.

### Tracciabilità
- Fonte: sezione `Chiamata materiali: staging call al magazzino`


## [SHARED] Gestione degli scarti: componenti, prodotto finale e cavità casting

### Contenuto deterministico
Tre tipologie di dichiarazione difetti nel processo di fusione:

| Tipo scarto | Oggetto | Modalità | Impatto |
|-------------|---------|----------|---------|
| **Scarto componente** | Materiale in ingresso | Immediato o quarantena | Riduce quantità disponibile e aggiorna fabbisogno |
| **Scarto prodotto finale** | Materiale prodotto | — | Impatta sulla quantità finale da produrre |
| **Scarto cavità Casting** | Singola cavità stampo | — | Informazione usata nei processi successivi (es. taglio) |

### Regole di business
- La quarantena sul componente implica una valutazione differita (non scarto immediato definitivo).
- Lo scarto di cavità è la modalità che abilita la propagazione del difetto inter-processo.

### Tracciabilità
- Fonte: sezione `Gestione degli scarti: componenti, prodotto finale e cavità casting`


## [SHARED] Completamento del Work Order: chiusura totale e parziale dei contenitori

### Contenuto deterministico
- Due modalità di completamento:
  - **Completamento totale**: contenitore pieno
  - **Completamento parziale**: es. fine turno

- Comportamento completamento parziale:
  - Il contenitore resta aperto per il turno successivo
  - Viene stampata un'etichetta con la quantità parziale

- Comportamento alla chiusura definitiva:
  - L'ordine viene chiuso anche in SAP
  - Scompare dalla lista degli ordini attivi

### Regole di business
- La chiusura parziale non informa SAP della chiusura ordine: solo la chiusura definitiva lo fa.
- La chiusura definitiva sincronizza lo stato ordine tra MES e SAP.

### Tracciabilità
- Fonte: sezione `Completamento del Work Order: chiusura totale e parziale dei contenitori`


## [SHARED] Documentazione operativa per Work Center e operazioni

### Contenuto deterministico
Due tipi di documenti disponibili:

| Tipo | Ambito |
|------|--------|
| Documenti del Work Center | Validi per tutti gli ordini del Work Center |
| Documenti specifici dell'operazione | Legati alla singola operazione |

- Formati supportati: PDF, immagini.
- I documenti vengono caricati in fase di **cut-over**.
- Sono consultabili dall'operatore prima o durante l'esecuzione.

### Regole di business
- La documentazione operativa è pre-caricata, non generata on-the-fly.
- La visibilità dipende dal contesto (Work Center vs operazione specifica).

### Tracciabilità
- Fonte: sezione `Documentazione operativa per Work Center e operazioni`


## [SHARED] Funzioni supervisore: cronologia, non conformità e ispezioni qualità

### Contenuto deterministico
Funzionalità disponibili per il supervisore sull'ordine di produzione:

| Funzione | Descrizione |
|----------|-------------|
| **Activity History** | Cronologia completa: chi ha eseguito, tempi di inizio, quantità, componenti assemblati, non conformità |
| **Non-Conformances** | Dettagli di ogni difetto: operazione di generazione e stato attuale |
| **Quality inspection** | Raccolta di tutte le ispezioni effettuate |
| **Material** | Lista dei materiali prodotti |

### Tracciabilità
- Fonte: sezione `Funzioni supervisore: cronologia, non conformità e ispezioni qualità`


## [SHARED] Gestione del tempo non produttivo: inserimento, associazione ordine e completamento

### Contenuto deterministico
- Si può registrare una singola attività non produttiva o creare un gruppo che aggrega più attività non produttive.
- L'operatore può collegare all'ordine l'attività non produttiva prevista dalla configurazione.
- L'operatore può selezionare il gruppo associato all'attività non produttiva.
- Dopo la selezione del gruppo, viene visualizzata la lista delle attività non produttive: fornisce la giustificazione del tempo di fermo.
- Al termine dell'evento non produttivo, l'operatore indica la conclusione nel sistema.

### Regole di business
- Il tempo non produttivo è registrato e giustificato formalmente nel MES.
- Le attività non produttive sono configurate a sistema (non create liberamente dall'operatore).
- La chiusura esplicita dell'evento non produttivo è a carico dell'operatore.

### Tracciabilità
- Fonte: sezione `Gestione del tempo non produttivo: inserimento, associazione ordine e completamento`


## [SHARED] Chiusura del training

### Contenuto deterministico
- Relatrice: **Annalisa Casciaro** — Technical Development, Software Development Specialist

### Tracciabilità
- Fonte: sezione `Chiusura del training`
