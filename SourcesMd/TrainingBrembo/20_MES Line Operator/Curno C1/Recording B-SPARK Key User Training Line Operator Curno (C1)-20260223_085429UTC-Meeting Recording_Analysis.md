---
title: "Key User Training Line Operator Curno C1 - Sessione 1 Overview e Navigazione Sistema - Analysis"
source_file: "SourcesMd/TrainingBrembo/20_MES Line Operator/Curno C1/Recording B-SPARK Key User Training Line Operator Curno (C1)-20260223_085429UTC-Meeting Recording.md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [CURNO]
derived_from: "SourcesMd/TrainingBrembo/20_MES Line Operator/Curno C1/Recording B-SPARK Key User Training Line Operator Curno (C1)-20260223_085429UTC-Meeting Recording.md"
---

# Recording B-SPARK Key User Training Line Operator Curno (C1)-20260223_085429UTC-Meeting Recording_Analysis

## [CURNO] Contesto della sessione e ruolo dei key user

### Contenuto deterministico
- Sessione introduttiva del percorso MES B-Spark per i key user Curno.
- Valeria Mosconi apre la sessione con note organizzative: chiusura alle 13, anticipo della sessione successiva di un'ora, survey finale e raccolta feedback.
- Samantha introduce il perimetro del programma B-Spark e chiarisce il doppio ruolo dei partecipanti: formazione personale + futura formazione agli end user pre-go-live.
- Sono indicati come riferimenti di processo Marco Campana e Carlo Panzeri.
- La documentazione è distribuita via repository / Teams e tramite navigator Excel per topic.

### Regole operative
- I key user non sono semplici ascoltatori: devono acquisire abbastanza padronanza per fare cascata formativa sugli operatori finali.

### Tracciabilità
- Sezioni origine: `Note organizzative, ruolo dei key user e obiettivi del training`
- Evidenze: `oggi siete qui in qualità di key user`, `formare quelli che saranno gli end user`, `navigator in Excel`

## [CURNO] Ruolo del MES tra ERP e produzione

### Contenuto deterministico
- Il MES è descritto come software che gestisce e controlla la linea produttiva.
- Funzioni base:
  - monitora il processo in tempo reale;
  - trasforma gli ordini SAP in istruzioni operative per operatori e macchine;
  - riporta a SAP consumi e informazioni di produzione.
- Il modello concettuale esplicito è a livelli:

```text
Livello 4 = ERP / pianificazione
Livello 3 = MES / orchestrazione-coordinamento
Livelli 1-2 = operatori, macchine, automazione / esecuzione
```

### Regole di business
- SAP decide cosa/quando produrre; il MES orchestra l'esecuzione e verifica che avvenga come pianificato.
- Il MES si colloca tra pianificazione e automazione, non sostituisce né ERP né controllo macchina.

### Tracciabilità
- Sezioni origine: `Cos'è il MES, vantaggi e livelli della produzione`, `Recap terminologico MES e posizionamento tra ERP e automazione`
- Evidenze: `MES prende le informazioni dell'ordine e trasforma in azioni`, `il MES monitora anche che tutto venga fatto come è stato stabilito`

## [CURNO] Plant modeling e process modeling

### Contenuto deterministico
- Il training distingue due modelli:

```text
Plant modeling  = struttura fisica dello stabilimento
Process modeling = logica con cui il prodotto viene realizzato
```

- Gerarchia fisica citata:

```text
Enterprise (Brembo)
  -> Site (Curno / Mapello)
    -> Production Line
      -> Work Center / Equipment
        -> Buffer
```

- Oggetti del process model:

```text
BOP / routing
BOM
Tool
Work Instructions
Quality checks
```

### Regole di business
- Il plant model lato MES è configurato manualmente; non arriva da SAP.
- Il process model guida operazioni, materiali, documenti e controlli qualità ereditati dal Work Order.

### Tracciabilità
- Sezioni origine: `Plant modeling e process modeling`, `Demo amministrativa: materials, containers, buffer e BOP`
- Evidenze: `tutto ciò che vedete qui è inserito manualmente`, `SAP non arriva nulla da SAP`, `il Workcorder eredita tutto ciò che c'è nella bop`

## [CURNO] Materiali e container: master data SAP e rischio di disallineamento

### Contenuto deterministico
- Materiali e container sono master data condivise con SAP.
- Materiali citati: materie prime, prodotti finiti, semilavorati, materiali di consumo.
- Il container MES corrisponde alla Handling Unit SAP.
- Il container eredita le proprie caratteristiche da un `Container Type`, inclusa la capacità massima.

### Regole di business ed eccezioni
- **Regola**: materiali, container e Work Order non devono essere creati manualmente in MES.
- **Motivazione**: evitare disallineamenti tra SAP e MES.

### Blocchi tecnici
```text
MES Container = SAP Handling Unit
Container <- Container Type (capacità, caratteristiche)
```

### Tracciabilità
- Sezioni origine: `Materiali, lotti, container e master data condivisa con SAP`, `Demo amministrativa: materials, containers, buffer e BOP`
- Evidenze: `non possono essere inseriti manualmente`, `solo SAP comanda e SAP spedisce il dato`

## [CURNO] Buffer, PSA e consumo materiali

### Contenuto deterministico
- Il buffer è l'area di stoccaggio associata al Work Center, fisicamente vicina alla stazione di lavoro.
- In SAP la stessa area è la `Production Staging Area (PSA)`.
- L'operatore consuma materiale tramite scansione barcode del container di input.
- Alla scansione, il MES:
  - verifica che il lotto sia corretto per ordine/operazione;
  - registra il consumo;
  - aggiorna SAP e le giacenze in tempo reale.
- Il sistema ha una funzione esplicita di `Verifica disponibilità`.

### Regole di business
- Il buffer è configurato manualmente in MES ma viene alimentato con stock governato da SAP.
- Se il lotto scansionato non è coerente con ordine/operazione, il MES blocca il flusso.
- La chiamata materiale richiede selezione del buffer corretto e viene propagata a SAP.

### Blocchi tecnici
```text
Work Center -> Buffer MES
SAP -> PSA / stock owner
Consumo barcode -> aggiornamento giacenze real time
```

### Tracciabilità
- Sezioni origine: `Buffer, consumo materiali, verifica disponibilità e chiamata materiale`, `Chiarimenti su ordine, materiali, team e buffer PSA`
- Evidenze: `production staging area`, `spedisce a SAP il lotto consumato`, `verifica esattamente ma questo lotto è corretto`

## [CURNO] BOM, BOP, operazioni e Work Order

### Contenuto deterministico
- La BOM è descritta come struttura gerarchica dei materiali necessari.
- La BOP è la sequenza di processi/operazioni; in SAP è il `routing`.
- Ogni attività eseguita nel Work Center è legata a un Work Order.
- Il Work Order contiene o eredita:

```text
operazioni
materiali
documenti
work instructions
quality inspections
attrezzature
```

- La relazione esplicita è:

```text
SAP -> invia Work Order
BOP -> definisce operazioni e contenuti
Work Order -> eredita la BOP e diventa esecuzione pratica
```

### Regole di business
- Non sono ammessi Work Order creati manualmente in MES.
- L'ordine è il punto di ingresso operativo per l'utente di linea.
- L'ultima operazione della BOP carica automaticamente l'output nel container di uscita.

### Tracciabilità
- Sezioni origine: `BOM, BOP, operazioni e Work Order`, `Ereditarietà BOP → Work Order e visibilità di materiali, documenti e quality`
- Evidenze: `Su MES viene chiamata Bop, su SAP viene chiamata routing`, `Il Workcorder è associato naturalmente al bop`

## [CURNO] Team management e abilitazione allo start

### Contenuto deterministico
- Prima dello start deve essere associato almeno un operatore al gruppo della postazione.
- L'operatore può essere aggiunto anche al volo.
- Un operatore può avviare o mettere in pausa l'operazione per tutto il gruppo.
- Se l'operatore dimentica di lasciare il team, il sistema può disassociarlo automaticamente a fine turno.

### Regole di business
- **Blocco hard**: senza operatore nel team non si può iniziare l'operatività.
- Il gruppo è associato al Work Center/equipment, non al singolo ordine in modo isolato.

### Tracciabilità
- Sezioni origine: `Chiarimenti su ordine, materiali, team e buffer PSA`, `Recap terminologico MES e posizionamento tra ERP e automazione`
- Evidenze: `non è possibile fare uno start di un ordine se non c'è almeno un operatore collegato`

## [CURNO] Demo amministrativa nel client Opcenter

### Contenuto deterministico
- La sessione mostra ricerche e navigazione in app amministrative Opcenter per:
  - Materials
  - Material Aggregate Unit / Container
  - Buffer
  - BOP
  - Work Order
- Si mostrano proprietà, history, revisione, date creazione/modifica e link tra BOP, operazioni e Work Order.
- La documentazione può essere visibile nelle operation/stazioni di lavoro e collegata a plant, prodotto o Work Center.

### Regole operative
- Esistono due prospettive applicative:
  1. UI operatore `Brembo Repetitive` per l'esecuzione;
  2. schermate amministrative Opcenter per consultazione di anagrafiche, ordini e relazioni.

### Tracciabilità
- Sezioni origine: `Demo amministrativa: materials, containers, buffer e BOP`, `Questioni operative: start, materiali, documentazione, stato ordine e output message`

## [CURNO] Documenti, quality e output message verso SAP

### Contenuto deterministico
- La documentazione di prodotto / operation è resa visibile nella schermata operatore lato destra.
- Esistono sezioni dedicate per quality station / quality checks e stato ordine.
- Nel Work Order è visibile anche `Output Message`, cioè la traccia dei dati inviati a SAP sia a livello operazione sia a livello ordine.
- È possibile risalire dal Work Order alla BOP tramite codice di `process` / `process need`.

### Regole di business
- I messaggi a SAP sono parte esplicita e consultabile del flusso.
- La documentazione operativa è considerata parte dell'esecuzione e non solo conoscenza teorica.

### Blocchi tecnici
```text
Work Order -> Output Message -> messaggi inviati a SAP
Work Order -> Process Need / Process -> BOP di riferimento
```

### Tracciabilità
- Sezioni origine: `Questioni operative: start, materiali, documentazione, stato ordine e output message`
- Evidenze: `nella voce output message vediamo sempre i dati che vengono spediti a SAP`
