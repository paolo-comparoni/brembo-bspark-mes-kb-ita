---
title: "Key User Training Quality Curno - Sessione Operativa e Sentencing - Analysis"
source_file: "SourcesMd/TrainingBrembo/30_Quality Key Users/B-SPARK Key User Training_ Quality (Curno).md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [CURNO]
derived_from: "SourcesMd/TrainingBrembo/30_Quality Key Users/B-SPARK Key User Training_ Quality (Curno).md"
---

# B-SPARK Key User Training_ Quality (Curno)_Analysis

## [CURNO] Apertura training, obiettivi e perimetro qualità

### Contenuto deterministico
- Sessione orientata al dominio qualità con focus su tracciabilità e sentencing.
- È esplicitata la migrazione operativa da AX verso Opcenter MES.
- Il training è impostato per chiarire sia visione funzionale sia operatività giornaliera.

### Regole operative
- In caso di termini non chiari i partecipanti devono fermare la sessione e chiedere chiarimenti.

### Tracciabilità
- Fonte: sezione `Apertura training, obiettivi e perimetro qualità`

## [SHARED] Architettura applicativa: ERP, MES, automazione e reporting

### Contenuto deterministico
- Il MES è il layer di integrazione tra ERP/SAP e automazione di fabbrica.
- I dati operativi sono consolidati per analisi e reporting Power BI.

### Blocchi tecnici
```text
SAP/ERP -> Opcenter MES -> Power BI / reportistica
Automazione linea -> Opcenter MES -> Eventi qualità tracciati
```

### Tracciabilità
- Fonte: sezione `Architettura applicativa: ERP, MES, automazione e reporting`

## [CURNO] Modalità di accesso e ambienti operativi

### Contenuto deterministico
- Accesso con credenziali Windows su URL aziendali condivisi.
- Distinzione tra ambiente produttivo e ambiente di esercitazione/pilot.
- Gestione utenti su modello enterprise con profili applicativi.

### Regole operative
- Errori di licenza/autenticazione richiedono escalation agli amministratori del sistema.

### Tracciabilità
- Fonte: sezione `Modalità di accesso e ambienti operativi`

## [SHARED] Due interfacce: quality manager (basic) e operatore bordo linea (repetitive)

### Contenuto deterministico
- Interfaccia Basic per configurazione e gestione entità qualità.
- Interfaccia Repetitive (Mendix) per operatività touch a bordo linea.
- Ruoli distinti: quality manager su Basic, operatore su Repetitive.

### Regole di business
- Il processo qualità richiede cooperazione tra front-end operatore e backoffice qualità.

### Blocchi tecnici
```text
Basic (Siemens standard pages)
  - sentencing
  - quality inspection
  - master data qualità

Repetitive (Mendix operator UI)
  - dichiarazioni operative
  - monitoraggio
  - consultazione documenti
```

### Tracciabilità
- Fonte: sezione `Due interfacce: quality manager (basic) e operatore bordo linea (repetitive)`

## [CURNO] Flusso operativo di quality: casi d'uso e percorso didattico

### Contenuto deterministico
- Percorso top-down: risultato finale -> dettaglio eventi -> configurazione.
- Use case citati: machining, washing, assembly, gestione batch/quarantena.

### Regole operative
- Le dimostrazioni sono orientate ai casi reali di impianto, non solo a funzioni isolate.

### Tracciabilità
- Fonte: sezione `Flusso operativo di quality: casi d'uso e percorso didattico`

## [CURNO] Dichiarazione scarti, quarantena e processo di sentencing

### Contenuto deterministico
- Gli scarti possono essere trattati come definitivi o candidati a valutazione.
- I candidati confluiscono in contenitori di quarantena.
- Il quality user decide l'esito operativo finale.

### Regole di business ed eccezioni
- Esiti possibili del sentencing:
  - rilascio,
  - rework,
  - scarto definitivo.
- Le decisioni di sentencing sono tracciate e influenzano il flusso successivo.

### Blocchi tecnici
```text
Scrap event -> Quarantine container -> Sentencing action -> System propagation
```

### Tracciabilità
- Fonte: sezione `Dichiarazione scarti, quarantena e processo di sentencing`

## [SHARED] Tracciabilità end-to-end: lotto, contenitore, ispezione

### Contenuto deterministico
- Catena dati di riferimento: lotto, contenitore, operazione, ispezione.
- Le ispezioni qualità sono collegate agli eventi produttivi e supportano audit.

### Regole di business
- L'avanzamento produttivo è condizionato dagli esiti qualità dove previsto dalla configurazione.

### Blocchi tecnici
```text
Lotto -> Container -> Operazione -> Quality Inspection -> Esito
```

### Tracciabilità
- Fonte: sezione `Tracciabilità end-to-end: lotto, contenitore, ispezione`

## [CURNO] Configurazione backoffice qualità e responsabilità key user

### Contenuto deterministico
- Il modulo qualità è configurabile per prodotto/linea.
- Responsabilità key user: difettosità, attributi ispezione, input operatore, regole decisionali.

### Regole operative
- La qualità deve mantenere allineate configurazioni e pratica operativa di linea.

### Tracciabilità
- Fonte: sezione `Configurazione backoffice qualità e responsabilità key user`

## [CURNO] Chiusura sessione e prossime attività

### Contenuto deterministico
- Priorità immediate: verifica accessi, completamento test, consolidamento uso quotidiano.
- Obiettivo finale: autonomia del team qualità su gestione quarantena e decisioni di esito.

### Tracciabilità
- Fonte: sezione `Chiusura sessione e prossime attività`
