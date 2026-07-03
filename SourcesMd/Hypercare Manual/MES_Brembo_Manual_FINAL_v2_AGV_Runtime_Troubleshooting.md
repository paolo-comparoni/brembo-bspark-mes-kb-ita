# MES_Brembo_Manual_FINAL_v2_AGV_Runtime_Troubleshooting

> Documento sorgente: `E:\BremboDocs\Hypercare Manual\MES_Brembo_Manual_FINAL_v2_AGV_Runtime_Troubleshooting.docx`  
> Tipo: Word (.docx)

**MES Brembo  
Operating, Functional, Back Office, Line Operator & Hypercare Manual**

Documento unico consolidato da sessioni training Hypercare, Back Office e Line Operator

*Versione finale draft – include capitoli UI Behaviour, Operating Model Operatore e Troubleshooting Operatore*

# Executive Summary

Il presente documento costituisce il manuale operativo, funzionale, di configurazione Back Office, Line Operator e di supporto Hypercare per la soluzione MES implementata presso Brembo, basata su Siemens Opcenter e integrata con sistemi SAP, EWM, CPI, Connect MOM e AGV.

Il documento consolida in un’unica vista organica i processi operativi, il comportamento dell’interfaccia utente, le logiche applicative, le configurazioni dati, le integrazioni e le pratiche di troubleshooting emerse dalle sessioni di training e preparazione al go-live.

## Obiettivo del documento

Fornire uno strumento unico che consenta agli operatori di linea di eseguire correttamente le attività operative quotidiane, ai key user e ai supervisori di comprendere logiche e vincoli di processo, al team Hypercare/AMS di diagnosticare rapidamente anomalie e al team IT/tecnico di analizzare errori applicativi, integrazioni e dati.

## Approccio operativo

Il manuale distingue tra comportamento standard, comportamento dipendente da configurazione, eccezione operativa e workaround. Particolare attenzione è dedicata al punto di vista dell’operatore: colori, indicatori, refresh, disponibilità dei comandi e feedback runtime sono trattati come elementi fondamentali dell’esperienza d’uso.

## Valore del documento

Il documento rappresenta una knowledge base operativa e tecnica riutilizzabile durante training utenti, go-live, hypercare, supporto AMS e futuri rollout. L’integrazione dei capitoli Line Operator consente di collegare le regole tecniche alla modalità con cui l’operatore vede e interpreta il sistema in linea.

# Registro fonti e perimetro del documento

Il documento consolida i contenuti estratti dalle registrazioni e trascrizioni disponibili relative al training per preparazione Hypercare, alla sessione Back Office del 12 marzo 2026 e alle sessioni Line Operator del 12 marzo 2026. Le informazioni sono organizzate per capitoli funzionali e operative, ma devono essere validate rispetto all’ambiente effettivo di produzione prima dell’uso operativo definitivo.

| **\#** | **Sessione**                                            | **Contenuti principali utilizzati**                                                                                         |
| ------ | ------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| 1      | 2026-03-24 – Training Hypercare                         | MTU, container, stock available, buffer, non conformità, scrap, rapporto BOM e quantità frazionarie.                        |
| 2      | 2026-03-27 – Training Hypercare                         | Matrice competenze, modello go-live/hypercare, quality inspection, original batch, disassemblaggio, e-treatment.            |
| 3      | 2026-03-31 – Training Hypercare                         | Governance deploy, persistent log, ETW, interlocking check, troubleshooting complete e consumo materiali.                   |
| 4      | 2026-04-07 – Training Hypercare                         | Assembly monofase, second assembly, multifase, flusso teso, complete e logiche di fase.                                     |
| 5      | 2026-04-10 – Training Hypercare                         | Connect MOM, SAP/EWM/CPI, retry, manual import, gestione errori integrazione e procedure AMS.                               |
| 6      | 2026-04-14 – Training Hypercare                         | AGV, baie, buffer, packaging material, call empty/return empty, stato chiamate e Connect MOM.                               |
| 7      | 2026-03-12 – Back Office – Juela Ndoka                  | Material master, proprietà materiali, relazione materiale-buffer-container type, ambiente test, configurazione Back Office. |
| 8      | 2026-03-12 – Line Operator – Francesco Panigo – Parte 1 | Flusso standard operatore, use case Casting/Cutting, accesso, UI operativa e Back Office light.                             |
| 9      | 2026-03-12 – Line Operator – Francesco Panigo – Parte 2 | Consumo materiali passo-passo, indicatori UI, stato verde, refresh, complete disponibile dopo completamento prerequisiti.   |

Nota di aggiornamento: la versione v2 integra anche la KT “Brembo - KT su argomenti specifici” del 26 giugno 2026, utilizzata per arricchire la sezione AGV Runtime & Troubleshooting e i workaround operativi AGV.

# 1\. Ambito della Soluzione MES

La soluzione MES supporta gestione ordini, consumo materiali, completamento operazioni, qualità, tracciabilità, integrazione con sistemi esterni e movimentazione automatica. Il sistema non deve essere interpretato solo come interfaccia operatore, ma come piattaforma di esecuzione e tracciabilità fortemente dipendente da dati master, configurazioni e integrazioni.

  - Gestione Work Order e Work Order Operation.

  - Gestione materiali, MTU, container e buffer.

  - Gestione scrap, difetti e non conformità.

  - Quality inspection e interlocking check.

  - Batch management e tracciabilità end-to-end.

  - Integrazione SAP/EWM/CPI tramite Connect MOM.

  - Movimentazione AGV e gestione baie.

  - Supporto Hypercare e troubleshooting tecnico-operativo.

  - Supporto operativo agli utenti di linea tramite feedback UI, indicatori e modello operativo standard.

# 2\. Accesso al Sistema e Navigazione

## 2.1 Accesso e contesto operativo

L’utente accede alla soluzione MES nel contesto di plant, area e work center. La corretta selezione del contesto è fondamentale perché ordini, buffer, materiali disponibili, configurazioni AGV e azioni operative dipendono dal perimetro selezionato.

## 2.2 Modalità di accesso per ruolo

| **Ruolo**                 | **Modalità di accesso prevista / tipica**                                                              | **Nota operativa**                                                                 |
| ------------------------- | ------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------- |
| Operatore di linea        | Accesso semplificato dalla postazione di linea, con riconoscimento postazione e/o badge dove previsto. | L’obiettivo è ridurre tempi di login e rischio di selezione errata.                |
| Back Office / Supervisore | Accesso tramite credenziali e pagine specifiche di configurazione o monitoraggio.                      | Utilizzato per consultazione avanzata, supervisione e alcune funzioni di supporto. |
| IT / AMS                  | Accesso tecnico ad ambiente, log, integrazioni e strumenti diagnostici.                                | Da utilizzare secondo governance e tracciabilità degli interventi.                 |

## 2.3 UI Repetitive

La UI Repetitive rappresenta la schermata principale per l’operatore di linea. Da qui l’utente visualizza gli ordini, avvia la sessione produttiva, consuma materiali, registra scarti, esegue controlli qualità e completa le operazioni.

## 2.4 Refresh e sincronizzazione

Alcuni problemi visualizzati in interfaccia possono dipendere da ritardo di refresh o mancato aggiornamento visivo. In questi casi il primo controllo operativo consiste nel ricaricare la pagina o uscire e rientrare nella funzione, verificando se il dato risulta coerente con il backend.

# 3\. Modello Operativo Standard dell’Operatore di Linea

## 3.1 Principio generale

Le sessioni Line Operator evidenziano che il flusso operativo dell’operatore segue uno schema concettualmente stabile: accesso, selezione del contesto, start ordine, consumo materiali, eventuali controlli qualità, dichiarazione difetti/scarti e complete. Ogni processo può avere peculiarità specifiche, ma il modello mentale di base resta comune.

## 3.2 Flusso standard

1.  Accedere alla postazione MES di linea.

2.  Verificare o selezionare il Work Center corretto.

3.  Identificare il Work Order da lavorare.

4.  Eseguire lo Start dell’ordine/operazione.

5.  Consumare i materiali richiesti secondo le indicazioni della UI.

6.  Eseguire eventuali controlli qualità o dichiarazioni richieste.

7.  Dichiarare difetti o scrap se necessario.

8.  Verificare che tutti i prerequisiti siano soddisfatti.

9.  Eseguire il Complete quando il sistema lo rende disponibile.

## 3.3 Varianti operative

Pur mantenendo un modello comune, il flusso può variare in funzione di tipo ordine, area produttiva, configurazione di qualità, presenza di flussi multifase o flusso teso, richieste AGV e vincoli di batch/original batch.

| **Scenario**       | **Possibile variante**                                                                       |
| ------------------ | -------------------------------------------------------------------------------------------- |
| Casting            | Possibile gestione di cavità, difetti e generazione di non conformità.                       |
| Cutting            | Possibile consumo di materiale proveniente da fase precedente e gestione di scrap propagato. |
| Assembly           | Possibile gestione monofase, multifase o flusso teso.                                        |
| Flusso teso        | Complete non sempre disponibile sulla prima fase; chiusura demandata alla fase finale.       |
| Quality Inspection | Azioni operative bloccate fino al completamento dei controlli richiesti.                     |

# 4\. Comportamento UI e Feedback Operatore

## 4.1 Importanza del feedback visivo

Per l’operatore di linea, il comportamento visivo della UI è parte integrante del processo operativo. Colori, icone, contatori e disponibilità dei pulsanti comunicano lo stato di avanzamento e aiutano l’utente a capire quali azioni sono ancora necessarie.

## 4.2 Stati visivi principali

| **Elemento UI**                    | **Interpretazione operativa**                                                                              | **Azione suggerita**                                           |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| Indicatore verde                   | La condizione associata risulta soddisfatta o l’azione è stata completata correttamente.                   | Proseguire con lo step successivo.                             |
| Icona o indicatore ancora presente | Esiste ancora un’azione richiesta o una condizione non completata.                                         | Verificare materiali, qualità, quantità o messaggio associato. |
| Assenza di icone residue           | Il flusso relativo allo step può essere considerato completato, salvo altre condizioni.                    | Verificare se il Complete è disponibile.                       |
| Pulsante Complete non disponibile  | Almeno un prerequisito non è soddisfatto oppure la configurazione non consente il complete in quella fase. | Verificare consumi, qualità, interlocking e tipo ordine.       |

## 4.3 Consumo materiali nella vista operatore

Durante il consumo materiali, la UI può mostrare materiali già consumati e materiali ancora da consumare. L’operatore deve interpretare la presenza di elementi residui come indicazione che il ciclo non è ancora completo. Quando tutti i materiali richiesti risultano consumati, gli indicatori si aggiornano e il sistema abilita le azioni successive, se consentite dalla configurazione.

## 4.4 Complete nella vista operatore

Il Complete deve essere eseguito solo quando il sistema lo rende disponibile. Se il pulsante non è disponibile, l’operatore non deve forzare il processo ma verificare consumi, controlli qualità, stato ordine e eventuali messaggi di blocco.

## 4.5 Refresh e latenza

Alcune modifiche possono non essere immediatamente visibili in UI. In particolare, nei casi di aggiornamento lento, refresh manuale o attesa breve possono essere necessari per vedere lo stato corretto. Se dopo refresh la UI resta incoerente, il problema deve essere segnalato come potenziale anomalia UI/backend.

# 5\. Back Office Light per Supervisori e Operatori Avanzati

## 5.1 Scopo

Accanto al Back Office di configurazione, esiste un insieme di funzioni di supporto alla linea che possono essere utili a supervisori o utenti abilitati per contestualizzare ciò che avviene nella UI operativa.

## 5.2 Funzioni tipiche

| **Funzione**           | **Utilizzo**                                                                             |
| ---------------------- | ---------------------------------------------------------------------------------------- |
| Print History          | Consultare storico stampe e ristampare etichette smarrite o danneggiate, se autorizzato. |
| Work Orders            | Consultare stato e dettaglio degli ordini ricevuti.                                      |
| Work Order in Progress | Monitorare avanzamento produzione e quantità.                                            |
| Genealogia as-built    | Consultare la tracciabilità effettiva dell’ordine/materiale.                             |
| Quality Inspections    | Visualizzare controlli qualità collegati all’ordine.                                     |
| Non Conformances       | Consultare stato e dettaglio delle non conformità.                                       |

## 5.3 Distinzione da Back Office di configurazione

Il Back Office Light non deve essere confuso con il Back Office di configurazione. Il primo supporta consultazione e operazioni limitate di supervisione; il secondo governa anagrafiche, materiali, buffer, container type e dati di configurazione che impattano il comportamento del sistema.

# 6\. Gestione Operativa Ordini di Produzione

## 6.1 Work Order

Il Work Order rappresenta l’ordine di produzione. Può contenere una o più operazioni e definisce il materiale da produrre, i materiali da consumare, la quantità pianificata e le regole operative associate.

## 6.2 Start ordine

Lo Start dell’ordine apre la sessione produttiva per l’operazione selezionata. A seguito dello start il sistema abilita le azioni compatibili con lo stato dell’ordine e con la configurazione del flusso.

## 6.3 Pausa, cambio ordine e disassemblaggio logico

In caso di pausa ordine o cambio produzione, i materiali allocati possono essere disallocati e resi nuovamente disponibili a buffer. Questo comportamento può generare nuove MTU o modificare codici e stati delle MTU esistenti.

# 7\. Consumo Materiali

## 7.1 Concetti base

Il consumo materiali collega il materiale fisico presente in linea all’ordine in esecuzione. Il sistema valida materiale, batch, stato MTU, buffer, work center e vincoli di original batch.

## 7.2 Consumo manuale

Il consumo manuale avviene tramite scansione o selezione del container/materiale. Il sistema verifica la coerenza rispetto all’ordine e alle configurazioni disponibili.

## 7.3 Consumo automatico e soft material

Per alcuni materiali configurati come soft, il sistema può proporre o eseguire un consumo automatico in fase di complete. Se il materiale non viene proposto, il complete può fallire a causa di interlocking check.

## 7.4 Consumo progressivo e stato materiali

Nel flusso reale, il consumo può avvenire progressivamente: alcuni componenti risultano già consumati, mentre altri restano ancora richiesti. L’operatore deve usare gli indicatori UI per verificare l’avanzamento del consumo prima di procedere al complete.

## 7.5 Materiale fisico presente ma non visibile

Scenario tipico: l’operatore vede fisicamente materiale in linea, ma il MES non lo mostra. Le cause più frequenti sono stock available non ricevuto, buffer non configurato, MTU non available, errore Connect MOM o mismatch tra buffer di area e work center.

10. Identificare plant, area, work center e buffer.

11. Verificare se lo stock available è arrivato.

12. Controllare Connect MOM.

13. Verificare stato e posizione della MTU.

14. Confermare che il buffer sia configurato correttamente per il work center.

# 8\. Completamento Operazioni (Complete)

## 8.1 Prerequisiti

  - Ordine avviato correttamente.

  - Materiali richiesti consumati o consumabili automaticamente.

  - Quality inspection obbligatorie completate.

  - Interlocking check soddisfatti.

  - Quantità coerenti con BOM e configurazione dell’operazione.

## 8.2 Complete e abilitazione pulsante

Il pulsante Complete diventa disponibile solo quando tutte le condizioni richieste risultano soddisfatte. Se non compare o non è abilitato, l’operatore deve verificare quali condizioni risultano ancora pendenti.

## 8.3 Ordini monofase

Negli ordini monofase, come First Assembly o Second Assembly, consumo e completamento avvengono nella stessa operazione.

## 8.4 Ordini multifase

Negli ordini multifase i materiali possono essere consumati nella prima operazione o distribuiti tra più operazioni. Il completamento finale può essere legato all’ultima fase del ciclo.

## 8.5 Flusso teso

Nel flusso teso la fase successiva può ricevere disponibilità già allo start della precedente. Il complete manuale della prima fase può non essere consentito e la chiusura può avvenire solo sull’ultima operazione.

# 9\. Gestione Qualità

## 9.1 Quality Inspection

Le quality inspection sono controlli obbligatori o configurabili associati all’ordine o all’operazione. Se non completati, possono bloccare complete, scrap o altre azioni operative.

## 9.2 Blocchi operativi

Un blocco causato da quality inspection mancante deve essere interpretato come comportamento funzionale atteso, non necessariamente come errore applicativo.

## 9.3 Evoluzioni

Le quality inspections possono essere richieste a inizio ordine, cambio turno o, in scenari futuri, secondo logiche time-based o unit-based.

# 10\. Gestione Difetti, Scrap e Non Conformità

## 10.1 Dichiarazione difetto

La dichiarazione difetto consente di registrare anomalie su materiale, cavità, main product o co-product. Può generare una non conformità collegata a container e MTU.

## 10.2 Propagazione scrap

In alcuni scenari la difettosità dichiarata in una fase, ad esempio casting, può propagarsi come scrap in una fase successiva, ad esempio cutting. Lo stato della non conformità cambia quando il materiale collegato viene consumato.

## 10.3 Main product e co-product

Lo scrap può avere impatti diversi se riferito a main product o co-product. In presenza di rapporti BOM non 1:1 possono emergere quantità frazionarie, che devono essere spiegate agli utenti come effetto della relazione tra input e output di processo.

# 11\. Modello Funzionale MES

## 11.1 Macro-processi

  - Casting: generazione origine materiale, batch e possibili difetti/cavità.

  - Cutting: consumo materiale e gestione scrap propagato.

  - Heat Treatment / E-treatment: processo termico con esito OK/NOK da sistemi esterni.

  - Finishing / Control / X-Ray: controlli e lavorazioni successive.

  - Assembly: ordini monofase, multifase e flusso teso.

  - Logistics / AGV: movimentazione automatica di container e materiali.

## 11.2 Dipendenze

Il prodotto di una fase diventa materiale consumabile da una fase successiva. Batch, MTU, container, buffer e original batch consentono la tracciabilità lungo l’intera catena produttiva.

# 12\. Batch Management e Tracciabilità

## 12.1 Native Batch

Il Native Batch identifica il batch associato all’ordine o alla fase produttiva.

## 12.2 Original Batch

L’Original Batch identifica l’origine della colata e viene propagato lungo il ciclo produttivo, supportando la tracciabilità end-to-end.

## 12.3 Regola di consumo

Un ordine che eredita un original batch deve consumare materiali compatibili con lo stesso original batch. In caso contrario, il sistema può bloccare il consumo.

## 12.4 Original batch mancante

Se un materiale non possiede original batch, l’azione corretta in Hypercare è risalire alla genealogia e validare il dato, evitando modifiche non governate.

# 13\. Material Tracking e Container

## 13.1 MTU

La Material Tracking Unit rappresenta l’unità materiale tracciata dal sistema e contiene informazioni quali batch, stato, quantità, codice e proprietà.

## 13.2 MTU Aggregate / Container

La MTU Aggregate rappresenta un aggregatore di MTU ed è spesso utilizzata come container logico o fisico.

## 13.3 Codice e batch

Il campo Code può rappresentare batch o serial number in funzione del Code Type. La corretta interpretazione del Code Type è fondamentale in troubleshooting.

# 14\. Back Office & Data Configuration

## 14.1 Scopo

Questa sezione descrive gli elementi di configurazione Back Office che impattano direttamente il comportamento del sistema in produzione. La sessione Back Office del 12 marzo evidenzia che materiali, buffer e container type sono oggetti centrali per comprendere disponibilità materiali, consumo e tracciabilità.

## 14.2 Ruolo del Back Office

Il Back Office rappresenta il livello di configurazione e gestione delle anagrafiche e delle relazioni dati utilizzate dal MES. Non è destinato all’uso quotidiano degli operatori di linea, ma a key user tecnici, industrializzazione, IT, AMS e supporto applicativo.

## 14.3 Distinzione ambienti

Durante il training è stato chiarito che l’ambiente utilizzato era un ambiente di test/training. Il comportamento osservato in test può differire dalla produzione a causa di dati incompleti, configurazioni non allineate, integrazioni parziali o versioni software diverse.

| **Ambiente**         | **Scopo**                            |
| -------------------- | ------------------------------------ |
| DEV                  | Sviluppo e configurazione.           |
| QA / TEST / TRAINING | Validazione funzionale e formazione. |
| PROD                 | Esecuzione reale della produzione.   |

## 14.4 Material Master

I materiali presenti nel MES provengono da ERP/SAP e vengono sincronizzati tramite job automatici. Il MES non deve essere considerato il sistema master dei materiali: esecuzione e tracciabilità sono in MES, mentre la responsabilità primaria dell’anagrafica materiale resta a monte.

### 14.4.1 Identificazione del materiale

Ogni materiale è identificato da Identifier e Revision, che insieme costituiscono un identificativo logico univoco. Nel dettaglio materiale sono visibili informazioni di overview e proprietà tecniche/funzionali.

### 14.4.2 Proprietà materiali

Le proprietà del materiale sono alimentate e aggiornate da ERP tramite job. Le modifiche manuali non governate devono essere evitate, perché possono creare disallineamenti tra sistema master e MES.

### 14.4.3 Pagina Materials

Nel Back Office la pagina Materials consente di visualizzare l’elenco dei materiali, aprire il dettaglio, consultare l’overview, leggere identifier, revision, descrizione e proprietà associate.

## 14.5 Relazione tra oggetti configurativi

Il modello dati evidenziato nel training collega materiali, buffer, container type e MTU. Questa relazione è fondamentale perché configurazioni errate a monte possono generare problemi runtime apparentemente operativi.

| **Oggetto**    | **Ruolo nel MES**                                                                           |
| -------------- | ------------------------------------------------------------------------------------------- |
| Material       | Entità logica proveniente da ERP; base della tracciabilità e delle regole di consumo.       |
| Buffer         | Area logica di disponibilità materiale, associata ad area o work center.                    |
| Container Type | Definisce caratteristiche del contenitore e può essere associato ai materiali utilizzabili. |
| MTU            | Unità materiale reale tracciata, con batch, stato, quantità e posizione.                    |

## 14.6 Impatto sulla produzione

| **Configurazione errata**         | **Effetto possibile in produzione**                        |
| --------------------------------- | ---------------------------------------------------------- |
| Materiale non allineato da ERP    | Materiale non disponibile o non consumabile.               |
| Buffer mancante o non associato   | Materiale fisico presente ma non visibile in MES.          |
| Container Type errato o duplicato | Errori in selezione contenitore, movimentazione o consumo. |
| Proprietà materiale mancanti      | Errori su controlli, regole o validazioni runtime.         |

## 14.7 Ownership dei dati

| **Sistema**  | **Responsabilità**                                             |
| ------------ | -------------------------------------------------------------- |
| ERP/SAP      | Master data materiali e proprietà di origine.                  |
| MES          | Esecuzione, tracciabilità, stato materiale e gestione runtime. |
| Integrazione | Sincronizzazione dati fra ERP/SAP, MES e sistemi esterni.      |

## 14.8 Indicazioni Hypercare

  - Verificare se il materiale esiste e risulta correttamente sincronizzato.

  - Controllare identifier, revision e proprietà principali.

  - Verificare associazione a buffer e container type.

  - Distinguere errore di configurazione da errore operativo.

  - Evitare modifiche manuali non tracciate su anagrafiche e proprietà.

# 15\. Gestione Stock e Buffer

## 15.1 Buffer

Il buffer rappresenta l’area logica in cui il MES vede disponibilità materiale. Il corretto mapping tra buffer, area e work center è critico per consumo e proposta materiali.

## 15.2 Stock Available

Lo Stock Available è il messaggio/comando con cui viene resa nota al MES la disponibilità materiale su un buffer. Può essere usato per ingresso materiale, rimozione o trasferimento.

| **Scenario**        | **Source**  | **Destination** |
| ------------------- | ----------- | --------------- |
| Ingresso materiale  | Vuoto       | Valorizzato     |
| Rimozione materiale | Valorizzato | Vuoto           |
| Trasferimento       | Valorizzato | Valorizzato     |

# 16\. Assembly e Produzione

La gestione Assembly include First Assembly, Second Assembly, Assembly multifase e flusso teso. La disponibilità del complete e la distribuzione dei consumi dipendono dal tipo di ordine e dalla sequenza operativa.

  - First/Second Assembly: ordine monofase con consumo e complete nella stessa operazione.

  - Assembly multifase: materiali distribuiti tra più operazioni.

  - Flusso teso: disponibilità a fasi successive già allo start, con complete normalmente sulla fase finale.

# 17\. Heat Treatment / E-Treatment

Il trattamento termico/E-treatment prevede interazione con sistemi esterni e database di frontiera. Il forno processa l’handling unit e restituisce un esito OK/NOK che il MES utilizza nel flusso successivo.

  - Handling unit non visibile al forno.

  - Esito non riportato nel database di frontiera.

  - MES che non rileva esito trattamento.

  - Necessità di verifica tecnica su integrazione dati.

# 18\. Integrazione Sistemi Esterni

## 18.1 Architettura

La soluzione integra MES, SAP/EWM, CPI e Connect MOM. Connect MOM rappresenta il punto centrale di tracciamento dei messaggi verso sistemi esterni.

## 18.2 Messaggi principali

| **Messaggio**           | **Significato operativo**                                                   |
| ----------------------- | --------------------------------------------------------------------------- |
| Good Issue              | Consumo materiale o dichiarazione uscita/scrap.                             |
| Production Confirmation | Conferma avanzamento o consuntivazione.                                     |
| Good Receipt            | Ricezione prodotto finito/semifinito verso SAP, tipicamente in fase finale. |

## 18.3 Retry e Manual Import

In caso di errore comunicativo, Connect MOM può gestire retry automatici. In scenari specifici è possibile ricorrere a manual import per riprocessare messaggi generati ma non correttamente gestiti dal sistema esterno.

# 19\. AGV e Movimentazione Materiale

## 19.1 Concetti base

Nelle linee abilitate, il MES invia richieste al sistema AGV per movimentare container e materiali. Il MES genera richieste e riceve risposte/stati, ma non controlla direttamente il movimento fisico del mezzo.

## 19.2 Chiamate AGV

| **Chiamata**          | **Descrizione**                               |
| --------------------- | --------------------------------------------- |
| Call Empty            | Richiesta container vuoto.                    |
| Return Empty          | Restituzione container vuoto.                 |
| Call Alveolari        | Richiesta contenitore con alveolari/divisori. |
| Return Alveolari      | Restituzione alveolari/contenitori dedicati.  |
| Return Chip Container | Ritiro contenitore trucioli/by-product.       |

## 19.3 Baie, buffer e packaging material

La baia rappresenta una posizione fisica/logica di deposito o ritiro AGV. La configurazione associa baie, buffer e packaging material per consentire alla UI di proporre le opzioni corrette.

19B. AGV Runtime & Troubleshooting

19B.1 Scopo

Questa sezione integra le indicazioni emerse nella sessione KT “Brembo - KT su argomenti specifici” del 26 giugno 2026, con focus sulla gestione runtime delle chiamate AGV, sugli stati visualizzati in UI e sulle verifiche da eseguire quando una richiesta rimane bloccata.

19B.2 Modello stato AGV

Le chiamate AGV sono rappresentate in UI con un sistema di stati visivi. Lo stato deve essere interpretato prima di ripetere o forzare una richiesta, perché segnala in quale punto del flusso EWM/AGV la chiamata si trova.

| **Stato UI** | **Significato operativo**                                                       | **Azione raccomandata**                                                               |
| ------------ | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| Grigio       | La richiesta non è ancora arrivata o non risulta ancora presa in carico da EWM. | Attendere e verificare eventuale aggiornamento; se persiste, controllare Connect MOM. |
| Giallo       | La richiesta è stata presa in carico ma non è ancora stata completata.          | Monitorare; se rimane bloccata, seguire la procedura di troubleshooting AGV.          |
| Verde        | La chiamata risulta completata con esito positivo.                              | Nessuna azione correttiva richiesta.                                                  |
| Rosso        | La chiamata è andata in errore.                                                 | Analizzare Connect MOM, call ID e log correlati.                                      |

19B.3 Tipologie di chiamate AGV

Le chiamate richiamate nella KT confermano le tipologie già documentate nel manuale: Call Empty, Return Empty, Call Alveolari, Return Alveolari e Return Chip Container. Queste azioni sono associate al pulsante AGV disponibile sulle linee abilitate.

19B.4 Chiamata AGV bloccata

Una chiamata AGV può rimanere in attesa se non viene ricevuto un feedback da EWM o dal sistema AGV. In questa condizione l’operatore può non riuscire a inviare una nuova richiesta, perché la UI considera ancora aperta la richiesta precedente.

19B.5 Troubleshooting multilivello

| **Livello**                        | **Verifica**                                                                     | **Obiettivo**                                                                        |
| ---------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| L1 – UI                            | Verificare stato semaforo, baia selezionata, packaging/materiale e pulsante AGV. | Capire se il problema è visibile e riproducibile lato operatore.                     |
| L2 – Connect MOM                   | Filtrare i log per AGV movement e recuperare il contenuto della richiesta.       | Identificare request, payload e call ID.                                             |
| L3 – Tester Tool / comando tecnico | Usare il call ID per simulare/inviare una response tecnica quando appropriato.   | Sbloccare una chiamata rimasta pendente in modo governato.                           |
| L4 – Database                      | Verificare lo stato delle chiamate AGV, ordinando correttamente per timestamp.   | Confermare lo stato effettivo e distinguere aggiornamenti apparenti da eventi reali. |

19B.6 Informazioni minime da raccogliere

Plant e work center interessato.

Tipo chiamata AGV eseguita.

Baia selezionata e packaging/materiale associato.

Colore/stato del semaforo AGV.

Orario dell’evento.

Call ID recuperato da Connect MOM, se disponibile.

Evidenza screenshot o log correlati.

# 20\. Modello Hypercare e Go-Live

## 20.1 Obiettivi

L’Hypercare sostiene la produzione durante e dopo il go-live, riducendo rischio di fermo, perdita tracciabilità o disallineamento verso sistemi esterni.

## 20.2 Modello di supporto

Il modello consigliato prevede referente in plant, supporto remoto specializzato e war room con competenze su processo, backend, Mendix, Connect MOM, AGV, infrastruttura e dati.

| **Ruolo**           | **Responsabilità**                                                                         |
| ------------------- | ------------------------------------------------------------------------------------------ |
| Supporto in plant   | Raccoglie sintomo, interagisce con operatori e capo turno, applica workaround autorizzati. |
| War room remota     | Analizza log, DB, integrazioni e coordina fix.                                             |
| Capo turno          | Valida decisioni operative in assenza del business.                                        |
| Key User / Business | Valida decisioni con impatto su produzione o qualità.                                      |
| AMS / Sviluppo      | Gestisce bug, fix, deploy e procedure strutturate.                                         |

# 21\. Gestione Incidenti

## 21.1 Informazioni minime

  - Data e ora evento.

  - Plant, area, work center e linea.

  - Work Order / Operation.

  - Azione eseguita.

  - Messaggio UI o screenshot.

  - Impatto su produzione, qualità, integrazione o dati.

  - Workaround applicato e approvazione.

  - Owner follow-up.

## 21.2 Template

| **Campo**             | **Descrizione**                              |
| --------------------- | -------------------------------------------- |
| ID                    | Identificativo incidente/ticket.             |
| Sintomo               | Descrizione breve.                           |
| Impatto               | Produzione, qualità, dati, integrazione, UI. |
| Root cause ipotizzata | Causa probabile.                             |
| Verifiche             | UI, log, DB, Connect MOM, ETW.               |
| Workaround            | Azione temporanea.                           |
| Follow-up             | Fix definitiva o change.                     |

# 22\. Troubleshooting – Metodo Standard

15. Confermare sintomo con l’operatore.

16. Riprodurre l’azione se possibile.

17. Verificare ordine, operazione, quantità, quality inspection e work center.

18. Distinguere problema UI/refresh da problema dati/backend.

19. Consultare Persistent Log e correlation ID.

20. Usare ETW se serve diagnosi runtime.

21. Verificare Connect MOM per integrazioni.

22. Verificare configurazioni Back Office: materiale, proprietà, buffer, container type.

23. Verificare DB solo con query selettive.

24. Applicare workaround approvato e documentare.

# 23\. Troubleshooting Operatore – Light

## 23.1 Scopo

Questa sezione è pensata per supportare l’operatore o il supervisore nella prima lettura del problema, prima dell’escalation tecnica. Non sostituisce il troubleshooting AMS, ma aiuta a classificare correttamente il sintomo.

| **Sintomo percepito**                 | **Possibile causa**                                                                                               | **Prima azione consigliata**                                                      |
| ------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Non vedo il materiale                 | Stock non disponibile, buffer errato, refresh non aggiornato, materiale non sincronizzato.                        | Eseguire refresh; verificare con supervisore se materiale e buffer sono corretti. |
| Non posso completare                  | Materiali mancanti, quality inspection pendente, interlocking check, tipo ordine non completabile in quella fase. | Verificare indicatori UI, consumi, controlli qualità e messaggi di blocco.        |
| Dati non aggiornati                   | UI non sincronizzata o aggiornamento lento.                                                                       | Attendere/refresh; se il problema persiste, segnalare.                            |
| Icone ancora presenti                 | Azioni non completate o condizioni residue.                                                                       | Rivedere lo step indicato dall’icona o chiedere supporto al supervisore.          |
| Indicatore non verde                  | Condizione funzionale non soddisfatta.                                                                            | Verificare il materiale, il controllo o l’azione associata.                       |
| Complete non visibile nel flusso teso | Comportamento previsto per alcune prime fasi di ordini Z003/flusso teso.                                          | Verificare il tipo ordine prima di aprire un incident.                            |

## 23.2 Regola di escalation

Se dopo refresh, verifica dei materiali, controlli qualità e riesame degli indicatori UI il problema persiste, l’anomalia deve essere escalata al supervisore o al team Hypercare, fornendo screenshot, work center, ordine, ora dell’evento e operazione eseguita.

# 24\. Logging e Diagnostica

## 24.1 Persistent Log

Il Persistent Log è la fonte principale per analisi post-evento. È utile filtrare per plant, timeframe e correlation ID, ricostruendo la sequenza dell’azione dal primo errore significativo.

## 24.2 ETW

ETW supporta la diagnosi live. Deve essere usato con plant corretto, runtime all nodes e provider rilevanti per backend/Mendix quando il problema non è chiaribile tramite log persistenti.

## 24.3 Connect MOM

Connect MOM va consultato in presenza di problemi SAP/EWM/CPI, stock available, Good Issue, Good Receipt, Production Confirmation, AGV e altri messaggi esterni.

# 25\. Troubleshooting per Caso d’Uso

## Materiale fisico presente ma non visibile

Verificare stock available, buffer, MTU status, Connect MOM e configurazione materiale-buffer-container type.

## Complete fallito

Controllare materiali consumati, quality inspection, interlocking check, quantità e log dell’azione.

## Interlocking check

Verificare il check scattato e se il blocco è funzionalmente corretto.

## Soft material non proposto

Verificare query MTU-buffer, equipment ID, parent area, proprietà materiale e mapping buffer.

## Original batch mancante

Risalire alla genealogia e validare il batch origine.

## Container type duplicato

Verificare dati master, identifier, name, associazioni materiali e possibili duplicazioni da WM/ERP.

## AGV call grigia

Controllare AGV movement history, Connect MOM, ACK/reply e configurazione baie-buffer-packaging material.

## UI non aggiornata

Provare refresh; se backend coerente, classificare come problema UI/refresh.

# 26\. Workaround Operativi

## 26.1 Principi

  - Ogni workaround deve essere proporzionato all’impatto produttivo.

  - Le modifiche DB devono essere ultima opzione e sempre tracciate.

  - Prima di UPDATE eseguire SELECT con stesso filtro.

  - Evitare modifiche massive; usare WHERE puntuali.

  - Documentare prima/dopo, approvazione e motivazione.

## 26.2 Standard vs eccezione

Le procedure standard devono restare separate dai workaround. Un workaround applicato in Hypercare non deve essere documentato come comportamento ordinario salvo validazione formale.

26B. Workaround Operativi AGV

26B.1 Principio generale

I workaround AGV devono essere considerati interventi controllati. Devono essere usati solo quando il processo è bloccato o la produzione richiede uno sblocco immediato, e devono essere tracciati nel registro incidenti con evidenza di causa, azione e validazione ricevuta.

26B.2 Workaround tecnico raccomandato

Il metodo preferibile consiste nel recuperare la chiamata AGV da Connect MOM, identificare il call ID e utilizzare lo strumento tecnico previsto per inviare o simulare una response coerente. Questo approccio mantiene il sistema più pulito e consente una tracciabilità migliore rispetto a un intervento manuale sulla UI.

26B.3 Workaround di emergenza UI

Nella KT è stato mostrato anche un workaround di emergenza basato sulla riabilitazione del pulsante di invio dalla UI tramite strumenti del browser. Questa modalità deve essere classificata come eccezionale, non standard, e non deve essere adottata come procedura ordinaria.

| **Workaround**                      | **Quando considerarlo**                                                                | **Rischio**                                                | **Governance richiesta**                                     |
| ----------------------------------- | -------------------------------------------------------------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------ |
| Connect MOM + call ID + tester tool | Quando c’è tempo per eseguire una verifica tecnica e si vuole mantenere tracciabilità. | Medio-basso se eseguito da personale autorizzato.          | Richiede accesso tecnico e registrazione dell’intervento.    |
| Riabilitazione manuale pulsante UI  | Solo in emergenza operativa e con pressione immediata sulla linea.                     | Alto: può mascherare stato pendente o duplicare richieste. | Da usare solo con autorizzazione e documentazione esplicita. |

26B.4 Regola di documentazione

Registrare orario, work center, tipo chiamata e stato UI prima dell’intervento.

Registrare call ID e riferimento Connect MOM se presente.

Documentare il workaround applicato e chi lo ha autorizzato.

Aprire follow-up tecnico se la causa non è stata risolta definitivamente.

# 27\. Governance e Best Practice

## 27.1 Release e deploy

Ogni pacchetto deve essere archiviato con naming chiaro, evidenza di build e data di deploy. Le azioni sugli ambienti devono essere tracciate in un change log condiviso.

## 27.2 Governance dati

Le configurazioni Back Office e i dati master devono essere gestiti con ownership chiara. Le modifiche manuali a materiali, proprietà, buffer e container type devono essere evitate o documentate come interventi controllati.

## 27.3 Governance contenuti training

Le informazioni provenienti da sessioni training devono essere classificate come confermate, contestuali, arricchimenti o da validare. I contenuti semplificati per operatori non devono sostituire le regole tecniche senza validazione funzionale.

# 28\. Appendici

## 28.1 Glossario

| **Termine**          | **Definizione**                                                             |
| -------------------- | --------------------------------------------------------------------------- |
| Work Order           | Ordine di produzione gestito dal MES.                                       |
| Work Order Operation | Operazione dell’ordine associata a work center.                             |
| Repetitive UI        | Interfaccia operativa dell’operatore di linea.                              |
| Back Office Light    | Funzioni di consultazione/supervisione a supporto della linea.              |
| Material             | Anagrafica materiale proveniente da ERP/SAP.                                |
| Identifier           | Codice identificativo del materiale.                                        |
| Revision             | Revisione del materiale; insieme all’identifier compone l’univocità logica. |
| Buffer               | Area logica di disponibilità materiale.                                     |
| Container Type       | Tipo contenitore utilizzato per movimentazione/consumo.                     |
| MTU                  | Material Tracking Unit, unità materiale tracciata.                          |
| MTU Aggregate        | Aggregatore/container di MTU.                                               |
| Native Batch         | Batch associato all’ordine o fase.                                          |
| Original Batch       | Batch origine colata propagato lungo il processo.                           |
| Stock Available      | Messaggio/comando di disponibilità stock.                                   |
| Connect MOM          | Componente di integrazione e logging messaggi.                              |
| ETW                  | Event Tracing for Windows per diagnostica runtime.                          |
| Persistent Log       | Log persistente usato per analisi post-evento.                              |
| AGV                  | Sistema di movimentazione automatica materiale/container.                   |

## 28.2 Checklist Operatore

  - Verificare di essere sul work center corretto.

  - Selezionare il Work Order corretto.

  - Eseguire Start solo quando il contesto è corretto.

  - Consumare tutti i materiali richiesti.

  - Verificare che gli indicatori siano coerenti e, se necessario, aggiornare la pagina.

  - Completare solo quando il sistema abilita il comando Complete.

  - Segnalare anomalie persistenti con screenshot e dettaglio ordine/work center.

## 28.3 Checklist Go-Live

  - Matrice competenze aggiornata.

  - Copertura turni confermata.

  - War room remota definita.

  - Accessi a UI, Back Office, log, DB e Connect MOM verificati.

  - Configurazioni materiali-buffer-container type validate.

  - Procedure AGV e baie disponibili.

  - Incident log e change log attivi.

## 28.4 Checklist Hypercare

  - Raccogliere screenshot e orario esatto.

  - Verificare riproducibilità.

  - Usare correlation ID se disponibile.

  - Controllare configurazione Back Office quando il problema riguarda materiale/buffer/container.

  - Consultare Connect MOM per integrazioni.

  - Usare ETW se necessario.

  - Non eseguire fix DB senza approvazione e filtro puntuale.
