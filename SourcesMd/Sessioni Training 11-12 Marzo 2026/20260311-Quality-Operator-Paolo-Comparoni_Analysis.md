---
title: "Quality Operator - Fondamenti, Master Data e Runtime (20260311) - Analysis"
source_file: "SourcesMd/Sessioni Training 11-12 Marzo 2026/20260311-Quality-Operator-Paolo-Comparoni.md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [CURNO, MAPELLO]
derived_from: "SourcesMd/Sessioni Training 11-12 Marzo 2026/20260311-Quality-Operator-Paolo-Comparoni.md"
---

# 20260311-Quality-Operator-Paolo-Comparoni_Analysis

## [SHARED] Obiettivi del training e ruolo del modulo Quality nel MES

### Contenuto deterministico
- Il training introduce il modulo Quality di Opcenter come parte integrata della soluzione MES.
- Il perimetro copre overview architetturale, esempi industriali, interfacce operatore e modello di gestione delle non conformità.
- La qualità è descritta come processo integrato con SAP, produzione, documenti digitali e reporting.

### Tracciabilità
- Fonte: sezione `Obiettivi del training e overview del modulo Quality`

## [SHARED] Architettura MES: SAP, routing/BOP, operatori e dati restituiti

### Contenuto deterministico
- SAP governa pianificazione, ordini e routing/BOP; il MES riceve questi dati e li trasforma in work order eseguibili.
- Il MES gestisce operatori, macchine, raccolta dati dal campo, integrazione con automazione e ritorno dati verso SAP.
- Il modulo Quality è uno dei moduli applicativi Opcenter e si innesta nel flusso standard di esecuzione.

### Blocchi tecnici
```text
SAP/ERP -> Routing/BOP e ordini -> Opcenter MES
Opcenter MES -> dati di produzione / qualità / movimentazioni -> SAP
```

### Tracciabilità
- Fonte: sezione `Architettura MES e integrazione con SAP`

## [SHARED] Modello operativo qualità: engineering, runtime e supervisione

### Contenuto deterministico
- Il flusso qualità è esplicitamente diviso in tre fasi: engineering/pianificazione, runtime operatore e supervisione storica.
- In engineering si definiscono caratteristiche, ispezioni e collegamenti ai processi.
- A runtime gli operatori eseguono controlli su terminale e generano dati as-built.
- In supervisione si analizzano risultati, non conformità e decisioni successive.

### Regole di business
- Le ispezioni sono collegate agli step di processo e condizionano l'operatività del work order.

### Tracciabilità
- Fonte: sezione `Tre fasi della gestione Quality`

## [SHARED] Frequenze di ispezione e regole di blocco dichiarazione

### Contenuto deterministico
- Siemens prevede ispezioni 100%, time-based e part/unit-based.
- Al go-live Brembo utilizza principalmente controlli configurati come 100%.
- Tutte le Quality Inspection sono richieste a inizio ordine e a cambio turno.

### Regole di business ed eccezioni
- Le ispezioni 100% sono bloccanti sulla dichiarazione.
- Le ispezioni time-based e part-based sono mostrate con icona dedicata; il blocco completo è previsto in evoluzione post go-live.
- Se un controllo è richiesto, l'operatore deve eseguirlo: non è previsto saltarlo facoltativamente.

### Tracciabilità
- Fonte: sezione `Frequenze di ispezione e obbligatorietà dei controlli`

## [SHARED] Original batch, cambio turno e livelli di tracciabilità materiali

### Contenuto deterministico
- Il sistema supporta la ripetizione dei controlli a cambio turno e a cambio lotto/codice.
- L'original batch vincola il consumo dei lotti MES a un sottoinsieme coerente del lotto SAP.
- Sono previsti tre livelli di tracciabilità materiali: hard, soft e no-trace.

### Regole di business ed eccezioni
- In modalità hard il materiale deve essere fisicamente e contabilmente disponibile nel pre-macchina, altrimenti il sistema blocca.
- In modalità soft il sistema può cercare il materiale a livello area, mantenendo comunque un controllo minimo.
- La configurazione della tracciabilità è parametrica per materiale/codice.

### Tracciabilità
- Fonte: sezione `Cambio turno, original batch e tracciabilità di consumo`

## [SHARED] Master data qualità: Characteristics, Failures, Inspection Definition

### Contenuto deterministico
- Le Characteristics sono l'anagrafica delle caratteristiche qualità riutilizzabili nei controlli.
- Le Failures rappresentano le anomalie/causali configurabili nel sistema.
- Le Inspection Definition collegano una caratteristica alla sua frequenza esecutiva.

### Regole di business
- La tolleranza operativa è contestualizzata nell'ispezione/piano, non nella sola anagrafica di caratteristica.
- Una stessa caratteristica può avere più Inspection Definition con frequenze diverse.

### Tracciabilità
- Fonte: sezione `Pagine Basic e master data qualità`

## [SHARED] Non conformità, life cycle e separazione tra inspection failure e scrap

### Contenuto deterministico
- Il sistema distingue tra ispezione fallita e dichiarazione diretta di scarto/quarantena.
- Le non-conformance hanno un proprio life cycle con stati e azioni di risoluzione.
- La supervisione qualità lavora sulle anomalie storiche e sulle code da analizzare.

### Regole di business ed eccezioni
- Nel setup discusso, una Quality Inspection fallita senza failure associata non genera automaticamente una non-conformance di scarto.
- La dichiarazione di scrap/quarantena genera invece il flusso operativo dedicato alla gestione materiale.

### Tracciabilità
- Fonte: sezione `Non-Conformance Life Cycle e distinzione con gli scarti`

## [SHARED] Strategia documentale e repository di riferimento

### Contenuto deterministico
- I documenti possono essere caricati e versionati nel MES con preview e categorie.
- I documenti possono essere associati a macchina, part number, work center o specifico contesto operativo.
- È esplicitata la volontà di convergere su un repository unico esterno e contestualizzato per l'operatore.

### Regole operative
- Se un documento è copiato nel MES, gli aggiornamenti del repository sorgente non si propagano automaticamente.
- L'obiettivo operativo è ridurre i caricamenti manuali duplicati e usare un repository unico quando possibile.

### Tracciabilità
- Fonte: sezione `Documents e strategia di repository`

## [SHARED] Enrichment di BOP e Work Order con controlli qualità e documenti

### Contenuto deterministico
- Le Quality Inspection possono essere collegate sia a livello BOP/routing sia direttamente a livello Work Order.
- L'associazione al BOP vale per i work order scaricati successivamente alla modifica.
- L'associazione diretta al Work Order serve come correzione puntuale su ordini già scaricati.

### Regole operative
- In caso di ordine già importato senza controlli, l'arricchimento diretto sul Work Order è il metodo rapido per sbloccare l'operatività.
- Se la modifica deve propagarsi in modo strutturale, va applicata anche al routing/BOP.

### Tracciabilità
- Fonte: sezione `Enrichment su processi e work order`

## [SHARED] Interfaccia runtime operatore, inspection obbligatorie e reporting

### Contenuto deterministico
- La pagina Repetitive mostra work center, work order, icone di obbligatorietà e accesso ai controlli qualità.
- Un'icona arancione segnala controlli obbligatori presenti sull'ordine.
- Sono disponibili viste storiche delle inspection eseguite e dei dettagli as-built dell'ordine.
- I risultati confluiscono anche nella reportistica e nelle analisi successive, inclusi report Power BI.

### Regole di business
- I controlli 100% obbligatori devono essere eseguiti dall'operatore prima della dichiarazione.
- La separazione tra pagina Basic e pagina Repetitive corrisponde a ruoli diversi: backoffice/supervisione vs linea.

### Tracciabilità
- Fonte: sezione `Pagina Repetitive, controlli obbligatori e reporting`
