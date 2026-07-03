---
title: "Hypercare Preparation Training - AGV, Baie e Flussi Logistici (2026-04-14) - Analysis"
source_file: "SourcesMd/HyperCare Training video/Brembo - Training per preparazione Hypercare_140426.md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [SHARED]
derived_from: "SourcesMd/HyperCare Training video/Brembo - Training per preparazione Hypercare_140426.md"
---

# Brembo - Training per preparazione Hypercare_140426_Analysis

## [CURNO] Contesto di plant: machining Curno e gestione AGV

### Contenuto deterministico
- Il caso esplicito di riferimento è il machining di Curno.
- L'AGV/GV è il vettore logistico automatico dei container nel plant.

### Regole di business
- In questo scenario le operazioni di linea dipendono dalla corretta interazione con il sistema AGV.

### Tracciabilità
- Fonte: sezione `Contesto di plant: machining Curno e gestione AGV`

## [SHARED] Attivazione AGV a livello Work Center

### Contenuto deterministico
- La funzionalità AGV si attiva sul work center/equipment.
- Parametro chiave: `ISA_Gv_Enabled`.
- Valore vuoto = comportamento di default non abilitato.

### Blocchi tecnici
```text
Equipment / Work Center property:
ISA_Gv_Enabled = true | false
(empty => false by default)
```

### Tracciabilità
- Fonte: sezione `Attivazione AGV a livello Work Center`

## [SHARED] Chiamate operative AGV da interfaccia Repetitive

### Contenuto deterministico
- L'interfaccia Repetitive espone cinque chiamate AGV operative.
- Le azioni coprono richiesta vuoti, ritorno vuoti, gestione alveolari e ritorno chip/byproduct.

### Regole operative
- L'operatore deve scegliere la chiamata coerente con la fase logistica corrente.

### Blocchi tecnici
```text
AGV actions:
- call empty
- return empty
- call alveolari
- return alveolari
- return chip container
```

### Tracciabilità
- Fonte: sezione `Chiamate operative AGV da interfaccia Repetitive`

## [SHARED] Baie, buffer, packaging specification e materiali di confezionamento

### Contenuto deterministico
- Le baie sono aree fisiche/geolocalizzate di deposito o ritiro.
- Ogni baia va associata a buffer e pack material.
- È possibile filtrare i container type ammessi nella baia.

### Regole di business
- Senza associazioni corrette di baia/buffer/materiali la chiamata AGV non è utilizzabile correttamente.

### Blocchi tecnici
```text
Baia
 -> Buffer association
 -> Pack material association
 -> Packaging/container constraints
```

### Tracciabilità
- Fonte: sezione `Baie, buffer, packaging specification e materiali di confezionamento`

## [SHARED] Semaforo chiamata AGV e scambio con sistema logistico

### Contenuto deterministico
- L'interfaccia mostra un semaforo di stato dopo il send.
- L'esito dipende dalle risposte del sistema logistico/EWM.
- Connect MOM è il punto di osservazione dei messaggi scambiati.

### Regole operative
- Dopo l'invio della richiesta AGV bisogna verificare sia stato UI sia tracciato messaggio.

### Blocchi tecnici
```text
Send request -> semaforo grigio -> attesa risposta -> stato finale aggiornato
```

### Tracciabilità
- Fonte: sezione `Semaforo chiamata AGV e scambio con sistema logistico`

## [SHARED] Backoffice Mendix e transizione dalle pagine Basic

### Contenuto deterministico
- Le nuove pagine AGV/configurazione sono state portate su Mendix.
- Basic resta disponibile come backoffice più completo.

### Regole di business
- Il supporto Hypercare deve conoscere sia il perimetro legacy Basic sia il perimetro nuovo Mendix.

### Tracciabilità
- Fonte: sezione `Backoffice Mendix e transizione dalle pagine Basic`
