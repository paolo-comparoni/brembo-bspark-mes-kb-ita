# Storyboard Training Operativo di Quality v3 (Curno)

> Documento sorgente: `E:\BremboDocs\SlideTrainingItalia\Storyboard Training Operativo di Quality v3 (Curno).docx`  
> Tipo: Word (.docx)

| **<span class="smallcaps">JOURNEY</span>** | **\#**                        |
| ------------------------------------------ | ----------------------------- |
| **<span class="smallcaps">AUTORE</span>**  | Paolo Comparoni (Engineering) |
| **<span class="smallcaps">AUTORE</span>**  | Emanuele Merlo (Engineering)  |
|                                            |                               |

[**1. INFORMAZIONI DOCUMENTO 3**](#informazioni-documento)

> [1.1 STORICO REVISIONI 3](#storico-revisioni)
> 
> [1.2 DOCUMENTI COLLEGATI 3](#documenti-collegati)

[**2. INTRODUZIONE AL TRAINING E CASI GUIDA 4**](#introduzione-al-training-e-casi-guida)

> [2.1 Introduzione al training e casi guida 4](#introduzione-al-training-e-casi-guida-1)
> 
> [2.2 Casi di Studio e Dati di Training 4](#casi-di-studio-e-dati-di-training)
> 
> [2.3 Confronto As-Is vs To-Be: L'evoluzione del Day-by-Day 6](#confronto-as-is-vs-to-be-levoluzione-del-day-by-day)

[**3. IL RISULTATO FINALE: REPORTISTICA EXTRA-SISTEMA (POWER BI) 10**](#il-risultato-finale-reportistica-extra-sistema-power-bi)

> [3.1 Navigazione Dati di Base (BOM & Routing Data Model) 10](#navigazione-dati-di-base-bom-routing-data-model)
> 
> [3.2 Genealogia Globale (Il Polpo) 10](#genealogia-globale)
> 
> [3.3 Analisi degli Scarti (Scrap Report) 10](#analisi-degli-scarti-scrap-report)
> 
> [3.4 Risultati delle Quality Inspection 10](#risultati-delle-quality-inspection)
> 
> [3.5 Monitoraggio Non-Conformances (NC) 10](#monitoraggio-non-conformances-nc)
> 
> [3.6 Situazione Logistica (Stock Report) 10](#situazione-logistica-stock-report)
> 
> [3.7 Production Report KPI 10](#production-report-kpi)

[**4. FLUSSO OPERATIVO DELL'UTENTE (OPCENTER MES) 11**](#flusso-operativo-dellutente-opcenter-mes)

> [4.1 Punto 1: Accesso al sistema, identificazione del contesto operativo e riconoscimento del Work Order 11](#punto-1-accesso-al-sistema-identificazione-del-contesto-operativo-e-riconoscimento-del-work-order)
> 
> [4.2 Punto 2: Visione operativa di documenti e controlli qualità 11](#punto-2-visione-operativa-di-documenti-e-controlli-qualità)
> 
> [4.3 Punto 3: Avvio dell'Ordine e Tracciabilità 12](#punto-3-avvio-dellordine-e-tracciabilità)
> 
> [4.4 Punto 4: Dichiarazione dei Consumi (Input Materiale) 13](#punto-4-dichiarazione-dei-consumi-input-materiale)
> 
> [4.5 Punto 5: Non Conformance Pezzo in Ingresso 14](#punto-5-non-conformance-pezzo-in-ingresso)
> 
> [4.6 Punto 6: Esecuzione delle Ispezioni e Blocco Funzionale 15](#punto-6-esecuzione-delle-ispezioni-e-blocco-funzionale)
> 
> [4.7 Punto 7: Non Conformance Pezzo in Uscita 16](#punto-7-non-conformance-pezzo-in-uscita)
> 
> [4.8 Punto 8: Decisione del Supervisore (Sentencing) e Integrazione SAP 17](#punto-8-decisione-del-supervisore-sentencing-e-integrazione-sap)
> 
> [4.9 Punto 9: Chiusura dell'Attività e Verifica Genealogia 20](#punto-9-chiusura-dellattività-e-verifica-genealogia)

[**5. CONFIGURAZIONE DI SISTEMA (ENGINEERING) 22**](#)

> [5.1 Punto 10: Master Data (Characteristics, Inspection Definition, Documents) 22](#punto-10-master-data-characteristics-inspection-definition-documents)
> 
> [5.2 Punto 11: Arricchimento (Enrichment) 23](#punto-11-arricchimento-enrichment)

[**6. Appendice: Modifica della Lingua di Sistema 25**](#appendice-modifica-della-lingua-di-sistema)

1.  # INFORMAZIONI DOCUMENTO
    
    1.  ## STORICO REVISIONI

<table>
<thead>
<tr class="header">
<th><span class="smallcaps">VERSIONE</span></th>
<th><span class="smallcaps">DESCRIZIONE MODIFICA</span></th>
<th><span class="smallcaps">AUTORE</span></th>
<th><span class="smallcaps">DATA</span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.0</td>
<td>Prima stesura</td>
<td><p>Paolo Comparoni</p>
<p>Emanuele Merlo</p></td>
<td>14-APR-2026</td>
</tr>
<tr class="even">
<td>2.0</td>
<td>Riorganizzazione conservativa della storyboard sulla base della revisione contenuti e pre-requisiti formativi</td>
<td>Paolo Comparoni; Emanuele Merlo</td>
<td>[TO BE CONFIRMED]</td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## DOCUMENTI COLLEGATI

| <span class="smallcaps">LINK</span> | <span class="smallcaps">COMMENTO</span> |
| ----------------------------------- | --------------------------------------- |
|                                     |                                         |
|                                     |                                         |

2.  # INTRODUZIONE AL TRAINING E CASI GUIDA
    
    1.  ## Introduzione al training e casi guida

Il programma di training è focalizzato sulle attività operative quotidiane. Il percorso formativo adotta un approccio dal basso verso l'alto: parte dalle interazioni quotidiane dell'utente con il sistema MES, per poi trattare le attività di back-office e le configurazioni che abilitano controlli, documenti e comportamenti di qualità. I casi studio presentati rappresentano i processi reali attivi nei due plant.

## Casi di Studio e Dati di Training

I casi di studio selezionati illustrano le dinamiche operative più frequenti riscontrate nei plant. Ogni esempio si basa su scenari reali e copre la gestione end-to-end del processo di qualità: dall'identificazione dell'ordine e delle specifiche tecniche, alla gestione delle non conformità, fino al sentencing e alla chiusura del flusso documentale. Tali esempi fungono da guida per l'applicazione pratica delle procedure descritte nei capitoli seguenti.

**Esempio 1: Machining (Washing)**

  - > **Work Center:** SWHPM01M (HIGH PRESSURE WASHING MACHINE)

  - > **Operazione:** LAVAGGIO ALTA PRESSIONE

  - > **Materiali e BOP associati:**
    
      - > 20D17837\_WSH (CORPO PINZA LAVORATO) -\> BOP 30229528 (WO di riferimento: 1131047)
    
      - > 20D17838\_WSH (CORPO PINZA LAVORATO) -\> BOP 30229531 (WO di riferimento: 1131320)

**Esempio 2: Assembly (Seconda Fase)**

  - > **Work Center:** SACSA012 (MONOBLOCCO 12 SECOND ASSEMBLY)

  - > **Operazione:** COLLAUDO + COMPLETAMENTO

  - > **Materiali e BOP associati:**
    
      - > **Pinze SX:**
        
          - > 20E63341 (PINZA M6.28/32/36 SX) -\> BOP 30235294 (WO: 1131063)
        
          - > 20E63345 (PINZA M6.28/32/36 SX) -\> BOP 30235298 (WO: 1131218)
        
          - > 20E63347 (PINZA M6.28/32/36 SX) -\> BOP 30235300 (WO: 1131208)
    
      - > **Pinze DX:**
        
          - > 20E63342 (PINZA M6.28/32/36 DX) -\> BOP 30235295 (WO: 1131240)
        
          - > 20E63344 (PINZA M6.28/32/36 DX) -\> BOP 30235297 (WO: 1131212)

**Esempio 3: Friction / Pads (Rettifica)**

  - > **Gruppo 1: Ordini MHT (Molding & Heat Treatment)**
    
      - > **Work Center:** FMPGM01M (GRINDING COMEC GROUP)
    
      - > **Operazione:** RETTIFICA (Fase intermedia del ciclo: Stampaggio -\> Rettifica -\> Forno Statico)
    
      - > **Materiali e BOP associati:**
        
          - > 47D66964VE\_MHT (PASTIGLIA VERNICIATA) -\> BOP 40010793 (WO: 1131127, 1131136)
        
          - > 47D66965VE\_MHT (PASTIGLIA VERNICIATA) -\> BOP 40010796 (WO: 1131131, 1131180)

  - > **Gruppo 2: Ordini SBP (Shot Blasting & Painting)**
    
      - > **Work Center:** FMPGM01M (GRINDING COMEC GROUP)
    
      - > **Operazione:** RETTIFICA PARALLELISMO (Fase intermedia del ciclo: Pallinatura -\> Rettifica -\> Verniciatura)
    
      - > **Materiali e BOP associati:**
        
          - > 47D66964VE\_SBP (PASTIGLIA VERNICIATA) -\> BOP 40010794 (WO: 1131036, 1131037, 1131152, 1131165)
        
          - > 47D66965VE\_SBP (PASTIGLIA VERNICIATA) -\> BOP 40010797 (WO: 1131014, 1131017, 1131154, 1131167)

##   

## Confronto As-Is vs To-Be: L'evoluzione del Day-by-Day

La logica di base del lavoro in linea non cambia: le informazioni essenziali (ordine, articolo, intestazioni) rimangono le stesse. Ciò che cambia radicalmente è il livello di sicurezza del processo (Poka-Yoke) e l'interattività dell'interfaccia, che ora guida l'operatore passo dopo passo. Di seguito il confronto tra l'attuale sistema Microsoft AX e la nuova Repetitive UI di Opcenter MES per le attività quotidiane.

**A. Lancio dell'Ordine ed Esecuzione dei Controlli di Qualità**

**AS-IS (Microsoft AX):** Oggi l'operatore visualizza una griglia testuale in Avanzamento di Fabbrica. Per registrare i controlli, deve ricordarsi fisicamente di cliccare sul pulsante "Dati Qualità per CDI" e inserire i risultati in una tabella.

**TO-BE (Opcenter Repetitive UI):** Il controllo qualità diventa un "task ineludibile". Quando l'operatore lancia l'ordine, il sistema fa comparire un'icona arancione a forma di aeroplanino (Show Quality) se ci sono test obbligatori (es. frequenza 100% a inizio turno).

_[immagine]_

**Figura A.1: Interfaccia Microsoft AX – Visualizzazione della griglia operativa con evidenza del comando "Modifica Dati di Qualità" per l'inserimento manuale dei dati.**

> _[immagine]_

**Figura A.2: Interfaccia Opcenter Repetitive UI – Visualizzazione del Work Order con attivazione del task "Show Quality" (icona arancione) per i controlli obbligatori.**

**La registrazione dei risultati (Il Blocco Poka-Yoke):** Nel nuovo "Quality Inspection Panel", l'operatore inserisce il valore misurato (es. altezza taglio o spessore pastiglia). A differenza di AX, il MES fornisce un feedback visivo immediato: barra VERDE se a disegno/conforme, barra ROSSA se fuori tolleranza. Soprattutto, finché l'ispezione non viene eseguita e validata, il MES disabilita (blocca) fisicamente i tasti "Complete" e "Partial Complete", impedendo di dichiarare la produzione o far avanzare il pezzo.

**B. Dichiarazione delle Difettosità e degli Scarti**

**AS-IS (Microsoft AX):** La dichiarazione dello scarto è legata alle registrazioni di consumo, con logiche che a volte possono generare errori nei giornali di magazzino se non si presta attenzione (es. consumi FIFO vs LIFO).

**TO-BE (Opcenter Repetitive UI):** L'operatore dispone di un pannello visivo dedicato (Defect Declaration Panel). Cliccando sul tasto "Defect", si apre una griglia con icone (coni di segnalazione) che mostrano chiaramente le causali di scarto applicabili a quel Work Center.

_[immagine]_

**Figura B.1: Interfaccia Microsoft AX – Procedura attuale per la dichiarazione degli scarti in produzione.**

_[immagine]_

**Figura B.2: Interfaccia Opcenter Repetitive UI – Defect Declaration Panel con icone grafiche per la selezione guidata delle causali di scarto.**

**C. Gestione Documentale Integrata**

Oggi l'operatore deve cercare i disegni tecnici, i RPF o i PDF separatamente su LinkerSys o cartelle di rete (MPM).

Con Opcenter, la documentazione è "in contesto": basta cliccare il tasto "Documents" a destra nello schermo e il sistema apre automaticamente la visualizzazione dei PDF, RPF e disegni legati esclusivamente a quell'ordine, a quella macchina o a quell'articolo.  
  
_[immagine]_

**Figura C.1: Interfaccia Opcenter Repetitive UI – Pannello "Linked Documents" con visualizzazione contestuale dei documenti tecnici associati al Work Order.**

# IL RISULTATO FINALE: REPORTISTICA EXTRA-SISTEMA (POWER BI)

In ottica puramente operativa, il flusso parte dalla visualizzazione del risultato finale. Le azioni compiute dagli operatori nel MES vanno ad alimentare direttamente i cruscotti aziendali su Power BI (aggiornati in modalità pseudo real-time). La consultazione di questi report è la procedura standard raccomandata per by-passare i limiti di navigazione dell'interfaccia base di Siemens e per avere il quadro completo della produzione e della qualità. Gli utilizzi principali di Power BI per il team Qualità e i Supervisori si dividono in:

## 3.1 Navigazione Dati di Base (BOM & Routing Data Model)

Permette di filtrare e navigare in modo intuitivo tra Ordini di Produzione, Materiali, Cicli di Lavoro (BOP) e Work Center, offrendo una panoramica immediata delle anagrafiche e del carico di lavoro.

_[immagine]_

## 3.2 Genealogia Globale

Strumento per la tracciabilità profonda. Consente di partire da un lotto scartato e ricostruire retrospettivamente l'intera storia produttiva, o di tracciare in avanti il destino dei pezzi di una colata.

_[immagine]_

## 3.3 Analisi degli Scarti (Scrap Report)

Cruscotti dedicati all'interrogazione delle Non Conformità definitive per materiale, Work Center, periodo e singolo collo (Handling Unit Poly).

_[immagine]_

## 3.4 Risultati delle Quality Inspection

Estrazione tabulare di tutti i test qualitativi eseguiti, essenziale per consultare rapidamente le note inserite dagli operatori a bordo macchina (es. anomalie su singole cavità).

_[immagine]_

## 3.5 Monitoraggio Non-Conformances (NC)

Lista completa delle anomalie aperte, in lavorazione o chiuse tramite Sentencing.

## 3.6 Situazione Logistica (Stock Report)

Accesso in sola lettura allo stato delle giacenze nei buffer di linea e allo storico dei movimenti di magazzino.

## 3.7 Production Report KPI

Valutazione degli indicatori di performance e del valore economico degli scarti (Scrap Value).

Una volta compreso il risultato atteso su questi cruscotti, il capitolo seguente illustra le esatte procedure a sistema (Opcenter MES) necessarie per generare tali dati in linea.

4.  # FLUSSO OPERATIVO DELL'UTENTE (OPCENTER MES)
    
    1.  ## Punto 1: Accesso al sistema, identificazione del contesto operativo e riconoscimento del Work Order

Effettuare l'accesso al sistema tramite la Repetitive UI, previa selezione del Work Center di competenza tramite l'icona aeroplanino. Identificare il plant, il Work Center, il Work Order, le quantità associate e la presenza di controlli qualità e documenti. Verificare lo stato dell'ordine attraverso i parametri di quantità (da avviare, in lavorazione, completati). L'icona 'Show Quality' e il pannello 'Documents' confermano l'associazione di piani di ispezione e documentazione tecnica al Work Order.

_[immagine]_

*Figura 1: Repetitive senza controlli di qualità*

## Punto 2: Visione operativa di documenti e controlli qualità

L'interfaccia di sistema si aggiorna dinamicamente in base alla configurazione del Work Order. In presenza di controlli qualità configurati, l'icona 'Show Quality' è evidenziata in arancione. Consultare la documentazione disponibile nel pannello di destra (Right Zone) e verificare l'impatto dei controlli di qualità sul completamento dell'attività operativa.

_[immagine]_

*Figura 2: Repetitive con controlli di quality e documentazione caricata*

## Punto 3: Avvio dell'Ordine e Tracciabilità

Il Work Order costituisce l'elemento centrale del flusso, collegando: materiali in ingresso, attività svolta, controlli eseguiti, eventuali non conformità, dichiarazioni di produzione e genealogia finale. Avviare l'ordine tramite il comando 'Start' inserendo la quantità di pezzi da lavorare.

_[immagine]_

*Figura 3: Avvio dell'ordine di lavorazione*

## Punto 4: Dichiarazione dei Consumi (Input Materiale)

L’operatore registra l’ingresso fisico dei componenti o del materiale di processo tramite scansione del barcode del contenitore o tramite selezione dell’unità materiale prevista dal flusso.

Questa azione scala automaticamente la quantità dal buffer o dallo stock intermedio e collega il materiale in ingresso all’ordine di lavorazione.

Per semplificare l’esercitazione ed evitare di ripercorrere i passaggi dei processi precedenti, l’unità di carico può essere creata manualmente nel sistema, assicurando la disponibilità immediata del materiale da consumare durante il training.

> _[immagine]_

*Figura 4: Materiale in pre-macchina*

> _[immagine]_

*Figura 5: Consumo materiali cassone*

La dichiarazione dei consumi è un punto fondamentale perché costruisce il legame tra esecuzione, genealogia e qualità del dato. L’utente deve comprendere che l’informazione di input materiale non è solo tecnica, ma determina la tracciabilità successiva dell’ordine.

## Punto 5: Non Conformance Pezzo in Ingresso

Per registrare materiale difettoso in ingresso, accedere al pannello 'Defect Declaration'. Selezionare la quantità da scartare o porre in quarantena dal contenitore di provenienza e associare la causale tecnica rilevata. Il sistema gestisce automaticamente la creazione del contenitore di scarto, la stampa dell'etichetta di reso, l'invio dei messaggi a SAP e l'aggiornamento automatico delle quantità buone.

_[immagine]_

*Figura 6: Non conformità di un pezzo in ingresso*

> _[immagine]_

*Figura 7: Identificatore dello scarto in entrata*

## Punto 6: Esecuzione delle Ispezioni e Blocco Funzionale

Le ispezioni obbligatorie (100% o inizio turno/ordine) attivano un blocco funzionale: i tasti 'Complete' e 'Partial Complete' risultano inibiti fino alla validazione dei test. La procedura distingue tra controlli attributivi (OK/NOK) e variabili (valori numerici con tolleranze). Utilizzare il 'Quality Inspection Panel' per inserire i valori reali e ricevere feedback visivo immediato (barra verde/rossa). I risultati sono salvati e consultabili nello storico dell'ordine.

> _[immagine]_

*Figura 8: Inserimento controlli risultati ispezioni di qualità*

## Punto 7: Non Conformance Pezzo in Uscita

Segnalare i difetti sul prodotto finale tramite il pulsante 'Defect Declaration', selezionando la causale tecnica e la quantità interessata. Lo stato 'Candidate' (Quarantena) sospende l'unità materiale (MTU), ne impedisce l'avanzamento alle fasi successive e genera una segnalazione di Non-Conformità tracciabile nel sistema.

_[immagine]_

*Figura 9: Dichiarazione quarantena pezzo prodotto*

_[immagine]_

*Figura 10: Identificativo cassone coi pezzi in quarantena*

## Punto 8: Decisione del Supervisore (Sentencing) e Integrazione SAP

Il Supervisore analizza le Non Conformità (NC) aperte dal terminale operatore e conclude il ciclo della qualità tramite il processo di Sentencing. Questa azione definisce il destino finale del materiale momentaneamente sospeso a sistema. Ogni volta che viene eseguito un Sentencing su materiale in quarantena, Opcenter MES genera automaticamente un messaggio in uscita (Outbound Message) verso SAP ERP, tecnicamente chiamato 'Good Movement'. Questo messaggio informa l'ERP su dove spostare contabilmente il materiale, garantendo l'allineamento tra la giacenza a sistema e la realtà fisica.

L'interfaccia di Sentencing presenta i seguenti stati applicabili:

  - > **Quarantine (current):** Stato Operativo: È lo stato di partenza in attesa di giudizio. L'unità (MTU) è bloccata e isolata dal flusso produttivo; il sistema impedisce l'avanzamento di quel contenitore. Non sono ancora stati inviati messaggi di risoluzione logistica a SAP.

  - > **CLOSE AND RETURN TO WORK (Buono):** Stato Operativo: Il materiale è stato giudicato idoneo (es. falso allarme, difetto rientrato o deroga) e deve rientrare immediatamente nel flusso della produzione. Impatto Tecnico/SAP: Il MES invia a SAP un messaggio di Good Movement che sposta contabilmente il materiale dal magazzino 'Quarantena' al magazzino 'Buono'. L'unità viene sbloccata in Opcenter, non vi è alcun impatto negativo sui KPI di linea e il Work Order può avanzare normalmente.

  - > **SCRAP (Scarto Interno Definitivo):** Stato Operativo: Il pezzo è irrecuperabile a causa di un difetto generato internamente e viene scartato definitivamente. Il contenitore verrà fisicamente spostato nella baia scarti. Impatto Tecnico/SAP: Viene inviato a SAP un Good Movement che sposta la quantità verso l'area 'Scrap'. SAP aggiorna il registro scarti e riduce definitivamente la quantità producibile per quell'ordine, alimentando automaticamente il KPI 'Scrap Rate'.

  - > **BREMBOREWORK (Rilavorazione Interna):** Stato Operativo: Il pezzo richiede una riparazione fisica all'interno dello stabilimento. Impatto Tecnico/SAP: Il supervisore chiude la NC indicando un codice di rework e selezionando uno specifico ciclo di rilavorazione (BoP). Opcenter genera dinamicamente un nuovo ordine di lavoro dedicato al rework, separato da quello originale. SAP riceve il movimento logistico verso l'area Rework e registra i costi aggiuntivi. Al termine della rilavorazione, la quantità viene reintrodotta nel Work Order di origine per proseguire il ciclo.

  - > **EXTERNAL REWORK (Rilavorazione Esterna / Conto Lavoro):** Stato Operativo: La riparazione del pezzo non può essere fatta internamente ma richiede l'invio a un fornitore esterno (es. per attività di carteggiatura o verniciatura di terzi). Impatto Tecnico/SAP: Il supervisore seleziona la voce nel MES, dopodiché la logistica lancerà in SAP un ordine di conto lavoro verso il fornitore esterno per gestire formalmente l'uscita del materiale, la lavorazione e il cambio codice al rientro in stabilimento.

  - > **EXTERNAL SCRAP (Scarto per Causa Esterna):** Stato Operativo: Il pezzo viene scartato, ma la non conformità è imputabile inequivocabilmente a un processo o a un fornitore esterno (es. difetto rilevato da controllo ai Raggi X post-lavorazione). Impatto Tecnico/SAP: Il materiale in Quarantena viene scartato, ma la separazione della causale permette di isolare la responsabilità e gestire correttamente il flusso di reso verso il fornitore, senza gravare sui KPI di scarto della produzione interna.

_[immagine]_

*Figura 11: Sentencing "Close and Return to Work"*

_[immagine]_

*Figura 12: Dichiarazione produzione*

## Punto 9: Chiusura dell'Attività e Verifica Genealogia

Al termine del processo, consultare la pagina 'As Built Order' per il registro storico completo dell'ordine. Tale sezione correla indissolubilmente: lotti consumati, risultati delle ispezioni, dichiarazioni di difetto, decisioni di sentencing, quantità prodotte e quantità scartate.

_[immagine]_

*Figura 13: Dichiarazione produzione (Conferma)*

_[immagine]_

*Figura 14: Tracciamento ispezioni di qualità*

_[immagine]_

*Figura 15: Tracciamento non conformità*

5.  # CONFIGURAZIONE DI SISTEMA (ENGINEERING)
    
    1.  ## Punto 10: Master Data (Characteristics, Inspection Definition, Documents)

La gestione dei dati anagrafici e delle configurazioni avviene in Back-Office (Basic UI) e si articola sulla definizione di Characteristics, Inspection Definition e Documents. Le caratteristiche (Attributive, Variabili, Visuali) sono collegate alle ispezioni, che definiscono le modalità di verifica operativa. Il sistema adotta il principio dell'ereditarietà: i parametri configurati nel Routing (BOP) vengono trasferiti nativamente ai Work Order al momento del download da SAP, rendendo i controlli immediatamente disponibili sul terminale operatore. La pagina 'Documents' funge da anagrafica centrale per file tecnici, disegni e istruzioni operative, integrando versioning e categorizzazione.

_[immagine]_

*Figura 16: Ispezioni di qualità*

_[immagine]_

*Figura 17: Impostazione tolleranza e valore nominale per il prodotto*

_[immagine]_

*Figura 18: Anagrafica Documenti*

## Punto 11: Arricchimento (Enrichment)

L’attività di arricchimento qualitativo avviene primariamente a livello di **Routing (BOP)**, dove lo scheletro del processo ricevuto da **SAP** viene integrato con i parametri tecnici e di qualità necessari all’esecuzione nel MES.

_[immagine]_

*Figura 19: Inserimento dei controlli di qualità nel routing*

Il sistema adotta il principio dell’**ereditarietà (Inheritance)**: al caricamento di una nuova versione di Routing, il MES tenta il merge automatico copiando i piani di controllo e i documenti dalla versione precedente.

In caso di incompatibilità strutturale tra versioni del Routing, ad esempio una variazione nel numero di operazioni, il processo di eredità automatica può non essere sufficiente e richiedere un intervento manuale di allineamento.

I Work Order ereditano nativamente tali configurazioni dal Routing di riferimento al momento del download da SAP, rendendo i controlli immediatamente disponibili sul terminale operatore.

L’arricchimento manuale della BOP tramite l’interfaccia **Basic UI** è un’operazione straordinaria e limitata alla configurazione di nuovi prodotti o a revisioni tecniche che comportano variazioni significative.

Qualora un ordine sia già stato importato da SAP privo di ispezioni, è possibile intervenire eccezionalmente sul singolo ordine tramite la pagina **Work Order Operation Detail**.

_[immagine]_

*Figura 20: Collegamento a documento esistente*

_[immagine]_

*Figura 21: Aggiunta delle quality inspection al Work Order*

Il salvataggio delle configurazioni abilita l’aggiornamento automatico del terminale operatore, dove l’ordine mostrerà:

  - > presenza di controlli qualità

  - > eventuale documentazione associata

  - > nuova esperienza utente coerente con quanto mostrato nella prima parte del training

Il corretto salvataggio delle configurazioni garantisce l'allineamento dei dati tra il sistema di Back-Office e l'interfaccia di produzione (Repetitive UI), rendendo disponibili le informazioni tecniche e i controlli qualità all'operatore di linea.

# Appendice: Modifica della Lingua di Sistema

Opcenter MES è un sistema nativamente multi-lingua, che consente di personalizzare la lingua di visualizzazione dell'interfaccia.

**Nota:** Per gli operatori impegnati sulle linee di produzione, l'interfaccia deve obbligatoriamente rimanere impostata in Italiano per garantire la massima comprensione delle procedure e la sicurezza dei processi. Questa opzione è destinata esclusivamente agli utenti di back-office o ai supervisori con necessità di consultazione in lingua diversa.

**Procedura di modifica della lingua:**

È possibile modificare la lingua dell'interfaccia seguendo una delle seguenti modalità:

  - > **Dalla schermata di accesso:**

  - > **Dal profilo utente (UMC):** Accedere alla pagina UMC, selezionare il menu "User Profile", aprire la scheda "Change Language", impostare la lingua desiderata dal menu a tendina e confermare cliccando su "Save".

  - > **Dal profilo utente (Repetitive UI):** Cliccare sull'icona utente (nell'angolo in basso a sinistra), accedere alla sezione "My Profile", selezionare la lingua dal menu a tendina e confermare l'operazione cliccando su "Save".

**Effetto:** Il sistema tradurrà in tempo reale i contenuti della home page, della barra laterale e i cruscotti operativi. (fare refresh del browser)

_[immagine]_

*Figura 6.1: Selezione della lingua nella schermata iniziale di Login.*

_[immagine]_

*Figura 6.2: Modifica delle impostazioni lingua tramite l'interfaccia UMC (User Management Center).*

_[immagine]_

*Figura 6.3: Configurazione della lingua nel profilo utente all'interno della Repetitive UI.*

  -
