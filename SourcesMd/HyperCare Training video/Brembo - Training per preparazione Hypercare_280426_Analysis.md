---
title: "Hypercare Preparation Training - Log, Event Viewer e Root Cause Analysis (2026-04-28) - Analysis"
source_file: "SourcesMd/HyperCare Training video/Brembo - Training per preparazione Hypercare_280426.md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [SHARED]
derived_from: "SourcesMd/HyperCare Training video/Brembo - Training per preparazione Hypercare_280426.md"
---

# Brembo - Training per preparazione Hypercare_280426_Analysis

## [SHARED] Event Viewer, application service log e lettura del tracciato tecnico

### Contenuto deterministico
- Il punto di partenza del troubleshooting tecnico è l'application service log / Event Viewer.
- Il log nativo è ricco ma poco maneggevole quando il perimetro è distribuito su molte macchine.

### Regole operative
- Per incidenti tecnici complessi il team deve sapere dove recuperare il log infrastrutturale nativo.

### Tracciabilità
- Fonte: sezione `Event Viewer, application service log e lettura del tracciato tecnico`

## [SHARED] Database centralizzato dei log e reverse engineering degli errori

### Contenuto deterministico
- Esiste un database aggregato con i log di tutte le macchine.
- Record ID e computer name vengono usati per ordinare la sequenza degli eventi.

### Blocchi tecnici
```text
Investigazione log:
- timestamp incidente
- computer name
- record ID
- evento precedente / successivo
```

### Tracciabilità
- Fonte: sezione `Database centralizzato dei log e reverse engineering degli errori`

## [SHARED] Relazione tra Connect MOM, errore parlante e analisi di secondo livello

### Contenuto deterministico
- Connect MOM è il primo livello di diagnosi.
- Il database log centralizzato è il secondo livello quando l'errore non è autoesplicativo.

### Regole operative
- Escalation di analisi:
  1. controlla Connect MOM
  2. se errore non parlante, passa ai log dettagliati

### Blocchi tecnici
```text
Layer 1 -> Connect MOM
Layer 2 -> Database log / Event Viewer aggregation
```

### Tracciabilità
- Fonte: sezione `Relazione tra Connect MOM, errore parlante e analisi di secondo livello`

## [SHARED] Bug noti, problemi di refresh e verifiche emerse dal training

### Contenuto deterministico
- È confermato un bug noto di refresh dopo scrap del prodotto finito.
- Il problema riguarda l'aggiornamento dei contatori UI e può risolversi con exit/re-enter o refresh.

### Regole di business ed eccezioni
- Un contatore non aggiornato in UI non implica automaticamente perdita del dato persistito.

### Tracciabilità
- Fonte: sezione `Bug noti, problemi di refresh e verifiche emerse dal training`

## [CURNO] Anomalie su utente, work order e container type duplicati

### Contenuto deterministico
- Sono discussi casi su Curno relativi a cutting, mismatch utente e duplicazione container type.
- Viene ipotizzato che alcuni duplicati dipendano da dati storici non cancellati correttamente.

### Regole operative
- Per i casi di dato anomalo bisogna raccogliere work order, work center e contesto impianto prima dell'analisi approfondita.

### Blocchi tecnici
```text
Dati minimi da raccogliere:
- plant / work center
- work order ID
- object ID coinvolto
- timestamp
```

### Tracciabilità
- Fonte: sezione `Anomalie su utente, work order e container type duplicati`

## [SHARED] Metodo Hypercare per classificare e analizzare un incidente

### Contenuto deterministico
- Il metodo proposto parte dal sintomo, poi dal tempo dell'evento, poi dall'analisi tecnica a strati.
- Il fine è distinguere rapidamente bug noto, refresh issue, errore dati o difetto reale.

### Regole operative
- La classificazione corretta dell'incidente riduce il tempo di diagnosi e di escalation.

### Tracciabilità
- Fonte: sezione `Metodo Hypercare per classificare e analizzare un incidente`
