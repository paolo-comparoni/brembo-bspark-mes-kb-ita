---
title: "Training Line Operator - Flusso Operativo Multi-Processo (20260312) - Analysis"
source_file: "SourcesMd/Sessioni Training 11-12 Marzo 2026/20260312-Line-Operator-Francesco-Panigo.md"
project: "Brembo B-Spark"
scope: "Core_Standard_Manual"
plants: [CURNO, MAPELLO]
derived_from: "SourcesMd/Sessioni Training 11-12 Marzo 2026/20260312-Line-Operator-Francesco-Panigo.md"
---

# 20260312-Line-Operator-Francesco-Panigo_Analysis

## [SHARED] Accesso al sistema, work center e login di turno

### Contenuto deterministico
- L'accesso al sistema può avvenire con Windows Authentication oppure con credenziali utente.
- Sulle postazioni di linea il work center è normalmente preassegnato; la selezione manuale è prevista per test o casi amministrativi.
- Gli operatori devono registrarsi nel gruppo di lavoro della macchina tramite badge/barcode o selezione manuale.

### Regole operative
- Senza almeno un operatore loggato il sistema non consente azioni operative sugli ordini.
- Il logout può essere automatico a fine turno oppure manuale dalla gestione del gruppo.

### Tracciabilità
- Fonte: sezione `Accesso, selezione work center e team macchina`

## [SHARED] Lista work order, stati ordine e ordinamenti disponibili

### Contenuto deterministico
- La landing page mostra i work order disponibili per il work center con dati di operazione, materiale e triade quantità.
- Gli stati visuali distinguono ordini nuovi, attivi, in pausa e ordini con scarti/quarantena.
- Sono previsti ordinamenti e filtri per status, start pianificato e ricerca diretta per work order.

### Regole di business ed eccezioni
- A regime, per la maggior parte dei work center, è ammesso un solo ordine attivo per macchina/unità.
- Nei gruppi multi-macchina la scelta della singola unità avviene allo start dell'ordine.

### Tracciabilità
- Fonte: sezione `Visualizzazione work order e logica di stato`

## [SHARED] Start ordine, quantità iniziale e gestione del container

### Contenuto deterministico
- Lo start richiede quantità iniziale e tipo di container/packing material.
- Il sistema può proporre la quantità nominale dell'ordine come default.
- La scelta del packing material imposta anche la capacità massima dichiarabile del container.

### Regole di business
- Il generic container consente dichiarazioni parziali ma impedisce di superare la capacità massima del contenitore.
- In alcuni contesti il container type è già parte integrante del flusso SAP/MES e serve per la corretta tracciabilità di imballo.

### Tracciabilità
- Fonte: sezione `Avvio ordine e selezione del container`

## [SHARED] Chiamata materiali, staging call e semaforo di stato

### Contenuto deterministico
- La chiamata materiale può essere fatta sia sull'ordine corrente sia in anticipo per l'ordine successivo tramite staging call.
- L'interfaccia mostra buffer di riferimento, materiale richiesto, quantità disponibile in pre-macchina e stato della chiamata.
- Il semaforo evidenzia se la chiamata è stata accettata, rifiutata o è in attesa di evasione.

### Regole operative
- La chiamata non richiede quantità manuale di dettaglio: l'operatore richiede l'unità di imballo prevista dal magazzino.
- Nei work center con più materiali o più ordini il sistema propone la lista contestuale dei materiali chiamabili.

### Tracciabilità
- Fonte: sezione `Chiamata materiali e staging anticipato`

## [SHARED] Tracciabilità consumi: modalità hard, soft e automatica

### Contenuto deterministico
- Il training distingue tre modalità di tracciabilità: hard, soft e senza tracciabilità.
- In modalità hard è necessario scansionare o digitare ogni identificativo materiale richiesto.
- In modalità soft il sistema propone materiali compatibili e può usare una logica automatica di consumo.

### Regole di business ed eccezioni
- Se manca anche un solo componente obbligatorio in modalità hard, il sistema blocca l'operazione.
- La modalità applicata dipende dal processo e dal tipo di materiale.

### Tracciabilità
- Fonte: sezione `Modalità di tracciabilità dei materiali`

## [SHARED] Tool, mold e original batch

### Contenuto deterministico
- Nei processi che lo richiedono l'operatore deve confermare il tool/stampo compatibile con l'ordine.
- Nel cutting e nei flussi derivati dal casting è usato il concetto di original batch.
- L'original batch vincola il consumo dei container compatibili e permette coerenza di genealogia.

### Regole di business ed eccezioni
- Se il lotto non ha original batch valorizzato o coerente, il consumo è bloccato fino alla correzione lato WMS.
- Lo stesso original batch può essere riusato su più ordini di taglio quando il flusso lo prevede.

### Tracciabilità
- Fonte: sezione `Tool di produzione e vincolo di original batch`

## [SHARED] Dichiarazione di buoni, parziali e chiusura del container

### Contenuto deterministico
- La dichiarazione di produzione avviene con il comando complete.
- Esiste una distinzione esplicita tra complete totale e partial container.
- Il sistema può riutilizzare un container parziale esistente oppure chiuderlo definitivamente con close partial container.

### Regole di business ed eccezioni
- Il partial container mantiene aperto un contenitore già avviato per successive integrazioni di quantità.
- Il close partial container trasforma il parziale in dichiarazione definitiva e crea la relativa giacenza.
- Non è prevista una dichiarazione a zero in assenza di un container già esistente.

### Tracciabilità
- Fonte: sezione `Complete, partial container e close partial container`

## [SHARED] Scarti di produzione, quarantena e scarti componente

### Contenuto deterministico
- L'interfaccia di defect declaration consente la scelta della causale, della quantità e dell'esito operativo.
- A seconda del processo è possibile fare scrap diretto oppure quarantena.
- Lo scarto può riguardare sia il materiale prodotto sia singoli componenti/materiali consumati.

### Regole di business ed eccezioni
- La quantità scartabile è limitata dalla quantità effettivamente consumata o producibile.
- In fonderia la quarantena non è normalmente usata; gli scarti alimentano il ritorno/fusione secondo logiche dedicate.
- Nel caso dei componenti, lo scarto è riferito alla specifica ending unit selezionata.

### Tracciabilità
- Fonte: sezione `Defect declaration su prodotto e componenti`

## [MAPELLO] Scarto cavità nel casting

### Contenuto deterministico
- Nel casting è previsto uno scarto per cavità/figura tramite numerazione delle posizioni dello stampo.
- Lo scarto cavità viene poi propagato alle fasi successive senza richiedere una nuova dichiarazione manuale sul taglio.
- È disponibile anche una vista storica delle cavity declaration già registrate.

### Regole operative
- La dichiarazione richiede corrispondenza tra posizione numerica della cavità e configurazione del tool.
- Nei casi con molte cavità o senza reale utilità operativa, il training segnala la possibilità di non usare questo dettaglio.

### Tracciabilità
- Fonte: sezione `Defect on cavity e propagazione dello scarto`

## [SHARED] Gruppi macchina, work unit e ordini su più macchine

### Contenuto deterministico
- In taglio, washing e altri gruppi multi-macchina l'ordine viene startato su una specifica unità del gruppo.
- Un ordine può essere lavorato su più macchine nel tempo, ma una singola unità non può avere più ordini attivi contemporaneamente.
- Il sistema chiede esplicitamente su quale macchina/unità si sta eseguendo il lavoro.

### Regole di business
- La limitazione vale sulla singola unità o work center effettivo, non sul gruppo logico nel suo complesso.
- La pausa dell'ordine libera la macchina per una successiva riattivazione o cambio ordine.

### Tracciabilità
- Fonte: sezione `Gruppi multi-macchina e selezione unità`

## [SHARED] Strumenti backoffice di supporto per operatori e capoturno

### Contenuto deterministico
- Esistono pagine di consultazione buffer e work order usate per recuperare ending unit, stock disponibile e dati di test.
- La pagina buffer mostra materiale, batch ed ending unit presenti nel pre-macchina.
- La pagina work order consente anche l'azione di abort per rimuovere ordini non più da utilizzare dalla lista operativa.

### Regole operative
- L'abort va usato da ruoli di coordinamento e non come azione ordinaria dell'operatore di linea.
- Queste pagine servono soprattutto per supporto, test e troubleshooting, non per il flusso standard di bordo macchina.

### Tracciabilità
- Fonte: sezione `Pagine di supporto buffer/work order e attività di capoturno`
