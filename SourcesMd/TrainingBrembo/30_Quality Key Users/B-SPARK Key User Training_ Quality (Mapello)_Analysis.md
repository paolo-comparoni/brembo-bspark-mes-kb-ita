---
title: "Key User Training Quality Mapello - Sessione Operativa e Backoffice - Analysis"
source_file: "SourcesMd/TrainingBrembo/30_Quality Key Users/B-SPARK Key User Training_ Quality (Mapello).md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [MAPELLO]
derived_from: "SourcesMd/TrainingBrembo/30_Quality Key Users/B-SPARK Key User Training_ Quality (Mapello).md"
---

# B-SPARK Key User Training_ Quality (Mapello)_Analysis

## [MAPELLO] Avvio sessione, allineamento partecipanti e setup iniziale

### Contenuto deterministico
- La sessione avvia con verifiche tecniche di collegamento e presenza.
- Vengono distribuiti i link per modalità operatore e modalità qualità.
- L'accesso agli ambienti è prerequisito per l'esecuzione del training.

### Regole operative
- Prima di procedere con i casi d'uso, tutti i partecipanti devono confermare accesso funzionante.

### Tracciabilità
- Fonte: sezione `Avvio sessione, allineamento partecipanti e setup iniziale`

## [MAPELLO] Accesso applicativo, troubleshooting licenze e login Windows

### Contenuto deterministico
- Login previsto tramite sessione Windows corrente.
- L'errore di controllo licenze è un caso operativo emerso nella sessione.
- La gestione dell'errore richiede supporto amministrativo.

### Regole di business ed eccezioni
- Eccezione operativa: senza licenza valida l'utente non può accedere alle schermate target.

### Blocchi tecnici
```text
Settings (ingranaggio) -> Use current Windows session -> Login
Errore licenza -> escalation amministratore
```

### Tracciabilità
- Fonte: sezione `Accesso applicativo, troubleshooting licenze e login Windows`

## [SHARED] Ruolo del modulo qualità nel modello MES di stabilimento

### Contenuto deterministico
- Il modulo qualità riceve eventi dal processo produttivo e li traduce in azioni qualità.
- La qualità governa conformità, quarantena e chiusura non conformità.

### Regole di business
- Le decisioni qualità devono essere coerenti con la tracciabilità di lotto/container.

### Tracciabilità
- Fonte: sezione `Ruolo del modulo qualità nel modello MES di stabilimento`

## [MAPELLO] Interfacce operative e responsabilità utenti

### Contenuto deterministico
- Interfaccia operatore: acquisizione eventi e dichiarazioni in real time.
- Interfaccia qualità: analisi, validazione e decisione.
- Separazione esplicita tra chi dichiara e chi delibera.

### Regole operative
- Il processo completo richiede passaggio strutturato da evento operatore a decisione key user.

### Blocchi tecnici
```text
Operatore (input evento) -> MES (registrazione) -> Quality user (valutazione/esito)
```

### Tracciabilità
- Fonte: sezione `Interfacce operative e responsabilità utenti`

## [MAPELLO] Flusso dichiarativo: produzione, scarti e non conformità

### Contenuto deterministico
- Gli operatori dichiarano output buono, scarti e anomalie.
- Ogni evento è collegato a ordine, materiale e contenitore.
- Le non conformità seguono percorsi differenziati per tipologia/criticità.

### Regole di business
- La qualità del dato dichiarato in linea condiziona direttamente la qualità del processo decisionale successivo.

### Tracciabilità
- Fonte: sezione `Flusso dichiarativo: produzione, scarti e non conformità`

## [MAPELLO] Gestione quarantena e decisioni di sentencing

### Contenuto deterministico
- I materiali non conformi entrano in quarantena.
- Il quality user applica una decisione finale con tre esiti standard.

### Regole di business ed eccezioni
- Il materiale in quarantena non deve rientrare nel flusso standard senza decisione di sentencing.
- Esiti ammessi:
  - rilascio,
  - rework,
  - scarto definitivo.

### Blocchi tecnici
```text
NC event -> Quarantine container -> Sentencing -> Release/Rework/Scrap
```

### Tracciabilità
- Fonte: sezione `Gestione quarantena e decisioni di sentencing`

## [SHARED] Quality inspection e regole di controllo

### Contenuto deterministico
- Le inspection sono parametrizzate per fase e prodotto.
- Alcuni controlli sono bloccanti rispetto alla prosecuzione operativa.
- Gli esiti alimentano sia il processo sia la reportistica.

### Regole di business
- Le regole di inspection devono riflettere rischio e criticità di processo.

### Tracciabilità
- Fonte: sezione `Quality inspection e regole di controllo`

## [MAPELLO] Backoffice qualità: configurazione attributi e manutenzione regole

### Contenuto deterministico
- Il key user mantiene configurazioni su difetti, attributi e frequenze controllo.
- La manutenzione configurativa è necessaria per coerenza processo-strumento.

### Regole operative
- Aggiornamenti backoffice devono seguire evoluzione reale del processo produttivo locale.

### Tracciabilità
- Fonte: sezione `Backoffice qualità: configurazione attributi e manutenzione regole`

## [MAPELLO] Reporting e continuità operativa

### Contenuto deterministico
- I dati qualità sono destinati a KPI e analisi trend.
- Il training chiude con indicazioni di adozione operativa continuativa.

### Regole di business
- L'affidabilità del reporting dipende da accuratezza dichiarativa e governance qualità.

### Tracciabilità
- Fonte: sezione `Reporting e continuità operativa`
