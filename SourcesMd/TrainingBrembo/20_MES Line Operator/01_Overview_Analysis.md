---
title: "Opcenter MES Training - Overview Line Operator - Analysis"
source_file: "SourcesMd/TrainingBrembo/20_MES Line Operator/01_Overview.md"
project: "Brembo B-Spark"
scope: "Core_Standard_Manual"
plants: [SHARED]
derived_from: "SourcesMd/TrainingBrembo/20_MES Line Operator/01_Overview.md"
---

# 01_Overview_Analysis

## [SHARED] Benvenuti in Opcenter

### Contenuto deterministico
- Il training è introduttivo e orientato alla preparazione delle persone all'eccellenza operativa.
- Il contesto temporale esplicito è **Febbraio 2026**.
- Il perimetro dichiarato è **OPCENTER MES TRAINING - OVERVIEW**.

### Tracciabilità
- Fonte: sezione `Benvenuti in Opcenter`
- Testo origine: `PREPARARE LE PERSONE ALL'ECCELLENZA OPERATIVA`, `Febbraio 2026`


## [SHARED] Modalità di training e canali di supporto

### Contenuto deterministico
- Il rollout di riferimento è **Brembo Rollout Italia**.
- I materiali di training sono resi disponibili tramite:
  - `General`
  - `Ishango_Learning HUB`
  - `Microsoft Teams`
  - `Navigator_Training Material`
- È presente un canale di supporto identificato come: `Brembo – ISHANGO_KU INFO_ITALY_W1`
- La partecipazione alle sessioni di training ricevute è dichiarata **obbligatoria**.

### Regole operative
- La fruizione del training non è opzionale.
- Il supporto ai key user/operatori è canalizzato su repository documentali e canali Teams dedicati.

### Tracciabilità
- Fonte: sezione `Modalità di training e canali di supporto`
- Testo origine: `La partecipazione alle sessione di training ricevute è da ritenersi Obbligatoria`


## [SHARED] Cos'è il MES

### Contenuto deterministico
- Opcenter è il software **MES (Manufacturing Execution System)**.
- Funzioni principali:
  - gestisce e monitora il processo produttivo in tempo reale;
  - copre il flusso dal rilascio dell'ordine alla realizzazione del prodotto finito;
  - trasforma gli ordini ERP/SAP in istruzioni operative per persone e macchine;
  - riporta all'ERP le informazioni di produzione.

### Regole di business
- Il MES opera come livello di trasformazione tra pianificazione ERP e attività esecutiva di fabbrica.
- La retroalimentazione verso SAP è parte nativa del modello operativo.

### Tracciabilità
- Fonte: sezione `Cos'è il MES`
- Testo origine: `Opcenter è il software MES (Manufacturing Execution System) che gestisce e monitora il processo produttivo in tempo reale, dal rilascio dell'ordine alla realizzazione del prodotto finito.`


## [SHARED] Vantaggi del MES

### Contenuto deterministico
Benefici dichiarati:
- Pianificazione chiara delle operazioni
- Monitoraggio in tempo reale
- Tracciabilità
- Controllo Qualità
- Riduzione degli errori
- Acquisizione dati semplificata
- Meno carta e burocrazia
- Istruzioni digitali chiare
- Riconoscimento della produttività

### Tracciabilità
- Fonte: sezione `Vantaggi del MES`


## [SHARED] Livelli della produzione: ERP, MES, operatori e automazione

### Contenuto deterministico

| Livello | Nome | Attori | Responsabilità |
|---------|------|--------|----------------|
| 4 | ERP / Pianificazione | Direzione, supply chain, amministrazione | Decidere cosa, quanto e quando produrre |
| 3 | MES / Coordinamento | Produzione, qualità, manutenzione, resp. reparto | Tradurre decisioni in azioni e monitorarne l'esecuzione |
| 1–2 | Operatori e automazione / Esecuzione | Operatori di linea, macchine e impianti | Esecuzione fisica del processo produttivo |

### Regole di business
- Il MES è il layer di coordinamento tra pianificazione ERP e esecuzione fisica di linea.
- Le responsabilità sono stratificate per livello ISA-like (non nominato esplicitamente nel documento).

### Tracciabilità
- Fonte: sezione `Livelli della produzione: ERP, MES, operatori e automazione`


## [SHARED] Come il MES rappresenta la produzione: plant modeling e process modeling

### Contenuto deterministico
- Il **Plant Modeling** rappresenta **dove avvengono le cose**.
- Gerarchia fisica dichiarata:

```
Enterprise (gruppo Brembo)
  └── Sito produttivo (es. Mapello / Curno)
        └── Production Lines (es. Casting D Line)
              └── Work Center / Equipment (unità produttive, stazioni, buffer)
```

- Il **Process Modeling** rappresenta **come avvengono le cose**.
- Oggetti logici definiti: BOP, BOM, Tool, Work Instructions, Controlli qualità.

### Regole di business
- La conoscenza operativa del MES dipende dalla combinazione di modello fisico e modello logico.
- Entrambi devono essere configurati per garantire l'esecuzione corretta.

### Tracciabilità
- Fonte: sezione `Come il MES rappresenta la produzione: plant modeling e process modeling`


## [SHARED] Esecuzione delle attività nei Work Center

### Contenuto deterministico
- Il layout dello stabilimento è configurato manualmente in Opcenter.
- Il layout deve rispecchiare la struttura produttiva reale.
- Nei Work Center gli operatori eseguono le attività guidati dal MES.
- Ogni attività è associata a uno specifico Work Order.

### Regole di business ed eccezioni
- La coerenza tra layout reale e configurazione Opcenter è un prerequisito funzionale.
- L'unità minima di aggancio dell'attività operativa è il Work Order.

### Tracciabilità
- Fonte: sezione `Esecuzione delle attività nei Work Center`


## [SHARED] Anagrafica materiali e ricezione dati da SAP

### Contenuto deterministico
- L'anagrafica materiali viene ricevuta tramite SAP.
- Categorie di lotti associate:

```
- Materie prime
- Prodotti finiti
- Semilavorati
- Materiali di consumo
```

### Regole di business ed eccezioni
- **Regola**: la master data dei materiali è di origine SAP.
- **Eccezione tecnica ammessa ma sconsigliata**: l'inserimento manuale è possibile.
- **Vincolo operativo**: l'inserimento manuale genera disallineamenti tra sistemi.

### Tracciabilità
- Fonte: sezione `Anagrafica materiali e ricezione dati da SAP`
- Nota del relatore: `L'inserimento manuale, seppur possibile, non è una buona pratica perché crea disallineamenti tra i sistemi.`


## [SHARED] Container come unità logistica e Handling Unit SAP

### Contenuto deterministico
- I lotti vengono movimentati nello stabilimento attraverso i Container.
- Ogni Container deriva da un **Container Type** da cui eredita le caratteristiche, inclusa la quantità massima contenibile per il materiale specifico.
- L'anagrafica dei Container viene ricevuta tramite SAP.
- Mappatura funzionale:

```
Container MES  =  Handling Unit SAP
```

### Regole di business ed eccezioni
- Il container è l'unità logistica di tracciabilità e movimentazione del lotto.
- L'inserimento manuale è possibile ma non raccomandato per gli stessi motivi dei materiali.

### Tracciabilità
- Fonte: sezione `Container come unità logistica e Handling Unit SAP`


## [SHARED] Flusso dei container tra buffer, consumo e produzione

### Contenuto deterministico
- I lotti vengono recapitati in contenitori presso il buffer/PSA associato al Work Center.
- Mappatura funzionale:

```
Buffer MES  =  PSA (Pre-Staging Area) SAP
```

- Il consumo del lotto avviene tramite scansione barcode:
  - consuma il lotto nel sistema;
  - aggiorna le giacenze in tempo reale;
  - attiva la verifica istantanea di coerenza lotto/ordine.
- Durante la lavorazione, i nuovi lotti prodotti vengono caricati in nuovi contenitori.
- Raggiunta la quantità stabilita: il MES stampa automaticamente un'etichetta e dichiara il contenitore pronto per la fase successiva.

### Regole di business
- Il materiale deve essere fisicamente/logicamente disponibile nel buffer associato al Work Center.
- Il consumo è evento transazionale legato alla scansione barcode.
- Il MES esegue controllo di coerenza lotto/ordine in tempo reale.
- La chiusura del contenitore di output è governata da soglia quantità.

### Tracciabilità
- Fonte: sezione `Flusso dei container tra buffer, consumo e produzione`


## [SHARED] Buffer, availability check e richiesta materiale a SAP

### Contenuto deterministico
- Precondizione di consumo: il materiale deve essere presente in buffer associato al Work Center.
- Funzione disponibile: `Verifica Disponibilità` / `Availability Check`.
- In caso di insufficienza è possibile eseguire una `Richiesta Materiale` verso SAP.
- I buffer vengono creati manualmente in Opcenter.

### Regole di business ed eccezioni
- **Regola decisionale**:
  - Quantità buffer sufficiente → produzione consentita
  - Quantità buffer insufficiente → possibile richiesta materiale verso SAP
- **Regola di configurazione**: i buffer sono oggetti configurati manualmente in Opcenter.

### Tracciabilità
- Fonte: sezione `Buffer, availability check e richiesta materiale a SAP`


## [SHARED] BOM – Distinta base dei materiali

### Contenuto deterministico
- La BOM rappresenta l'elenco gerarchico di materie prime, componenti e semilavorati necessari per fabbricare un prodotto finito.
- Ogni voce specifica la quantità esatta richiesta.
- Struttura ad albero: guida prelievo e consumo materiali, garantendo tracciabilità dei componenti nelle fasi di assemblaggio.

### Regole di business
- La BOM è l'oggetto di riferimento per i fabbisogni materiali.
- La tracciabilità del consumo dipende dalla struttura BOM.

### Tracciabilità
- Fonte: sezione `BOM – Distinta base dei materiali`


## [SHARED] BOP – Distinta dei processi

### Contenuto deterministico
- Le As-Planned BOP sono strutture gerarchiche che contengono uno o più processi suddivisi in operazioni.
- Nel BOP si definiscono: singole fasi, macchinari necessari, materiali input/output.
- Mappatura funzionale:

```
BOP MES  =  Routing SAP
```

### Regole di business
- Il BOP governa la sequenza esecutiva del processo manifatturiero.

### Tracciabilità
- Fonte: sezione `BOP – Distinta dei processi`


## [SHARED] Operazioni e completamento produttivo

### Contenuto deterministico
- Ogni operazione è composta da una serie di attività correlate.
- Flusso esecutivo operatore:
  1. Avviare l'operazione nel sistema
  2. Dichiarare la quantità di pezzi da lavorare
  3. Completare le attività per la quantità dichiarata
  4. Il sistema registra l'operazione come Completata
- Se l'operazione è l'ultima della BOP → la quantità prodotta viene caricata automaticamente nel container di output.

### Regole di business
- L'avvio operazione e la dichiarazione quantità sono prerequisiti esecutivi obbligatori.
- Il completamento operazione è basato su quantità lavorata (anche parziale).
- L'ultima operazione della BOP attiva il caricamento automatico nel container di output.

### Tracciabilità
- Fonte: sezione `Operazioni e completamento produttivo`


## [SHARED] Work Order come oggetto centrale di esecuzione

### Contenuto deterministico
- Il Work Order è il punto di partenza dell'esecuzione del processo produttivo.
- Il Work Order collega tutte le informazioni esecutive.
- I Work Order sono normalmente trasmessi al MES da SAP secondo il piano di produzione.
- Contenuto di un Work Order:

```
- Quantità da produrre
- Materiali necessari
- Attrezzi
- Istruzioni operative
- Controlli qualità
```

- Ciclo operatore: Start Work Order → esecuzione → registrazione conclusione → backflush verso SAP.

### Regole di business ed eccezioni
- **Regola di integrazione**: i Work Order sono tipicamente generati a monte in SAP.
- **Regola transazionale**: la conclusione del Work Order abilita il backflush automatico dei consumi verso SAP.
- **Eccezione implicita**: il termine «solitamente» lascia aperta la possibilità di un canale non SAP.

### Tracciabilità
- Fonte: sezione `Work Order come oggetto centrale di esecuzione`
- Testo origine: `Solitamente i Work Order vengono trasmessi al MES da SAP`


## [SHARED] Team management e gestione del gruppo di lavoro

### Contenuto deterministico
- Ogni operatore viene assegnato a un Team specifico.
- L'operatore si unisce al Team prima di iniziare le attività.
- I Team sono flessibili e creabili on the fly.
- Un membro del Team può avviare o mettere in pausa l'operazione per l'intero gruppo.
- Al termine delle attività, l'operatore lascia il Team.

### Regole di business
- Il Team è l'unità organizzativa operativa di esecuzione collaborativa.
- È supportata l'associazione dinamica dell'operatore in tempo reale.
- Le azioni di start/pause hanno effetto a livello di gruppo.

### Tracciabilità
- Fonte: sezione `Team management e gestione del gruppo di lavoro`


## [SHARED] Chiusura del training

### Contenuto deterministico
- Relatrice: **Annalisa Casciaro** — Technical Development, Software Development Specialist

### Tracciabilità
- Fonte: sezione `Chiusura del training`
