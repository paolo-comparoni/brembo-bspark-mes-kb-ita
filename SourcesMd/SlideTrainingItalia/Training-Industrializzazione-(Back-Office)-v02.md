# Training-Industrializzazione-(Back-Office)-v02

> Documento sorgente: `E:\BremboDocs\SlideTrainingItalia\Training-Industrializzazione-(Back-Office)-v02.pptx`  
> Tipo: PowerPoint (.pptx) · Slide: 32


## Slide 1: BREMBO B-SPARK TRAINING

- BREMBO B-SPARK TRAINING

- Industrializzazione (Back-Office)

- ROLLOUT ITALIA 2026

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY


## Slide 2: Scopo della sessione – target audience

- TARGET AUDIENCE
- Key User Industrializzazione

- Scopo della sessione – target audience

- BREMBO B-Spark – Training Industrializzazione

- 2

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- OBIETTIVO
- Lo scopo della sessione è fornire le competenze necessarie per la gestione e manutenzione delle anagrafiche tecniche all'interno del nuovo sistema MES Opcenter.
- Il training si focalizza sulla configurazione di Equipment (gerarchie e tipi), Tooling, Materiali e Bill of Process (BOP), garantendo la corretta associazione della documentazione tecnica necessaria alla produzione per i siti di Curno e Mapello.

- + TRAINING INDUSTRIALIZZAZIONE
- + CURNO E MAPELLO


## Slide 3: Lista delle funzionalità contenute nel training

- Lista delle funzionalità contenute nel training

- BREMBO – Training Industrializzazione

- 3

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY


## Slide 4: (senza titolo)

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- 4

- Materiali

- Anagrafica
- Pre-macchina (Buffer)


## Slide 5: Materiali

- BREMBO B-Spark – Training Industrializzazione

- 5

- Materiali

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY


## Slide 6: Pre-macchina (Buffer)

- BREMBO B-Spark – Training Industrializzazione

- 6

- Pre-macchina (Buffer)

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY


## Slide 7: (senza titolo)

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- 7

- Equipment

- Anagrafica
- Gerarchia
- Proprietà


## Slide 8: Equipment

- BREMBO B-Spark – Training Industrializzazione

- 8

- Equipment

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY


## Slide 9: Equipment

- BREMBO B-Spark – Training Industrializzazione

- 9

- Equipment

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- In Opcenter, gli Equipment non sono semplici nomi in una lista, ma rappresentano la replica digitale di ogni componente del plant.
- La struttura riflette fedelmente la realtà fisica:
- Enterprise / Site: Il livello più alto.
- Plant / Area: La ripartizione logica e geografica.
- Production Line: Il flusso di processo.
- Work Center / Unit: La singola macchina o postazione.

- Ogni elemento possiede delle Proprietà che definiscono il comportamento del sistema in base a dove si trova l’operatore.
- Configurazione Dinamica: abilitare, disabilitare o nascondere specifiche feature
- Business Logic: Definizione di vincoli e limitazioni tecniche proprie di quel determinato asset.
- Integrazione Hardware: Collegamento diretto con periferiche esterne (es. stampanti di etichette, bilance, PLC) associate univocamente a quell'equipment.


## Slide 10: Gerarchia Equipment

- BREMBO B-Spark – Training Industrializzazione

- 10

- Gerarchia Equipment

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- "Il sistema si adatta alla macchina, non l'operatore al sistema."
- Grazie a questa struttura, l'operatore vede solo ciò che serve per quella specifica unità, riducendo l'errore umano e velocizzando l'esecuzione.
- Permettendo comunque una configurabilità che aiuta la risoluzione di eventuali blocchi o problemi


## Slide 11: Equipment - Proprietà di Processo

- BREMBO B-Spark – Training Industrializzazione

- 11

- Equipment - Proprietà di Processo

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- StartFollowingOperations / Autostart:
  - True: Attiva il restart automatico dell'operazione. Quando un operatore completa una dichiarazione di produzione, se l'ordine non è ancora terminato, il sistema avvia automaticamente una nuova fase per la quantità residua. Questo è utile nelle linee ad alta cadenza per ridurre i tempi morti di inserimento dati.
  - False (Oxidation e HTT): In questi reparti la gestione è "a cassone" o a telaio. Poiché spesso più contenitori di ordini diversi entrano contemporaneamente nei forni o negli impianti, un riavvio automatico dello stesso ordine non sarebbe coerente con il flusso logistico che prevede il completamento di lotti fisici distinti.
- IsAutomated:
  - Se impostato su True, il MES abilita l'integrazione diretta con i PLC delle macchine (es. macchine conta-pezzi o conchigliatrici in fonderia). Il sistema smette di fare affidamento solo sull'inserimento manuale e legge automaticamente i sensori di campo per contare i "colpi" (casting strokes) e i pezzi prodotti.


## Slide 12: Equipment - Proprietà di Processo

- BREMBO B-Spark – Training Industrializzazione

- 12

- Equipment - Proprietà di Processo

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- StartFollowingOperations / Autostart:
  - True: Attiva il restart automatico dell'operazione. Quando un operatore completa una dichiarazione di produzione, se l'ordine non è ancora terminato, il sistema avvia automaticamente una nuova fase per la quantità residua. Questo è utile nelle linee ad alta cadenza (Assembly e Machining) per ridurre i tempi morti di inserimento dati.
  - False (Oxidation e HTT): In questi reparti la gestione è "a cassone" o a telaio. Poiché spesso più contenitori di ordini diversi entrano contemporaneamente nei forni o negli impianti, un riavvio automatico dello stesso ordine non sarebbe coerente con il flusso logistico che prevede il completamento di lotti fisici distinti.
- IsAutomated:
  - Se impostato su True, il MES abilita l'integrazione diretta con i PLC delle macchine (es. macchine conta-pezzi o conchigliatrici in fonderia). Il sistema smette di fare affidamento solo sull'inserimento manuale e legge automaticamente i sensori di campo per contare i "colpi" (casting strokes) e i pezzi prodotti.


## Slide 13: Equipment – Proprietà Gestione Scrap e Quarantena

- BREMBO B-Spark – Training Industrializzazione

- 13

- Equipment – Proprietà Gestione Scrap e Quarantena

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- SendGoodReceiptForScrap:
- SendGoodReceiptForQuarantine:
  - Questo parametro decide se inviare a SAP un messaggio di "Entrata Merci" per i pezzi non conformi.
  - False (Fonderia): In fonderia, lo scarto (es. pezzi fusi male) non viene stoccato come "codice materiale scarto", ma viene re-immesso nel ciclo produttivo come lega da rifondere (chili di ritorno). Inviare un'entrata merci creerebbe giacenze fittizie di pezzi che in realtà tornano a essere materia prima.
  - True (Altri reparti): In assemblaggio o lavorazione meccanica, un pezzo scartato è un'unità fisica che deve essere tracciata formalmente su SAP in un magazzino logico di scarto o quarantena per fini contabili e di inventario.


## Slide 14: Equipment – Proprietà per Tracciabilità e Logistica

- BREMBO B-Spark – Training Industrializzazione

- 14

- Equipment – Proprietà per Tracciabilità e Logistica

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- IsAGVEnabled:
  - Se attivo, il MES interfaccia le chiamate materiali con i sistemi di trasporto automatico AGV. È specifico per le lavorazioni meccaniche di Curno dove lo spostamento dei contenitori tra i buffer di linea e il magazzino è asservito da questi veicoli.
- EnableOriginalBatchCheck:
  - Identifica se per quel centro di lavoro è obbligatorio tracciare il lotto di colata originale. È obbligatorio per Fonderia e Friction perché garantisce la genealogia completa. Permette di risalire dal pezzo finito all'esatto lotto di fusione del metallo o alla miscela di polveri originale.


## Slide 15: Equipment – Proprietà per la Configurazione delle Stampanti

- BREMBO B-Spark – Training Industrializzazione

- 15

- Equipment – Proprietà per la Configurazione delle Stampanti

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- PrinterName:
  - Definisce la stampante predefinita della risorsa (Work Center o Unit) per l'emissione delle etichette standard dei contenitori.
- GoodsLabelPrinterName:
  - Proprietà specifica utilizzata per indirizzare la stampa delle etichette dei prodotti conformi.
- NCLabelPrinterName:
  - Identifica la stampante dedicata alle dichiarazioni di Non Conformità, ovvero per le etichette di Scarto e Quarantena.
- ReworkPrinterName:
  - Specifica la stampante riservata esclusivamente ai pezzi dichiarati come Rework (da rilavorare).

- Nota: Il sistema segue una logica gerarchica; se la proprietà è configurata a livello di Unit, questa ha la precedenza sulla configurazione del Work Center.
- I nomi delle stampanti inseriti in queste proprietà devono corrispondere esattamente ai nomi delle stampanti configurati nel software di gestione delle etichette (es. BarTender), che riceve i dati dal MES e gestisce il layout final


## Slide 16: (senza titolo)

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- 16

- Tool (Stampi)

- Caricamento Immagini
- Mappatura codici di cavità
- Usage Count
- Stroke Ratio


## Slide 17: Tool – Caricamento Immagini

- BREMBO B-Spark – Training Industrializzazione

- 17

- Tool – Caricamento Immagini

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- Caricamento Immagine Stampo:
  - L’immagine (JPEG/PNG) deve essere caricata nella pagina Tool Definition (livello Famiglia/Generic).
  - Percorso: Tool Definition > Seleziona Stampo > Tab «Documents» > Link New/Existing Document.
  - L'immagine caricate sarà visibile all'operatore sul MES durante la produzione.


## Slide 18: Tool – Caricamento Immagini

- BREMBO B-Spark – Training Industrializzazione

- 18

- Tool – Caricamento Immagini

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- Esempio vista pagina operatore


## Slide 19: Tool – Part Numbers

- BREMBO B-Spark – Training Industrializzazione

- 19

- Tool – Part Numbers

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- Mappatura Codici Cavità (Part Numbers):
  - Per abilitare il tasto "Defect on Cavity", è necessario mappare le posizioni dell'immagine con i codici fuso.
  - Percorso: Materials > Seleziona Materiale > Tab «Properties».
  - Inserire i codici fuso nei campi PartNumber 1, PartNumber 2, ecc., seguendo la numerazione definita nell'immagine dello stampo.
  - Se questa configurazione è assente, l'operatore riceverà un errore e non potrà avviare l'ordine di produzione al Casting.


## Slide 20: Tool – Proprietà

- BREMBO B-Spark – Training Industrializzazione

- 20

- Tool – Proprietà

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- Stroke Ratio (Moltiplicità):
  - Definisce quanti pezzi vengono prodotti per ogni singolo ciclo/battuta dello stampo.
  - Casse Anime: Impostare il valore in base alla quantità di anime prodotte simultaneamente (es. ratio = 4 se lo stampo produce 4 anime a colpo).
  - Fonderia: Generalmente impostato a 1 (gestione per colata).


## Slide 21: Tool – Proprietà

- BREMBO B-Spark – Training Industrializzazione

- 21

- Tool – Proprietà

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- Max Usage Count (Contatore Colpi):
  - Max Usage Count: Definito nella Tool Definition. Rappresenta la soglia di vita utile dello stampo (es. 100.000 colpi).
  - Raggiunta la soglia, il MES blocca la produzione per richiedere la sostituzione o revisione.


## Slide 22: (senza titolo)

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- 22

- Routing (As Planned BOP)

- Anagrafica
- Dettagli


## Slide 23: Anagrafica Processi

- BREMBO B-Spark – Training Industrializzazione

- 23

- Anagrafica Processi

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY


## Slide 24: (senza titolo)

- BREMBO B-Spark – Training Industrializzazione

- 24

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- BOP/Routings

- In Opcenter, il Routing (o Bill of Process - BOP) non è solo un elenco di fasi, ma la base su cui vengono costruiti e arricchiti gli ordini di produzione.I routing vengono importati direttamente dal sistema ERP. La loro gestione non avviene nel MES, garantendo l'integrità del dato "master".Una volta in Opcenter, il routing diventa lo scheletro che viene "vestito" con le informazioni operative necessarie all'esecuzione (Documenti, Ispezioni, Operazioni, ecc).
- Sebbene non vengano creati localmente, comprendere la struttura dei routing è essenziale per:
- Prevedere il Flusso: Comprendere e gestire correttamente i futuri ordini in ingresso.
- Analisi dei Componenti: Identificare esattamente cosa compone l'ordine (materiali, risorse, tempi) e come questi debbano interagire con gli Equipment (visti nella slide precedente).
- Controllo di Processo: Garantire che ogni fase della lavorazione segua la sequenza logica e tecnica stabilita a livello enterprise.


## Slide 25: (senza titolo)

- 25

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- Documenti

- Gestione
- Associazioni


## Slide 26: Documenti

- I documenti sono utilizzati per fornire all’Operatore informazioni di supporto durante l’esecuzione delle attività operative.
- I documenti possono essere associati alle seguenti entità di sistema:
- Materials
- Tool Definitions
- Process Operations
- Work Order Operations
- WorkCenter

- BREMBO B-Spark – Training Industrializzazione

- 26

- Documenti

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY


## Slide 27: Documenti linkati al materiale

- BREMBO B-Spark – Training Industrializzazione

- 27

- Documenti linkati al materiale

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY


## Slide 28: Documenti linkati al workcenter

- BREMBO B-Spark – Training Industrializzazione

- 28

- Documenti linkati al workcenter

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY


## Slide 29: (senza titolo)

- 29

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- Glossario Minimo


## Slide 30: Glossario Minimo

- BREMBO B-Spark – Training Industrializzazione

- 30

- Glossario Minimo

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

| TERMINE | EQUIVALENTE | DESCRIZIONE |
| --- | --- | --- |
| Work Order (WO) | Production Order | Rappresenta l'ordine di produzione. Nel MES è considerato il "mattone" base per l'esecuzione fisica, mentre in SAP ha una valenza strategica e finanziaria. |
| BOP (Bill of Process) | Routing | Definisce la sequenza di operazioni necessarie per produrre un materiale. Nel MES viene "arricchito" con dati tecnici (es. ispezioni, documenti) non presenti in SAP. |
| Equipment | Work Center / Risorsa | Rappresenta l'attrezzatura fisica. Nel MES, "Equipment" è un termine generico che può riferirsi a diversi livelli della gerarchia (Sito, Area, Linea, Macchina). |
| Buffer / Pre-macchina | PSA (Production Supply Area) | Aree fisiche di stoccaggio temporaneo a bordo linea. Nel MES sono identificate dai codici PS di SAP per garantire l'allineamento dei materiali. |
| Container | Handling Unit (HU) / CDI | L'unità fisica (es. cassone, pallet) che contiene i pezzi. In SAP è fondamentale per la gestione logistica del magazzino; nel MES è l'oggetto su cui si dichiarano i pezzi prodotti. |
| Process NId (Identifier) | GroupId (PLNNR) | Identificativo tecnico del routing/processo. |
| Revision | Group Counter (PLNAL) | Indica la versione specifica di un routing per lo stesso materiale. In SAP è il contatore progressivo. |


## Slide 31: Glossario Minimo

- BREMBO B-Spark – Training Industrializzazione

- 31

- Glossario Minimo

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

| TERMINE | EQUIVALENTE | DESCRIZIONE |
| --- | --- | --- |
| Materiali Master | Anagrafica Materiali | L'anagrafica che definisce codici e proprietà dei materiali. SAP è il sistema "Master" da cui questi dati scendono verso il MES. |
| MTU (Material Tracking Unit) | - | Unità minima tracciata nel MES che si muove in fabbrica. Corrisponde a un'istanza fisica del materiale (spesso legata a un lotto o contenitore). |
| Failure / Defect | Scrap / Materiale difettoso | Identifica un'anomalia tecnica. Nel MES viene gestita attraverso un'anagrafica dedicata per suggerire le causali di scarto a SAP. |
| Backflush | Scarico a posteriori | Processo di consumo automatico dei componenti in SAP in base a quanto dichiarato come prodotto nel MES. |
| Original Batch | Lotto di colata | Identificativo del lotto di fusione originale utilizzato negli stabilimenti di fonderia per garantire la genealogia. |


## Slide 32: Grazie

- Grazie

- ENGINEERING / THE DIGITAL TRANSFORMATION COMPANY

- Juela Ndoka

- Technical Leader
