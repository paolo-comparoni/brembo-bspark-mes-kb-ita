---
title: "Training Line Operator - Dimostrazione Flusso di Lavoro (20260312) - Analysis"
source_file: "SourcesMd/TrainingBrembo/20_MES Line Operator/Training_LineOperator_20260312.md"
project: "Brembo B-Spark"
scope: "Core_Standard_Manual"
plants: [CURNO]
derived_from: "SourcesMd/TrainingBrembo/20_MES Line Operator/Training_LineOperator_20260312.md"
---

# Training_LineOperator_20260312_Analysis

## [CURNO] Accesso al sistema con Windows Authentication

### Contenuto deterministico
- Il login avviene tramite **Windows Authentication**.
- Procedura: click su «rotellina» → «use your current windows…»
- Il contesto esplicito è **Curno**: Opcenter Execution - Login.

### Regole operative
- Non è richiesto un login applicativo dedicato: si utilizza la sessione Windows corrente.

### Tracciabilità
- Fonte: sezione `Accesso al sistema con Windows Authentication`
- Testo origine: `Curno: Opcenter Execution - Login`


## [CURNO] Use Case 1 Casting – Composizione team di turno e selezione ordine di lavorazione

### Contenuto deterministico
- Ogni macchina ha il proprio gruppo di lavoro.
- L'operatore deve registrarsi nel Team associato alla postazione **prima** di qualsiasi operazione sul Work Order.
- Metodo rapido di registrazione: **scansione badge** (barcode) → riconoscimento automatico e aggiunta al team.
- Regola sistemistica bloccante: se non c'è almeno 1 operatore registrato nel team della stazione, non è possibile avviare né gestire ordini.
- Il MES è sincronizzato con SAP: gli ordini rilasciati dalla pianificazione compaiono direttamente alla postazione con tutti i dettagli.
- Ogni riquadro ordine mostra tre quantità:
  1. Pezzi ancora da avviare
  2. Pezzi in lavorazione
  3. Pezzi completati

- Indicatori di stato:

| Icona | Significato |
|-------|-------------|
| Cerchio verde | Ordine nuovo |
| Cerchio con rombo giallo | Ordine in pausa |
| Cerchio con lunetta blu | Ordine attivo |
| Triangolo arancione | Ordine con scarti o quarantena (richiede attenzione) |

- Sono disponibili filtri e ordinamenti per la lista ordini.

### Regole di business ed eccezioni
- **Blocco sistemistico**: nessun operatore nel team → blocco avvio e gestione ordini.
- **Logica selezione WO**: non esplicitamente documentata; nota del relatore pone la domanda aperta:
  - `Con quale logica viene scelto il WO dalla lista? C'è un piano di produzione? Gli ordini con completamento parziale sono prioritari?` (domanda non risolta nel documento)

### Tracciabilità
- Fonte: sezione `Use Case 1 Casting – Composizione team di turno e selezione ordine di lavorazione`
- Nota del relatore: `Con quale logica viene scelto il WO dalla lista? C'è un piano di produzione? Gli ordini con completamento parziale sono prioritari?`


## [CURNO] Use Case 1 Casting – Visualizzazione e avvio dell'ordine di lavorazione

### Contenuto deterministico
- L'interfaccia mostra i dettagli dell'ordine di lavorazione prima dell'avvio.
- La sezione è presentata come dimostrazione visiva (slide con screenshot applicativo).

### Tracciabilità
- Fonte: sezione `Use Case 1 Casting – Visualizzazione e avvio dell'ordine di lavorazione`


## [CURNO] Use Case 1 Casting – Gestione contenitore parziale a cambio turno

### Contenuto deterministico
- Se all'avvio di un ordine esiste un container parziale, il MES lo segnala e suggerisce di completarlo per primo.
- Caso d'uso principale: **cambio turno** — il nuovo operatore si "aggancia" al cassone lasciato dal collega del turno precedente.
- Funzione disponibile per il supervisore: **Close Partial Container**
  - Chiude definitivamente il cassone con la quantità ridotta attuale
  - Invia l'informazione a SAP
  - Caso d'uso: cambio materiale urgente o decisione supervisore di non riempire ulteriormente

### Regole di business ed eccezioni
- **Regola di default**: cassone parziale esistente → MES propone di completarlo prima di aprirne uno nuovo.
- **Eccezione autorizzata supervisore**: Close Partial Container → chiusura forzata con quantità ridotta.
- **Integrazione SAP**: la chiusura forzata viene comunicata a SAP.

### Tracciabilità
- Fonte: sezione `Use Case 1 Casting – Gestione contenitore parziale a cambio turno`
- Testo origine: `l'operatore che entra nel turno può "agganciarsi" al cassone lasciato a metà dal collega del turno precedente`
- Testo origine: `l'operatore può utilizzare la funzione Close Partial Container per chiuderlo definitivamente`


## [CURNO] Use Case 1 Casting – Avvio ordine, stato avanzamento e controllo materiali

### Contenuto deterministico
- Avvio ordine senza contenitori parziali: flusso standard.
- **Tolleranza quantità**: se si tenta di avviare una quantità superiore al pianificato, il sistema può bloccare o permettere l'avvio in base alla tolleranza configurata in fase di pianificazione.

- Campi visualizzati nell'interfaccia ordine avviato:

```
Final Material & Description   → codice tecnico e descrizione prodotto
Production Finish Good         → quantità massima completabile in base ai materiali consumati/scansionati
Good Quantity (Buoni)          → totale pezzi conformi già completati
Scrap Quantity (Scarti)        → totale pezzi dichiarati scarti o difettosi
Quantità Richiesta             → totale necessario per completare l'ordine
Quantità Disponibile/Mancante  → evidenzia mancanze con icone di avviso
```

### Regole di business ed eccezioni
- **Production Finish Good** è determinato dai materiali effettivamente consumati/scansionati, non dalla quantità pianificata.
- Le mancanze di materiale vengono segnalate con icone di avviso per sollecitare approvvigionamento.
- La tolleranza è configurata a livello di pianificazione (non modificabile dall'operatore).

### Tracciabilità
- Fonte: sezione `Use Case 1 Casting – Avvio ordine, stato avanzamento e controllo materiali`
- Testo origine: `NOTA: Se si cerca di avviare una quantità superiore a quella pianificata, il sistema potrebbe bloccare o permettere l'avvio in base alla tolleranza impostata in fase di pianificazione.`


## [CURNO] Use Case 1 Casting – Semaforo stato chiamata materiali

### Contenuto deterministico
Sistema a semaforo per lo stato della chiamata materiali:

```
Grigio  → Richiesta inviata, non ancora presa in carico
Giallo  → Presa in carico dal magazzino
Verde   → Materiale disponibile
Rosso   → Errore o movimentazione bloccata
```

### Regole di business
- Il semaforo fornisce feedback visivo in tempo reale sullo stato della richiesta logistica.
- Il rosso indica una condizione anomala che richiede intervento (non un semplice ritardo).

### Tracciabilità
- Fonte: sezione `Use Case 1 Casting – Semaforo stato chiamata materiali`


## [CURNO] Use Case 1 Casting – Dichiarazione di produzione e Original Batch

### Contenuto deterministico
- Azione: pulsante **COMPLETE** per dichiarare la produzione dei pezzi buoni.
- Selezione obbligatoria: **Container Type** (tipo di imballo) — istruisce SAP sui materiali di confezionamento (coperchi, layer).
- Assegnazione dell'**Original Batch** (lotto di colata):
  - Garantisce tracciabilità totale fino a fine processo.
  - È un identificatore bloccante: il sistema impedisce la miscelazione di lotti diversi nello stesso cassone in tutte le fasi successive.

### Regole di business ed eccezioni
- **Regola di integrità Original Batch**: nessun lotto misto nello stesso cassone, in nessuna fase successiva.
- **Regola di configurazione stampo** (nota del relatore):
  - Se lo stampo non è mappato nel backend con il Part Number corretto → il MES blocca lo Start.
  - Responsabilità della corretta anagrafica stampi: **Back Office**.

### Blocchi tecnici
- Campo chiave assegnato in questa fase:
```
Original Batch  → identificatore di lotto di colata, propagato lungo tutta la catena produttiva
Container Type  → tipo imballo comunicato a SAP per la gestione materiali di confezionamento
```

### Tracciabilità
- Fonte: sezione `Use Case 1 Casting – Dichiarazione di produzione e Original Batch`
- Nota del relatore: `Se lo stampo non è mappato nel backend con il Part Number corretto, il MES blocca lo Start. È responsabilità del Back Office garantire che l'anagrafica stampi sia aggiornata.`


## [CURNO] Use Case 1 Casting – Chiusura ordine e Shadow Movement verso SAP

### Contenuto deterministico
- **Chiusura Totale**: l'ordine passa in stato `Complete`.
- **Chiusura Parziale**: usata a fine turno; stampa etichetta temporanea; il collega subentrante può completare il cassone.
- **Shadow Movement**:
  - Dopo il completamento, il MES notifica SAP.
  - SAP sposta **virtualmente** il materiale verso la fase successiva (es. Cutting).
  - Nessun intervento manuale richiesto.

### Regole di business
- Il Shadow Movement è automatico e avviene alla chiusura dell'ordine.
- Il movimento virtuale in SAP non richiede azioni operative aggiuntive.
- La chiusura parziale non attiva il Shadow Movement definitivo verso SAP.

### Tracciabilità
- Fonte: sezione `Use Case 1 Casting – Chiusura ordine e Shadow Movement verso SAP`
- Testo origine: `il MES informa SAP che sposta virtualmente il materiale verso la fase successiva (es. Cutting) senza interventi manuali.`


## [CURNO] Use Case 2 Cutting – Dichiarazione co-prodotti e by-products

### Contenuto deterministico
- **Co-products**: da 1 materiale di input (ragno fuso) si ottengono più prodotti distinti (es. pinza destra + pinza sinistra).
- Il sistema mostra entrambi i codici nel pannello di completamento (es. prodotto 800 = principale, prodotto 900 = co-prodotto).
- L'operatore deve dichiarare le quantità per **ciascun codice**.
- I pezzi buoni di ciascun prodotto vanno in cassoni CDI separati con propria etichetta CDI.
- L'ordine di dichiarazione (prima main, poi co-product o viceversa) non è obbligatorio.
- **Blocco sistemistico**: non è possibile chiudere l'ordine con quantità residue di co-prodotto non dichiarate.
- **By-products** (es. materozze, trucioli): tracciati automaticamente dal sistema e comunicati a SAP per gestione ritorni e rifusioni.
- Macchina di riferimento citata nel documento: **GMPOB02M**

### Regole di business ed eccezioni
- **Regola di completamento**: prodotto principale non chiudibile se co-prodotto ha quantità residue.
- **Blocco sistemistico**: sistema blocca la procedura di chiusura ordine fino a dichiarazione completa di tutti i co-prodotti.
- **Regola by-products**: la tracciabilità dei sottoprodotti è automatica, non richiede azione operatore.

### Blocchi tecnici
```
Co-product declaration:
  - Prodotto principale (es. codice 800)  → cassone CDI separato + etichetta CDI
  - Co-prodotto (es. codice 900)          → cassone CDI separato + etichetta CDI
  - By-product (es. trucioli, materozze)  → tracciato automaticamente → comunicato a SAP
```

### Tracciabilità
- Fonte: sezione `Use Case 2 Cutting – Dichiarazione co-prodotti e by-products`
- Nota del relatore: `Macchina GMPOB02M`
- Testo origine: `Non è possibile completare interamente la produzione del prodotto principale se rimangono quantità residue di co-prodotto non dichiarate`


## [CURNO] Back-office linea: Work in Progress App e ristampa etichette CDI

### Contenuto deterministico
- Funzionalità: **Print History** — consente di monitorare e gestire l'attività di etichettatura del sistema.
- Caso d'uso principale per il supervisore: ristampa di etichette CDI smarrite o danneggiate tramite consultazione dello storico stampe.

### Regole di business
- La ristampa etichette CDI è una funzione supervisore, non operatore.
- Lo storico stampe è consultabile dal back-office della linea tramite Work in Progress App.

### Tracciabilità
- Fonte: sezione `Back-office linea: Work in Progress App e ristampa etichette CDI`
