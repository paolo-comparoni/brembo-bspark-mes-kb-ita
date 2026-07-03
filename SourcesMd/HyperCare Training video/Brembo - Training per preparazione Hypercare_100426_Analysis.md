---
title: "Hypercare Preparation Training - Connect MOM, Messaggi e Integrazioni (2026-04-10) - Analysis"
source_file: "SourcesMd/HyperCare Training video/Brembo - Training per preparazione Hypercare_100426.md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [SHARED]
derived_from: "SourcesMd/HyperCare Training video/Brembo - Training per preparazione Hypercare_100426.md"
---

# Brembo - Training per preparazione Hypercare_100426_Analysis

## [SHARED] Errori di Connect MOM e casi tipici di fallimento messaggio

### Contenuto deterministico
- Errori comuni: materiali mancanti rispetto all'ordine e failure su messaggi logistici.
- È citato esplicitamente un errore `500` su Connect MOM in un caso con stato `empty`.

### Blocchi tecnici
```text
Failure examples:
- ordine ricevuto ma materiali/componenti mancanti
- stato empty da EWM / middleware logistico
- errore 500 in Connect MOM
```

### Tracciabilità
- Fonte: sezione `Errori di Connect MOM e casi tipici di fallimento messaggio`

## [SHARED] Architettura di integrazione tra MES, SAP, EWM e AGV

### Contenuto deterministico
- Connect MOM traccia la comunicazione tra MES e sistemi esterni.
- Il flusso citato coinvolge SAP, EWM/SPI, AGV/Toyota e componenti middleware.
- Il MES non abilita direttamente le macchine automatiche.

### Regole di business
- Il perimetro critico del MES è la coerenza dei messaggi e della tracciabilità, non il comando diretto delle macchine.

### Blocchi tecnici
```text
MES -> Connect MOM -> SAP / EWM / AGV middleware
MES <- response / status <- sistemi esterni
```

### Tracciabilità
- Fonte: sezione `Architettura di integrazione tra MES, SAP, EWM e AGV`

## [SHARED] Limiti del MES come point of failure e impatto sulla tracciabilità

### Contenuto deterministico
- La produzione fisica può proseguire anche senza intervento diretto MES sulle macchine.
- Se però si perdono consumi, produzioni, etichette o conferme, si perde la visibilità di processo.
- La non tracciabilità è presentata come rischio operativo e potenzialmente di compliance.

### Regole di business
- Il danno principale di un fault MES in questo contesto è il disallineamento dati con impatto su audit e richiamo prodotto.

### Tracciabilità
- Fonte: sezione `Limiti del MES come point of failure e impatto sulla tracciabilità`

## [SHARED] Procedure di recovery: retry, resend e manual import

### Contenuto deterministico
- Sono citati meccanismi automatici di retry.
- È disponibile una cartella di `manual import` per forzare il reinvio.
- Il resend è utilizzabile quando il messaggio esiste ma non è arrivato a destinazione.
- Se il messaggio non viene generato, il problema richiede fix applicativo/codice.

### Regole di business ed eccezioni
- Messaggio generato ma non consegnato -> workaround possibile.
- Messaggio non generato -> workaround insufficiente.

### Blocchi tecnici
```text
Caso A: message generated, delivery failed
-> retry / resend / manual import

Caso B: message not generated
-> analisi codice / fix applicativo
```

### Tracciabilità
- Fonte: sezione `Procedure di recovery: retry, resend e manual import`

## [SHARED] Preparazione Hypercare: riconoscere l'errore e scegliere il workaround corretto

### Contenuto deterministico
- Il team deve saper distinguere errori di dato, comunicazione e generazione messaggio.
- La conoscenza di Connect MOM è considerata competenza base per il presidio live.

### Regole operative
- Prima di applicare workaround bisogna classificare il fault nel punto corretto della catena di integrazione.

### Tracciabilità
- Fonte: sezione `Preparazione Hypercare: riconoscere l'errore e scegliere il workaround corretto`
